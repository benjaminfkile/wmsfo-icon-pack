# WMSFO Icon Pack

60 two-tone SVG icons for the Where's My Santa Fly Over site and admin panel. Christmas, winter, and a handful of utility and brand icons, all drawn on the same rule so they sit together at any size.

Open `index.html` in a browser to see the whole set in light and dark, at 16, 24, 40, and 48 px, and in a sample page layout. The sheet has a name filter and a colour mode switch.

## Drawing rule

- 24 x 24 grid, 1.5 stroke, round caps and joins.
- Stroke and the soft tint fill use `currentColor`, so the icon takes whatever text or accent colour surrounds it.
- Each icon gets one or two fixed pops from five colours: red `#e0524b`, gold `#f0b32e`, green `#3fae7a`, snow `#ffffff`, cocoa `#9a5b2f`.
- Pops are written as `fill="var(--icon-red, #e0524b)"`, so they can be overridden with CSS variables when inlined and fall back to the fixed colour when loaded through `<img>`.
- Utility and brand icons (calendar, envelope, globe, phone, cloud, facebook, instagram, snowflake) are tint only.

## Files

```
icons/          one .svg per icon, named by id
icons/library.json   id, display name, and tags for every icon
index.html      the review sheet
```

## Usage

Inline the SVG when you want the icon to follow the theme:

```html
<span style="color: #0b6bb5">
  <!-- contents of icons/holly.svg -->
</span>
```

Or load it as an image when a plain colour is fine:

```html
<img src="icons/holly.svg" width="24" height="24" alt="">
```

Override a pop colour for a whole area with a CSS variable:

```css
.footer { --icon-gold: #d9a520; }
```

`library.json` lists every icon with its tags, so a picker can group by `holiday`, `winter`, `food`, `utility`, and so on.
