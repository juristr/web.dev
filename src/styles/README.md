# Styles

## Structure

The styles for this project attempt to (loosely) follow an ITCSS model.
Learn more @ https://speakerdeck.com/dafed/managing-css-projects-with-itcss

- settings: Global variables
- tools: Mixins and functions
- generic: Ground-zero styles and unclassed HTML elements (type selectors)
- components: Chunks of UI
- pages: Page-specific styles (use sparingly if at all)
- overrides: Utility classes for things like text alignment, box shadows, etc.

## Rules

- Do not use `@import` except in the `all.scss` files. This helps to avoid
  double-importing a resource and bloating the stylesheet.
- List dependencies at the top of each file. Example:
```
// Dependencies:
// tools/_functions.scss
```

- Use [hyphenated BEM style](https://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/).
- Prefix classes with `w-` which stands for 'web'. This helps us namespace our
  CSS so we don't conflict with DevSite.
- Only nest 2 levels deep.
- Add a comment, `// DevSite override`, to any CSS that's used to override a
  DevSite style. Add the comment on the same line as the style.

  ```
  color: pink; // DevSite override
  ```

## Linting

We use [Stylelint](https://github.com/sasstools/sass-lint) to match Google's
internal SCSS style guide.

- [Styelint rules quick reference](https://github.com/sasstools/sass-lint/tree/master/docs/rules).

## Tips

- To preview your SASS you can use [Sassmeister](https://www.sassmeister.com/).