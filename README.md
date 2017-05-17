# environment

## [VSCode](https://code.visualstudio.com/)

Шрифт: https://github.com/tonsky/FiraCode

* [Beautify](https://marketplace.visualstudio.com/items?itemName=HookyQR.beautify)

```json
{
	"editor.fontFamily": "Fira Code Light",
	"editor.fontSize": 14,
	"editor.lineHeight": 21,
	"editor.fontLigatures": true,
	"editor.renderWhitespace": "all",
	"editor.minimap.enabled": true,
	"editor.renderIndentGuides": true,
	"editor.wordWrap": "on",
	"editor.snippetSuggestions": "top",
	"window.reopenFolders": "all",
	"window.openFilesInNewWindow": "default",
	"files.associations": {
		"*.pcss": "css",
		"*.styl": "stylus"
	},
	"files.autoGuessEncoding": true,
	"files.exclude": {
		"**/.git": true,
		"**/.svn": true,
		"**/.hg": true,
		"**/.DS_Store": true,
		"**/bitrix": true
	},
	"workbench.editor.showTabs": false,
	"workbench.colorTheme": "Default Dark+",
	"workbench.iconTheme": "vs-seti",
	"workbench.welcome.enabled": true,
	"emmet.preferences": {
		"css.autoInsertVendorPrefixes": false,
		"css.syntaxes": ["css, less, sass, scss, stylus, styl, postcss"]
	},
	"files.autoSave": "off",
	"editor.insertSpaces": false
}
```

```json
[
	{ "key": "ctrl+shift+g", "command": "editor.emmet.action.wrapWithAbbreviation" },
	{ "key": "ctrl+shift+;", "command": "editor.emmet.action.removeTag" },
	{ "key": "ctrl+shift+'", "command": "editor.emmet.action.updateTag" },
	{ "key": "ctrl+alt+left", "command": "editor.emmet.action.selectPreviousItem" },
	{ "key": "ctrl+alt+right", "command": "editor.emmet.action.selectNextItem" },
	{ "key": "shift+alt+left", "command": "editor.emmet.action.balanceInward" },
	{ "key": "shift+alt+right", "command": "editor.emmet.action.balanceOutward" }
]
```


## [Sublime](https://www.sublimetext.com/)

* BracketHighlighter
* Color Highlighter
* Diffy
* DocBlockr
* Emmet
* Google Search
* Hayaku - tools for writing CSS faster
* Javascript Beautify
* Material Theme
* Open-Include
* Package Control
* SideBarEnhancements

```json
{
	"always_show_minimap_viewport": true,
	"bold_folder_labels": true,
	"color_scheme": "Packages/Material Theme/schemes/Material-Theme-Darker.tmTheme",
	"enable_tab_scrolling": false,
	"fallback_encoding": "Cyrillic (Windows 1251)",
	"font_size": 11,
	"highlight_line": true,
	"highlight_modified_tabs": false,
	"ignored_packages":
	[
		"Vintage"
	],
	"indent_guide_options":
	[
		"draw_normal",
		"draw_active"
	],
	"line_padding_bottom": 1,
	"line_padding_top": 1,
	"overlay_scroll_bars": "enabled",
	"show_encoding": true,
	"tab_size": 4,
	"theme": "Material-Theme-Darker.sublime-theme",
	"word_wrap": true
}
```

```json
[
	{ "keys": ["ctrl+d"], "command": "duplicate_line" },
	{ "keys": ["ctrl+shift+d"], "command": "find_under_expand" },
	{ "keys": ["ctrl+shift+u"], "command": "google_search" },
	{
		"keys": [
			"shift+ctrl+g"
		], 
		"command": "wrap_as_you_type", 
		"context": [
			{
				"operand": false, 
				"operator": "equal", 
				"match_all": true, 
				"key": "setting.is_widget"
			}, 
			{
				"match_all": true, 
				"key": "emmet_action_enabled.wrap_as_you_type"
			}
		]
	}
]
```


## Pixapp

```js
var gui = window.require('nw.gui');
var spawn = window.require('child_process').spawn;
var exec = window.require('child_process').exec;

module.exports = {

	// панель с чатом
	im: {
		isActive: true,
		url: 'https://www.samsonpost.ru/desktop_app/'
	},

	// реакция на время
	timeCheck: {
		isActive: true,

		// как часто проверять условия
		interval: 1000,

		// когда обновлять условия
		renewCheck: function (dateOld, dateNew) {
			return dateOld.getDay() !== dateNew.getDay();
		},

		// проверки
		checks: [

			// показ пробок
			{

				// что нужно проверить
				check: function (date) {
					return date.getHours() === 18 && date.getMinutes() === 0
				},
				
				// что нужно сделать
				action: function () {
					gui.Shell.openExternal('https://yandex.ru/maps/193/voronezh/?l=trf');
				}
			},

			// показ ссылок
			{
				check: function (date) {
					return date.getHours() === 12 && date.getMinutes() === 0
				},
				action: function () {

					// СДЕЛАТЬ
					// удалить, когда не нужно будет указывать полный путь к Опере
					// или когда данные с вебплатформдайли будут сами обновляться
					console.log( process.env.PATH );

					spawn('C:\\Program Files (x86)\\OperaNew\\launcher.exe', ['?', 'http://webplatformdaily.org/']).on('error', function (e) {
						console.log(e);
					});

					gui.Shell.openExternal('http://tools.samsonpost.ru/to-markdown/');
					// gui.Shell.openExternal('http://pixhub.ru/tools/kb/');
					gui.Shell.openExternal('https://twitter.com/webstandards_ru/');
				}
			},

			// старт пщпщпщ
			{
				check: function (date) {
					return date.getHours() === 12 && date.getMinutes() === 35
				},
				action: function () {
					exec('start D:\\common\\games\\CS1.6\\Counter-Strike\\hlds.exe -console -game cstrike', {
						cwd: 'D:\\common\\games\\CS1.6\\Counter-Strike'
					}).on('error', function (e) {
						console.log(e);
					});
				}
			}
		]
	}
}
```

## Пщпщпщ

```
// http://txdv.github.io/cstrike-cvarlist/

// disable autoaim
sv_aim 0

// disable clients' ability to pause the server
pausable 0

// default server name. Change to "Bob's Server", etc.
hostname "INT 1.6 Server"

// maximum client movement speed 
sv_maxspeed 320

mp_timelimit 40

mp_friendlyfire 0

mp_forcechasecam 1

mp_c4timer 30

mp_roundtime 1.5
mp_buytime 1.5

mp_freezetime 2

sv_cheats 0
rcon_password "pierrdunn"

maxplayers 32

// load ban files
exec listip.cfg
exec banned.cfg

map de_westwood

```
