---
Order: 4
Area: getstarted
TOCTitle: User Interface
ContentId: 3a33f35b-cded-4f7f-8674-6f2ba5fca023
PageTitle: Visual Studio Code User Interface
DateApproved: 9/10/2020
MetaDescription: A quick overview of the Visual Studio Code user interface. Learn about the editor, window management, and special UI to handle source control, extension management, full text search and more.
---
# 用户界面

本质上，Visual Studio Code 是代码编辑器。 像许多其他代码编辑器一样，VS Code 在左边采用通用的用户界面和资源管理器布局，以显示有权访问的所有文件和文件夹，而在右边的编辑器则显示已打开文件的内容。

![code basics hero](https://code.visualstudio.com/assets/docs/getstarted/userinterface/hero.png)

## 基本布局

VS Code具有简单直观的布局，可最大程度地为编辑器提供空间，同时为浏览和访问文件夹或项目的整个上下文留出足够的空间。 用户界面分为五个区域：

* **Editor** - 编辑文件的主要区域。 可以在垂直和水平方向上并排打开任意多个编辑器。
* **Side Bar** - 包含诸如资源管理器之类的不同视图，可在您处理项目时为您提供帮助。
* **Status Bar** - 有关打开的项目和您编辑的文件的信息。
* **Activity Bar** - 它位于最左侧，可让您在视图之间切换，并为您提供特定于上下文的其他指示符，例如启用 Git 时传出更改的数量。
* **Panels** - 可以在编辑器区域下方显示不同的面板，以输出或调试信息，错误和警告或集成终端。 面板也可以向右移动以获得更多垂直空间。

每次启动 VS Code 时，文件夹、布局和打开的文件将与上次关闭时的状态相同。

每个打开的编辑器顶部都有一个卡片式标题（`Tab`），用于显示打开的文件。要了解更多有关卡片式标题的信息，请参见下面的[卡片式标题](/docs/getstarted/userinterface.md＃卡片式标题）(`Tab`)。

>**提示:** 可以把侧边栏（`Side Bar`）移到右边 (**View** > **Move Side Bar Right**) ，或切换到不可见 (`kb(workbench.action.toggleSidebarVisibility)`)。

## 并排编辑

可以横向或竖向并排打开多个编辑器网格用来编辑文件。 如果已经打开了个文件, 在另一侧打开其他文件的方法有下面几种。

* 按住`kbstyle(Alt)` 键，在资源管理视图中点击要打开的文件。
* `kb(workbench.action.splitEditor)` 命令将正在编辑的文件分裂到两个编辑器中。
* 在资源管理视图上下文中使用**打开到侧边** 命令(`kb(explorer.openToSide)`) 
* 在编辑器右上角点击 **Split Editor** 按钮。
* 从资源管理视图中拖动一个文件到编辑器视图中任意一侧（当鼠标接近边框时会显示区域突显块）。
* 在**快速打开** (`kb(workbench.action.quickOpen)`) 设置有效时，组合键`kbstyle(Ctrl+Enter)` (macOS: `kbstyle(Cmd+Enter)`) 将快速打开[预显](#预显模式)的文件。

![Side by Side editing](images/userinterface/sidebyside.png)

Whenever you open another file, the editor that is active will display the content of that file. So if you have two editors side by side and you want to open file 'foo.cs' into the right-hand editor, make sure that editor is active (by clicking inside it) before opening file 'foo.cs'.

By default editors will open to the right-hand side of the active one. You can change this behavior through the setting `workbench.editor.openSideBySideDirection` and configure to open new editors to the bottom of the active one instead.

When you have more than one editor open you can switch between them quickly by holding the `kbstyle(Ctrl)` (macOS: `kbstyle(Cmd)`) key and pressing `kbstyle(1)`, `kbstyle(2)`, or `kbstyle(3)`.

>**Tip:** You can resize editors and reorder them. Drag and drop the editor title area to reposition or resize the editor.

## 迷你导航图

迷你导航图 (代码大纲) gives you a high-level overview of your source code, which is useful for quick navigation and code understanding. A file's minimap is shown on the right side of the editor. You can click or drag the shaded area to quickly jump to different sections of your file.

![minimap](images/userinterface/minimap.png)

>**Tip:** You can move the minimap to the left hand side or disable it completely by respectively setting `"editor.minimap.side": "left"` or `"editor.minimap.enabled": false` in your user or workspace [settings](/docs/getstarted/settings.md).

### 缩进参考线

The image above also shows indentation guides (vertical lines) which help you quickly see matching indent levels. If you would like to disable indent guides, you can set `"editor.renderIndentGuides": false` in your user or workspace [settings](/docs/getstarted/settings.md).

## 面包屑导航

The editor has a navigation bar above its contents called [Breadcrumbs](https://en.wikipedia.org/wiki/Breadcrumb_(navigation)). It shows the current location and allows you to quickly navigate between folders, files, and symbols.

![Breadcrumbs](images/userinterface/breadcrumbs.png)

Breadcrumbs always show the file path and if the current file type has language support for symbols, the symbol path up to the cursor position. You can disable breadcrumbs with the **View** > **Show Breadcrumbs** toggle command. For more information about the breadcrumbs feature, such as how to customize their appearance, see the [Breadcrumbs](/docs/editor/editingevolved.md#breadcrumbs) section of the [Code Navigation](/docs/editor/editingevolved.md) article.

## 资源管理视图

The Explorer is used to browse, open, and manage all of the files and folders in your project. VS Code is file and folder based - you can get started immediately by opening a file or folder in VS Code.

After opening a folder in VS Code, the contents of the folder are shown in the Explorer. You can do many things from here:

* Create, delete, and rename files and folders.
* Move files and folders with drag and drop.
* Use the context menu to explore all options.

>**Tip:** You can drag and drop files into the Explorer from outside VS Code to copy them (if the explorer is empty VS Code will open them instead)

![Explorer Menu](images/userinterface/explorer_menu.png)

VS Code works very well with other tools that you might use, especially command-line tools. If you want to run a command-line tool in the context of the folder you currently have open in VS Code, right-click the folder and select **Open in Command Prompt** (or **Open in Terminal** on macOS or Linux).

You can also navigate to the location of a file or folder in the native Explorer by right-clicking on a file or folder and selecting **Reveal in Explorer** (or **Reveal in Finder** on macOS or **Open Containing Folder** on Linux).

>**Tip:** Type `kb(workbench.action.quickOpen)` (**Quick Open**) to quickly search and open a file by its name.

By default, VS Code excludes some folders from the Explorer (for example. `.git`). Use the `files.exclude` [setting](/docs/getstarted/settings.md) to configure rules for hiding files and folders from the Explorer.

>**Tip:** This is really useful to hide derived resources files, like `\*.meta` in Unity, or `\*.js` in a TypeScript project. For Unity to exclude the `\*.cs.meta` files, the pattern to choose would be: `"**/*.cs.meta": true`. For TypeScript, you can exclude generated JavaScript for TypeScript files with: `"**/*.js": {"when": "$(basename).ts"}`.

### Multi-selection

You can select multiple files in the **File Explorer** and **OPEN EDITORS** view to run actions (Delete, Drag and Drop, Open to the Side) on multiple items. Use the `Ctrl/Cmd` key with `click` to select individual files and `Shift` + `click` to select a range. If you select two items, you can now use the context menu **Compare Selected** command to quickly diff two files.

**Note:** In earlier VS Code releases, clicking with the `Ctrl/Cmd` key pressed would open a file in a new Editor Group to the side. If you would still like this behavior, you can use the `workbench.list.multiSelectModifier` setting to change multi-selection to use the `Alt` key.

```json
"workbench.list.multiSelectModifier": "alt"
```

### 文档树筛选

You can type to filter the currently visible files in the **File Explorer**. With the focus on the **File Explorer** start to type part of the file name you want to match. You will see a filter box in the top-right of the **File Explorer** showing what you have typed so far and matching file names will be highlighted. When you press the cursor keys to move up and down the file list, it will jump between matching files or folders.

Hovering over the filter box and selecting **Enable Filter on Type** will show only matching files/folders. Use the 'X' **Clear** button to clear the filter.

![Filtering files in the File Explorer](images/userinterface/file-explorer-filter.png)

### 大纲视图

The Outline view is a separate section in the bottom of the File Explorer. When expanded, it will show the symbol tree of the currently active editor.

![Outline view](images/userinterface/outline-view.png)

The Outline view has different **Sort By** modes, optional cursor tracking, and supports the usual open gestures. It also includes an input box which finds or filters symbols as you type. Errors and warnings are also shown in the Outline view, letting you see at a glance a problem's location.

For symbols, the view relies on information computed by your installed extensions for different file types. For example, the built-in Markdown support returns the Markdown header hierarchy for a Markdown file's symbols.

![Markdown Outline view](images/userinterface/markdown-outline-view.png)

There are several Outline view [settings](/docs/getstarted/settings.md) which allow you to enable/disable icons and control the errors and warnings display (all enabled by default):

* `outline.icons` - Toggle rendering outline elements with icons.
* `outline.problems.enabled` - Show errors and warnings on outline elements.
* `outline.problems.badges` - Toggle using badges for errors and warnings.
* `outline.problems.colors` - Toggle using colors for errors and warnings.

## 打开编辑器

At the top of the Explorer is a view labeled **OPEN EDITORS**. This is a list of active files or previews. These are files you previously opened in VS Code that you were working on. For example, a file will be listed in the **OPEN EDITORS** view if you:

* Make a change to a file.
* Double-click a file's header.
* Double-click a file in the Explorer.
* Open a file that is not part of the current folder.

Just click an item in the **OPEN EDITORS** view, and it becomes active in VS Code.

Once you are done with your task, you can remove files individually from the **OPEN EDITORS** view, or you can remove all files by using the **View: Close All Editors** or **View: Close All Editors in Group** actions.

## 视图

The File Explorer is just one of the Views available in VS Code. There are also Views for:

* **Search** - Provides global search and replace across your open folder.
* **Source Control** - VS Code includes Git source control by default.
* **Run** - VS Code's Run and Debug View displays variables, call stacks, and breakpoints.
* **Extensions** - Install and manage your extensions within VS Code.
* **Custom views** - Views contributed by extensions.

> **Tip:** You can open any view using the **View: Open View** command.

![views](images/userinterface/views.png)

You can show or hide views from within the main view and also reorder them by drag and drop.

![view management](images/userinterface/view-management.png)

### 动作边栏

The **Activity Bar** on the left lets you quickly switch between Views. You can also reorder Views by dragging and dropping them on the **Activity Bar** or remove a View entirely (right click **Hide from Activity Bar**).

![activity bar context menu](images/userinterface/activity-bar-context-menu.png)

## 命令面板

VS Code is equally accessible from the keyboard. The most important key combination to know is `kb(workbench.action.showCommands)`, which brings up the **Command Palette**. From here, you have access to all of the functionality of VS Code, including keyboard shortcuts for the most common operations.

![Command Palette](images/userinterface/commands.png)

The **Command Palette** provides access to many commands. You can execute editor commands, open files, search for symbols, and see a quick outline of a file, all using the same interactive window. Here are a few tips:

* `kb(workbench.action.quickOpen)` will let you navigate to any file or symbol by typing its name
* `kb(workbench.action.quickOpenPreviousRecentlyUsedEditorInGroup)` will cycle you through the last set of files opened
* `kb(workbench.action.showCommands)` will bring you directly to the editor commands
* `kb(workbench.action.gotoSymbol)` will let you navigate to a specific symbol in a file
* `kb(workbench.action.gotoLine)` will let you navigate to a specific line in a file

Type `?` into the input field to get a list of available commands you can execute from here:

![Quick Open Help](images/userinterface/quickopenhelp.png)

## 配置编辑器

VS Code gives you many options to configure the editor. From the **View** menu, you can hide or toggle various parts of the user interface, such as the **Side Bar**, **Status Bar**, and **Activity Bar**.

### 隐藏菜单栏 (Windows, Linux)

You can hide the Menu Bar on Windows and Linux with the **View** > **Toggle Menu Bar** command. You can still access the Menu Bar by pressing the `kbstyle(Alt)` key (`window.menuBarVisibility` setting).

### 设置

Most editor configurations are kept in settings which can be modified directly. You can set options globally through user settings or per project/folder through workspace settings. Settings values are kept in a `settings.json` [file](/docs/getstarted/settings.md#settings-file-locations).

* Select **File** > **Preferences** > **Settings** (or press `kb(workbench.action.openSettings)`) to edit the user `settings.json` file.
* To edit workspace settings, select the **WORKSPACE SETTINGS** tab to edit the workspace `settings.json` file.

>**Note for macOS users:** The **Preferences** menu is under **Code** not **File**. For example, **Code** > **Preferences** > **Settings**.

![workspace settings](images/userinterface/workspace-settings.png)

You will see the VS Code [Default Settings](/docs/getstarted/settings.md#default-settings) in the left window and your editable `settings.json` on the right. You can easily filter settings in the `Default Settings` using the search box at the top. Copy a setting over to the editable `settings.json` on the right by clicking on the edit icon to the left of the setting. Settings with a fixed set of values allow you to pick a value as part of their edit icon menu.

After editing your settings, type `kb(workbench.action.files.save)` to save your changes. The changes will take effect immediately.

>**Note:** Workspace settings will override User settings and are useful for sharing project specific settings across a team.

### 静默模式

Zen Mode lets you focus on your code by hiding all UI except the editor (no Activity Bar, Status Bar, Side Bar and Panel), going to full screen and centering the editor layout. Zen mode can be toggled using **View** menu, **Command Palette** or by the shortcut `kb(workbench.action.toggleZenMode)`. Double `kbstyle(Esc)` exits Zen Mode. The transition to full screen can be disabled via `zenMode.fullScreen`. Zen Mode can be further tuned by the following settings: `zenMode.hideStatusBar`, `zenMode.hideTabs`, `zenMode.fullScreen`, `zenMode.restore`, and `zenMode.centerLayout`.

### Centered editor layout

Centered editor layout allows you to center align the editor area. This is particularly useful when working with a single editor on a large monitor. You can use the sashes on the side to resize the view (hold down the `Alt` key to independently move the sashes).

## 卡片式标题

Visual Studio Code shows open items with Tabs (tabbed headings) in the title area above the editor.

When you open a file, a new Tab is added for that file.

![tabs hero](images/userinterface/tabs-hero.png)

Tabs let you quickly navigate between items and you can Drag and Drop Tabs to reorder them.

When you have more open items than can fit in the title area, you can use the **Show Opened Editors** command (available through the `...` More button) to display a drop-down list of tabbed items.

If you don't want to use Tabs, you can disable the feature by setting the `workbench.editor.showTabs` [setting](/docs/getstarted/settings.md) to false:

```json
    "workbench.editor.showTabs": false
```

See the section below to optimize VS Code when [working without Tabs](/docs/getstarted/userinterface.md#working-without-tabs).

### 卡片式标题排序

By default, new Tabs are added to the right of the existing Tabs but you can control where you'd like new Tabs to appear with the `workbench.editor.openPositioning` setting.

For example, you might like new tabbed items to appear on the left:

```json
    "workbench.editor.openPositioning": "left"
```

## 预显模式

When you single-click or select a file in the Explorer, it is shown in a preview mode and reuses an existing Tab. This is useful if you are quickly browsing files and don't want every visited file to have its own Tab. When you start editing the file or use double-click to open the file from the Explorer, a new Tab is dedicated to that file.

Preview mode is indicated by italics in the Tab heading:

![preview mode](images/userinterface/preview-tab.png)

If you'd prefer to not use preview mode and always create a new Tab, you can control the behavior with these settings:

* `workbench.editor.enablePreview` to globally enable or disable preview editors
* `workbench.editor.enablePreviewFromQuickOpen` to enable or disable preview editors when opened from **Quick Open**

## 编辑器组

When you split an editor (using the **Split Editor** or **Open to the Side** commands), a new editor region is created which can hold a group of items. You can open as many editor regions as you like side by side vertically and horizontally.

You can see these clearly in the **OPEN EDITORS** section at the top of the Explorer view:

![tabs editor groups](images/userinterface/tabs-editor-groups.png)

You can Drag and Drop editor groups on the workbench, move individual Tabs between groups and quickly close entire groups (**Close All**).

>**Note:** VS Code uses editor groups whether or not you have enabled Tabs.  Without Tabs, editor groups are a stack of your open items with the most recently selected item visible in the editor pane.

## 网格编辑器布局

By default, editor groups are laid out in vertical columns (for example when you split an editor to open it to the side). You can easily arrange editor groups in any layout you like, both vertically and horizontally:

![Grid Editor Layout](images/userinterface/grid-layout.gif)

To support flexible layouts, you can create empty editor groups. By default, closing the last editor of an editor group will also close the group itself, but you can change this behavior with the new setting `workbench.editor.closeEmptyGroups: false`:

![Grid Empty](images/userinterface/grid-empty.png)

There are a predefined set of editor layouts in the new **View** > **Editor Layout** menu:

![Grid Editor Layout Menu](images/userinterface/grid-layout-menu.png)

Editors that open to the side (for example by clicking the editor toolbar **Split Editor** action) will by default open to the right-hand side of the active editor. If you prefer to open editors below the active one, configure the new setting `workbench.editor.openSideBySideDirection: down`.

There are many keyboard commands for adjusting the editor layout with the keyboard alone, but if you prefer to use the mouse, drag and drop is a fast way to split the editor into any direction:

![Grid Editor Drag and Drop](images/userinterface/grid-dnd.gif)

>**Pro Tip**: If you press and hold the `Alt` key while hovering over the toolbar action to split an editor, it will offer to split to the other orientation. This is a fast way to split either to the right or to the bottom.

![Grid Alt Click](images/userinterface/grid-alt.gif)

### 键盘快捷键

Here are some handy keyboard shortcuts to quickly navigate between editors and editor groups.

>If you'd like to modify the default keyboard shortcuts, see [Key Bindings](/docs/getstarted/keybindings.md) for details.

* `kb(workbench.action.nextEditor)` go to the right editor.
* `kb(workbench.action.previousEditor)` go to the left editor.
* `kb(workbench.action.quickOpenPreviousRecentlyUsedEditorInGroup)` open the previous editor in the editor group MRU list.
* `kb(workbench.action.focusFirstEditorGroup)` go to the leftmost editor group.
* `kb(workbench.action.focusSecondEditorGroup)` go to the center editor group.
* `kb(workbench.action.focusThirdEditorGroup)` go to the rightmost editor group.
* `kb(workbench.action.closeActiveEditor)` close the active editor.
* `kb(workbench.action.closeEditorsInGroup)` close all editors in the editor group.
* `kb(workbench.action.closeAllEditors)` close all editors.

## 在没有卡片式标题的情况下工作

If you prefer not to use Tabs (tabbed headings), you can disable Tabs (tabbed headings) entirely by setting `workbench.editor.showTabs` to false.

### 让预显模式失效

Without Tabs, the **OPEN EDITORS** section of the File Explorer is a quick way to do file navigation.  With [preview editor mode](/docs/getstarted/userinterface.md#preview-mode), files are not added to the **OPEN EDITOR** list nor editor group on single-click open. You can disable this feature through the `workbench.editor.enablePreview` and `workbench.editor.enablePreviewFromQuickOpen` settings.

### 用 “Ctrl+Tab” 在已打开的编辑器之间导航

You can change keybindings for `kbstyle(Ctrl+Tab)` to show you a list of all opened editors from the history independent from the active editor group.

Edit your [keybindings](/docs/getstarted/keybindings.md) and add the following:

```json
{ "key": "ctrl+tab", "command": "workbench.action.openPreviousEditorFromHistory" },
{ "key": "ctrl+tab", "command": "workbench.action.quickOpenNavigateNext", "when": "inQuickOpen" },
```

### 用关闭一个编辑器来关闭整个组

If you liked the behavior of VS Code closing an entire group when closing one editor, you can bind the following in your [keybindings](/docs/getstarted/keybindings.md).

macOS:

```json
{ "key": "cmd+w", "command": "workbench.action.closeEditorsInGroup" }
```

Windows/Linux:

```json
{ "key": "ctrl+w", "command": "workbench.action.closeEditorsInGroup" }
```

## 窗口管理

VS Code has some options to control how windows (instances) should be opened or restored between sessions.

The settings `window.openFoldersInNewWindow` and `window.openFilesInNewWindow` are provided to configure opening new windows or reusing the last active window for files or folders and possible values are `default`, `on` and `off`.

If configured to be `default`, we will make the best guess about reusing a window or not based on the context from where the open request was made. Flip this to `on` or `off` to always behave the same. For example, if you feel that picking a file or folder from the **File** menu should always open into a new window, set this to `on`.

Note: There can still be cases where this setting is ignored (for example, when using the `-new-window` or `-reuse-window` command-line option).

The `window.restoreWindows` setting tells VS Code how to restore the opened windows of your previous session. By default, VS Code will restore all windows you worked on during your previous session (setting: `all`). Change this setting to `none` to never reopen any windows and always start with an empty VS Code instance. Change it to `one` to reopen the last opened window you worked on or `folders` to only restore windows that had folders opened.

## 下一个目标

了解了 VS Code 的总体布局，就可以通过下一章节的内容根据自己的喜好定制编辑器了。

Now that you know the overall layout of VS Code, start to customize the editor to how you like to work by looking at the following topics:

* [改变主题](/docs/getstarted/themes.md) - Set a Color and/or File Icon theme to your preference.

## 常见问题

### 如何改变缩进参考线的颜色?

The indent guide colors are customizable as are most VS Code UI elements. To [customize](/docs/getstarted/theme-color-reference.md) the indent guides color for your active color theme, use the `workbench.colorCustomizations` [setting](/docs/getstarted/settings.md) and modify the `editorIndentGuide.background` value.

For example, to make the indent guides bright blue, add the following to your `settings.json`:

```json
"workbench.colorCustomizations": {
    "editorIndentGuide.background": "#0000ff"
}
```

### Can I hide the OPEN EDITORS section in the Explorer?

Yes, you can hide the **OPEN EDITORS** list with the `explorer.openEditors.visible` [setting](/docs/getstarted/settings.md), which declares how many items to display before a scroll bar appears. Setting `"explorer.openEditors.visible": 0` will hide **OPEN EDITORS** when you have an open folder. The list will still be displayed if you are using VS Code to view loose files.
