# Snippets

- [Seamless Chat Bar](https://nspc911.github.io/vc-themes/snippets/SeamlessChatBar.theme.css)

  Moves `Someone is typing`, `Cooldown is active`, `Ypu are viewing older messages` and `Replying to someone` such that they are seamless with the message bar<br>[<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1322496323202715689)<br>`Variables`
  ```css
:root {
    /* Use if your theme overwrites the color like Nocturnal
    --channeltextarea-background: var(--backgroundColor01);*/
    /* set to 0px if no applauncher */
    --scb-applauncher-padding: -52px; /* default = -52px */
    /* border radius of bar */
    --scb-border-radius: 8px; /* default = 8px */
}
```
- [HSL x Better Folders](https://nspc911.github.io/vc-themes/snippets/HSL-BF.theme.css)

  Fixes Horizontal Server List breaking the extra sidebar of Better Folders<br>[<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1326506110345023538)<br>`Variables`
  ```css
:root {
    --bfhsl-make-folder-hover: 1 /* set to 1 if you want the sidebar to 'hover' */
}
```
- Pin a server

  Allows you to pin any server of your choice to replace the pinned Discovery icon. **The server must not be in a folder**<br>[<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1327967783778254868)<br>`Variables`<br>No variables, but you need to change `<server name>` to your server's name

- [Client Theme for Visual Refresh](https://nspc911.github.io/vc-themes/snippets/VisualRefreshClientTheme.theme.css)

  Adds the compatibility for Client Theme to work on Visual Refresh (may change if Discord fixes the variables)<br>[<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1331976527545368646)

- No Favourite Channel Icon

  Removes the channel icons from channels while using Favorites v2 <br>[<kbd>Jump to message</kbd>](https://discord.com/channels/1015060230222131221/1028106818368589824/1337032719602946079)

<sub>
Footnotes:
1. If a snippet doesn't have a url, refer to the message.
<sub>
