# environment

## [VSCode](https://code.visualstudio.com/)

Шрифт: https://github.com/tonsky/FiraCode

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
	"window.reopenFolders": "all",
	"window.openFilesInNewWindow": "default",
	"files.associations": {
		"*.pcss": "css"
	},
	 "files.exclude": {
		"**/.git": true,
		"**/.svn": true,
		"**/.hg": true,
		"**/.DS_Store": true,
		"**/node_modules": true
	},
	"workbench.editor.showTabs": false,
	"workbench.iconTheme": "vs-seti",
	"workbench.welcome.enabled": true,
	"emmet.preferences": {
		"css.autoInsertVendorPrefixes": false,
		"css.syntaxes": ["css, less, sass, scss, stylus, styl, postcss"]
	},
	"files.autoSave": "off"
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
