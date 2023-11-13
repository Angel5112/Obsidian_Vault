### Hotkeys

*Modo Insert:*  Presionar i

*Salir del Modo Insert:*  Presionar Esc

*Modo de Comandos:*  Presionar :

*Colapsar Directorios:*  Presionar o

*Deshacer Cambios:*  U

#### Explorador de Archivos

*Salir del Modo Edición:*  Esc

*Explorador de Archivos:*  Ctrl + N

*Volver al Explorador de Archivos:*  Ctrl + W + W

*Crear Directorio:*  Presionar A y agregar / al final

*Crear Archivo:*  En el explorador de archivos -> Presionar A

*Copiar Archivo:*  En el explorador de archivos -> Presionar C

*Pegar Archivo:*  En el explorador de archivos -> Presionar P

*Renombrar un Archivo:*  En el explorador de archivos -> Presionar R

*Eliminar un Archivo:*  En el explorador de archivos -> Presionar D

#### Barra de Navegación

*Barra de Navegación:*  Space + F + F

*Barra de Navegación (Archivos Abiertos):*  Space + F + B

#### Cheatsheet

*Abrir Cheatsheet:*  Space + C + H

*Ayuda de Comandos:*  Space + wait

#### Navegación de Paneles

*Abrir Panel Vertical:*  Crea un panel vertical -> `: + vsp`

*Abrir Panel Horizontal:*  Crea un panel horizontal -> `: + sp`

*Cerrar Panel:*  Cierra un panel -> `: + q`

*Ir a Panel Izquierdo:* Ctrl + H

*Ir a Panel Derecho:*  Ctrl + L

*Ir a Panel Inferior:*  Ctrl + J

*Ir a Panel Superior:*  Ctrl + K

*Mostrar / Ocultar Numero de Lineas:*  Space + N

*Invertir Numero de Lineas:*  Space + R + N

#### Tabs

*Ir a la siguiente Tab:*  Tab

*Ir a la Tab anterior:*  Shift + Tab

*Cerrar una Tab:*  Space + X

### Neovim
#### Instalación de Neovim
1. Usar el comando -> `sudo snap install nvim --classic`
2. Para facilitar ejecución, crear un alias -> `alias vim=nvim`
3. Guarda el alias a nivel global -> `echo "alias vim=nvim" >> .bashrc`

#### Instalación de NVChad
1. Guardar cualquier configuración de neovim -> `mv ~/.config/nvim ~/.config/nvim.backup`
2. Eliminar cualquier cache de neovim -> `rm -rf ~/.local/share/nvim`
3.  Clonar el repositorio de NVChad -> `git clone https://github.com/NvChad/NvChad ~/.config/nvim --depth 1`
4. Abrir neovim -> `vim`
5. No aceptar la configuración recomendada y esperar la instalación de los paquetes.

#### Cambiar Temas en Neovim
1. Presiona -> Space + T + H
2. Selecciona el tema de preferencia (Personalmente uso Catpuccin)

#### Syntax Highlighting
1. Abrir la terminal de comandos de neovim -> `:`
2. Usar el comando -> `TSInstall <programming language>`

#### Customizar Neovim
1. Abrir con un editor -> `~/.config/nvim`
2. Abrir `chadrc.lua`
3. Agregar `M.plugins = 'custom.plugins'`
4. Crear archivo **plugins.lua**
5. Agregar:
~~~lua
local plugins = {
	{
	# Plugins 
	}
}

return plugins
~~~
6.  Agregar el plugin deseado dentro de los brackets.
7. Asignarle un tipo de archivo al plugin (**ft = plugin_name"**).
8. Activar el plugin -> `: + Lazy sync`
<br>
### Configuración para Python
#### Activar Sugerencias y Autocompletado
1. Abrir el directorio -> `~/.config/nvim`
2. En el archivo **plugins.lua,** insertar el siguiente codigo:
~~~lua
{
	"williamboman/mason.nvim",
	opts = {
		ensure_installed = {
			"pyright",   # Necesitas tener node >= v20
		},
	},
}
~~~
3. Salir de neovim.
4. Ejecutar el comando -> `MasonInstallAll`
5. Agregar el **lsp-config** mediante el siguiente código (nuevo plugin):
~~~lua
	"neovim/nvim-lspconfig",
	config = function()
		require "plugins.configs.lspconfig"
		require "custom.configs.lspconfig"
	end,
~~~
6. Crear en **configs** el archivo **lspconfig.lua**
7. Insertar el siguiente código:
```lua
local config = require("plugins.configs.lspconfig")

local on_attach = config.on_attach
local capabilities = config.capabilities

local lspconfig = require("lspconfig")

lspconfig.pyright.setup({
  on_attach = on_attach,
  capabilities = capabilities,
  filetypes = {"python"},
})
```
8. Comprobar el resultado con cualquier código de Python.

#### Análisis y Manejo de Errores
1. Usar **null-ls** junto a plugins como **mypy y ruff**
2. Agregar **null-ls** como un plugin and **plugins.lua:**
```lua
{
	"jose-elias-alvarez/null-ls.nvim",
	ft = {"python"},
	opts = function()
		return require "custom.configs.null-ls"
	end,
},
```
3. Crear el archivo **null-ls.lua** en `custom/configs`
4. Agregar a **null-ls.lua** el siguiente codigo:
```lua
local null_ls = require("null-ls")

local opts = {
	sources = {
		null_ls.builtins.diagnostics.mypy,
		null_ls.builtins.diagnostics.ruff,
	}
}
return opts
```
5. Agregar `"mypy"` y `"ruff"` en la tabla **ensure_installed** de **plugins.lua** del **mason.nvim**
6. Ejecutar el comando **MasonInstallAll**
7. Probar el resultado con código Python.

#### Autoformateado
1. Usar la herramienta de autoformateado de **Black**
2. Agregar `"black"` en la tabla **ensure_installed** de **plugins.lua** del **mason.nvim**
3. Ejecutar el comando **MasonInstallAll**
4. Agregar en **null-ls.lua** (dentro de sources) el siguiente código: `null_ls.builtins.formatting.black,`
5. Agregar el siguiente código para el autoformateado al guardar:
```lua
local augroup = vim.api.nvim_create_augroup("LspFormatting", {})
# Configuracion previa de null-ls

# Debajo de }. de sources

on_attach = function(client, bufnr)
	if client.supports_method("textDocument/formatting") then
		vim.api.nvim_clear_autocmds({
			group = augroup,
			buffer = bufnr,
		})
		vim.api.nvim_create_autocmd("BufWritePre", {
			group = augroup,
			buffer = bufnr,
			callback = function()
				vim.lsp.buf.format({ bufnr = bufnr })
			end,
		})
	end
end,

# Parte final de la configuracion previa de null-ls
```
6. Probar el resultado con un código de Python.

#### Debugger para Python
1. En **plugins.lua** agregar el siguiente código:
```lua
{
	"rcarriga/nvim-dap-ui",
	dependencies = "mfussenegger/nvim-dap",
	config = function()
		local dap = require("dap")
		local dapui = require("dapui")
		dapui.setup()
		dap.listeners.after.event_initialized["dapui_config"] = function()
			dapui.open()
		end
		dap.listeners.before.event_terminated["dapui_config"] = function()
			dapui.close()
		end
		dap.listeners.before.event_exited["dapui_config"] = function()
			dapui.close()
		end
	end
},
{
	"mfussenegger/nvim-dap",
	config = function(_, opts)
		require("core.utils").load_mappings("dap")
	end
},
{
	"mfussenegger/nvim-dap-python",
	ft = "python",
	dependencies = {
		"mfussenegger/nvim-dap",
		"rcarriga/nvim-dap-ui",
	},
	config = function(_, opts)
		local path = "~/.local/share/nvim/mason/packages/debugpy/venv/bin/python"
		require("dap-python").setup(path)
		require("core.utils").load_mappings("dap-python")
	end,
}

# Dentro del ensure_installed de mason.nvim

	"debugpy",
```
2. Ejecutar el comando **MasonInstallAll**
3. Agregar hotkeys para los breakpoints y la ejecucion de **dap-python**
4. Crear el archivo **mappings.lua** en `custom/configs`
5. Agregar el código:
```lua
local M = {}

M.dap = {
	plugin = true,
	n = {
		["<leader>db"] = {"<cmd> DapToggleBreakpoint <CR>"}
	}
}

M.dap_python = {
	plugin = true,
	n = {
		["<leader>dpr"] = {
			function()
				require("dap-python").test_method()
			end
		}
	}
}

return M
```
6. En **chadrc.lua** agregar debajo de plugins -> `M.mappings = require "custom.configs.mappings"`
7. Probar los resultados en código de Python.
8. Debugger -> Space + D + P + R  (Necesita de **Tests**)
9. Agregar Breakpoint -> Space + D + B
<br>
#### Tags

#courses 