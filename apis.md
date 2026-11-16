# Project Structure

```
└── docs
    └── markdown
        ├── apis
        │   ├── action.md
        │   ├── apis.md
        │   ├── assets.md
        │   ├── broadcast.md
        │   ├── context-menu.md
        │   ├── fog.md
        │   ├── grid.md
        │   ├── history.md
        │   ├── interaction.md
        │   ├── items.md
        │   ├── local.md
        │   ├── modal.md
        │   ├── notification.md
        │   ├── party.md
        │   ├── player.md
        │   ├── popover.md
        │   ├── room.md
        │   ├── scene.md
        │   ├── theme.md
        │   ├── tool.md
        │   └── viewport.md
        └── reference
            ├── billboard.md
            ├── bounding-box.md
            ├── builders.md
            ├── curve.md
            ├── dynamic-fog.md
            ├── effect.md
            ├── effects.md
            ├── filters.md
            ├── image-upload.md
            ├── image.md
            ├── item.md
            ├── items.md
            ├── label.md
            ├── light.md
            ├── line.md
            ├── manifest.md
            ├── math-2.md
            ├── math-m.md
            ├── math.md
            ├── matrix.md
            ├── metadata.md
            ├── path.md
            ├── permission.md
            ├── player.md
            ├── pointer.md
            ├── reference.md
            ├── ruler.md
            ├── scene-upload.md
            ├── shape.md
            ├── text-content.md
            ├── text.md
            ├── vector2.md
            ├── vector3.md
            └── wall.md
```

# File Contents

## docs\markdown\apis\action.md

```markdown
# Action

## `OBR.action`

An extensions action is shown in the top left of a room.

When an action is clicked a popover will be shown for that action.

The action is defined in the extensions [Manifest](../reference/manifest.md) file.

# Reference

## Methods

### `getWidth`

``` prism-code
async getWidth()
```

Get the action popovers width.

Returns a number or undefined.

------------------------------------------------------------------------

### `setWidth`

``` prism-code
async setWidth(width)
```

Set the action popovers width.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                  |
| :---: | :----: | :--------------------------- |
| width | number | The new width of the popover |

------------------------------------------------------------------------

### `getHeight`

``` prism-code
async getHeight()
```

Get the action popovers height.

Returns a number or undefined.

------------------------------------------------------------------------

### `setHeight`

``` prism-code
async setHeight(height)
```

Set the action popovers height.

**Parameters**

|  NAME  |  TYPE  | DESCRIPTION                   |
| :----: | :----: | :---------------------------- |
| height | number | The new height of the popover |

------------------------------------------------------------------------

### `getBadgeText`

``` prism-code
async getBadgeText()
```

Get the actions badge text.

Returns a string or undefined.

------------------------------------------------------------------------

### `setBadgeText`

``` prism-code
async setBadgeText(badgeText)
```

Set the actions badge text.

**Parameters**

|   NAME    |  TYPE  | DESCRIPTION                                                              |
| :-------: | :----: | :----------------------------------------------------------------------- |
| badgeText | string | The new badge text of the action. Set as `undefined` to remove the badge |

------------------------------------------------------------------------

### `getBadgeBackgroundColor`

``` prism-code
async getBadgeBackgroundColor()
```

Get the actions badge background color.

Returns a string or undefined.

------------------------------------------------------------------------

### `setBadgeBackgroundColor`

``` prism-code
async setBadgeBackgroundColor(badgeBackgroundColor)
```

Set the actions badge background color.

**Parameters**

|         NAME         |  TYPE  | DESCRIPTION                                  |
| :------------------: | :----: | :------------------------------------------- |
| badgeBackgroundColor | string | The new badge background color of the action |

------------------------------------------------------------------------

### `getIcon`

``` prism-code
async getIcon()
```

Get the actions icon.

Returns a string.

------------------------------------------------------------------------

### `setIcon`

``` prism-code
async setIcon(icon)
```

Set the actions icon.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                |
| :---: | :----: | :------------------------- |
| icon  | string | The new icon of the action |

------------------------------------------------------------------------

### `getTitle`

``` prism-code
async getTitle()
```

Get the actions title.

Returns a string.

------------------------------------------------------------------------

### `setTitle`

``` prism-code
async setTitle(title)
```

Set the actions title.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                 |
| :---: | :----: | :-------------------------- |
| title | string | The new title of the action |

------------------------------------------------------------------------

### `open`

``` prism-code
async open()
```

Open the action.

------------------------------------------------------------------------

### `close`

``` prism-code
async close()
```

Close the action.

------------------------------------------------------------------------

### `isOpen`

``` prism-code
async isOpen()
```

Returns true if the action is open

------------------------------------------------------------------------

### `onOpenChange`

``` prism-code
onOpenChange(callback);
```

**Parameters**

|   NAME   |            TYPE            | DESCRIPTION                                        |
| :------: | :------------------------: | :------------------------------------------------- |
| callback | (isOpen: boolean) =\> void | A callback for when the action is opened or closed |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onOpenChange` event with a React `useEffect`.
 * `onOpenChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.action.onOpenChange((isOpen) => {
      // React to the action opening or closing
    }),
  []
);
```

------------------------------------------------------------------------

```

## docs\markdown\apis\apis.md

```markdown
# APIs

## `OBR`

The base API to interact with Owlbear Rodeo

# Reference

**Properties**

|    NAME     |  TYPE   | DESCRIPTION                                                          |
| :---------: | :-----: | :------------------------------------------------------------------- |
|   isReady   | boolean | True if the SDK has been loaded and is ready to send messages        |
| isAvailable | boolean | True if the current site is embedded in an instance of Owlbear Rodeo |

**Example**

``` prism-code
if (OBR.isAvailable) {
  // The current site is embedded in Owlbear Rodeo
}
```

## Methods

### `onReady`

``` prism-code
onReady(callback);
```

**Parameters**

|   NAME   |    TYPE     | DESCRIPTION                               |
| :------: | :---------: | :---------------------------------------- |
| callback | () =\> void | A callback for when when the SDK is ready |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onReady` event with a React `useEffect`.
 * `onReady` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.onReady(() => {
      // interact with the SDK
    }),
  []
);
```

------------------------------------------------------------------------

## 📄️ Action

OBR.action

## 📄️ Assets

OBR.assets

## 📄️ Broadcast

OBR.broadcast

## 📄️ Context Menu

OBR.contextMenu

## 📄️ Interaction

OBR.interaction

## 📄️ Modal

OBR.modal

## 📄️ Notification

OBR.notification

## 📄️ Party

OBR.party

## 📄️ Player

OBR.player

## 📄️ Popover

OBR.popover

## 📄️ Room

OBR.room

## 🗃️ Scene

5 items

## 📄️ Theme

OBR.theme

## 📄️ Tool

OBR.tool

## 📄️ Viewport

OBR.viewport

```

## docs\markdown\apis\assets.md

```markdown
# Assets

## `OBR.assets`

The assets API allows you to interact with the current users storage.

# Reference

## Methods

### `uploadImages`

``` prism-code
async uploadImages(images, typeHint)
```

Open a folder picker to allow a user to upload the given `images`.

**Parameters**

|   NAME   |               TYPE                | DESCRIPTION                                                 |
| :------: | :-------------------------------: | :---------------------------------------------------------- |
|  images  |  [ImageUpload](#imageupload)\[\]  | The images to upload                                        |
| typeHint | [ImageAssetType](#imageassettype) | An optional hint for which image type to use when uploading |

**Example**

Upload images from a HTMLInputElement element using the [ImageUploadBuilder](../reference/image-upload.md)

``` prism-code
import OBR, { buildImageUpload } from "@owlbear-rodeo/sdk";

<input
  type="file"
  onChange={async (e) => {
    const files = e.target.files;
    if (files) {
      const uploads = [];
      for (const file of files) {
        // Note: we need to create a new file from the contents of the input file.
        // This needs to be done due to browser security policies for sharing files
        const data = await file.arrayBuffer();
        const newFile = new File([data], file.name, { type: file.type });
        uploads.push(buildImageUpload(newFile).build());
      }
      await OBR.assets.uploadImages(uploads);
    }
  }}
/>;
```

------------------------------------------------------------------------

### `uploadScenes`

``` prism-code
async uploadScenes(scenes, disableShowScenes)
```

Open a folder picker to allow a user to upload the given `scenes`.

**Parameters**

|       NAME        |              TYPE               | DESCRIPTION                                                                  |
| :---------------: | :-----------------------------: | :--------------------------------------------------------------------------- |
|      scenes       | [SceneUpload](#sceneupload)\[\] | The scenes to upload                                                         |
| disableShowScenes |             boolean             | An optional flag to disable showing the Atlas after uploading the new scenes |

**Examples**

Upload a new empty scene with a hexagon grid using the [SceneUploadBuilder](../reference/scene-upload.md)

``` prism-code
import OBR, { buildSceneUpload } from "@owlbear-rodeo/sdk";

const scene = buildSceneUpload()
  .gridType("HEX_HORIZONTAL")
  .name("Hex Scene")
  .build();
OBR.assets.uploadScenes([scene]);
```

Upload a new scene with a map from a HTMLInputElement

``` prism-code
import OBR, { buildSceneUpload, buildImageUpload } from "@owlbear-rodeo/sdk";

<input
  type="file"
  onChange={async (e) => {
    const files = e.target.files;
    if (files) {
      const file = files[0];
      // Note: we need to create a new file from the contents of the input file.
      // This needs to be done due to browser security policies for sharing files
      const data = await file.arrayBuffer();
      const newFile = new File([data], file.name, { type: file.type });
      const image = buildImageUpload(newFile).build();
      const scene = buildSceneUpload()
        .baseMap(image)
        .name("Image Scene")
        .build();
      await OBR.assets.uploadScenes([scene]);
    }
  }}
/>;
```

------------------------------------------------------------------------

### `downloadImages`

``` prism-code
async downloadImages(multiple, defaultSearch, typeHint)
```

Open an image picker to allow a user to share images with the extension.

Returns an array of [ImageDownload](#imagedownload)s

**Parameters**

|     NAME      |               TYPE                | DESCRIPTION                                                        |
| :-----------: | :-------------------------------: | :----------------------------------------------------------------- |
|   multiple    |              boolean              | An optional boolean, if true the user can pick multiple images     |
| defaultSearch |              string               | An optional default value for the search input in the image picker |
|   typeHint    | [ImageAssetType](#imageassettype) | An optional hint for which image type to select                    |

------------------------------------------------------------------------

### `downloadScenes`

``` prism-code
async downloadScenes(multiple, defaultSearch)
```

Open a scene picker to allow a user to share scenes with the extension.

Returns an array of [SceneDownload](#scenedownload)s

**Parameters**

|     NAME      |  TYPE   | DESCRIPTION                                                        |
| :-----------: | :-----: | :----------------------------------------------------------------- |
|   multiple    | boolean | An optional boolean, if true the user can pick multiple scenes     |
| defaultSearch | string  | An optional default value for the search input in the scene picker |

------------------------------------------------------------------------

## Type Definitions

### ImageUpload

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |                     TYPE                     | DESCRIPTION                                                                                                                                                                                |
| :----------: | :------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     file     |                 File \| Blob                 | The image file to upload                                                                                                                                                                   |
|     name     |                    string                    | The name of the new image, if left blank and a File input is used the `file.name` property will be used                                                                                    |
|     grid     | [ImageGrid](../reference/image.md#imagegrid) | The default grid settings for this image                                                                                                                                                   |
|   rotation   |                    number                    | The default rotation for this image in degrees                                                                                                                                             |
|    scale     |      [Vector2](../reference/vector2.md)      | The default scale for this image                                                                                                                                                           |
|     text     | [TextContent](../reference/text-content.md)  | The text displayed over the image                                                                                                                                                          |
| textItemType |              "LABEL" \| "TEXT"               | The type of text to use for this image. The "LABEL" option will display the text as a label on the bottom of the image. The "TEXT" option will display the text over the top of the image. |
|   visible    |                   boolean                    | The default visible settings for this image                                                                                                                                                |
|    locked    |                   boolean                    | The default locked settings for this image                                                                                                                                                 |
| description  |                    string                    | An optional description of the item used by assistive technology                                                                                                                           |

------------------------------------------------------------------------

### SceneUpload

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME    |               TYPE               | DESCRIPTION                                                          |
| :-------: | :------------------------------: | :------------------------------------------------------------------- |
|   name    |              string              | The name of the scene                                                |
|   grid    |      [Grid](grid.md#grid-1)      | The grid for the scene                                               |
|    fog    |       [Fog](fog.md#fog-1)        | The fog settings for the scene                                       |
|   items   | [Item](../reference/item.md)\[\] | The default items for the scene                                      |
|  baseMap  |   [ImageUpload](#imageupload)    | An optional map image that will be used as the base for this scene   |
| thumbnail |           File \| Blob           | An optional image file to use as the initial thumbnail for the scene |

------------------------------------------------------------------------

### ImageDownload

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |                        TYPE                        | DESCRIPTION                                                                                                                                                                                |
| :----------: | :------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     name     |                       string                       | The name of the image                                                                                                                                                                      |
|    image     | [ImageContent](../reference/image.md#imagecontent) | The image contents                                                                                                                                                                         |
|     grid     |    [ImageGrid](../reference/image.md#imagegrid)    | The grid settings for this image                                                                                                                                                           |
|   rotation   |                       number                       | The rotation for this image in degrees                                                                                                                                                     |
|    scale     |         [Vector2](../reference/vector2.md)         | The scale for this image                                                                                                                                                                   |
|     text     |    [TextContent](../reference/text-content.md)     | The text displayed over the image                                                                                                                                                          |
| textItemType |                 "LABEL" \| "TEXT"                  | The type of text to use for this image. The "LABEL" option will display the text as a label on the bottom of the image. The "TEXT" option will display the text over the top of the image. |
|   visible    |                      boolean                       | The visible settings for this image                                                                                                                                                        |
|    locked    |                      boolean                       | The locked settings for this image                                                                                                                                                         |
| description  |                       string                       | An optional description of the item used by assistive technology                                                                                                                           |
|     type     |         [ImageAssetType](#imageassettype)          | The type of this image                                                                                                                                                                     |

------------------------------------------------------------------------

### SceneDownload

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |               TYPE               | DESCRIPTION                    |
| :---: | :------------------------------: | :----------------------------- |
| name  |              string              | The name of the scene          |
| grid  |      [Grid](grid.md#grid-1)      | The grid for the scene         |
|  fog  |       [Fog](fog.md#fog-1)        | The fog settings for the scene |
| items | [Item](../reference/item.md)\[\] | The items for the scene        |

------------------------------------------------------------------------

### ImageAssetType

|  TYPE  | values                                                              |
| :----: | :------------------------------------------------------------------ |
| string | "MAP" \| "PROP" \| "MOUNT" \| "CHARACTER" \| "ATTACHMENT" \| "NOTE" |

------------------------------------------------------------------------

```

## docs\markdown\apis\broadcast.md

```markdown
# Broadcast

## `OBR.broadcast`

The broadcast api allows you to send ephemeral messages to other players in the room.

# Reference

## Methods

### `sendMessage`

``` prism-code
async sendMessage(channel, data)
```

Send a message to other players on a given channel.

**Parameters**

|  NAME   |                 TYPE                  |                          DESCRIPTION                           |
| :-----: | :-----------------------------------: | :------------------------------------------------------------: |
| channel |                string                 |                     The channel to send to                     |
|  data   |                  any                  | Any value that can be JSON serialized. Limited to 16KB in size |
| options | [BroadcastOptions](#broadcastoptions) |     Options to control how the message is sent (optional)      |

**Example**

``` prism-code
OBR.broadcast.sendMessage("rodeo.owlbear.example", "Hello, World!");
```

------------------------------------------------------------------------

### `onMessage`

``` prism-code
onMessage(channel, callback);
```

**Parameters**

|   NAME   |                        TYPE                         | DESCRIPTION                                                               |
| :------: | :-------------------------------------------------: | :------------------------------------------------------------------------ |
| channel  |                       string                        | The channel to receive from                                               |
| callback | (event: [BroadcastEvent](#broadcastevent)) =\> void | A callback for when a message is sent from another player on this channel |

Returns a function that when called will unsubscribe from message events for this channel.

**Example**

``` prism-code
/**
 * Use an `onMessage` event with a React `useEffect`.
 * `onMessage` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.broadcast.onMessage("rodeo.owlbear.example", (event) => {
      // Use the data from the event
    }),
  []
);
```

------------------------------------------------------------------------

## Type Definitions

### BroadcastEvent

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |  TYPE  | DESCRIPTION                                        |
| :----------: | :----: | :------------------------------------------------- |
|     data     |  any   | The data for this event                            |
| connectionId | string | The connection id of the player who sent the event |

------------------------------------------------------------------------

### BroadcastOptions

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |             TYPE             | DESCRIPTION                                                                                                                                                                               |
| :---------: | :--------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| destination | "REMOTE" \| "LOCAL" \| "ALL" | Choose where the broadcast is sent. "REMOTE" sends to other connected players, "LOCAL" will send to the current player and "ALL" will send to all connected players. Defaults to "REMOTE" |

```

## docs\markdown\apis\context-menu.md

```markdown
# Context Menu

## `OBR.contextMenu`

A context menu is shown when an item is selected, this API allows you to extend that menu with custom buttons.

# Reference

## Methods

### `create`

``` prism-code
async create(contextMenu)
```

Create a context menu item.

**Parameters**

|    NAME     |                TYPE                 | DESCRIPTION                     |
| :---------: | :---------------------------------: | :------------------------------ |
| contextMenu | [ContextMenuItem](#contextmenuitem) | The context menu item to create |

------------------------------------------------------------------------

### `remove`

``` prism-code
async remove(id)
```

Remove a context menu item.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                          |
| :---: | :----: | :----------------------------------- |
|  id   | string | The ID of the context menu to remove |

------------------------------------------------------------------------

## Type Definitions

### ContextMenuItem

A single context menu item.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |                        TYPE                         | DESCRIPTION                                                             |
| :------: | :-------------------------------------------------: | :---------------------------------------------------------------------- |
|    id    |                       string                        | The ID of this context menu item                                        |
|  icons   |       [ContextMenuIcon](#contextmenuicon)\[\]       | An array of icons to use                                                |
| onClick  | [ContextMenuClickHandler](#contextmenuclickhandler) | A callback function triggered when the context menu item is clicked     |
| shortcut |                       string                        | An optional key combination to use as a shortcut                        |
|  embed   |        [ContextMenuEmbed](#contextmenuembed)        | An optional embedded url to provide custom controls in the context menu |

------------------------------------------------------------------------

### ContextMenuIcon

An icon for a context menu item.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |                      TYPE                       | DESCRIPTION                                                |
| :----: | :---------------------------------------------: | :--------------------------------------------------------- |
|  icon  |                     string                      | The url of the icon as either a relative or absolute path  |
| label  |                     string                      | The label to use for the tooltip of the icon               |
| filter | [ContextMenuIconFilter](#contextmenuiconfilter) | An optional filter to control when this icon will be shown |

------------------------------------------------------------------------

### ContextMenuIconFilter

A filter to control when an icon will be shown. If this filter returns true then this icon will be shown. If no filter returns true then the context menu item won't be shown.

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |                                        TYPE                                        | DESCRIPTION                                                                                                  |
| :---------: | :--------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------- |
|     min     |                                       number                                       | An optional minimum number of items selected, defaults to 1                                                  |
|     max     |                                       number                                       | An optional maximum number of items selected                                                                 |
| permissions | ("UPDATE" \| "DELETE" \| "CREATE" \| [Permission](../reference/permission.md))\[\] | An optional array of permissions needed for the selected items, defaults to no permissions needed            |
|    roles    |                               ("GM" \| "PLAYER")\[\]                               | An optional array of roles needed for the player, defaults to no role needed                                 |
|    every    |                 [KeyFilter](../reference/filters.md#keyfilter)\[\]                 | An optional array of filters to run on the selected items. Every item must pass this filter for a success    |
|    some     |                 [KeyFilter](../reference/filters.md#keyfilter)\[\]                 | An optional array of filters to run on the selected items. Only one item must pass this filter for a success |

------------------------------------------------------------------------

### ContextMenuClickHandler

A callback when a context menu item is clicked.

|   TYPE   |
| :------: |
| function |

**Parameters**

|   NAME    |                   TYPE                    | DESCRIPTION                  |
| :-------: | :---------------------------------------: | :--------------------------- |
|  context  | [ContextMenuContext](#contextmenucontext) | The context for this menu    |
| elementId |                  string                   | The ID of the button clicked |

------------------------------------------------------------------------

### ContextMenuContext

The context for a menu item.

|  TYPE  |
| :----: |
| object |

**Properties**

|      NAME       |                    TYPE                     | DESCRIPTION                                   |
| :-------------: | :-----------------------------------------: | :-------------------------------------------- |
|      items      |      [Item](../reference/item.md)\[\]       | An array of Items that are currently selected |
| selectionBounds | [BoundingBox](../reference/bounding-box.md) | A bounding box for the current selection      |

------------------------------------------------------------------------

### ContextMenuEmbed

An embedded view in the context menu popup.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |  TYPE  | DESCRIPTION                               |
| :----: | :----: | :---------------------------------------- |
|  url   | string | The url of the site to embed              |
| height | number | An optional height of the embed in pixels |

------------------------------------------------------------------------

```

## docs\markdown\apis\fog.md

```markdown
# Fog

## `OBR.scene.fog`

Interact with the base fog settings for this scene.

# Reference

## Methods

### `getColor`

``` prism-code
async getColor()
```

Get the color of the scenes fog.

Returns a string.

------------------------------------------------------------------------

### `setColor`

``` prism-code
async setColor(color)
```

Set the color of the scenes fog.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION              |
| :---: | :----: | :----------------------- |
| color | string | The new color of the fog |

------------------------------------------------------------------------

### `getStrokeWidth`

``` prism-code
async getStrokeWidth()
```

Get the stroke width of the scenes fog.

Returns a number.

------------------------------------------------------------------------

### `setStrokeWidth`

``` prism-code
async setStrokeWidth(width)
```

Set the stroke width of the scenes fog.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION              |
| :---: | :----: | :----------------------- |
| width | number | The new width fog stroke |

------------------------------------------------------------------------

### `getFilled`

``` prism-code
async getFilled()
```

Returns true if the scene if filled with fog.

------------------------------------------------------------------------

### `setFilled`

``` prism-code
async setFilled(filled)
```

Set the filled state of the scenes fog.

**Parameters**

|  NAME  |  TYPE   | DESCRIPTION                     |
| :----: | :-----: | :------------------------------ |
| filled | boolean | The new filled state of the fog |

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |            TYPE             | DESCRIPTION                         |
| :------: | :-------------------------: | :---------------------------------- |
| callback | (fog: [Fog](#fog)) =\> void | A callback for when the fog changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.scene.fog.onChange((fog) => {
      // React to fog changes
    }),
  []
);
```

------------------------------------------------------------------------

## Type Definitions

### Fog

The fog state for a scene.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |         TYPE          | DESCRIPTION                  |
| :----: | :-------------------: | :--------------------------- |
| filled |        boolean        | Is the fog filling the scene |
| style  | [FogStyle](#fogstyle) | The style of the fog         |

------------------------------------------------------------------------

### FogStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |  TYPE  | DESCRIPTION                         |
| :---------: | :----: | :---------------------------------- |
|    color    | string | The color of the fog                |
| strokeWidth | number | An optional width of the fog stroke |

------------------------------------------------------------------------

```

## docs\markdown\apis\grid.md

```markdown
# Grid

## `OBR.scene.grid`

Interact with the scene's grid.

# Reference

## Methods

### `getDpi`

``` prism-code
async getDpi()
```

Get the dots per inch (DPI) of the grid. Determines the resolution of one grid cell. For square grids this represents both the width and height of the grid cell. For vertically oriented hex grids this is the width of the grid cell. For horizontally oriented hex grids this is the height of the grid cell. For isometric and dimetric grids this is the post-transform height of the grid cell.

returns a number.

------------------------------------------------------------------------

### `getScale`

``` prism-code
async getScale()
```

Get the current scale of the grid.

Returns a [GridScale](#gridscale).

------------------------------------------------------------------------

### `setScale`

``` prism-code
async setScale(scale)
```

Set the scale of the grid as a raw string.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                   |
| :---: | :----: | :---------------------------- |
| scale | string | The new raw scale of the grid |

**Example**

``` prism-code
OBR.scene.grid.setScale("5ft");
```

------------------------------------------------------------------------

### `getColor`

``` prism-code
async getColor()
```

Get the current color of the grid.

Returns a [GridColor](#gridcolor).

------------------------------------------------------------------------

### `setColor`

``` prism-code
async setColor(color)
```

Set the color of the grid.

**Parameters**

| NAME  |          TYPE           | DESCRIPTION               |
| :---: | :---------------------: | :------------------------ |
| color | [GridColor](#gridcolor) | The new color of the grid |

**Example**

``` prism-code
OBR.scene.grid.setColor("DARK");
```

------------------------------------------------------------------------

### `getOpacity`

``` prism-code
async getOpacity()
```

Get the current opacity of the grid between 0 and 1.

Returns a number.

------------------------------------------------------------------------

### `setOpacity`

``` prism-code
async setOpacity(opacity)
```

Set the opacity of the grid.

**Parameters**

|  NAME   |  TYPE  | DESCRIPTION                                 |
| :-----: | :----: | :------------------------------------------ |
| opacity | number | The new opacity of the grid between 0 and 1 |

------------------------------------------------------------------------

### `getType`

``` prism-code
async getType()
```

Get the current grid type.

Returns a [GridType](#gridtype).

------------------------------------------------------------------------

### `setType`

``` prism-code
async setType(type)
```

Set the type of the grid.

**Parameters**

| NAME  |         TYPE          | DESCRIPTION              |
| :---: | :-------------------: | :----------------------- |
| type  | [GridType](#gridtype) | The new type of the grid |

**Example**

``` prism-code
OBR.scene.grid.setType("HEX_VERTICAL");
```

------------------------------------------------------------------------

### `getLineType`

``` prism-code
async getLineType()
```

Get the current grid line type.

Returns a [GridLineType](#gridlinetype).

------------------------------------------------------------------------

### `setLineType`

``` prism-code
async setLineType(lineType)
```

Set the type of the grid line.

**Parameters**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
| lineType | [GridLineType](#gridlinetype) | The new type of the grid line |

**Example**

``` prism-code
OBR.scene.grid.setLineType("DASHED");
```

------------------------------------------------------------------------

### `getMeasurement`

``` prism-code
async getMeasurement()
```

Get the current grid measurement type.

Returns a [GridMeasurement](#gridmeasurement).

------------------------------------------------------------------------

### `setMeasurement`

``` prism-code
async setMeasurement(measurement)
```

Set the measurement type of the grid.

**Parameters**

|    NAME     |                TYPE                 | DESCRIPTION                          |
| :---------: | :---------------------------------: | :----------------------------------- |
| measurement | [GridMeasurement](#gridmeasurement) | The new measurement type of the grid |

**Example**

``` prism-code
OBR.scene.grid.setMeasurement("EUCLIDEAN");
```

------------------------------------------------------------------------

### `getLineWidth`

``` prism-code
async getLineWidth()
```

Get the current line width of the grid in pixels.

Returns a number.

------------------------------------------------------------------------

### `setLineWidth`

``` prism-code
async setLineWidth(lineWidth)
```

Set the width of the grid lines.

**Parameters**

|   NAME    |  TYPE  | DESCRIPTION                                               |
| :-------: | :----: | :-------------------------------------------------------- |
| lineWidth | number | The new line width of the grid, must be greater than zero |

------------------------------------------------------------------------

### `snapPosition`

``` prism-code
async snapPosition(position, snappingSensitivity, useCorners)
```

Snap a [Vector2](../reference/vector2.md) position to the nearest grid cell using the current grid settings.

Returns a [Vector2](../reference/vector2.md) with the new position.

**Parameters**

|        NAME         |                TYPE                | DESCRIPTION                                                                                                                                                                  |
| :-----------------: | :--------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|      position       | [Vector2](../reference/vector2.md) | The position to snap                                                                                                                                                         |
| snappingSensitivity |               number               | An optional number between 0 and 1. Leave undefined to use the users snapping preference. A value of 0 will disable snapping. A value of 1 will completely snap to the grid. |
|     useCorners      |              boolean               | An optional boolean. If true the corners of the grid cell will be valid snap locations. Defaults to true.                                                                    |
|      useCenter      |              boolean               | An optional boolean. If true the center of the grid cell will be a valid snap location. Defaults to true.                                                                    |

------------------------------------------------------------------------

### `getDistance`

``` prism-code
async getDistance(from, to)
```

Get the distance between two [Vector2](../reference/vector2.md)s on the Scenes grid.

Returns the shortest distance between the two inputs using the current [GridMeasurement](#gridmeasurement) for the scene. When set to "EUCLIDEAN" this will be the exact distance. For all other measurement types this will be an integer of how many grid cells were traversed.

**Parameters**

| NAME  |                TYPE                | DESCRIPTION                  |
| :---: | :--------------------------------: | :--------------------------- |
| from  | [Vector2](../reference/vector2.md) | The start position in pixels |
|  to   | [Vector2](../reference/vector2.md) | The end position in pixels   |

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |              TYPE              | DESCRIPTION                          |
| :------: | :----------------------------: | :----------------------------------- |
| callback | (grid: [Grid](#grid)) =\> void | A callback for when the grid changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.scene.grid.onChange((grid) => {
      // React to grid changes
    }),
  []
);
```

------------------------------------------------------------------------

## Type Definitions

### Grid

The grid for a scene.

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |                TYPE                 | DESCRIPTION                                                                                                                                                                                                                                                                                         |
| :---------: | :---------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     dpi     |               number                | Dots per inch of the scene. Determines the resolution of one grid cell. For square grids this represents both the width and height of the grid cell. For vertically oriented hex grids this is the width of the grid cell. For horizontally oriented hex grids this is the height of the grid cell. |
|    style    |       [GridStyle](#gridstyle)       | The style of the grid                                                                                                                                                                                                                                                                               |
|    type     |        [GridType](#gridtype)        | The type of the grid                                                                                                                                                                                                                                                                                |
| measurement | [GridMeasurement](#gridmeasurement) | The measurement type of the grid                                                                                                                                                                                                                                                                    |
|    scale    |               string                | The raw scale of the grid. For example `5ft`                                                                                                                                                                                                                                                        |

------------------------------------------------------------------------

### GridStyle

The style of a grid.

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |             TYPE              | DESCRIPTION                                  |
| :---------: | :---------------------------: | :------------------------------------------- |
|  lineType   | [GridLineType](#gridlinetype) | The style of the grid line                   |
| lineOpacity |            number             | The opacity of the grid line between 0 and 1 |
|  lineColor  |    [GridColor](#gridcolor)    | The color of the grid line                   |
|  lineWidth  |            number             | The width of the grid line                   |

------------------------------------------------------------------------

### GridLineType

The type of a grid line.

|  TYPE  | values                          |
| :----: | :------------------------------ |
| string | "SOLID" \| "DASHED" \| "DOTTED" |

------------------------------------------------------------------------

### GridColor

The color of a grid line.

|  TYPE  | values                                     |
| :----: | :----------------------------------------- |
| string | "DARK" \| "LIGHT" \| "HIGHLIGHT" \| string |

------------------------------------------------------------------------

### GridType

The type of a grid.

|  TYPE  | values                                                                      |
| :----: | :-------------------------------------------------------------------------- |
| string | "SQUARE" \| "HEX_VERTICAL" \| "HEX_HORIZONTAL" \| "DIMETRIC" \| "ISOMETRIC" |

------------------------------------------------------------------------

### GridMeasurement

The type of a grid measurement.

|  TYPE  | values                                                     |
| :----: | :--------------------------------------------------------- |
| string | "CHEBYSHEV" \| "ALTERNATING" \| "EUCLIDEAN" \| "MANHATTAN" |

------------------------------------------------------------------------

### GridScale

The scale of a grid.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |                TYPE                 | DESCRIPTION                                       |
| :----: | :---------------------------------: | :------------------------------------------------ |
|  raw   |               string                | The raw grid scale. For example `5ft`             |
| parsed | [ParsedGridScale](#parsedgridscale) | The raw grid scale parsed into a more usable form |

### ParsedGridScale

The raw grid scale parsed into a more usable form

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME    |  TYPE  | DESCRIPTION                                                           |
| :--------: | :----: | :-------------------------------------------------------------------- |
| multiplier | number | The number multiplier of the scale. For example `5` for a `5ft` scale |
|    unit    | string | The unit of the scale. For example `ft` for a `5ft` scale             |
|   digits   | number | The precision of the scale. For example `2` for a `5.00ft` scale      |

------------------------------------------------------------------------

```

## docs\markdown\apis\history.md

```markdown
# History

## `OBR.scene.history`

Interact with the undo/redo stack of the scene.

# Reference

## Methods

### `undo`

``` prism-code
async undo()
```

Undo the previous action.

------------------------------------------------------------------------

### `redo`

``` prism-code
async redo()
```

Redo the an action that was undone.

------------------------------------------------------------------------

### `canUndo`

``` prism-code
async canUndo()
```

Returns true if there is an action on the undo stack.

------------------------------------------------------------------------

### `canRedo`

``` prism-code
async canRedo()
```

Returns true if there is an action on the redo stack.

------------------------------------------------------------------------

```

## docs\markdown\apis\interaction.md

```markdown
# Interaction

## `OBR.interaction`

Manage interactions with Owlbear Rodeo.

An interaction allows you to provide high frequency updates to Owlbear Rodeo without needing to worry about networking.

Interactions in Owlbear Rodeo use an interpolated snapshot system where high frequency updates are applied in real-time locally but sampled at a lower frequency to be sent over the network to other players.

On the receiving end low frequency snapshots are buffered and interpolated to ensure smooth playback.

Not all item values are available when using an interaction. See [here](#interactive-values) for available values.

# Reference

## Methods

### `startItemInteraction`

``` prism-code
async startItemInteraction(items)
```

Start an interaction with an item or a list of items in a scene.

These items can be newly created or be references to already existing items in the scene.

Interaction Time Limit

To prevent accidental network usage interactions expire after 30 seconds.

When this happens the interaction will stop sending network traffic but new updates will still be applied locally.

**Parameters**

|   NAME    |                               TYPE                               |            DESCRIPTION             |
| :-------: | :--------------------------------------------------------------: | :--------------------------------: |
| baseState | [Item](../reference/item.md) \| [Item](../reference/item.md)\[\] | The item or items to interact with |

Returns an [InteractionManager](#interactionmanager) that can be used to update and stop this interaction.

**Example**

``` prism-code
/**
 * Create a pointer tool mode that starts an interaction on drag start,
 * updates that interaction on drag move and stops the interaction
 * on drag end/cancel.
 */
let interaction = null;
OBR.tool.createMode({
  id: "com.example.pointer",
  icons: [
    {
      icon: "/icon.svg",
      label: "Custom Pointer",
      filter: {
        activeTools: ["rodeo.owlbear.tools/pointer"],
      },
    },
  ],
  async onToolDragStart(_, event) {
    const pointer = buildPointer().position(event.pointerPosition).build();
    interaction = await OBR.interaction.startItemInteraction(pointer);
  },
  onToolDragMove(_, event) {
    if (interaction) {
      const [update] = interaction;
      update((pointer) => {
        pointer.position = event.pointerPosition;
      });
    }
  },
  onToolDragEnd() {
    if (interaction) {
      const [_, stop] = interaction;
      stop();
    }
    interaction = null;
  },
  onToolDragCancel() {
    if (interaction) {
      const [_, stop] = interaction;
      stop();
    }
    interaction = null;
  },
});
```

------------------------------------------------------------------------

## Type Definitions

### InteractionManager

| TYPE  |
| :---: |
| array |

**Properties**

| INDEX |  NAME  |           TYPE            | DESCRIPTION                                        |
| :---: | :----: | :-----------------------: | :------------------------------------------------- |
|   0   | update | DispatchInteractionUpdate | A function to dispatch updates to this interaction |
|   1   |  stop  |         function          | A function to stop the interaction                 |

------------------------------------------------------------------------

### DispatchInteractionUpdate

Interaction's use Immer to provide updates. This function represents an Immer producer that provides a recipe for making immutable updates.

|   TYPE   |
| :------: |
| function |

|  NAME  |       TYPE        | DESCRIPTION                                                             |
| :----: | :---------------: | :---------------------------------------------------------------------- |
| update | UpdateInteraction | A callback to apply an update to the previous state of this interaction |

------------------------------------------------------------------------

### UpdateInteraction

An Immer recipe for updating the current state of an interaction.

|   TYPE   |
| :------: |
| function |

| NAME  | TYPE  | DESCRIPTION                         |
| :---: | :---: | :---------------------------------- |
| draft | Draft | An immer draft of the current state |

------------------------------------------------------------------------

## Interactive Values

When you update a value using an interaction a faster rendering path will be used. This fast path works by skipping the processing of any hierarchy data and updating values directly on the renderer. Because of this method not all parameters are available when changing values in an interaction.

Below is a list of items and the values that can be updated in an interaction:

### [Item](../reference/item.md)

|   NAME   |                TYPE                | DESCRIPTION                          |
| :------: | :--------------------------------: | :----------------------------------- |
| position | [Vector2](../reference/vector2.md) | The position of this item            |
| rotation |               number               | The rotation of this item in degrees |
|  scale   | [Vector2](../reference/vector2.md) | The scale of this item               |

### [Curve](../reference/curve.md)

|  NAME  |                  TYPE                  | DESCRIPTION                |
| :----: | :------------------------------------: | :------------------------- |
| points | [Vector2](../reference/vector2.md)\[\] | The list of points to draw |

### [Image](../reference/image.md)

| NAME  |                        TYPE                        | DESCRIPTION                                        |
| :---: | :------------------------------------------------: | :------------------------------------------------- |
| image | [ImageContent](../reference/image.md#imagecontent) | Only the `width` and `height` of the image content |
| grid  |    [ImageGrid](../reference/image.md#imagegrid)    | The grid scale of the image                        |

### [Label](../reference/label.md)

| NAME  |                    TYPE                     | DESCRIPTION                         |
| :---: | :-----------------------------------------: | :---------------------------------- |
| text  | [TextContent](../reference/text-content.md) | Only the `plainText` can be updated |

### [Line](../reference/line.md)

|     NAME      |                TYPE                | DESCRIPTION                    |
| :-----------: | :--------------------------------: | :----------------------------- |
| startPosition | [Vector2](../reference/vector2.md) | The start position of the line |
|  endPosition  | [Vector2](../reference/vector2.md) | The end position of the line   |

### [Path](../reference/path.md)

|   NAME   |              TYPE               | DESCRIPTION                  |
| :------: | :-----------------------------: | :--------------------------- |
| commands | [PathCommand](#pathcommand)\[\] | The list of drawing commands |

### [Ruler](../reference/ruler.md)

|     NAME      |                TYPE                | DESCRIPTION                       |
| :-----------: | :--------------------------------: | :-------------------------------- |
| startPosition | [Vector2](../reference/vector2.md) | The start position of the ruler   |
|  endPosition  | [Vector2](../reference/vector2.md) | The end position of the ruler     |
|  measurement  |               string               | The value to display on the ruler |

### [Shape](../reference/shape.md)

|  NAME  |  TYPE  | DESCRIPTION             |
| :----: | :----: | :---------------------- |
| width  | number | The width of the shape  |
| height | number | The height of the shape |

--

```

## docs\markdown\apis\items.md

```markdown
# Items

## `OBR.scene.items`

An [Item](../reference/item.md) is the basic building block of everything shown in a Scene.

For all available items see [here](../reference/items.md).

# Reference

## Methods

### `getItems`

``` prism-code
async getItems(filter)
```

Get then current items in the scene.

**Parameters**

|  NAME  |           TYPE            | DESCRIPTION                                   |
| :----: | :-----------------------: | :-------------------------------------------- |
| filter | [ItemFilter](#itemfilter) | An optional filter to run on the scenes items |

**Example**

Get items with the given ids.

``` prism-code
const uuid = "55c04fba-9fa3-483b-8cf8-287737cbea9b";
const items = await OBR.scene.items.getItems([uuid]);
```

Get all images.

``` prism-code
import { isImage } from "@owlbear-rodeo/sdk";

const images = await OBR.scene.items.getItems(isImage);
```

Get all images on the Character layer

``` prism-code
import { isImage } from "@owlbear-rodeo/sdk";

const characters = await OBR.scene.items.getItems(
  (item) => item.layer === "CHARACTER" && isImage(item)
);
```

Get all images on the Character layer using Typescript

``` prism-code
import { Image, isImage } from "@owlbear-rodeo/sdk";

const characters = await OBR.scene.items.getItems(
  (item): item is Image => item.layer === "CHARACTER" && isImage(item)
);
```

------------------------------------------------------------------------

### `updateItems`

``` prism-code
async updateItems(filterOrItems, update)
```

Update existing items in the scene.

To track changes and ensure immutability the update function uses an Immer `WritableDraft`.

**Parameters**

|     NAME      |                                TYPE                                 | DESCRIPTION                                                                              |
| :-----------: | :-----------------------------------------------------------------: | :--------------------------------------------------------------------------------------- |
| filterOrItems |    [ItemFilter](#itemfilter) \| [Item](../reference/item.md)\[\]    | Either a filter or a list of items to update                                             |
|    update     | (draft: WritableDraft\<[Item](../reference/item.md)\[\]\>) =\> void | An update function that allows you to update an Immer `WritableDraft` of the input items |

**Example**

Lock all images

``` prism-code
import { isImage } from "@owlbear-rodeo/sdk";

await OBR.scene.items.updateItems(isImage, (images) => {
  for (let image of images) {
    image.locked = true;
  }
});
```

Turn all shapes pink

``` prism-code
import { isShape } from "@owlbear-rodeo/sdk";

await OBR.scene.items.updateItems(isShape, (shapes) => {
  for (let shape of shapes) {
    shape.style.fillColor = "pink";
  }
});
```

Hide all attachments

``` prism-code
OBR.scene.items.updateItems(
  (item) => item.layer === "ATTACHMENT",
  (items) => {
    for (let item of items) {
      item.visible = false;
    }
  }
);
```

Hide selected items when clicking a context menu item

``` prism-code
OBR.contextMenu.create({
  id: "rodeo.owlbear.example",
  icons: [
    {
      icon: "icon.svg",
      label: "Example",
    },
  ],
  onClick(context) {
    OBR.scene.items.updateItems(context.items, (items) => {
      for (let item of items) {
        item.visible = false;
      }
    });
  },
});
```

------------------------------------------------------------------------

### `addItems`

``` prism-code
async addItems(items)
```

Add new items to the scene.

To create new items you can use the item [Builders](../reference/builders.md).

**Parameters**

| NAME  |               TYPE               | DESCRIPTION            |
| :---: | :------------------------------: | :--------------------- |
| items | [Item](../reference/item.md)\[\] | A list of items to add |

**Example**

Add a circle shape to the scene

``` prism-code
import OBR, { buildShape } from "@owlbear-rodeo/sdk";

const item = buildShape().width(10).height(10).shapeType("CIRCLE").build();
OBR.scene.items.addItems([item]);
```

------------------------------------------------------------------------

### `deleteItems`

``` prism-code
async deleteItems(ids)
```

Delete existing items by their IDs.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                            |
| :---: | :--------: | :------------------------------------- |
|  ids  | string\[\] | A list of items to delete by their IDs |

**Example**

Delete selected items when clicking a context menu item

``` prism-code
OBR.contextMenu.create({
  id: "rodeo.owlbear.example",
  icons: [
    {
      icon: "icon.svg",
      label: "Example",
    },
  ],
  onClick(context) {
    const ids = context.items.map((item) => item.id);
    OBR.scene.items.deleteItems(ids);
  },
});
```

------------------------------------------------------------------------

### `getItemAttachments`

``` prism-code
async getItemAttachments(ids)
```

Get all items, attachments and sub-attachments for a set of item IDs.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                             |
| :---: | :--------: | :-------------------------------------- |
|  ids  | string\[\] | A list of items to look up by their IDs |

Returns a list of [Items](../reference/item.md).

**Example**

Delete selected items and their attachments when clicking a context menu item

``` prism-code
OBR.contextMenu.create({
  id: "rodeo.owlbear.example",
  icons: [
    {
      icon: "icon.svg",
      label: "Example",
    },
  ],
  async onClick(context) {
    const ids = context.items.map((item) => item.id);
    const allItems = await OBR.scene.items.getItemAttachments(ids);
    const allIds = allItems.map((item) => item.id);
    OBR.scene.items.deleteItems(allIds);
  },
});
```

------------------------------------------------------------------------

### `getItemBounds`

``` prism-code
async getItemBounds(ids)
```

Get the axis-aligned bounding box for the given items.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                             |
| :---: | :--------: | :-------------------------------------- |
|  ids  | string\[\] | A list of items to look up by their IDs |

Returns a [BoundingBox](../reference/bounding-box.md).

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |                        TYPE                        | DESCRIPTION                                                                                                            |
| :------: | :------------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------- |
| callback | (items: [Item](../reference/item.md)\[\]) =\> void | A callback for when an item changes. The items array will include all items in the scene, not just those that changed. |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.scene.items.onChange((items) => {
      // React to item changes
    }),
  []
);
```

------------------------------------------------------------------------

## Type Definitions

### ItemFilter

A filter to run on a list of items.

|   TYPE   |
| :------: |
| function |

**Parameters**

| NAME  |             TYPE             | DESCRIPTION                   |
| :---: | :--------------------------: | :---------------------------- |
| item  | [Item](../reference/item.md) | The item to run the filter on |

Returns a boolean. If true the item passes the filter and will be used. If false the item will be ignored.

------------------------------------------------------------------------

```

## docs\markdown\apis\local.md

```markdown
# Local

## `OBR.scene.local`

An [Item](../reference/item.md) is the basic building block of everything shown in a Scene.

For all available items see [here](../reference/items.md).

This API is a mirror to the [Items](items.md) API but only interacts with local items.

A local item is a temporary item that will only be seen by the current user.

They are most useful for displaying feedback to the user such as showing a label when using a custom tool.

# Reference

## Methods

### `getItems`

``` prism-code
async getItems(filter)
```

Get then current local items in the scene.

**Parameters**

|  NAME  |           TYPE            | DESCRIPTION                                         |
| :----: | :-----------------------: | :-------------------------------------------------- |
| filter | [ItemFilter](#itemfilter) | An optional filter to run on the scenes local items |

**Example**

Get local items with the given ids.

``` prism-code
const uuid = "55c04fba-9fa3-483b-8cf8-287737cbea9b";
const items = await OBR.scene.local.getItems([uuid]);
```

------------------------------------------------------------------------

### `updateItems`

``` prism-code
async updateItems(filterOrItems, update, fastUpdate)
```

Update existing local items in the scene.

To track changes and ensure immutability the update function uses an Immer `WritableDraft`.

**Parameters**

|     NAME      |                                TYPE                                 | DESCRIPTION                                                                                                                                                               |
| :-----------: | :-----------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| filterOrItems |    [ItemFilter](#itemfilter) \| [Item](../reference/item.md)\[\]    | Either a filter or a list of local items to update                                                                                                                        |
|    update     | (draft: WritableDraft\<[Item](../reference/item.md)\[\]\>) =\> void | An update function that allows you to update an Immer `WritableDraft` of the input local items                                                                            |
|  fastUpdate   |                               boolean                               | If true a faster update method will be used. Not all values can be updated using this method so check [here](interaction.md#interactive-values) to see if this will work. |

**Example**

Update the position of a known local item

``` prism-code
const uuid = "55c04fba-9fa3-483b-8cf8-287737cbea9b";

await OBR.scene.local.updateItems([uuid], (items) => {
  for (let item of items) {
    item.position.x += 100;
  }
});
```

------------------------------------------------------------------------

### `addItems`

``` prism-code
async addItems(items)
```

Add new local items to the scene.

To create new items you can use the item [Builders](../reference/builders.md).

**Parameters**

| NAME  |               TYPE               | DESCRIPTION            |
| :---: | :------------------------------: | :--------------------- |
| items | [Item](../reference/item.md)\[\] | A list of items to add |

**Example**

Add a label to the scene

``` prism-code
import OBR, { buildLabel } from "@owlbear-rodeo/sdk";

const item = buildLabel().plainText("Test").build();
OBR.scene.local.addItems([item]);
```

------------------------------------------------------------------------

### `deleteItems`

``` prism-code
async deleteItems(ids)
```

Delete existing items by their IDs.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                            |
| :---: | :--------: | :------------------------------------- |
|  ids  | string\[\] | A list of items to delete by their IDs |

**Example**

Delete a known local item

``` prism-code
const uuid = "55c04fba-9fa3-483b-8cf8-287737cbea9b";

OBR.scene.local.deleteItems([uuid]);
```

------------------------------------------------------------------------

### `getItemAttachments`

``` prism-code
async getItemAttachments(ids)
```

Get all items, attachments and sub-attachments for a set of item IDs.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                             |
| :---: | :--------: | :-------------------------------------- |
|  ids  | string\[\] | A list of items to look up by their IDs |

Returns a list of [Items](../reference/item.md).

------------------------------------------------------------------------

### `getItemBounds`

``` prism-code
async getItemBounds(ids)
```

Get the axis-aligned bounding box for the given items.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                             |
| :---: | :--------: | :-------------------------------------- |
|  ids  | string\[\] | A list of items to look up by their IDs |

Returns a [BoundingBox](../reference/bounding-box.md).

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |                        TYPE                        | DESCRIPTION                                                                                                                       |
| :------: | :------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------------- |
| callback | (items: [Item](../reference/item.md)\[\]) =\> void | A callback for when a local item changes. The items array will include all local items in the scene, not just those that changed. |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.scene.local.onChange((items) => {
      // React to item changes
    }),
  []
);
```

------------------------------------------------------------------------

## Type Definitions

### ItemFilter

A filter to run on a list of items.

|   TYPE   |
| :------: |
| function |

**Parameters**

| NAME  |             TYPE             | DESCRIPTION                   |
| :---: | :--------------------------: | :---------------------------- |
| item  | [Item](../reference/item.md) | The item to run the filter on |

Returns a boolean. If true the item passes the filter and will be used. If false the item will be ignored.

------------------------------------------------------------------------

```

## docs\markdown\apis\modal.md

```markdown
# Modal

## `OBR.modal`

The modal API allows you to display custom UI over the top of the Owlbear Rodeo interface as a modal.

# Reference

## Methods

### `open`

``` prism-code
async open(modal)
```

Open a new modal.

**Parameters**

| NAME  |       TYPE        | DESCRIPTION       |
| :---: | :---------------: | :---------------- |
| modal | [Modal](#modal-1) | The modal to open |

**Example**

``` prism-code
OBR.contextMenu.create({
  id: "rodeo.owlbear.example",
  icons: [
    {
      icon: "icon.svg",
      label: "Example",
    },
  ],
  onClick() {
    OBR.modal.open({
      id: "rodeo.owlbear.example/modal",
      url: "/modal",
      height: 300,
      width: 400,
    });
  },
});
```

------------------------------------------------------------------------

### `close`

``` prism-code
async close(id)
```

Close an open modal.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                  |
| :---: | :----: | :--------------------------- |
|  id   | string | The ID of the modal to close |

------------------------------------------------------------------------

## Type Definitions

### Modal

|  TYPE  |
| :----: |
| object |

**Properties**

|         NAME         |  TYPE   | DESCRIPTION                                                                    |
| :------------------: | :-----: | :----------------------------------------------------------------------------- |
|          id          | string  | The ID of this modal                                                           |
|         url          | string  | The url of the site to embed                                                   |
|        width         | number  | An optional width of the modal in pixels                                       |
|        height        | number  | An optional height of the modal in pixels                                      |
|      fullScreen      | boolean | An optional boolean, if true the modal will take up the whole screen           |
|     hideBackdrop     | boolean | An optional boolean, if true the dark backdrop will be hidden                  |
|      hidePaper       | boolean | An optional boolean, if true the colored background will be removed            |
| disablePointerEvents | boolean | An optional boolean, if true the modal will not react to mouse or touch events |

```

## docs\markdown\apis\notification.md

```markdown
# Notification

## `OBR.notification`

Show notifications in the Owlbear Rodeo interface.

# Reference

## Methods

### `show`

``` prism-code
async show(message, variant?)
```

Show a notification.

**Parameters**

|  NAME   |                           TYPE                           |                  DESCRIPTION                   |
| :-----: | :------------------------------------------------------: | :--------------------------------------------: |
| message |                          string                          |    The message to show in the notification     |
| variant | "DEFAULT" \| "ERROR" \| "INFO" \| "SUCCESS" \| "WARNING" | An optional style variant for the notification |

Returns the notification ID as a string.

------------------------------------------------------------------------

### `close`

``` prism-code
async close(id)
```

Close a notification.

**Parameters**

| NAME  |  TYPE  |             DESCRIPTION             |
| :---: | :----: | :---------------------------------: |
|  id   | string | The ID of the notification to close |

------------------------------------------------------------------------

```

## docs\markdown\apis\party.md

```markdown
# Party

## `OBR.party`

The party api gives you access to other players currently in the room.

# Reference

## Methods

### `getPlayers`

``` prism-code
async getPlayers()
```

Get the other players currently in the room.

Returns an array of [Players](#player).

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |                           TYPE                           | DESCRIPTION                                                       |
| :------: | :------------------------------------------------------: | :---------------------------------------------------------------- |
| callback | (players: [Player](../reference/player.md)\[\]) =\> void | A callback for when any connected player joins, leaves or changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.party.onChange((party) => {
      // React to party changes
    }),
  []
);
```

------------------------------------------------------------------------

```

## docs\markdown\apis\player.md

```markdown
# Player

## `OBR.player`

The player API gives you access to the current player using Owlbear Rodeo.

# Reference

**Properties**

| NAME  |  TYPE  | DESCRIPTION                                                                                     |
| :---: | :----: | :---------------------------------------------------------------------------------------------- |
|  id   | string | The user ID for this player. This will be shared if the same player joins a room multiple times |

------------------------------------------------------------------------

## Methods

### `getSelection`

``` prism-code
async getSelection()
```

Get the current selection for this player.

Returns an array of [Item](../reference/item.md) IDs or undefined if the player has no current selection.

------------------------------------------------------------------------

### `select`

``` prism-code
async select(items, replace?)
```

Select items for the player.

**Parameters**

|  NAME   |    TYPE    | DESCRIPTION                                                                                                                             |
| :-----: | :--------: | :-------------------------------------------------------------------------------------------------------------------------------------- |
|  items  | string\[\] | An array of item IDs to select                                                                                                          |
| replace |  boolean   | An optional boolean, if true the users selection will be replaced, if false the selection will be combined with their current selection |

------------------------------------------------------------------------

### `deselect`

``` prism-code
async deselect(items)
```

Deselect a set of items or all items.

**Parameters**

| NAME  |    TYPE    | DESCRIPTION                                                                          |
| :---: | :--------: | :----------------------------------------------------------------------------------- |
| items | string\[\] | An optional array if item IDs to deselect, if undefined all items will be deselected |

------------------------------------------------------------------------

### `getName`

``` prism-code
async getName()
```

Get the name for this player.

Returns a string.

------------------------------------------------------------------------

### `setName`

``` prism-code
async setName(name)
```

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                  |
| :---: | :----: | :--------------------------- |
| name  | string | The new name for this player |

------------------------------------------------------------------------

### `getColor`

``` prism-code
async getColor()
```

Get the color for this player.

Returns a string.

------------------------------------------------------------------------

### `setColor`

``` prism-code
async setColor(color)
```

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                   |
| :---: | :----: | :---------------------------- |
| color | string | The new color for this player |

------------------------------------------------------------------------

### `getSyncView`

``` prism-code
async getSyncView()
```

Get whether this player currently has sync view enabled

Returns a boolean.

------------------------------------------------------------------------

### `setSyncView`

``` prism-code
async setSyncView(syncView)
```

**Parameters**

|   NAME   |  TYPE   | DESCRIPTION                             |
| :------: | :-----: | :-------------------------------------- |
| syncView | boolean | The new sync view state for this player |

------------------------------------------------------------------------

### `getId`

``` prism-code
async getId()
```

Get the user ID for this player. In most cases the `id` property should be used instead as it is synchronous.

This will be shared if the same player joins a room multiple times.

Returns a string.

------------------------------------------------------------------------

### `getRole`

``` prism-code
async getRole()
```

Get the current role for this player.

returns `"GM" | "PLAYER"`.

------------------------------------------------------------------------

### `getMetadata`

``` prism-code
async getMetadata()
```

Get the current metadata for this player.

returns a [Metadata](../reference/metadata.md) object.

------------------------------------------------------------------------

### `setMetadata`

``` prism-code
async setMetadata(update)
```

Update the metadata for this player.

See [Metadata](../reference/metadata.md) for best practices when updating metadata.

**Parameters**

|  NAME  |                      TYPE                       | DESCRIPTION                                                                                                                                |
| :----: | :---------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------- |
| update | Partial\<[Metadata](../reference/metadata.md)\> | A partial update to this players metadata. The included values will be spread among the current metadata to avoid overriding other values. |

------------------------------------------------------------------------

### `hasPermission`

``` prism-code
async hasPermission(permission)
```

Does this player have the given permission.

**Parameters**

|    NAME    |                   TYPE                   | DESCRIPTION             |
| :--------: | :--------------------------------------: | :---------------------- |
| permission | [Permission](../reference/permission.md) | The permission to check |

Returns a boolean.

------------------------------------------------------------------------

### `getConnectionId`

``` prism-code
async getConnectionId()
```

Get the current connection ID for this player.

This will be unique if the same player joins the room multiple times.

Returns a string.

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |                        TYPE                         | DESCRIPTION                                               |
| :------: | :-------------------------------------------------: | :-------------------------------------------------------- |
| callback | (player: [Player](../reference/player.md)) =\> void | A callback for when a value on the current player changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.player.onChange((player) => {
      // React to player changes
    }),
  []
);
```

------------------------------------------------------------------------

```

## docs\markdown\apis\popover.md

```markdown
# Popover

## `OBR.popover`

The popover API allows you to display custom UI over the top of the Owlbear Rodeo interface.

# Reference

## Methods

### `open`

``` prism-code
async open(popover)
```

Open a new popover.

**Parameters**

|  NAME   |         TYPE          | DESCRIPTION         |
| :-----: | :-------------------: | :------------------ |
| popover | [Popover](#popover-1) | The popover to open |

**Example**

``` prism-code
OBR.contextMenu.create({
  id: "rodeo.owlbear.example",
  icons: [
    {
      icon: "icon.svg",
      label: "Example",
    },
  ],
  onClick(_, elementId) {
    OBR.popover.open({
      id: "rodeo.owlbear.example/popover",
      url: "/popover",
      height: 80,
      width: 200,
      anchorElementId: elementId,
    });
  },
});
```

------------------------------------------------------------------------

### `close`

``` prism-code
async close(id)
```

Close an open popover.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                    |
| :---: | :----: | :----------------------------- |
|  id   | string | The ID of the popover to close |

------------------------------------------------------------------------

### `getWidth`

``` prism-code
async getWidth(id)
```

Get the width of a popover.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION           |
| :---: | :----: | :-------------------- |
|  id   | string | The ID of the popover |

------------------------------------------------------------------------

### `getHeight`

``` prism-code
async getHeight(id)
```

Get the height of a popover.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION           |
| :---: | :----: | :-------------------- |
|  id   | string | The ID of the popover |

------------------------------------------------------------------------

### `setWidth`

``` prism-code
async setWidth(id)
```

Set the width of a popover.

**Parameters**

| NAME  |  TYPE  | DESCRIPTION              |
| :---: | :----: | :----------------------- |
|  id   | string | The ID of the popover    |
| width | number | The width of the popover |

------------------------------------------------------------------------

### `setHeight`

``` prism-code
async setHeight(id)
```

Set the height of a popover.

**Parameters**

|  NAME  |  TYPE  | DESCRIPTION               |
| :----: | :----: | :------------------------ |
|   id   | string | The ID of the popover     |
| height | number | The height of the popover |

------------------------------------------------------------------------

## Type Definitions

### Popover

|  TYPE  |
| :----: |
| object |

**Properties**

|       NAME       |                                          TYPE                                          | DESCRIPTION                                                                                 |
| :--------------: | :------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------ |
|        id        |                                         string                                         | The ID of this popover                                                                      |
|       url        |                                         string                                         | The url of the site to embed                                                                |
|      width       |                                         number                                         | The width of the popover in pixels                                                          |
|      height      |                                         number                                         | The height of the popover in pixels                                                         |
| anchorElementId  |                                         string                                         | An optional ID of the element to anchor the popover to                                      |
|  anchorPosition  |                             { left: number; top: number }                              | An optional position to anchor the popover to                                               |
|   anchorOrigin   | { horizontal: "CENTER" \| "LEFT" \| "RIGHT"; vertical: "BOTTOM" \| "CENTER" \| "TOP" } | An optional origin for the popover anchor                                                   |
| transformOrigin  | { horizontal: "CENTER" \| "LEFT" \| "RIGHT"; vertical: "BOTTOM" \| "CENTER" \| "TOP" } | An optional origin for the popover transform                                                |
| anchorReference  |                                "ELEMENT" \| "POSITION"                                 | Optionally use either the elementId as the anchor or the position                           |
|    hidePaper     |                                        boolean                                         | An optional boolean, if true the colored background will be removed                         |
| disableClickAway |                                        boolean                                         | An optional boolean, if true the popover will remain open when the user clicks away from it |
| marginThreshold  |                                        boolean                                         | An optional number, how close the popover is allowed to get to the document borders         |

```

## docs\markdown\apis\room.md

```markdown
# Room

## `OBR.room`

The room API gives you access to the current room the extension is being used in.

# Reference

**Properties**

| NAME  |  TYPE  | DESCRIPTION                       |
| :---: | :----: | :-------------------------------- |
|  id   | string | A unique ID for the current room. |

------------------------------------------------------------------------

## Methods

### `getPermissions`

``` prism-code
async getPermissions()
```

Get the current permissions for players in this room.

Returns a [Permission](../reference/permission.md) array.

------------------------------------------------------------------------

### `onPermissionsChange`

``` prism-code
onPermissionsChange(callback);
```

**Parameters**

|   NAME   |                                 TYPE                                 | DESCRIPTION                                                     |
| :------: | :------------------------------------------------------------------: | :-------------------------------------------------------------- |
| callback | (permissions: [Permission](../reference/permission.md)\[\]) =\> void | A callback for when the permissions of the current room changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onPermissionsChange` event with a React `useEffect`.
 * `onPermissionsChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.room.onPermissionsChange((permissions) => {
      // React to rooms permissions change
    }),
  []
);
```

------------------------------------------------------------------------

### `getMetadata`

``` prism-code
async getMetadata()
```

Get the current metadata for this room.

returns a [Metadata](../reference/metadata.md) object.

------------------------------------------------------------------------

### `setMetadata`

``` prism-code
async setMetadata(update)
```

Update the metadata for this room.

See [Metadata](../reference/metadata.md) for best practices when updating metadata.

Room metadata is intended for small bits of stored data for an extension.

In total the room metadata must be under 16kB.

**Parameters**

|  NAME  |                      TYPE                       | DESCRIPTION                                                                                                                              |
| :----: | :---------------------------------------------: | :--------------------------------------------------------------------------------------------------------------------------------------- |
| update | Partial\<[Metadata](../reference/metadata.md)\> | A partial update to this rooms metadata. The included values will be spread among the current metadata to avoid overriding other values. |

------------------------------------------------------------------------

### `onMetadataChange`

``` prism-code
onMetadataChange(callback);
```

**Parameters**

|   NAME   |                           TYPE                            | DESCRIPTION                                                  |
| :------: | :-------------------------------------------------------: | :----------------------------------------------------------- |
| callback | (metadata: [Metadata](../reference/metadata.md)) =\> void | A callback for when the metadata of the current room changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onMetadataChange` event with a React `useEffect`.
 * `onMetadataChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.room.onMetadataChange((metadata) => {
      // React to rooms metadata changes
    }),
  []
);
```

------------------------------------------------------------------------

```

## docs\markdown\apis\scene.md

```markdown
# Scene

## `OBR.scene`

A scene is an infinite space for you to lay out images, drawings, fog and more.

# Reference

## Methods

### `isReady`

``` prism-code
async isReady()
```

Returns true if there is a scene opened and it is ready to interact with.

------------------------------------------------------------------------

### `onReadyChange`

``` prism-code
onReadyChange(callback);
```

**Parameters**

|   NAME   |           TYPE            | DESCRIPTION                                                   |
| :------: | :-----------------------: | :------------------------------------------------------------ |
| callback | (ready: boolean) =\> void | A callback for when the current scene changes its ready state |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onReadyChange` event with a React `useEffect`.
 * `onReadyChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.scene.onReadyChange((ready) => {
      if (ready) {
        // interact with the scene
      }
    }),
  []
);
```

------------------------------------------------------------------------

### `getMetadata`

``` prism-code
async getMetadata()
```

Get the current metadata for this scene.

returns a [Metadata](../reference/metadata.md) object.

------------------------------------------------------------------------

### `setMetadata`

``` prism-code
async setMetadata(update)
```

Update the metadata for this scene.

See [Metadata](../reference/metadata.md) for best practices when updating metadata.

**Parameters**

|  NAME  |                      TYPE                       | DESCRIPTION                                                                                                                               |
| :----: | :---------------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------- |
| update | Partial\<[Metadata](../reference/metadata.md)\> | A partial update to this scenes metadata. The included values will be spread among the current metadata to avoid overriding other values. |

------------------------------------------------------------------------

### `onMetadataChange`

``` prism-code
onMetadataChange(callback);
```

**Parameters**

|   NAME   |                           TYPE                            | DESCRIPTION                              |
| :------: | :-------------------------------------------------------: | :--------------------------------------- |
| callback | (metadata: [Metadata](../reference/metadata.md)) =\> void | A callback for when the metadata changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onMetadataChange` event with a React `useEffect`.
 * `onMetadataChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.scene.onMetadataChange((metadata) => {
      // React to metadata changes
    }),
  []
);
```

------------------------------------------------------------------------

## 📄️ Fog

OBR.scene.fog

## 📄️ Grid

OBR.scene.grid

## 📄️ History

OBR.scene.history

## 📄️ Items

OBR.scene.items

## 📄️ Local

OBR.scene.local

```

## docs\markdown\apis\theme.md

```markdown
# Theme

## `OBR.theme`

The theme API gives you access to the current theme used by Owlbear Rodeo.

# Reference

## Methods

### `getTheme`

``` prism-code
async getTheme()
```

Get the current Owlbear Rodeo theme.

Returns a [Theme](#theme-1) object.

------------------------------------------------------------------------

### `onChange`

``` prism-code
onChange(callback);
```

**Parameters**

|   NAME   |                TYPE                 | DESCRIPTION                                   |
| :------: | :---------------------------------: | :-------------------------------------------- |
| callback | (theme: [Theme](#theme-1)) =\> void | A callback for when the current theme changes |

Returns a function that when called will unsubscribe from change events.

**Example**

``` prism-code
/**
 * Use an `onChange` event with a React `useEffect`.
 * `onChange` returns an unsubscribe event to make this easy.
 */
useEffect(
  () =>
    OBR.theme.onChange((theme) => {
      // React to theme changes
    }),
  []
);
```

------------------------------------------------------------------------

## Type Definitions

### Theme

The palette of a theme

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME    |                TYPE                 | DESCRIPTION                       |
| :--------: | :---------------------------------: | :-------------------------------- |
|    mode    |          "DARK" \| "LIGHT"          | The color mode of the theme       |
|  primary   |      [ThemeColor](#themecolor)      | The primary color of the theme    |
| secondary  |      [ThemeColor](#themecolor)      | The secondary color of the theme  |
| background | [ThemeBackground](#themebackground) | The background color of the theme |
|    text    |       [ThemeText](#themetext)       | The text color of the theme       |

------------------------------------------------------------------------

### ThemeColor

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |  TYPE  | DESCRIPTION                                     |
| :----------: | :----: | :---------------------------------------------- |
|     main     | string | The main color                                  |
|    light     | string | A lightened version of the main color           |
|     dark     | string | A darkened version of the main color            |
| contrastText | string | A text color that contrasts with the main color |

------------------------------------------------------------------------

### ThemeBackground

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME   |  TYPE  | DESCRIPTION                                                      |
| :-----: | :----: | :--------------------------------------------------------------- |
| default | string | The base background color                                        |
|  paper  | string | A highlight background color used for raised background elements |

------------------------------------------------------------------------

### ThemeText

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME    |  TYPE  | DESCRIPTION                                                      |
| :-------: | :----: | :--------------------------------------------------------------- |
|  primary  | string | The primary text color                                           |
| secondary | string | A secondary text color that recedes compared to the primary text |
| disabled  | string | A disabled text color used for disabled elements                 |

------------------------------------------------------------------------

```

## docs\markdown\apis\tool.md

```markdown
# Tool

## `OBR.tool`

Manage custom tools, tool modes and tool actions.

# Reference

## Methods

### `create`

``` prism-code
async create(tool)
```

Create a new tool.

**Parameters**

| NAME  |      TYPE       |      DESCRIPTION       |
| :---: | :-------------: | :--------------------: |
| tool  | [Tool](#tool-1) | The new tool to create |

------------------------------------------------------------------------

### `remove`

``` prism-code
async remove(id)
```

Remove an existing tool.

**Parameters**

| NAME  |  TYPE  |         DESCRIPTION          |
| :---: | :----: | :--------------------------: |
|  id   | string | The ID of the tool to remove |

------------------------------------------------------------------------

### `getActiveTool`

``` prism-code
async getActiveTool()
```

Returns a string of the current active tool ID.

------------------------------------------------------------------------

### `onToolChange`

``` prism-code
onToolChange(callback);
```

**Parameters**

|   NAME   |         TYPE          | DESCRIPTION                                  |
| :------: | :-------------------: | :------------------------------------------- |
| callback | (id: string) =\> void | A callback for when the current tool changes |

Returns a function that when called will unsubscribe from change events.

------------------------------------------------------------------------

### `createAction`

``` prism-code
async createAction(action)
```

Create a new tool action.

**Parameters**

|  NAME  |           TYPE            |          DESCRIPTION          |
| :----: | :-----------------------: | :---------------------------: |
| action | [ToolAction](#toolaction) | The new tool action to create |

------------------------------------------------------------------------

### `removeAction`

``` prism-code
async removeAction(id)
```

Remove an existing tool action.

**Parameters**

| NAME  |  TYPE  |             DESCRIPTION             |
| :---: | :----: | :---------------------------------: |
|  id   | string | The ID of the tool action to remove |

------------------------------------------------------------------------

### `createMode`

``` prism-code
async createMode(mode)
```

Create a new tool mode.

**Parameters**

| NAME  |         TYPE          |         DESCRIPTION         |
| :---: | :-------------------: | :-------------------------: |
| mode  | [ToolMode](#toolmode) | The new tool mode to create |

------------------------------------------------------------------------

### `removeMode`

``` prism-code
async removeMode(id)
```

Remove an existing tool mode.

**Parameters**

| NAME  |  TYPE  |            DESCRIPTION            |
| :---: | :----: | :-------------------------------: |
|  id   | string | The ID of the tool mode to remove |

------------------------------------------------------------------------

### `activateMode`

``` prism-code
async activateMode(toolId, modeId)
```

Activate a specific mode for a given tool.

**Parameters**

|  NAME  |  TYPE  |             DESCRIPTION             |
| :----: | :----: | :---------------------------------: |
| toolId | string |         The ID of the tool          |
| modeId | string | The ID of the tool mode to activate |

------------------------------------------------------------------------

### `getActiveToolMode`

``` prism-code
async getActiveToolMode()
```

Returns a string of the current active tool mode ID.

------------------------------------------------------------------------

### `onToolModeChange`

``` prism-code
onToolModeChange(callback);
```

**Parameters**

|   NAME   |         TYPE          | DESCRIPTION                                       |
| :------: | :-------------------: | :------------------------------------------------ |
| callback | (id: string) =\> void | A callback for when the current tool mode changes |

Returns a function that when called will unsubscribe from change events.

------------------------------------------------------------------------

### `getMetadata`

``` prism-code
async getMetadata(id)
```

Get the metadata for the given tool.

**Parameters**

| NAME  |  TYPE  |    DESCRIPTION     |
| :---: | :----: | :----------------: |
|  id   | string | The ID of the tool |

Returns a [Metadata](../reference/metadata.md) object.

------------------------------------------------------------------------

### `setMetadata`

``` prism-code
async setMetadata(toolId, update)
```

Update the metadata for a given tool.

**Example**

Update the stroke color of a custom drawing tool

``` prism-code
async function handleChange(value: string) {
  await OBR.tool.setMetadata("com.example.drawing", {
    strokeColor: value,
  });
}
```

This does not override any metadata properties that already exist. For example if the metadata looks like this:

``` prism-code
{
  strokeWidth: 1,
  strokeColor: "red"
}
```

And `handleChange("blue")` is called in the example above then the resulting metadata will look like this:

``` prism-code
{
  strokeWidth: 1,
  strokeColor: "blue"
}
```

**Parameters**

|  NAME  |                      TYPE                       |                                     DESCRIPTION                                     |
| :----: | :---------------------------------------------: | :---------------------------------------------------------------------------------: |
| toolId |                     string                      |                                 The ID of the tool                                  |
| update | Partial\<[Metadata](../reference/metadata.md)\> | The metadata data update to use. The metadata is spread into the existing metadata. |

------------------------------------------------------------------------

## Type Definitions

### Tool

A tool in the toolbar.

|  TYPE  |
| :----: |
| object |

**Properties**

|      NAME       |                                            TYPE                                            | DESCRIPTION                                                                                                                                                        |
| :-------------: | :----------------------------------------------------------------------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|       id        |                                           string                                           | The ID of this tool                                                                                                                                                |
|      icons      |                                 [ToolIcon](#toolicon)\[\]                                  | The icons for this tool                                                                                                                                            |
|    disabled     |                                 [ToolFilter](#toolfilter)                                  | An optional filter for checking if the tool should be disabled                                                                                                     |
|     onClick     | (context: [ToolContext](#toolcontext), elementId: string) =\> void \| undefined \| boolean | An optional callback for when the tool icon is clicked. By default the clicked tool will be activated. If defined return true to perform the default click action. |
|    shortcut     |                                           string                                           | An optional key shortcut for this tool                                                                                                                             |
|   defaultMode   |                                           string                                           | An optional ID of the mode to be activated by default                                                                                                              |
| defaultMetadata |                            [Metadata](../reference/metadata.md)                            | An optional Metadata object to use as default                                                                                                                      |

------------------------------------------------------------------------

### ToolAction

A tool action defines an item in the tool menu bar.

Unlike a tool mode an action is a clickable item but won't be activated when clicked.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |                                TYPE                                | DESCRIPTION                                                      |
| :------: | :----------------------------------------------------------------: | :--------------------------------------------------------------- |
|    id    |                               string                               | The ID of this action                                            |
|  icons   |                     [ToolIcon](#toolicon)\[\]                      | The icons for this action                                        |
| disabled |                     [ToolFilter](#toolfilter)                      | An optional filter for checking if the action should be disabled |
| onClick  | (context: [ToolContext](#toolcontext), elementId: string) =\> void | An optional callback for when the action icon is clicked         |
| shortcut |                               string                               | An optional key shortcut for this action                         |

------------------------------------------------------------------------

### ToolMode

A tool mode will be activated when clicked.

Once a mode is active it will receive pointer events such as `onToolMove` and `onToolDragMove`.

|  TYPE  |
| :----: |
| object |

**Properties**

|       NAME        |                                                  TYPE                                                   | DESCRIPTION                                                                                                                                                                                              |
| :---------------: | :-----------------------------------------------------------------------------------------------------: | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|        id         |                                                 string                                                  | The ID of this mode                                                                                                                                                                                      |
|       icons       |                                        [ToolIcon](#toolicon)\[\]                                        | The icons for this mode                                                                                                                                                                                  |
|     disabled      |                                        [ToolFilter](#toolfilter)                                        | An optional filter for checking if the mode should be disabled                                                                                                                                           |
|      onClick      |       (context: [ToolContext](#toolcontext), elementId: string) =\> void \| undefined \| boolean        | An optional callback for when the mode icon is clicked. By default the clicked mode will be activated. If defined return true to perform the default click action.                                       |
|     shortcut      |                                                 string                                                  | An optional key shortcut for this mode                                                                                                                                                                   |
|      cursors      |                                      [ToolCursor](#toolcursor)\[\]                                      | An optional array of cursors                                                                                                                                                                             |
|    onToolClick    | (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void \| undefined \| boolean | An optional callback for when a single click is made by the tool. By default the clicked item will be selected if it is unlocked. If defined return true to perform the default click action.            |
| onToolDoubleClick | (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void \| undefined \| boolean | An optional callback for when a double click is made by the tool. By default the clicked item will be selected event if it is locked. If defined return true to perform the default double click action. |
|    onToolDown     |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when the pointer enters the down state                                                                                                                                          |
|    onToolMove     |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when the pointer moves                                                                                                                                                          |
|     onToolUp      |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when the pointer enters the up state                                                                                                                                            |
|  onToolDragStart  |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when a drag starts on the viewport                                                                                                                                              |
|  onToolDragMove   |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when dragging on the viewport                                                                                                                                                   |
|   onToolDragEnd   |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when a drag ends on the viewport                                                                                                                                                |
| onToolDragCancel  |             (context: [ToolContext](#toolcontext), event: [ToolEvent](#toolevent)) =\> void             | An optional callback for when a drag event is canceled by either switching modes or pressing the Escape key                                                                                              |
|    onActivate     |                                 (context: [ToolContext](#toolcontext))                                  | An optional callback for when the tool mode is activated                                                                                                                                                 |
|   onDeactivate    |                                 (context: [ToolContext](#toolcontext) )                                 | An optional callback for when the tool mode is deactivated                                                                                                                                               |
|     onKeyDown     |              (context: [ToolContext](#toolcontext), event: [KeyEvent](#keyevent)) =\> void              | An optional callback for when a key is pressed                                                                                                                                                           |
|      onKeyUp      |              (context: [ToolContext](#toolcontext), event: [KeyEvent](#keyevent)) =\> void              | An optional callback for when a key is released                                                                                                                                                          |
|    preventDrag    |                                    [ToolModeFilter](#toolmodefilter)                                    | An optional filter for checking if the drag event should be prevented. If the filter returns true the default drag operation will be used which mimics the Move tool.                                    |

------------------------------------------------------------------------

### ToolContext

Holds the state of the tool.

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME    |                 TYPE                 | DESCRIPTION                                    |
| :--------: | :----------------------------------: | :--------------------------------------------- |
| activeTool |                string                | The ID of the current active tool              |
| activeMode |                string                | An optional ID of the current active tool mode |
|  metadata  | [Metadata](../reference/metadata.md) | The metadata of the current active tool        |

------------------------------------------------------------------------

### ToolEvent

A pointer event for a tool mode.

|  TYPE  |
| :----: |
| object |

**Properties**

|      NAME       |                TYPE                | DESCRIPTION                                                      |
| :-------------: | :--------------------------------: | :--------------------------------------------------------------- |
| pointerPosition | [Vector2](../reference/vector2.md) | The pointer position relative to the viewport                    |
|     target      |    [Item](../reference/item.md)    | An optional target for the pointer event                         |
|   transformer   |              boolean               | If we have a target are we selecting a transformer control point |
|     altKey      |              boolean               | Is the Alt key pressed down                                      |
|    shiftKey     |              boolean               | Is the Shift key pressed down                                    |
|     ctrlKey     |              boolean               | Is the Ctrl key pressed down                                     |
|     metaKey     |              boolean               | Is the Meta key pressed down                                     |

------------------------------------------------------------------------

### KeyEvent

A key event for a tool mode.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |  TYPE   | DESCRIPTION                                                        |
| :------: | :-----: | :----------------------------------------------------------------- |
|   code   | string  | A string representation of the physical key pressed                |
|   key    | string  | A string representation of the key                                 |
|  altKey  | boolean | Is the Alt key pressed down                                        |
| shiftKey | boolean | Is the Shift key pressed down                                      |
| ctrlKey  | boolean | Is the Ctrl key pressed down                                       |
| metaKey  | boolean | Is the Meta key pressed down                                       |
|  repeat  | boolean | Is the key being held down such that it is automatically repeating |

------------------------------------------------------------------------

### ToolIcon

An icon for a tool.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |           TYPE            | DESCRIPTION                                                |
| :----: | :-----------------------: | :--------------------------------------------------------- |
|  icon  |          string           | The url of the icon as either a relative or absolute path  |
| label  |          string           | The label to use for the tooltip of the icon               |
| filter | [ToolFilter](#toolfilter) | An optional filter to control when this icon will be shown |

------------------------------------------------------------------------

### ToolFilter

A filter to control if various tools, actions or modes will be shown.

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |                        TYPE                        | DESCRIPTION                                                                  |
| :---------: | :------------------------------------------------: | :--------------------------------------------------------------------------- |
| activeTools |                     string\[\]                     | An optional array of tool IDs that can be active                             |
| activeModes |                     string\[\]                     | An optional array of tool mode IDs that can be active                        |
| permissions |    [Permission](../reference/permission.md)\[\]    | An optional permissions filter                                               |
|    roles    |               ("GM" \| "PLAYER")\[\]               | An optional array of roles needed for the player, defaults to no role needed |
|  metadata   | [KeyFilter](../reference/filters.md#keyfilter)\[\] | An optional array of filters to run on the current tool metadata             |

------------------------------------------------------------------------

### ToolModeFilter

A filter to use for a tool mode.

Extends [ToolFilter](#toolfilter).

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |                        TYPE                        | DESCRIPTION                                                              |
| :------: | :------------------------------------------------: | :----------------------------------------------------------------------- |
|  target  | [KeyFilter](../reference/filters.md#keyfilter)\[\] | An optional array of filters to run on the current target of a tool mode |
| dragging |                      boolean                       | An optional boolean to check the dragging state of the current tool mode |

------------------------------------------------------------------------

### ToolCursor

A cursor to use for a tool mode.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |               TYPE                | DESCRIPTION                                        |
| :----: | :-------------------------------: | :------------------------------------------------- |
| cursor |              string               | A css cursor string e.g. "pointer"                 |
| filter | [ToolModeFilter](#toolmodefilter) | An optional filter to run on the current tool mode |

------------------------------------------------------------------------

```

## docs\markdown\apis\viewport.md

```markdown
# Viewport

## `OBR.viewport`

Control the viewport of the current scene.

The viewport represents this players view of the current scene.

# Reference

## Methods

### `reset`

``` prism-code
async reset()
```

Reset the viewport to the initial view.

If no map exists in the scene this will be the origin. If a map exists the viewport will fit to this map.

Returns a [ViewportTransform](#viewporttransform) with the transform it was reset to.

------------------------------------------------------------------------

### `animateTo`

``` prism-code
async animateTo(transform)
```

Animate the viewport to the given transform.

**Parameters**

|   NAME    |                  TYPE                   |           DESCRIPTION           |
| :-------: | :-------------------------------------: | :-----------------------------: |
| transform | [ViewportTransform](#viewporttransform) | The new transform to animate to |

------------------------------------------------------------------------

### `animateToBounds`

``` prism-code
async animateTo(bounds)
```

Animate the viewport to the given bounding box.

**Parameters**

|  NAME  |                    TYPE                     |          DESCRIPTION           |
| :----: | :-----------------------------------------: | :----------------------------: |
| bounds | [BoundingBox](../reference/bounding-box.md) | The bounding box to animate to |

**Example**

Zoom on to the selected items when clicking a context menu item

``` prism-code
OBR.contextMenu.create({
  id: "rodeo.owlbear.example",
  icons: [
    {
      icon: "icon.svg",
      label: "Example",
    },
  ],
  async onClick(context) {
    OBR.viewport.animateToBounds(context.selectionBounds);
  },
});
```

------------------------------------------------------------------------

### `getPosition`

``` prism-code
async getPosition()
```

Get the current position of the viewport.

Returns a [Vector2](../reference/vector2.md).

------------------------------------------------------------------------

### `setPosition`

``` prism-code
async setPosition(position)
```

Set the position of the viewport.

**Parameters**

|   NAME   |                TYPE                |           DESCRIPTION            |
| :------: | :--------------------------------: | :------------------------------: |
| position | [Vector2](../reference/vector2.md) | The new position of the viewport |

------------------------------------------------------------------------

### `getScale`

``` prism-code
async getScale()
```

Get the current scale of the viewport.

A scale of 1 represents a 1:1 scale.

Returns a number.

------------------------------------------------------------------------

### `setScale`

``` prism-code
async setScale(scale)
```

Set the scale of the viewport.

**Parameters**

| NAME  |  TYPE  |          DESCRIPTION          |
| :---: | :----: | :---------------------------: |
| scale | number | The new scale of the viewport |

------------------------------------------------------------------------

### `getWidth`

``` prism-code
async getWidth()
```

Get the width of the viewport.

Returns a number.

------------------------------------------------------------------------

### `getHeight`

``` prism-code
async getHeight()
```

Get the height of the viewport.

Returns a number.

------------------------------------------------------------------------

### `transformPoint`

``` prism-code
async transformPoint(point)
```

Transform a point from the viewport coordinate space into the screens coordinate space.

**Parameters**

| NAME  |                TYPE                |      DESCRIPTION       |
| :---: | :--------------------------------: | :--------------------: |
| point | [Vector2](../reference/vector2.md) | The point to transform |

Returns a [Vector2](../reference/vector2.md).

------------------------------------------------------------------------

### `inverseTransformPoint`

``` prism-code
async inverseTransformPoint(point)
```

Transform a point from the screens coordinate space into the viewport coordinate space.

**Parameters**

| NAME  |                TYPE                |      DESCRIPTION       |
| :---: | :--------------------------------: | :--------------------: |
| point | [Vector2](../reference/vector2.md) | The point to transform |

Returns a [Vector2](../reference/vector2.md).

------------------------------------------------------------------------

## Type Definitions

### ViewportTransform

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |                TYPE                | DESCRIPTION                  |
| :------: | :--------------------------------: | :--------------------------- |
| position | [Vector2](../reference/vector2.md) | The position of the viewport |
|  scale   |               number               | The scale of the viewport    |

```

## docs\markdown\reference\billboard.md

```markdown
# Billboard

A billboard image that loads from a url.

Billboards are scaled in screen-space. This means that they will stay the same size independent to the zoom level of the scene.

*Local Only:* this Item can only be added to the local scene using the `OBR.scene.local` API.

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |                 TYPE                  | DESCRIPTION                 |
| :---: | :-----------------------------------: | :-------------------------- |
| type  |              "BILLBOARD"              | The type of item            |
| image | [ImageContent](image.md#imagecontent) | The image to show           |
| grid  |    [ImageGrid](image.md#imagegrid)    | The grid scale of the image |
| style |   [BillboardStyle](#billboardstyle)   | The style of the billboard  |

## Type Definitions

### BillboardStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |  TYPE  | DESCRIPTION                                                         |
| :----------: | :----: | :------------------------------------------------------------------ |
| maxViewScale | number | An optional maximum the billboard will use for screen-space scaling |
| minViewScale | number | An optional minimum the billboard will use for screen-space scaling |

```

## docs\markdown\reference\bounding-box.md

```markdown
# BoundingBox

An axis-aligned bounding box

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |         TYPE          | DESCRIPTION                          |
| :----: | :-------------------: | :----------------------------------- |
|  min   | [Vector2](vector2.md) | The top left of the bounding box     |
|  max   | [Vector2](vector2.md) | The bottom right of the bounding box |
| width  |        number         | The width of the bounding box        |
|  min   |        number         | The height of the bounding box       |
| center | [Vector2](vector2.md) | The center of the bounding box       |

```

## docs\markdown\reference\builders.md

```markdown
# Builders

Each item has a builder that makes it easy to create new items

The asset API also has builders to make it easy to upload new assets

## 📄️ CurveBuilder

A builder for the Curve item.

## 📄️ ImageUploadBuilder

A builder for a new ImageUpload.

## 📄️ ImageBuilder

A builder for the Image item.

## 📄️ GenericItemBuilder

An abstract Builder for all Items.

## 📄️ LabelBuilder

A builder for the Label item.

## 📄️ LightBuilder

A builder for the Light item.

## 📄️ LineBuilder

A builder for the Line item.

## 📄️ PathBuilder

A builder for the Path item.

## 📄️ PointerBuilder

A builder for the Pointer item.

## 📄️ RulerBuilder

A builder for the Ruler item.

## 📄️ SceneUploadBuilder

A builder for a new SceneUpload.

## 📄️ ShapeBuilder

A builder for the Shape item.

## 📄️ TextBuilder

A builder for the Text item.

## 📄️ WallBuilder

A builder for the Wall item.

```

## docs\markdown\reference\curve.md

```markdown
# Curve

A shape with a list of 2D points

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |           TYPE            | DESCRIPTION                |
| :----: | :-----------------------: | :------------------------- |
|  type  |          "CURVE"          | The type of item           |
| points | [Vector2](vector2.md)\[\] | The list of points to draw |
| style  | [CurveStyle](#curvestyle) | The style of the curve     |

## Type Definitions

### CurveStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME      |    TYPE    | DESCRIPTION                                                                                                                                   |
| :-----------: | :--------: | :-------------------------------------------------------------------------------------------------------------------------------------------- |
|   fillColor   |   string   | The fill color of the shape                                                                                                                   |
|  fillOpacity  |   number   | The fill opacity of the shape between 0 and 1                                                                                                 |
|  strokeColor  |   string   | The stroke color of the shape                                                                                                                 |
| strokeOpacity |   number   | The stroke opacity of the shape between 0 and 1                                                                                               |
|  strokeWidth  |   number   | The stroke width of the shape in pixels                                                                                                       |
|  strokeDash   | number\[\] | The pattern of the stroke dash                                                                                                                |
|    tension    |   number   | How much curvature to apply between points in the curve. A value of 0 will make a straight edge shape. A value of 1 will cause a large curve. |
|    closed     |  boolean   | An optional boolean when true the curve ends where it started                                                                                 |

```

## docs\markdown\reference\dynamic-fog.md

```markdown
# Dynamic Fog

The Dynamic Fog system is controlled with the [Light](light.md) and [Wall](wall.md) items.

Lights support soft edges with the `falloff` parameter and soft shadows with the `sourceRadius` parameter. Walls support single sided shadows by disabling the `doubleSided` parameter and collision with lights and tokens with the `blocking` parameter.

### Elevation

The Dynamic Fog takes over the `zIndex` parameter for both wall and lights to control how each is processed.

For wall and lights the `zIndex` is used to filter which walls affect which lights. For example a light with a `zIndex` of 1 will only be affected by a wall with a `zIndex` of 1 or greater. This can be used to create multiple elevated surfaces for multiple storied maps.

Secondly the `zIndex` value is used to determine whether the dynamic fog is drawn below or above the static fog in a Scene. Any `zIndex` value below 0 will cause the dynamic lighting to be drawn below static fog while any `zIndex` equal or greater to 0 will be drawn above. This means any positive `zIndex` will cut away from existing fog while negative `zIndex` values will be hidden by existing fog. This property also interacts with elevation where the absolute value of the zIndex is used to create each elevation. So a light with a `zIndex` of -1 will only be affected by a wall with a `zIndex` of -1 or less.

### Secondary Lighting

Each light can be of `lightType` `PRIMARY`, `SECONDARY` or `AUXILIARY` a primary light is a regular shadow casting light that when visible will always cut away from the fog. A secondary light however only effects fog that can be seen by a primary light. For example setting a light above the enemies campfire as secondary will mean that the camp will only be visible once a player with a primary light gains line of sight to that fire. An auxiliary light will cast shadows like a primary light but it will not trigger any secondary lights.

### Performance

The Dynamic Fog is processed on the GPU using various vertex and fragment shaders then composited back into the OBR Scene. The performance of the Dynamic Fog depends on how many walls/lights are used but also on what parameters are used for each item.

There are two rendering paths implemented depending on what parameters are used for the lights and walls in a Scene. The faster rendering path will be used for any light that has a `sourceRadius` of 0. This will disable the soft shadows but can handle many more lights before potential performance issues occur. It is recommended if you are going to add many lights (more than a few dozen) to a Scene that those lights use a `sourceRadius` of 0. In a single Scene you can mix soft shadowed and hard shadowed lights. For example you can use soft shadowed lights for key character lights but fallback to hard shadowed lights for environment objects. A caveat to this exists with the `doubleSided` parameter for walls. Currently enabling this parameter on any wall in a Scene will force all lights to use the soft shadowed rendering path no matter on the `sourceRadius` of the light.

If a secondary light is on screen then a second shadow pass needs to be done. This secondary pass will need to render all primary lights a second time (even those off screen). This will possibly 2x the render time for dynamic fog so we recommend using secondary lighting in smaller Scenes or those with cheaper lighting.

```

## docs\markdown\reference\effect.md

```markdown
# Effect

An custom shader that is run on the GPU.

*Local Only:* this Item can only be added to the local scene using the `OBR.scene.local` API.

*Experimental:* this Item is currently experimental and the API is likely to change.

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

|    NAME    |                    TYPE                    | DESCRIPTION                                                                                   |
| :--------: | :----------------------------------------: | :-------------------------------------------------------------------------------------------- |
|    type    |                  "EFFECT"                  | The type of item                                                                              |
|   width    |                   number                   | The width of effect when set to "STANDALONE"                                                  |
|   height   |                   number                   | The height of effect when set to "STANDALONE"                                                 |
| effectType | "STANDALONE" \| "ATTACHMENT" \| "VIEWPORT" | The type of effect. See [here](effects.md#effect-type) for more                               |
|    sksl    |                   string                   | The shader code to use in the Skia shading language. See [here](effects.md) for more          |
|  uniforms  |           [Uniform](#uniform%5D)           | The current uniforms to pass into the effect. See [here](effects.md#custom-uniforms) for more |
| blendMode  |          [BlendMode](#blendmode)           | The blend mode to use for the effect                                                          |

## Type Definitions

### Uniform

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |                                      TYPE                                       | DESCRIPTION                                                      |
| :---: | :-----------------------------------------------------------------------------: | :--------------------------------------------------------------- |
| name  |                                     string                                      | The name of the uniform. This must match the name in the shader  |
| value | number \| [Vector2](vector2.md) \| [Vector3](vector3.md) \| [Matrix](matrix.md) | The value of the uniform. This must match the type in the shader |

### BlendMode

|  TYPE  | values                                                                                                                                                                                                                                                                                                                                                                                   |
| :----: | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| string | "CLEAR" \| "SRC" \| "DST" \| "SRC_OVER" \| "DST_OVER" \| "SRC_IN" \| "DST_IN" \| "SRC_OUT" \| "DST_OUT" \| "SRC_ATOP" \| "DST_ATOP" \| "XOR" \| "PLUS" \| "MODULATE" \| "SCREEN" \| "OVERLAY" \| "DARKEN" \| "LIGHTEN" \| "COLOR_DODGE" \| "COLOR_BURN" \| "HARD_LIGHT" \| "SOFT_LIGHT" \| "DIFFERENCE" \| "EXCLUSION" \| "MULTIPLY" \| "HUE" \| "SATURATION" \| "COLOR" \| "LUMINOSITY" |

```

## docs\markdown\reference\effects.md

```markdown
# Effects

[Effects](effect.md) allow you to create custom shaders that can generate pixels that will be shown in an Owlbear Rodeo Scene.

Effects are written in SkSL which is the shading language used by Skia (the renderer used in Owlbear Rodeo).

It is similar to OpenGL/WebGL's GLSL but with a few differences.

The main function takes in a `float2` coordinate that is in pixel units and it returns a `half4` for the color of the pixel.

For example here is a UV gradient written in SkSL.

uv.frag

``` prism-code
uniform vec2 size;

half4 main(float2 coord) {
  vec2 p = coord / size;
  return half4(p, 0.0, 1.0);
}
```

This could then be used in an Owlbear Rodeo extension:

``` prism-code
import OBR, { buildEffect } from "@owlbear-rodeo/sdk";

const sksl = `
uniform vec2 size;

half4 main(float2 coord) {
  vec2 p = coord / size;
  return half4(p, 0.0, 1.0);
}
`;

const effect = buildEffect()
  .effectType("STANDALONE")
  .width(300)
  .height(300)
  .sksl(sksl)
  .build();

OBR.scene.local.addItems([effect]);
```

This will result in a 300x300 square with a UV gradient.

note

Because of the `coord` input this UV gradient starts in the top left compared to the bottom left coordinate system found in WebGL.

## Built-In Uniforms

Above we use the `size` uniform to convert the pixel coordinate `coord` input into a 0-1 range. Alongside this there are a few more uniforms provided by default to an Effect.

|   NAME    |  TYPE  | DESCRIPTION                                           |
| :-------: | :----: | :---------------------------------------------------- |
|   size    |  vec2  | The current size in pixels of the Effect              |
| position  |  vec2  | The current position of the item in world coordinates |
|   scale   |  vec2  | The current scale of the item                         |
| rotation  | number | The current rotation of the item in degrees           |
|   model   |  mat3  | The local transform of the item                       |
|   view    |  mat3  | The viewport transform                                |
| modelView |  mat3  | The full transform of the item                        |
|   time    | float  | The current unix time of the computer in seconds      |

**Example**

A UV gradient changing with the `time` uniform.

``` prism-code
import OBR, { buildEffect } from "@owlbear-rodeo/sdk";

const sksl = `
uniform vec2 size;
uniform float time;

half4 main(float2 coord) {
  vec2 p = coord / size;
  return half4(p, abs(sin(time)), 1.0);
}
`;

const effect = buildEffect()
  .effectType("STANDALONE")
  .width(300)
  .height(300)
  .sksl(sksl)
  .build();

OBR.scene.local.addItems([effect]);
```

UV gradient changing over time

## Custom Uniforms

An effect can define custom uniforms that will be passed into the shader.

**Example**

Defining two colors as [Vector3](vector3.md)'s.

``` prism-code
import OBR, { buildEffect } from "@owlbear-rodeo/sdk";

const sksl = `
uniform vec2 size;
uniform vec3 colorA;
uniform vec3 colorB;

half4 main(float2 coord) {
  vec2 p = coord / size;
  return half4(mix(colorA, colorB, p.x), 1.0);
}
`;

const effect = buildEffect()
  .effectType("STANDALONE")
  .uniforms([
    { name: "colorA", value: { x: 0.72, y: 0.17, z: 0.15 } },
    { name: "colorB", value: { x: 0.08, y: 0.39, z: 0.75 } },
  ])
  .width(300)
  .height(300)
  .sksl(sksl)
  .build();

OBR.scene.local.addItems([effect]);
```

## Effect Type

Effects come in three types "STANDALONE" \| "ATTACHMENT" \| "VIEWPORT".

Standalone Effects take the width, height and position values of the item and draw a rectangle in the scene. Attachment Effects fill the bounds of the item their attached to with the `attachedTo` value on the item. Viewport Effects fill the viewport.

**Example**

A vignette viewport effect that darkens the edges of the viewport.

``` prism-code
import OBR, { buildEffect } from "@owlbear-rodeo/sdk";

const sksl = `
uniform vec2 size;
uniform mat3 view;

half4 main(float2 coord) {
  // Convert to screen-space coordinates
  vec2 viewCoord = (vec3(coord, 1) * view).xy;
  vec2 p = viewCoord / size;
  // Center p
  p = p * 2.0 - 1.0;
  // Convert p to a circle
  float d = length(p);
  // Use d as an alpha mask
  return half4(vec3(0.0), d);
}
`;

const effect = buildEffect().effectType("VIEWPORT").sksl(sksl).build();

OBR.scene.local.addItems([effect]);
```

## Post Process

When an Effect is placed on the "POST_PROCESS" layer it has access to a new uniform called `scene`. This uniform is of type `shader` and allows this Effect to query the current color value of the Scene.

**Example**

Invert the red and blue channels of everything covered by the attached item.

``` prism-code
import OBR, { buildEffect } from "@owlbear-rodeo/sdk";

const sksl = `
uniform shader scene;
uniform mat3 modelView;

half4 main(float2 coord) {
  vec2 uv = (vec3(coord, 1) * modelView).xy;
  return scene.eval(uv).bgra;
}
`;

// Replace this with the item ID you would like to attach to
const attachedToId = "123";

const effect = buildEffect()
  .effectType("ATTACHMENT")
  .sksl(sksl)
  .locked(true)
  .disableHit(true)
  .layer("POST_PROCESS")
  .attachedTo(attachedToId)
  .build();

OBR.scene.local.addItems([effect]);
```

```

## docs\markdown\reference\filters.md

```markdown
# Filters

A common pattern in the Owlbear Rodeo SDK is the use of a Filter object to control when certain values are used.

A prevalent example is the [IconFilter](../apis/context-menu.md#contextmenuiconfilter) used in the Context Menu.

There is often times when a context menu item should have different icons depending on what is selected. For example the hidden icon should show an open eye if the selected items are visible. If the items are hidden it should show a closed eye instead.

Instead of needing to write an imperative program that listens to changes in the context menu and calls a `setIcon` method we uses a declarative approach. To create a menu item that switches between two icons we initialize our item with two icons. Each icon then has a filter that will tell Owlbear Rodeo which icon to use.

Here's an example of a visibility toggle context menu item.

``` prism-code
OBR.contextMenu.create({
  id: "com.example.visibility",
  icons: [
    {
      icon: "/show.svg",
      label: "Hide",
      // Only use the `show` icon when all selected items are visible
      filter: {
        every: [{ key: "visible", value: true }],
      },
    },
    // Use the `hide` icon by default
    {
      icon: "/hide.svg",
      label: "Show",
    },
  ],
  onClick(context) {
    OBR.scene.items.updateItems(context.items, (items) => {
      const isVisible = items.every((item) => item.visible);
      for (let item of items) {
        item.visible = !isVisible;
      }
    });
  },
});
```

In the example above a KeyFilter is used to check that the [`visible`](item.md) key is set to true on all selected items. If this filter passes then the `show.svg` icon is used. If this filter does not pass then the `hide.svg` icon is used.

### KeyFilter

The key filter is common type of filter used to check a key-value pair on an object.

**Example**

``` prism-code
// The visible property must be `true`
const a = [{ key: "visible", value: true }];

// The visible property must be `true` and the type must not equal `DRAWING`
const b = [
  { key: "visible", value: true },
  { key: "type", value: "DRAWING", operator: "!=" },
];

// The visible property must be `true` or the type must not equal `DRAWING`
const c = [
  { key: "visible", value: true, coordinator: "||" },
  { key: "type", value: "DRAWING", operator: "!=" },
];
```

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |         TYPE         | DESCRIPTION                                                                                                                                     |
| :---------: | :------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------- |
|     key     | string \| string\[\] | The path to the key to check. Works the same as the `path` property in lodash.get                                                               |
|    value    |       unknown        | The value to check                                                                                                                              |
|  operator   |     "==" \| "!="     | The operator to use for the check. By default "==" is used meaning the passed value has to equal the test value.                                |
| coordinator |    "&&" \| "\|\|"    | When an array of filters are used what logical coordinator should be used to combine them. By default a logical "and" operation is used (`&&`). |

```

## docs\markdown\reference\image-upload.md

```markdown
# ImageUploadBuilder

A builder for a new [ImageUpload](../apis/assets.md#imageupload).

# Reference

### `constructor`

``` prism-code
buildImageUpload(file);
```

Create an image upload builder for the given file.

**Parameters**

| NAME  |     TYPE     | DESCRIPTION              |
| :---: | :----------: | :----------------------- |
| file  | File \| Blob | The image file to upload |

------------------------------------------------------------------------

## Methods

### `dpi`

``` prism-code
dpi(dpi);
```

Set the grid [`dpi`](../apis/assets.md#imageupload).

**Parameters**

| NAME  |  TYPE  | DESCRIPTION               |
| :---: | :----: | :------------------------ |
|  dpi  | number | The dpi of the image grid |

Returns the current builder.

------------------------------------------------------------------------

### `offset`

``` prism-code
offset(offset);
```

Set the grid [`offset`](../apis/assets.md#imageupload).

**Parameters**

|  NAME  |         TYPE          | DESCRIPTION                  |
| :----: | :-------------------: | :--------------------------- |
| offset | [Vector2](vector2.md) | The offset of the image grid |

Returns the current builder.

------------------------------------------------------------------------

### `name`

``` prism-code
name(name);
```

Set the upload [`name`](../apis/assets.md#imageupload).

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                                                                                                  |
| :---: | :----: | :----------------------------------------------------------------------------------------------------------- |
| name  | string | The name of the uploaded image. If left blank and a File input is used the `file.name` property will be used |

Returns the current builder.

------------------------------------------------------------------------

### `description`

``` prism-code
description(description: string)
```

Set the items [`description`](../apis/assets.md#imageupload).

**Parameters**

|    NAME     |  TYPE  | DESCRIPTION     |
| :---------: | :----: | :-------------- |
| description | string | The description |

Returns the current builder.

------------------------------------------------------------------------

### `rotation`

``` prism-code
rotation(rotation);
```

Set the image [`rotation`](../apis/assets.md#imageupload).

**Parameters**

|   NAME   |  TYPE  | DESCRIPTION                                  |
| :------: | :----: | :------------------------------------------- |
| rotation | number | The default rotation of the image in degrees |

Returns the current builder.

------------------------------------------------------------------------

### `scale`

``` prism-code
scale(scale);
```

Set the image [`scale`](../apis/assets.md#imageupload).

**Parameters**

| NAME  |         TYPE          | DESCRIPTION                    |
| :---: | :-------------------: | :----------------------------- |
| scale | [Vector2](vector2.md) | The default scale of the image |

Returns the current builder.

------------------------------------------------------------------------

### `locked`

``` prism-code
locked(locked);
```

Set the items [`locked`](../apis/assets.md#imageupload) boolean.

**Parameters**

|  NAME  |  TYPE   | DESCRIPTION        |
| :----: | :-----: | :----------------- |
| locked | boolean | The locked setting |

Returns the current builder.

------------------------------------------------------------------------

### `visible`

``` prism-code
visible(visible);
```

Set the items [`visible`](../apis/assets.md#imageupload) boolean.

**Parameters**

|  NAME   |  TYPE   | DESCRIPTION         |
| :-----: | :-----: | :------------------ |
| visible | boolean | The visible setting |

Returns the current builder.

------------------------------------------------------------------------

### `text`

``` prism-code
text(text);
```

Set the images [`text content`](../apis/assets.md#imageupload).

**Parameters**

| NAME  |              TYPE              | DESCRIPTION                    |
| :---: | :----------------------------: | :----------------------------- |
| text  | [TextContent](text-content.md) | The content of the images text |

Returns the current builder.

------------------------------------------------------------------------

### `textItemType`

``` prism-code
textItemType(textItemType);
```

Set the images [`text item type`](../apis/assets.md#imageupload).

**Parameters**

|     NAME     |       TYPE        | DESCRIPTION                 |
| :----------: | :---------------: | :-------------------------- |
| textItemType | "LABEL" \| "TEXT" | The type of the images text |

Returns the current builder.

------------------------------------------------------------------------

### `textWidth`

``` prism-code
textWidth(width);
```

Set the image texts [`width`](../apis/assets.md#imageupload).

**Parameters**

| NAME  |                 TYPE                 | DESCRIPTION    |
| :---: | :----------------------------------: | :------------- |
| width | [TextSize](text-content.md#textsize) | The text width |

Returns the current builder.

------------------------------------------------------------------------

### `textHeight`

``` prism-code
textHeight(height);
```

Set the image texts [`height`](../apis/assets.md#imageupload).

**Parameters**

|  NAME  |                 TYPE                 | DESCRIPTION     |
| :----: | :----------------------------------: | :-------------- |
| height | [TextSize](text-content.md#textsize) | The text height |

Returns the current builder.

------------------------------------------------------------------------

### `richText`

``` prism-code
richText(richText);
```

Set the image texts [`richText`](../apis/assets.md#imageupload).

**Parameters**

|   NAME   |                 TYPE                 | DESCRIPTION   |
| :------: | :----------------------------------: | :------------ |
| richText | [RichText](text-content.md#richtext) | The rich text |

Returns the current builder.

------------------------------------------------------------------------

### `plainText`

``` prism-code
plainText(plainText);
```

Set the image texts [`plainText`](../apis/assets.md#imageupload).

**Parameters**

|   NAME    |  TYPE  | DESCRIPTION    |
| :-------: | :----: | :------------- |
| plainText | string | The plain text |

Returns the current builder.

------------------------------------------------------------------------

### `textType`

``` prism-code
textType(textType);
```

Set the image texts [`textType`](../apis/assets.md#imageupload).

**Parameters**

|   NAME   |       TYPE        | DESCRIPTION   |
| :------: | :---------------: | :------------ |
| textType | "PLAIN" \| "RICH" | The text type |

Returns the current builder.

------------------------------------------------------------------------

### `textPadding`

``` prism-code
textPadding(padding);
```

Set the image text styles [`padding`](text-content.md#textstyle).

**Parameters**

|  NAME   |  TYPE  | DESCRIPTION      |
| :-----: | :----: | :--------------- |
| padding | number | The text padding |

Returns the current builder.

------------------------------------------------------------------------

### `fontFamily`

``` prism-code
fontFamily(fontFamily);
```

Set the image text styles [`fontFamily`](text-content.md#textstyle).

**Parameters**

|    NAME    |  TYPE  | DESCRIPTION          |
| :--------: | :----: | :------------------- |
| fontFamily | string | The text font family |

Returns the current builder.

------------------------------------------------------------------------

### `fontSize`

``` prism-code
fontSize(fontSize);
```

Set the image text styles [`fontSize`](text-content.md#textstyle).

**Parameters**

|   NAME   |  TYPE  | DESCRIPTION        |
| :------: | :----: | :----------------- |
| fontSize | number | The text font size |

Returns the current builder.

------------------------------------------------------------------------

### `fontWeight`

``` prism-code
fontWeight(fontWeight);
```

Set the image text styles [`fontWeight`](text-content.md#textstyle).

**Parameters**

|    NAME    |  TYPE  | DESCRIPTION          |
| :--------: | :----: | :------------------- |
| fontWeight | number | The text font weight |

Returns the current builder.

------------------------------------------------------------------------

### `textAlign`

``` prism-code
textAlign(textAlign);
```

Set the image text styles [`textAlign`](text-content.md#textstyle).

**Parameters**

|   NAME    |             TYPE              | DESCRIPTION                   |
| :-------: | :---------------------------: | :---------------------------- |
| textAlign | "LEFT" \| "CENTER" \| "RIGHT" | The text horizontal alignment |

Returns the current builder.

------------------------------------------------------------------------

### `textAlignVertical`

``` prism-code
textAlignVertical(textAlignVertical);
```

Set the image text styles [`textAlignVertical`](text-content.md#textstyle).

**Parameters**

|       NAME        |             TYPE              | DESCRIPTION                 |
| :---------------: | :---------------------------: | :-------------------------- |
| textAlignVertical | "BOTTOM" \| "MIDDLE" \| "TOP" | The text vertical alignment |

Returns the current builder.

------------------------------------------------------------------------

### `textFillColor`

``` prism-code
textFillColor(fillColor);
```

Set the image text styles [`fillColor`](text-content.md#textstyle).

**Parameters**

|   NAME    |  TYPE  | DESCRIPTION          |
| :-------: | :----: | :------------------- |
| fillColor | string | The texts fill color |

Returns the current builder.

------------------------------------------------------------------------

### `textFillOpacity`

``` prism-code
textFillOpacity(fillOpacity);
```

Set the image text styles [`fillOpacity`](text-content.md#textstyle).

**Parameters**

|    NAME     |  TYPE  | DESCRIPTION            |
| :---------: | :----: | :--------------------- |
| fillOpacity | number | The texts fill opacity |

Returns the current builder.

------------------------------------------------------------------------

### `textStrokeColor`

``` prism-code
textStrokeColor(strokeColor);
```

Set the image text styles [`strokeColor`](text-content.md#textstyle).

**Parameters**

|    NAME     |  TYPE  | DESCRIPTION            |
| :---------: | :----: | :--------------------- |
| strokeColor | string | The texts stroke color |

Returns the current builder.

------------------------------------------------------------------------

### `textStrokeOpacity`

``` prism-code
textStrokeOpacity(strokeOpacity);
```

Set the image text styles [`strokeOpacity`](text-content.md#textstyle).

**Parameters**

|     NAME      |  TYPE  | DESCRIPTION              |
| :-----------: | :----: | :----------------------- |
| strokeOpacity | number | The texts stroke opacity |

Returns the current builder.

------------------------------------------------------------------------

### `textStrokeWidth`

``` prism-code
textStrokeWidth(strokeWidth);
```

Set the image text styles [`strokeWidth`](text-content.md#textstyle).

**Parameters**

|    NAME     |  TYPE  | DESCRIPTION            |
| :---------: | :----: | :--------------------- |
| strokeWidth | number | The texts stroke width |

Returns the current builder.

------------------------------------------------------------------------

### `textLineHeight`

``` prism-code
textLineHeight(lineHeight);
```

Set the image text styles [`lineHeight`](text-content.md#textstyle).

**Parameters**

|    NAME    |  TYPE  | DESCRIPTION           |
| :--------: | :----: | :-------------------- |
| lineHeight | number | The texts line height |

Returns the current builder.

------------------------------------------------------------------------

### `build`

``` prism-code
build();
```

Returns the final [ImageUpload](../apis/assets.md#imageupload).

------------------------------------------------------------------------

```

## docs\markdown\reference\image.md

```markdown
# Image

An image item that loads from a url

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |              TYPE              | DESCRIPTION                                                                                                                                                                                |
| :----------: | :----------------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|     type     |            "IMAGE"             | The type of item                                                                                                                                                                           |
|    image     | [ImageContent](#imagecontent)  | The image to show                                                                                                                                                                          |
|     grid     |    [ImageGrid](#imagegrid)     | The grid scale of the image                                                                                                                                                                |
|     text     | [TextContent](text-content.md) | The text displayed over the image                                                                                                                                                          |
| textItemType |       "LABEL" \| "TEXT"        | The type of text to use for this image. The "LABEL" option will display the text as a label on the bottom of the image. The "TEXT" option will display the text over the top of the image. |

## Type Definitions

### ImageContent

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |  TYPE  | DESCRIPTION                                                    |
| :----: | :----: | :------------------------------------------------------------- |
| width  | number | The width of the image in pixels                               |
| height | number | The height of the image in pixels                              |
|  mime  | string | The mime type of the image e.g. "image/jpeg" or "video/mp4"    |
|  url   | string | The url of the image to load. The image must have CORS enabled |

### ImageGrid

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |           TYPE            | DESCRIPTION                                                                          |
| :----: | :-----------------------: | :----------------------------------------------------------------------------------- |
| offset | [Vector2](vector2.md)\[\] | Offset relative to the image dimensions                                              |
|  dpi   |          number           | Dots per inch of the image. Determines the resolution of one grid cell in the image. |

```

## docs\markdown\reference\item.md

```markdown
# Item

The abstract interface for all Items.

|  TYPE  |
| :----: |
| object |

**Properties**

|           NAME            |                     TYPE                      | DESCRIPTION                                                          |
| :-----------------------: | :-------------------------------------------: | :------------------------------------------------------------------- |
|            id             |                    string                     | The ID of this item (read only)                                      |
|           type            |                    string                     | The type of item                                                     |
|           name            |                    string                     | The name of the item                                                 |
|          visible          |                    boolean                    | Is this item visible                                                 |
|          locked           |                    boolean                    | Is this item locked                                                  |
|       createdUserId       |                    string                     | The user ID of the player who created this item                      |
|          zIndex           |                    number                     | The depth order of this item compared to other items on this layer   |
|       lastModified        |                    string                     | When this item was last modified (read only)                         |
|    lastModifiedUserId     |                    string                     | The user ID of the player who last modified this item (read only)    |
|         position          |             [Vector2](vector2.md)             | The position of this item                                            |
|         rotation          |                    number                     | The rotation of this item in degrees                                 |
|           scale           |             [Vector2](vector2.md)             | The scale of this item                                               |
|         metadata          |            [Metadata](manifest.md)            | Custom metadata for this item                                        |
|           layer           |                [Layer](#layer)                | The layer that this item is on                                       |
|        attachedTo         |                    string                     | The optional ID of the item this is attached to                      |
|        disableHit         |                    boolean                    | An optional boolean to disable the hit detection for this item       |
|     disableAutoZIndex     |                    boolean                    | An optional boolean to disable the auto z-index update for this item |
| disableAttachmentBehavior | [AttachmentBehavior](#attachmentbehavior)\[\] | An optional array of attachment behaviors to disable                 |
|        description        |                    string                     | An optional description used by assistive technology                 |

## Type Definitions

### Layer

|  TYPE  | values                                                                                                                                                                            |
| :----: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| string | "MAP" \| "GRID" \| "DRAWING" \| "PROP" \| "MOUNT" \| "CHARACTER" \| "ATTACHMENT" \| "NOTE" \| "TEXT" \| "RULER" \| "FOG" \| "POINTER" \| "POST_PROCESS" \| "CONTROL" \| "POPOVER" |

### AttachmentBehavior

|  TYPE  | values                                                                             |
| :----: | :--------------------------------------------------------------------------------- |
| string | "VISIBLE" \| "SCALE" \| "ROTATION" \| "POSITION" \| "DELETE" \| "LOCKED" \| "COPY" |

```

## docs\markdown\reference\items.md

```markdown
# Items

Items that can be added to a Scene

## 📄️ Billboard

A billboard image that loads from a url.

## 📄️ Curve

A shape with a list of 2D points

## 📄️ Effect

An custom shader that is run on the GPU.

## 📄️ Image

An image item that loads from a url

## 📄️ Item

The abstract interface for all Items.

## 📄️ Label

A text label with a colored background

## 📄️ Light

An light that interacts with the Dynamic Fog system.

## 📄️ Line

A straight line between two points

## 📄️ Path

A raw path defined with a list of drawing commands

## 📄️ Pointer

A circle shape that when moved leaves a trail

## 📄️ Ruler

A straight line ruler

## 📄️ Shape

A circle, rectangle, triangle or hexagon

## 📄️ Text

A text item without any background

## 📄️ Wall

An invisible wall that interacts with the Dynamic Fog system.

```

## docs\markdown\reference\label.md

```markdown
# Label

A text label with a colored background

Labels are scaled in screen-space. This means that they will stay the same size independent to the zoom level of the scene.

Labels do not support rich text or user editing.

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |              TYPE              | DESCRIPTION                     |
| :---: | :----------------------------: | :------------------------------ |
| type  |            "LABEL"             | The type of item                |
| text  | [TextContent](text-content.md) | The text displayed in the label |
| style |   [LabelStyle](#labelstyle)    | The style of the label          |

## Type Definitions

### LabelStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|       NAME        |                TYPE                 | DESCRIPTION                                                     |
| :---------------: | :---------------------------------: | :-------------------------------------------------------------- |
|  backgroundColor  |               string                | The background color of the label                               |
| backgroundOpacity |               number                | The background opacity of the label                             |
|   cornerRadius    |               string                | The radius of the labels corner in pixels                       |
|   pointerWidth    |               number                | An optional width for the label arrow in pixels                 |
|   pointerHeight   |               number                | An optional height for the label arrow in pixels                |
| pointerDirection  | "UP" \| "DOWN" \| "LEFT" \| "RIGHT" | An optional direction for the label arrow                       |
|   maxViewScale    |               number                | An optional maximum the label will use for screen-space scaling |
|   minViewScale    |               number                | An optional minimum the label will use for screen-space scaling |

```

## docs\markdown\reference\light.md

```markdown
# Light

An light that interacts with the Dynamic Fog system.

Outside of interacting with the fog system this item has no visuals.

The `zIndex` parameter for this item is treated specially see [Dynamic Fog](dynamic-fog.md#elevation) for a break down on how this works.

*Local Only:* this Item can only be added to the local scene using the `OBR.scene.local` API.

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|       NAME        |                  TYPE                   | DESCRIPTION                                                                                                                                                                                                             |
| :---------------: | :-------------------------------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
|       type        |                 "LIGHT"                 | The type of item                                                                                                                                                                                                        |
| attenuationRadius |                 number                  | The outer radius of affect for this light source in world coordinates                                                                                                                                                   |
|   sourceRadius    |                 number                  | The inner radius for this light in world coordinates. This affects how hard/soft the shadows of this light will be as well as the collision distance for blocking Walls                                                 |
|      falloff      |                 number                  | The falloff for the outer edge of the light. This is in normalized coordinates where 0 represents no falloff and 1 full falloff. This value can be driven above 1 for even greater falloff                              |
|    innerAngle     |                 number                  | The inner angle to constrain this light from a circle to a cone. For a hard shadowed cone the `innerAngle` and `outerAngle` should be the same. For soft shadowed the `innerAngle` should be less than the `outerAngle` |
|    outerAngle     |                 number                  | The outer angle to constrain this light from a circle to a cone. For a hard shadowed cone the `innerAngle` and `outerAngle` should be the same. For soft shadowed the `innerAngle` should be less than the `outerAngle` |
|     lightType     | "PRIMARY" \| "SECONDARY" \| "AUXILIARY" | The type of light. See [here](dynamic-fog.md#secondary-lighting) for more                                                                                                                                               |

```

## docs\markdown\reference\line.md

```markdown
# Line

A straight line between two points

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME      |          TYPE           | DESCRIPTION                    |
| :-----------: | :---------------------: | :----------------------------- |
|     type      |         "LINE"          | The type of item               |
| startPosition |  [Vector2](vector2.md)  | The start position of the line |
|  endPosition  |  [Vector2](vector2.md)  | The end position of the line   |
|     style     | [LineStyle](#linestyle) | The style of the curve         |

## Type Definitions

### LineStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME      |    TYPE    | DESCRIPTION                                    |
| :-----------: | :--------: | :--------------------------------------------- |
|  strokeColor  |   string   | The stroke color of the line                   |
| strokeOpacity |   number   | The stroke opacity of the line between 0 and 1 |
|  strokeWidth  |   number   | The stroke width of the line in pixels         |
|  strokeDash   | number\[\] | The pattern of the line dash                   |

```

## docs\markdown\reference\manifest.md

```markdown
# Manifest

A manifest contains information about the extension and is necessary for loading an extension.

|  TYPE  |
| :----: |
| object |

**Properties**

|       NAME       |                     TYPE                      | DESCRIPTION                                                               |
| :--------------: | :-------------------------------------------: | :------------------------------------------------------------------------ |
|       name       |                    string                     | The name of the extension, limited to 45 characters                       |
|     version      |                    string                     | The version number of the extension                                       |
| manifest_version |                    number                     | The targeted manifest version                                             |
|   description    |                    string                     | The description of the extension, limited to 128 characters               |
|       icon       |                    string                     | An optional path to the extensions icon                                   |
|      author      |                    string                     | An optional author to display for the extension                           |
|   homepage_url   |                    string                     | An optional link to a home page for the extension                         |
|      action      |       [ManifestAction](#manifestaction)       | An optional action for this extension                                     |
|  background_url  |                    string                     | An optional url to load as a background script                            |
|   permissions    | [ManifestPermission](#manifestpermission)\[\] | An optional array of permissions to give to all iframes of your extension |

## Type Definitions

### ManifestAction

The action definition for a manifest.

To control the action after an extension has been loaded see the [Action API](../apis/action.md).

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME   |  TYPE  | DESCRIPTION                            |
| :-----: | :----: | :------------------------------------- |
|  title  | string | The initial title of the action        |
|  icon   | string | The initial icon of the action         |
| popover | string | The url of the popover page to load    |
|  width  | number | An optional max width for the popover  |
| height  | number | An optional max height for the popover |

### ManifestPermission

Permissions used with the iframe allow property of your extension and a reason why you need it.

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |                       TYPE                        | DESCRIPTION                |
| :----: | :-----------------------------------------------: | :------------------------- |
|  name  | [ManifestPermissionName](#manifestpermissionname) | The name of the permission |
| reason |                      string                       | The reason for use         |

### ManifestPermissionName

The currently supported values available for a manifest permission

|  TYPE  | values                                                                                                                                |
| :----: | :------------------------------------------------------------------------------------------------------------------------------------ |
| string | "clipboard-write" \| "clipboard-read" \| "autoplay" \| "bluetooth" \| "camera" \| "microphone" \| "usb" \| "display-capture" \| "hid" |

```

## docs\markdown\reference\math-2.md

```markdown
# Math2

Math class for [Vector2](vector2.md)'s.

## Example

### Add two [Vector2](vector2.md)'s

``` prism-code
const a: Vector2 = { x: 100, y: 100 };
const b: Vector2 = { x: 50, y: 50 };
const c = Math2.add(a, b);
```

# Reference

## Methods

### `magnitudeSquared`

``` prism-code
magnitudeSquared(p);
```

Returns the squared length of vector `p`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   p   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `magnitude`

``` prism-code
magnitude(p);
```

Returns the length of vector `p`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   p   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `normalize`

``` prism-code
normalize(p);
```

Returns `p` normalized, if length of `p` is 0 `{x: 0, y: 0}` is returned

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   p   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `dot`

``` prism-code
dot(a, b);
```

Returns the dot product between `a` and `b`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |
|   b   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `subtract`

``` prism-code
subtract(a, b);
```

Returns `a` minus `b`

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `add`

``` prism-code
add(a, b);
```

Returns `a` plus `b`

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `multiply`

``` prism-code
multiply(a, b);
```

Returns `a` multiplied by `b`

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `divide`

``` prism-code
divide(a, b);
```

Returns `a` divided by `b`

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `rotate`

``` prism-code
rotate(point, origin, angle);
```

Rotates a point around a given origin by an angle in degrees

Returns the rotated point

**Parameters**

|  NAME  |         TYPE          | DESCRIPTION                  |
| :----: | :-------------------: | :--------------------------- |
| point  | [Vector2](vector2.md) | Point to rotate              |
| origin | [Vector2](vector2.md) | Origin of the rotation       |
| angle  |        number         | Angle of rotation in degrees |

------------------------------------------------------------------------

### `min`

``` prism-code
min(a, b);
```

Returns the min of `a` and `b` as a Vector

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `componentMin`

``` prism-code
min(a);
```

Returns the component wise minimum of `a`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `max`

``` prism-code
max(a, b);
```

Returns the max of `a` and `b` as a Vector

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `componentMax`

``` prism-code
max(a);
```

Returns the component wise maximum of `a`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `roundTo`

``` prism-code
roundTo(p, to);
```

Rounds `p` to the nearest value of `to`

Returns the rounded vector

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   p   | [Vector2](vector2.md) |
|  to   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `floorTo`

``` prism-code
floorTo(p, to);
```

Floors `p` to the nearest value of `to`

Returns the floored vector

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   p   | [Vector2](vector2.md) |
|  to   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `sign`

``` prism-code
sign(a);
```

Returns the component wise sign of `a`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `abs`

``` prism-code
abs(a);
```

Returns the component wise absolute of `a`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `pow`

``` prism-code
pow(a, b);
```

Returns `a` to the power of `b`

**Parameters**

| NAME  |              TYPE               |
| :---: | :-----------------------------: |
|   a   |      [Vector2](vector2.md)      |
|   b   | [Vector2](vector2.md) \| number |

------------------------------------------------------------------------

### `clamp`

``` prism-code
clamp(a, min max)
```

Returns `a` clamped between `min` and `max`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |
|  min  |        number         |
|  max  |        number         |

------------------------------------------------------------------------

### `boundingBox`

``` prism-code
boundingBox(points);
```

Returns an axis-aligned [BoundingBox](bounding-box.md) around an array of points

**Parameters**

|  NAME  |           TYPE            |
| :----: | :-----------------------: |
| points | [Vector2](vector2.md)\[\] |

------------------------------------------------------------------------

### `pointInPolygon`

``` prism-code
pointInPolygon(p, points);
```

Checks to see if a point is in a polygon

Returns true if the given point `p` is inside the polygon made by `points`

**Parameters**

|  NAME  |           TYPE            |
| :----: | :-----------------------: |
|   p    |   [Vector2](vector2.md)   |
| points | [Vector2](vector2.md)\[\] |

------------------------------------------------------------------------

### `compare`

``` prism-code
compare(a, b, threshold);
```

Returns true if the the distance between `a` and `b` is under `threshold`

**Parameters**

|   NAME    |         TYPE          |
| :-------: | :-------------------: |
|     a     | [Vector2](vector2.md) |
|     b     | [Vector2](vector2.md) |
| threshold |        number         |

------------------------------------------------------------------------

### `distance`

``` prism-code
distance(a, b);
```

Returns the euclidean distance between `a` and `b`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |
|   b   | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `lerp`

``` prism-code
lerp(a, b, alpha);
```

Returns the linear interpolation between `a` and `b` by `alpha`

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
|   a   | [Vector2](vector2.md) |
|   b   | [Vector2](vector2.md) |
| alpha |        number         |

------------------------------------------------------------------------

### `centroid`

``` prism-code
centroid(points);
```

Returns the centroid of the given points

**Parameters**

|  NAME  |           TYPE            |
| :----: | :-----------------------: |
| points | [Vector2](vector2.md)\[\] |

------------------------------------------------------------------------

```

## docs\markdown\reference\math-m.md

```markdown
# MathM

Math class for a 2D transformation [Matrix](matrix.md).

## Examples

### Find the relative transform between two items

``` prism-code
const a = buildShape().build();
const b = buildShape().build();

const aTransform = MathM.fromItem(a);
const bTransform = MathM.fromItem(b);

const invATransform = MathM.inverse(aTransform);
const relativeBTransform = MathM.multiply(invATransform, bTransform);
```

### Find the world position of a line's `startPosition`

``` prism-code
const line = buildLine().build();

const lineTransform = MathM.fromItem(line);
const startTransform = MathM.fromPosition(line.startPosition);

const worldTransform = MathM.multiply(lineTransform, startTransform);

const worldPosition = MathM.decompose(worldTransform).position;
```

# Reference

## Methods

### `inverse`

``` prism-code
inverse(matrix);
```

Returns the inverse of the given `matrix`

**Parameters**

|  NAME  |        TYPE         |
| :----: | :-----------------: |
| matrix | [Matrix](matrix.md) |

------------------------------------------------------------------------

### `multiply`

``` prism-code
multiply(a, b);
```

Returns `a` multiplied by `b`

**Parameters**

| NAME  |        TYPE         |
| :---: | :-----------------: |
|   a   | [Matrix](matrix.md) |
|   b   | [Matrix](matrix.md) |

------------------------------------------------------------------------

### `fromPosition`

``` prism-code
fromPosition(position);
```

Create a new transformation matrix from a position

Returns a [Matrix](matrix.md)

**Parameters**

|   NAME   |         TYPE          |
| :------: | :-------------------: |
| position | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `fromRotation`

``` prism-code
fromRotation(rotation);
```

Create a new transformation matrix from a rotation

Returns a [Matrix](matrix.md)

**Parameters**

|   NAME   |  TYPE  | DESCRIPTION         |
| :------: | :----: | :------------------ |
| rotation | number | Rotation in degrees |

------------------------------------------------------------------------

### `fromScale`

``` prism-code
fromScale(scale);
```

Create a new transformation matrix from a scale

Returns a [Matrix](matrix.md)

**Parameters**

| NAME  |         TYPE          |
| :---: | :-------------------: |
| scale | [Vector2](vector2.md) |

------------------------------------------------------------------------

### `fromItem`

``` prism-code
fromItem(item);
```

Create a new transformation matrix from a [Item](item.md)

Returns a [Matrix](matrix.md)

**Parameters**

| NAME  |      TYPE       |
| :---: | :-------------: |
| item  | [Item](item.md) |

------------------------------------------------------------------------

### `decompose`

``` prism-code
decompose(matrix);
```

Decompose a matrix into its individual parts

Returns the position, scale and rotation (in degrees) of the matrix

**Parameters**

|  NAME  |        TYPE         |
| :----: | :-----------------: |
| matrix | [Matrix](matrix.md) |

------------------------------------------------------------------------

```

## docs\markdown\reference\math.md

```markdown
# Math

To help with updating item transforms the SDK ships with two static Math libraries.

## 📄️ Math2

Math class for Vector2's.

## 📄️ MathM

Math class for a 2D transformation Matrix.

```

## docs\markdown\reference\matrix.md

```markdown
# Matrix

A 3x3 2D transformation matrix

| TYPE  |
| :---: |
| array |

**Properties**

``` prism-code
[
  m1, m2, m3,
  m4, m5, m6,
  m7, m8, m9
]
```

### Example

A translation matrix shifted by `x` and `y`

``` prism-code
[
  1, 0, x,
  0, 1, y,
  0, 0, 1
]
```

```

## docs\markdown\reference\metadata.md

```markdown
# Metadata

The Metadata object is a common pattern in the Owlbear Rodeo SDK that allows your extension to store/share custom data.

All items in a scene have a metadata property that allows you to store custom data.

All players also have a metadata property that allows you to share custom data associated with that player.

**Best Practices**

When using a metadata property be aware that you will be sharing this resource with other extensions. This means it is necessary that you do all you can to avoid namespace collisions.

Our recommendation is that you prefix all your keys in the metadata with a common identifier for your extension.

The convention used in our tutorial and example projects is to use a reverse domain name notation such as `com.example.metadata` that represents the domain for your extension.

For example the metadata used in our [initiative tracker tutorial](https://docs.owlbear.rodeo/extensions/tutorial-initiative-tracker/implement-the-context-menu-item) looks like this:

``` prism-code
{
  "com.tutorial.initiative-tracker/metadata": {
    initiative: number,
  },
};
```

|           TYPE            |
| :-----------------------: |
| Record\<string, unknown\> |

```

## docs\markdown\reference\path.md

```markdown
# Path

A raw path defined with a list of drawing commands

If you just want to draw a freeform shape see the simpler [Curve](curve.md) item

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |              TYPE               | DESCRIPTION                   |
| :------: | :-----------------------------: | :---------------------------- |
|   type   |             "PATH"              | The type of item              |
| commands | [PathCommand](#pathcommand)\[\] | The list of drawing commands  |
|  style   |     [PathStyle](#pathstyle)     | The style of the path         |
| fillRule |             string              | Either "nonzero" or "evenodd" |

## Type Definitions

### PathStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME      |    TYPE    | DESCRIPTION                                     |
| :-----------: | :--------: | :---------------------------------------------- |
|   fillColor   |   string   | The fill color of the shape                     |
|  fillOpacity  |   number   | The fill opacity of the shape between 0 and 1   |
|  strokeColor  |   string   | The stroke color of the shape                   |
| strokeOpacity |   number   | The stroke opacity of the shape between 0 and 1 |
|  strokeWidth  |   number   | The stroke width of the shape in pixels         |
|  strokeDash   | number\[\] | The pattern of the stroke dash                  |

### PathCommand

|                                                                                             TYPE                                                                                             |
| :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [MoveCommand](#movecommand) \| [LineCommand](#linecommand) \| [QuadCommand](#quadcommand) \| [ConicCommand](#coniccommand) \| [CubicCommand](#cubiccommand) \| [CloseCommand](#closecommand) |

### Command

| TYPE  | values                                |
| :---: | :------------------------------------ |
| Enum  | MOVE, LINE, QUAD, CONIC, CUBIC, CLOSE |

## Commands

### MoveCommand

Begins a new sub-path at the given `(x, y)`.

Reference.

|    TYPE    | values                             |
| :--------: | :--------------------------------- |
| number\[\] | \[[Command.Move](#command), x, y\] |

### LineCommand

Draw a line from the last point to the given `(x, y)`.

Reference.

|    TYPE    | values                             |
| :--------: | :--------------------------------- |
| number\[\] | \[[Command.Line](#command), x, y\] |

### QuadCommand

Draw a quadratic curve from the last point to `(x2, y2)` with the control point `(x1, y1)`.

Reference.

|    TYPE    | values                                       |
| :--------: | :------------------------------------------- |
| number\[\] | \[[Command.Quad](#command), x1, y1, x2, y2\] |

### ConicCommand

Draw a conic from the last point to `(x2, y2)` with the control point `(x1, y1)` and the weight `w`.

Reference.

|    TYPE    | values                                           |
| :--------: | :----------------------------------------------- |
| number\[\] | \[[Command.Conic](#command), x1, y1, x2, y2, w\] |

### CubicCommand

Draw a cubic from the last point to `(x3, y3)` with the control points `(x1, y1)` and `(x2, y2)`.

Reference.

|    TYPE    | values                                                |
| :--------: | :---------------------------------------------------- |
| number\[\] | \[[Command.Cubic](#command), x1, y1, x2, y2, x3, y3\] |

### CloseCommand

Close the current sub-path.

Reference.

|    TYPE    | values                        |
| :--------: | :---------------------------- |
| number\[\] | \[[Command.Close](#command)\] |

```

## docs\markdown\reference\permission.md

```markdown
# Permission

The user can set various permissions that allow them to control what features the player has access to.

This is controlled by a list of enum strings representing create, update and delete permissions for each layer.

|  TYPE  | values                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| :----: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| string | "FOG_CREATE" \| "FOG_UPDATE" \| "FOG_DELETE" \| "MAP_CREATE" \| "MAP_UPDATE" \| "MAP_DELETE" \| "PROP_CREATE" \| "PROP_UPDATE" \| "PROP_DELETE" \| "MOUNT_CREATE" \| "MOUNT_UPDATE" \| "MOUNT_DELETE" \| "CHARACTER_CREATE" \| "CHARACTER_UPDATE" \| "CHARACTER_DELETE" \| "CHARACTER_OWNER_ONLY" \| "ATTACHMENT_CREATE" \| "ATTACHMENT_UPDATE" \| "ATTACHMENT_DELETE" \| "NOTE_CREATE" \| "NOTE_UPDATE" \| "NOTE_DELETE" \| "DRAWING_CREATE" \| "DRAWING_UPDATE" \| "DRAWING_DELETE" \| "RULER_CREATE" \| "RULER_UPDATE" \| "RULER_DELETE" \| "POINTER_CREATE" \| "POINTER_UPDATE" \| "POINTER_DELETE" \| "TEXT_CREATE" \| "TEXT_UPDATE" \| "TEXT_DELETE"; |

```

## docs\markdown\reference\player.md

```markdown
# Player

A player connected to a room.

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME     |          TYPE           | DESCRIPTION                                                                                              |
| :----------: | :---------------------: | :------------------------------------------------------------------------------------------------------- |
|      id      |         string          | The user ID for this player. This will be shared if the same player joins a room multiple times          |
| connectionId |         string          | The ID for this players connection. This will be unique if the same player joins the room multiple times |
|     role     |    "GM" \| "PLAYER"     | The current role for the player                                                                          |
|  selection   |       string\[\]        | An optional array of item IDs referencing what this player has selected                                  |
|    color     |         string          | The chosen color for this player                                                                         |
|   syncView   |         boolean         | Whether this player has sync view enabled                                                                |
|   metadata   | [Metadata](metadata.md) | The custom metadata for this player                                                                      |

------------------------------------------------------------------------

```

## docs\markdown\reference\pointer.md

```markdown
# Pointer

A circle shape that when moved leaves a trail

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |   TYPE    | DESCRIPTION                         |
| :----: | :-------: | :---------------------------------- |
|  type  | "POINTER" | The type of item                    |
| color  |  string   | The color of the pointer            |
| radius |  number   | The radius of the pointer in pixels |

```

## docs\markdown\reference\reference.md

```markdown
# Reference

Common types and interfaces for the SDK

## 📄️ BoundingBox

An axis-aligned bounding box

## 🗃️ Builders

14 items

## 📄️ Dynamic Fog

The Dynamic Fog system is controlled with the Light and Wall items.

## 📄️ Effects

Effects allow you to create custom shaders that can generate pixels that will be shown in an Owlbear Rodeo Scene.

## 📄️ Filters

A common pattern in the Owlbear Rodeo SDK is the use of a Filter object to control when certain values are used.

## 🗃️ Items

14 items

## 📄️ Manifest

A manifest contains information about the extension and is necessary for loading an extension.

## 🗃️ Math

2 items

## 📄️ Matrix

A 3x3 2D transformation matrix

## 📄️ Metadata

The Metadata object is a common pattern in the Owlbear Rodeo SDK that allows your extension to store/share custom data.

## 📄️ Permission

The user can set various permissions that allow them to control what features the player has access to.

## 📄️ Player

A player connected to a room.

## 📄️ TextContent

Describes all information needed to display text.

## 📄️ Vector2

A point with an x and y coordinate

## 📄️ Vector3

A point with an x, y and z coordinate

```

## docs\markdown\reference\ruler.md

```markdown
# Ruler

A straight line ruler

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME      |           TYPE            | DESCRIPTION                       |
| :-----------: | :-----------------------: | :-------------------------------- |
|     type      |          "RULER"          | The type of item                  |
| startPosition |   [Vector2](vector2.md)   | The start position of the ruler   |
|  endPosition  |   [Vector2](vector2.md)   | The end position of the ruler     |
|  measurement  |          string           | The value to display on the ruler |
|     style     | [RulerStyle](#rulerstyle) | The style of the ruler            |

## Type Definitions

### RulerStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME   |         TYPE         | DESCRIPTION                              |
| :-----: | :------------------: | :--------------------------------------- |
| variant | "FILLED" \| "DASHED" | The visual style of the ruler background |

```

## docs\markdown\reference\scene-upload.md

```markdown
# SceneUploadBuilder

A builder for a new [SceneUpload](../apis/assets.md#sceneupload).

# Reference

## Methods

### `name`

``` prism-code
name(name);
```

Set the upload [`name`](../apis/assets.md#sceneupload).

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                    |
| :---: | :----: | :----------------------------- |
| name  | string | The name of the uploaded scene |

Returns the current builder.

------------------------------------------------------------------------

### `fogFilled`

``` prism-code
fogFilled(filled);
```

Set the scenes fog [`filled`](../apis/fog.md).

**Parameters**

|  NAME  |  TYPE   | DESCRIPTION                     |
| :----: | :-----: | :------------------------------ |
| filled | boolean | The new filled state of the fog |

Returns the current builder.

------------------------------------------------------------------------

### `fogColor`

``` prism-code
fogColor(color);
```

Set the scenes fog [`color`](../apis/fog.md).

**Parameters**

| NAME  |  TYPE  | DESCRIPTION              |
| :---: | :----: | :----------------------- |
| color | string | The new color of the fog |

Returns the current builder.

------------------------------------------------------------------------

### `fogStrokeWidth`

``` prism-code
fogStrokeWidth(width);
```

Set the scenes fog [`strokeWidth`](../apis/fog.md).

**Parameters**

| NAME  |  TYPE  | DESCRIPTION              |
| :---: | :----: | :----------------------- |
| width | number | The new width fog stroke |

Returns the current builder.

------------------------------------------------------------------------

### `gridScale`

``` prism-code
gridScale(scale);
```

Set the scenes grid [`scale`](../apis/grid.md).

**Parameters**

| NAME  |  TYPE  | DESCRIPTION                   |
| :---: | :----: | :---------------------------- |
| scale | string | The new raw scale of the grid |

Returns the current builder.

------------------------------------------------------------------------

### `gridColor`

``` prism-code
gridColor(color);
```

Set the scenes grid [`color`](../apis/grid.md).

**Parameters**

| NAME  |                  TYPE                  | DESCRIPTION               |
| :---: | :------------------------------------: | :------------------------ |
| color | [GridColor](../apis/grid.md#gridcolor) | The new color of the grid |

Returns the current builder.

------------------------------------------------------------------------

### `gridOpacity`

``` prism-code
gridOpacity(opacity);
```

Set the scenes grid [`opacity`](../apis/grid.md).

**Parameters**

|  NAME   |  TYPE  | DESCRIPTION                                 |
| :-----: | :----: | :------------------------------------------ |
| opacity | number | The new opacity of the grid between 0 and 1 |

Returns the current builder.

------------------------------------------------------------------------

### `gridLineType`

``` prism-code
gridLineType(lineType);
```

Set the scenes grid [`lineType`](../apis/grid.md).

**Parameters**

|   NAME   |                     TYPE                     | DESCRIPTION                   |
| :------: | :------------------------------------------: | :---------------------------- |
| lineType | [GridLineType](../apis/grid.md#gridlinetype) | The new type of the grid line |

Returns the current builder.

------------------------------------------------------------------------

### `gridMeasurement`

``` prism-code
gridMeasurement(measurement);
```

Set the scenes grid [`measurement`](../apis/grid.md).

**Parameters**

|    NAME     |                        TYPE                        | DESCRIPTION                          |
| :---------: | :------------------------------------------------: | :----------------------------------- |
| measurement | [GridMeasurement](../apis/grid.md#gridmeasurement) | The new measurement type of the grid |

Returns the current builder.

------------------------------------------------------------------------

### `gridType`

``` prism-code
gridType(type);
```

Set the scene grids [`type`](../apis/grid.md).

**Parameters**

| NAME  |                 TYPE                 | DESCRIPTION              |
| :---: | :----------------------------------: | :----------------------- |
| type  | [GridType](../apis/grid.md#gridtype) | The new type of the grid |

Returns the current builder.

------------------------------------------------------------------------

### `items`

``` prism-code
items(items);
```

Set the scenes default [items](item.md).

**Parameters**

| NAME  |        TYPE         | DESCRIPTION                          |
| :---: | :-----------------: | :----------------------------------- |
| Items | [Item](item.md)\[\] | The default items used for the scene |

Returns the current builder.

------------------------------------------------------------------------

### `baseMap`

``` prism-code
baseMap(baseMap);
```

Set the scenes base map that should be included with this scene during upload.

**Parameters**

|  NAME   |                     TYPE                     | DESCRIPTION                  |
| :-----: | :------------------------------------------: | :--------------------------- |
| baseMap | [ImageUpload](../apis/assets.md#imageupload) | The image to upload as a map |

Returns the current builder.

------------------------------------------------------------------------

### `build`

``` prism-code
build();
```

Returns the final [SceneUpload](../apis/assets.md#sceneupload).

------------------------------------------------------------------------

```

## docs\markdown\reference\shape.md

```markdown
# Shape

A circle, rectangle, triangle or hexagon

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME    |                        TYPE                        | DESCRIPTION             |
| :-------: | :------------------------------------------------: | :---------------------- |
|   type    |                      "SHAPE"                       | The type of item        |
|   width   |                       number                       | The width of the shape  |
|  height   |                       number                       | The height of the shape |
| shapeType | "RECTANGLE" \| "CIRCLE" \| "TRIANGLE" \| "HEXAGON" | The type of shape       |
|   style   |             [ShapeStyle](#shapestyle)              | The style of the shape  |

## Type Definitions

### ShapeStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|     NAME      |    TYPE    | DESCRIPTION                                     |
| :-----------: | :--------: | :---------------------------------------------- |
|   fillColor   |   string   | The fill color of the shape                     |
|  fillOpacity  |   number   | The fill opacity of the shape between 0 and 1   |
|  strokeColor  |   string   | The stroke color of the shape                   |
| strokeOpacity |   number   | The stroke opacity of the shape between 0 and 1 |
|  strokeWidth  |   number   | The stroke width of the shape in pixels         |
|  strokeDash   | number\[\] | The pattern of the stroke dash                  |

```

## docs\markdown\reference\text-content.md

```markdown
# TextContent

Describes all information needed to display text.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME    |          TYPE           | DESCRIPTION                                                                                                      |
| :-------: | :---------------------: | :--------------------------------------------------------------------------------------------------------------- |
| richText  |  [RichText](#richtext)  | The text formatted as a set of nodes. Used when the "RICH" type is set                                           |
| plainText |         string          | The text without any formatting. Used when the "PLAIN" type is set.                                              |
|   type    |    "PLAIN" \| "RICH"    | Does this text support rich text formatting like headings. If "PLAIN" a faster text rendering path will be used. |
|   style   | [TextStyle](#textstyle) | The style of the text                                                                                            |
|   width   |  [TextSize](#textsize)  | The width of this text content                                                                                   |
|  height   |  [TextSize](#textsize)  | The height of this text content                                                                                  |

## Type Definitions

### RichText

An array of text [descendents](#descendent).

**Examples**

A single paragraph with the text `Owlbear Rodeo`

``` prism-code
[
  {
    "type": "paragraph",
    "children": [{ "text": "Owlbear Rodeo" }]
  }
]
```

A heading, subhead and paragraph.

``` prism-code
[
  {
    "type": "heading-one",
    "children": [
      {
        "text": "Heading"
      }
    ]
  },
  {
    "type": "heading-two",
    "children": [
      {
        "text": "Subhead"
      }
    ]
  },
  {
    "type": "paragraph",
    "children": [
      {
        "text": "Paragraph"
      }
    ]
  }
]
```

A paragraph with regular, bold and italics.

``` prism-code
{
  "type": "paragraph",
  "children": [
    {
      "text": "Regular "
    },
    {
      "text": "Bold",
      "bold": true
    },
    {
      "text": " "
    },
    {
      "text": "Italics",
      "italic": true
    }
  ]
}
```

A bulleted list with a bold item.

``` prism-code
[
  {
    "type": "bulleted-list",
    "children": [
      {
        "type": "list-item",
        "children": [
          {
            "text": "List 1"
          }
        ]
      },
      {
        "type": "list-item",
        "children": [
          {
            "text": "List 2",
            "bold": true
          }
        ]
      },
      {
        "type": "list-item",
        "children": [
          {
            "text": "List 3"
          }
        ]
      }
    ]
  }
]
```

|             TYPE              |
| :---------------------------: |
| [Descendent](#descendent)\[\] |

### Descendent

An array of [elements](#element) or [text](#text) blocks.

|         TYPE          |
| :-------------------: |
| (Element \| Text)\[\] |

### Element

|                                                                                                                               TYPE                                                                                                                               |
| :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: |
| [BulletedListElement](#bulletedlistelement) \| [NumberedListElement](#numberedlistelement) \| [HeadingOneElement](#headingoneelement) \| [HeadingTwoElement](#headingtwoelement) \| [ListItemElement](#listitemelement) \| [ParagraphElement](#paragraphelement) |

### Text

|  TYPE  |
| :----: |
| object |

**Properties**

|  NAME  |  TYPE   | DESCRIPTION                                         |
| :----: | :-----: | :-------------------------------------------------- |
|  text  | string  | The text to display                                 |
| italic | boolean | An optional boolean to enable italics for this text |
|  bold  | boolean | An optional boolean to enable bold for this text    |

### TextStyle

|  TYPE  |
| :----: |
| object |

**Properties**

|       NAME        |             TYPE              | DESCRIPTION                                           |
| :---------------: | :---------------------------: | :---------------------------------------------------- |
|     fillColor     |            string             | The fill color of the text                            |
|    fillOpacity    |            number             | The fill opacity of the text between 0 and 1          |
|    strokeColor    |            string             | The stroke color of the text                          |
|   strokeOpacity   |            number             | The stroke opacity of the text between 0 and 1        |
|    strokeWidth    |            number             | The stroke width of the text in pixels                |
|     textAlign     | "LEFT" \| "CENTER" \| "RIGHT" | The horizontal alignment of the text                  |
| textAlignVertical | "BOTTOM" \| "MIDDLE" \| "TOP" | The vertical alignment of the text                    |
|    fontFamily     |            string             | The font for the text                                 |
|     fontSize      |            number             | The size of the text in pixels                        |
|    fontWeight     |            number             | The weight of the text                                |
|    lineHeight     |            number             | The line height of the text relative to the font size |
|      padding      |            number             | The padding for the text in pixels                    |

### TextSize

The size of a text block either in pixels or the string `"AUTO"` for automatic sizing based on the content.

|       TYPE       |
| :--------------: |
| number \| "AUTO" |

## Text Elements

### BulletedListElement

Equivalent to the `<ul>` HTML element.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
|   type   |        "bulleted-list"        | The type of this element      |
| children | [Descendent](#descendent)\[\] | The children for this element |

### NumberedListElement

Equivalent to the `<ol>` HTML element.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
|   type   |        "numbered-list"        | The type of this element      |
| children | [Descendent](#descendent)\[\] | The children for this element |

### HeadingOneElement

Equivalent to the `<h1>` HTML element.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
|   type   |         "heading-one"         | The type of this element      |
| children | [Descendent](#descendent)\[\] | The children for this element |

### HeadingTwoElement

Equivalent to the `<h2>` HTML element.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
|   type   |         "heading-two"         | The type of this element      |
| children | [Descendent](#descendent)\[\] | The children for this element |

### ListItemElement

Equivalent to the `<li>` HTML element.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
|   type   |          "list-item"          | The type of this element      |
| children | [Descendent](#descendent)\[\] | The children for this element |

### ParagraphElement

Equivalent to the `<p>` HTML element.

|  TYPE  |
| :----: |
| object |

**Properties**

|   NAME   |             TYPE              | DESCRIPTION                   |
| :------: | :---------------------------: | :---------------------------- |
|   type   |          "paragraph"          | The type of this element      |
| children | [Descendent](#descendent)\[\] | The children for this element |

```

## docs\markdown\reference\text.md

```markdown
# Text

A text item without any background

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |              TYPE              | DESCRIPTION        |
| :---: | :----------------------------: | :----------------- |
| type  |             "TEXT"             | The type of item   |
| text  | [TextContent](text-content.md) | The text displayed |

```

## docs\markdown\reference\vector2.md

```markdown
# Vector2

A point with an x and y coordinate

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |  TYPE  | DESCRIPTION                   |
| :---: | :----: | :---------------------------- |
|   x   | number | The x coordinate of the point |
|   y   | number | The y coordinate of the point |

```

## docs\markdown\reference\vector3.md

```markdown
# Vector3

A point with an x, y and z coordinate

|  TYPE  |
| :----: |
| object |

**Properties**

| NAME  |  TYPE  | DESCRIPTION                   |
| :---: | :----: | :---------------------------- |
|   x   | number | The x coordinate of the point |
|   y   | number | The y coordinate of the point |
|   z   | number | The z coordinate of the point |

```

## docs\markdown\reference\wall.md

```markdown
# Wall

An invisible wall that interacts with the Dynamic Fog system.

The `zIndex` parameter for this item is treated specially see [Dynamic Fog](dynamic-fog.md#elevation) for a break down on how this works.

*Local Only:* this Item can only be added to the local scene using the `OBR.scene.local` API.

Extends [Item](item.md)

|  TYPE  |
| :----: |
| object |

**Properties**

|    NAME     |           TYPE            | DESCRIPTION                                                                                                                                            |
| :---------: | :-----------------------: | :----------------------------------------------------------------------------------------------------------------------------------------------------- |
|    type     |          "WALL"           | The type of item                                                                                                                                       |
|   points    | [Vector2](vector2.md)\[\] | The list of points to for the wall                                                                                                                     |
| doubleSided |          boolean          | Whether this wall will produce shadows from both sides. If false the shadowed side of the wall will be determined by the winding of the `points` array |
|  blocking   |          boolean          | Whether this wall will stop lights (or anything a light is attached to) from moving through it                                                         |

```

