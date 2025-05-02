# Advanced Variables

<sub>This has been inferred from <a href="https://discord.com/channels/1015060230222131221/1134844326933954622/1355074670713372804">Vencord > #theme-development > 💬</a></sub>

According to [mdn web docs](https://developer.mozilla.org/en-US/docs/Web/CSS/@property/syntax#browser_compatibility), this part is a recent addition to Firefox, and has existed on Chromium/Electron a long time back.

Usually, when allowing a user to set a CSS variable, you are forced to use either of the following
```css
:root {
  --var-1: 0; /* set to 1 to toggle */
  --var-2: none; /* set to 'block' to toggle */
  --var-3: #000000; /* allows hex values */
}
```
for which all of them use some sort of commenting. What if you could use JSON Schema-like objects but for CSS Variables?

Introducing `@property`

`@property` acts as a variable that can have a select amount of allowed inputs, restricting the user's allowed input range and potentially preventing breakage of snippets, while acting as intuitive as possible

```css
@property --var-1 {
  syntax: 'on | off';
  inherits: false;
  initial-value: off;
}
```
In the above scenario, the variable `--var-1` can only be set to either <kbd>on</kbd> or <kbd>off</kbd>, and anything else will be rejected. Moreover, the variable cannot be inherited by child elements due to `inherits: false`, which means it is a lot more easier to handle such variables

How about other syntaxes?
```css
/* Accepts only a color */
syntax: "<color>";
/* Accepts either a number with unit or a percentage value */
syntax: "<length> | <percentage>";

/* Space-separated list of colors */
syntax: "<color>+";

/* Comma-separated list of numbers with unit */
syntax: "<length>#";

/* Accepts either 'small', 'medium' or 'large' */
syntax: "small | medium | large";

/* Accepts either a number with unit or 'auto' */
syntax: "<length> | auto";

/* Allows everything */
syntax: "*";
```
What about other accepted types?
```css
/* Accepts an angle like 90deg */
syntax: "<angle>";

/* Accepts a color like #000000 or rgb(0,0,0) or hsl(0,0,0) */
syntax: "<color>";

/* Accepts an image like linear-gradient or url to images */
syntax: "<image>";

/* Accepts an integer without a unit */
syntax: "<integer>";

/* Accepts an integer with a unit */
syntax: "<length>";

/* Accepts an integer with a unit or percentage or even calc() values with both */
syntax: "<length-percentage>";

/* Accepts integers including floating point */
syntax: "<number>";

/* Accepts a percentage */
syntax: "<percentage>";

/* Accepts a screen density like 10dpi */
syntax: "<resolution>";

/* Accepts a string */
syntax: "<string>";

/* Accepts a time */
syntax: "<time>";

/* Accepts a timing function like ease, or even bezier */
syntax: "<transform-function>";

/* <transform-function> but space-seperated */
syntax: "<transform-list>";

/* Accepts a valid url */
syntax: "<url>";
```

So with this, how does a variable with `on/off` work?

Thats where `@container` comes.

```css
@property --highlight-on-hover {
  syntax: "on | off";
  inherits: false;
  initial-value: on;
}
@container bodyContainered style(--highlight-on-hover: on) {
  *:hover {
    color: white !important
  }
}
body {
  container-name: bodyContainered
}
```

In the above example, `--highlight-on-hover` is a toggle. But how is it applied?

`@container` defines a containment context, `bodyContainered`. `@container` has a neat feature where it applies the select CSS rules only if the rules inside the bracket are valid. In this case, it checks whether `--highlight-on-hover` is set to `on`, and only then will it set those hovered on to use a white text. Afterwards, you have to set the `body` element to use the `bodyContainered` containment context, so that the rule can be applied.

That's it, this is your guide to advanced CSS variables
