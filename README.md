# Obsidian Snippets

```
.___  ________  __________  ________  ___.
|   \ \       \ \        / /       / /   |
|    \ \       \ \      / /_______/ /    |
|     \ \       \ \    / ________  /     |
|      \ \       \ \  / /       / /      |
|_______\ \_______\ \/ /_______/ /_______|
```

A collection of both personal and third-party [Obsidian](https://obsidian.md/) snippets. Please note that all third-party code belongs to the original authors. Credits and source are included at the top of each snippet. All snippsets should work with **Obsidian Publish.**

> [!note] 
> For more information about CSS Snippets and implementing them, see the [offical documentation](https://help.obsidian.md/Extending+Obsidian/CSS+snippets).

## Snippets
---
See below for a list of all snippets included, authors, use, and purpose.

### MCL Multi Column.css
Snippet is from author [efemkay](https://github.com/efemkay/obsidian-modular-css-layout) and all credit goes to them (link to [LICENSE](https://github.com/efemkay/obsidian-modular-css-layout/blob/main/LICENSE)). While the snippet has many uses, I personally like the [Multi Column Callout](https://github.com/efemkay/obsidian-modular-css-layout?tab=readme-ov-file#multi-column-callout) feature. I like to combine this with the callout outlines. Use:

```
> [!multi-column]
>
>> [!note] First Callout
>> Some text.
>
>> [!warning] Second Callout
>> More text.
```

### S - Embed Adjustments.css
Snippet is from author [SIRvb](https://github.com/SlRvb/Obsidian--ITS-Theme/tree/85e546f7c6c1abf803bcb8677aca58b4e4e5977c) and all credit goes to them (link to [LICENSE](https://github.com/SlRvb/Obsidian--ITS-Theme/blob/85e546f7c6c1abf803bcb8677aca58b4e4e5977c/LICENSE)). Basically this gives control over how an embed appears. I use it for the `clean` and `no-title` functions, which makes the embeded note appear seamless in the document. This is useful for [Obsidian Publish](https://obsidian.md/publish) sites, as the `embed-strict` from the [Obsidian Minimal Publsh](https://github.com/kepano/obsidian-minimal-publish) theme doesn't appear to be implemented as of yet. For complete documentation, see [SIRvb's documentation](https://publish.obsidian.md/slrvb-docs/ITS+Theme/Embed+Adjustments). Use:

```
![[Note|clean no-title]]
```

### banner_image.css
Original snippet is from author [Bluemoondragon07](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/Fun%20Mini%20Snippets/CSS%20banners%2C%20icons%2C%20%26%20More.md), but I use a modified version from user [CheLin](https://forum.obsidian.md/t/banner-images-icons-experimental-more-image-options-css-snippet/53738/16). [Link to LICENSE here](https://github.com/Bluemoondragon07/Obsidian-amazing-snippets/blob/main/LICENSE).

Banner images appear to be a bit touchy in **Obsidian,** and I use mine for **Publish**. This snippet worked the best for me, but there are more complex or advanced options out there that might work better for you.

Note that this snippet can cause unexpected issues depending on your file names. The use of `img[alt*="banner]` in this snippet applies to all "alt" attributes for "img" elements. However, in Obsidian the alt text by default is the file name. So if your file name is something like "banner_image.jpg," the snippet will see it as a banner image. You can modify The alt text using `|`, for example: `![[banner.jpg|not_a_banner]]`. Just something to keep in mind if you encounter unexpected results.

I also modified the snippet to remove reference of `.mod-header`. This class applies to all embeded files, not just images. When embeding both a note and a banner image in the same document, the `padding-top` would apply to the file, creating extra padding around the file. I removed this reference, and instead add padding to the top of `.markdown-preview-size`, which just adds fixed padding to the top of the reading pane.

Additionally, one feature of this snippet is the ability to stack multiple images. This can be nice feature to overlay text on another image. However, the text might be stretched or warped depending on your view (such on mobile). I fixed this by adding `alt*="contain"`, which changes the `object-fit` attribute to `contain` instead of `cover`.

Use:

```
---
cssclasses:
    - obsidian-banner
---

![[image.png|banner]]
![[stacked_image.png|banner contain]]
```

### blockquote_styling.css
I took this exact snippet from the **r-u-s-h-i-k-e-s-h/Obsidian-CSS-Snippets** repo, but the original is by user [kneecaps from discord](https://discord.com/channels/686053708261228577/702656734631821413/1042896580539330560).

You might need to change the colors, but otherwise should work without issue. Note that this will change all default quote blocks in your notes.

Use:

```
> This is the quote.
> <cite>Author</cite>
```

### blog_post_callout.css and custom_callouts.css
Created by me. Simple callout styles. Colors might need to be changed depending on your theme.

### cards-box-link.css
This snippet was written by me, but I took the idea from the official Obsidian site on the [Import notes](https://help.obsidian.md/import) page.

Basically this is a custom class that extends the [Minimal Cards](https://minimal.guide/cards) functionality. It transforms any `list-cards` into clickable links. Note that this will overwrite the styling for all cards in that note.

If you'd like to utilize multiple card styles in a single note, you will need to create a separate note with the different style and embed it in the primary note. A little messy, but it works.

Use:

```
---
cssclasses:
    - list-cards
    - cards-box-link
---
```

### center_headings.css
Simple snippet that centers the headings in the content pane.

### image_border.css
Adds a border and drop shadow around embeded images.

### outlined_callouts.css
I took this exact snippet from the **r-u-s-h-i-k-e-s-h/Obsidian-CSS-Snippets** repo, but the original is by user [sailKite from discord](https://discord.com/channels/686053708261228577/702656734631821413/1042896580539330560). Changes callouts on a page to an outline style.

Use:

```
---
cssclasses:
    - callouts-outlined
---
```

### profile_image.css
This snippet was written by me, but I took the idea from: https://yomaru.dev/home. All credit goes to the original author.

This makes an image round a fixed height, width and a border. You will likely need to change the border color to match your theme.

Use:

```
---
cssclasses:
    - profile-image
---

![[image|profile-image]]
```

### center_callout_body.css
Modify callouts to center content. By default callouts are set to "12px 12x 12px 24px," this overrides the "24px" to "12px."

Use:

```
[!info|center]
```

### noteinfo_callout.css
Custom callout I created with inspiration from [Marco Noris's](https://lab.marconoris.com/) publish site.

Basically this creates a custom callout that is centered and only designed to show simple note info, like the date or author of the note. I also took some formating from the [kneecaps blockquote styling](https://github.com/Rudesind/obsidian-snippets?tab=readme-ov-file#blockquote_stylingcss), and a little bit from [outlined callouts](https://github.com/Rudesind/obsidian-snippets?tab=readme-ov-file#outlined_calloutscss).

Note that this snippet is designed to only have text in the title. Adding any body text will have unpleasent styling.

Use:

```
[!noteinfo] Date · Author
```
