# Palette

Are you tired of searching for a reasonable color palette? Or looking for any other theme that isn't Catppucin?

Use this amazing CSS tip to make your own palettes!

Referenced from [mdn web](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_colors/Relative_colors)

Say you have a primary color, like `#88c0d0`, the Nord Palette's accent color

```css
--primary: #88c0d0;
```

you only have **two** options to make variants of the primary color.

1. Seperate by HSL

```css
--primary-h: 193;
--primary-s: 43%;
--primary-l: 67%;
```

Then use `calc()` to change the lightness

Cons: It looks very messy when you want to modify it

```css
--background: hsl(
  var(--primary-h),
  var(--primary-s),
  calc(var(--primary-l) / 2)
);
```

2. Use color-mix.

```css
--primary: #88c0d0;
--background: color-mix(in oklch, var(--primary), transparent);
```

Cons: Resultant color isn't accurate

## Introducing, **Relative Colors**!

Syntax:

```css
--background: color(
  from <color> <colorspace> channel1 channel2 channel3 / opacity
);
```

- `<color>` refers to any color variable made with `rgb()`, `hsl()`, etc
- `<colorspace>` refers to any color space like `oklch` or `oklab`
- `channelN` refers to the color type's channels, like `r`, `g`, and `b` in `rgb`
- `opacity` is the transparency of the color

### So why Relative Colors?

Relative colors can be modified with `calc()`, so if you want to dim the color by 50%, you can do this

```css
--background: color(
  from var(--primary) oklch calc(r / 2) calc(g / 2) calc(b / 2)
);
```

Hmm, why is it so cluttered?

What if we use HSL?

```css
--primary: #88c0d0;
--background: hsl(from var(--primary) oklch h s calc(l / 2));
```

Wait a minute, you can convert an RGB value to HSL? This changes everything!!

You can make inverse colors

```css
--accent: hsl(from var(--primary) oklch calc(h + 360) s l);
```

unsaturated colors

```css
--no-sat: hsl(from var(--primary) oklch h 0 l);
```

or tweak it until you like it, the possibilities of colors are endless!
