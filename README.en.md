# LOLICON E-Hentai / ExHentai Enhancer

**English** | [简体中文](README.md)

Personal userscript
Auto Window Adaptation, Adjustable Thumbnails (size/margin/columns), Quick Favorite, Infinite Scroll, Load More Thumbnails, Quick Tag & Search Enhancer, Tag Auto-Complete, Thumbnail Preview

## Install

Userscript:
[Greasy Fork](https://greasyfork.org/scripts/516145)
[Sleazy Fork](https://sleazyfork.org/scripts/516145)

## Features

### Layout Adjust

- **Layout Control Mode** - Core thumbnail layout adaptation logic. Choose between **Zoom First** and **Column First** (configurable separately for List and Gallery)
- **Zoom First** - Keeps the configured zoom scale while columns adjust automatically. Supports **Auto**, **Max/Min Column**, and **Max/Min Width**
- **Column First** - Keeps a fixed column count while thumbnails scale with window width. Supports Min/Max **Zoom limits**
- **Square Thumbnail** - Crop thumbnails into a uniform square aspect ratio
- **Checkerboard Background Fix** - Automatically adjusts the checkerboard background when using custom thumbnail column counts to prevent misalignment
- **Thumbnail Margin/Spacing** - Adjust spacing between thumbnails and around them
- **Page Margin/Padding** - Adjust spacing between the page container, window, and content
- **Full Width Layout** - Expand the page to the maximum available width

### Thumbnail Preview

- **Thumbnail Preview Mode** - Show enlarged preview on hover or via shortcut. Supports **Off** / **Hover** / **Shortcut** / **Hover + Shortcut** (configurable separately for List and Gallery)
- **Hover Delay** - The waiting time before preview is triggered on hover
- **Preview Shortcut** - Choose the shortcut key (Ctrl or Shift) to trigger preview, with optional **auto-close on key release**
- **Auto-Close on Leave** - Automatically close the preview when the mouse leaves the preview area
- **Initial Preview Size** - Calculation logic for preview size. Choose **Fixed Scale** or **Fit to Screen**
- **Fixed Scale** - Display preview at the configured **Zoom Scale**, with optional **Scale Limit** to restrict the maximum size
- **Fit to Screen** - Automatically calculate optimal preview size based on window size; **Fit Mode** offers **Contain** or **Cover**
- **Auto Load Large Image** - When enabled, automatically loads the high-resolution image when preview opens, replacing the blurry thumbnail (Note: consumes viewing quota)
- **Keyboard Shortcuts** - While preview is open, press Space to load the large image or cycle through preview sizes, use ← → ↑ ↓ arrow keys to navigate between thumbnails, hold Space while navigating to automatically load the large image

### Search & Tags

- **Quick Tag** - Save frequently used search tags for quick insertion into the search box, supports grouped management
  - **Interactions**
    - Left-click a tag: add/remove it, mouse wheel to cycle match modes (OR ~ orange / exclude - red), drag to reorder
    - Left-click the `[ + ]` button: open the add panel (Tag: enter name and syntax, Group: name only), the `[ ↵ ]` button inserts a line break
    - Right-click any button: open the tag editor and jump to the corresponding line, edit all tags in text format, changes sync in real time, Save to apply changes, Cancel to revert
  - **Groups**: Click the group navigation bar to switch between tag sets. Supports cross-group drag & drop (drag a tag onto a group header to categorize it)
  - **Format**: `[tag]` / `[name @ tag]` / `[name @ tag1 tag2 ...]`, use `[# name]` to create a group, use `[ _ ]` (underscore) to insert line breaks
  - [Search Guide](https://ehwiki.org/wiki/Gallery_Searching)
- **Gallery Tag Search** - Click any tag on the gallery page to automatically open the search bar and insert the tag for quick searching
  - Supports left-click to add or remove tags, mouse wheel to cycle through match modes (OR ~ Orange / Exclude - Red)
- **Tag Auto-Complete** - Provides tag suggestions in the search bar, gallery tag input, and quick tag add panel
  - Hold Ctrl/Cmd while clicking a suggestion to insert it as an exclude tag (adds a - prefix)
  - Powered by [EhTagTranslation](https://github.com/EhTagTranslation/Database) tag database, first use requires a one-time ~6MB download
- **Search Enhancements** - Double-click inside the search box to select the full tag. The search button supports right-click/Ctrl+click to open in a new tab. The clear button only clears the input and does not refresh the page
- **Gallery Categories Enhancement** - Right-click to single-select a category (auto-deselects others)

### Browsing Enhancements

- **Infinite Scroll (List)** - Automatically load the next page when you scroll to the bottom
- **More Thumbnails (Gallery)** - Automatically load more thumbnails as you scroll in the gallery page
  - Both features above support a configurable auto-load page limit (Default: 0 = Unlimited)
  - Supports continuous loading by automatically following newly loaded content, with configurable auto-load delay
  - After reaching the limit, you can still load more manually, and previous pages can also be loaded manually
- **Quick Favorite** - Add to favorites without popups, supports multiple layouts, menu sizes, and click or hover activation
- **Scrollable Thumbnails** - Transform the gallery page thumbnail area into an independent scrolling container to maintain page layout stability when viewing numerous thumbnails

### Other Features

- **Show Index** - Display an index number before each gallery title
- **Live URL Update** - Update the address bar URL in real time based on browsing progress on the search results page, making it easier to bookmark your current position
- **Show Full Title on Hover** - Display the full gallery title when hovering over truncated titles
- **EH/ExH Switch Button** - Quick switch button at the top to jump between E-Hentai and ExHentai

### Advanced Settings

- **Request Interval** - Control the **firing interval** between consecutive HTTP requests
  - Excessive requests may trigger site limits
- **Max Concurrent Requests** - Control the maximum number of simultaneous HTTP requests
  - Excessive requests may trigger site limits
- **Log Level** - Control console log verbosity for debugging and troubleshooting
- **Language** - Script UI language (Auto / English / 简体中文 / 繁体中文 / 日本語 / 한국어 / Русский)
- **Script Theme** - Controls the script interface color mode. Supports **Auto** (adapts to the page background) / **Dark** / **Light**
- **Site Limit Warning** - Automatically pauses related requests and displays a warning when the image viewing limit (509) or other site access restrictions are detected. No configuration required.
- **Settings Management** - Export Settings Backup, Restore Settings Backup, Reset Settings, Disable All Toggles

---

- The Auto Window Adaptation feature was inspired by AmadeusAI's "Wide Hentai 2019" and Owyn's "Wide ExHentai"
- The Quick Tag feature was inspired by greasy_su's "ExHentai Viewer"
- Tag Auto-Complete feature ported from [EhSyringe](https://github.com/EhTagTranslation/EhSyringe)
