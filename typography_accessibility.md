## What are some best practices for choosing font colors in terms of contrast ratio and accessibility Web Content Accessibility Guidelines (WCAG)?

The contrast ratio tells how bright a color is in respect to another. It's measured in a scale being 1:1 for colors that have the same brightness and 21:1 for the biggest contrast between black and white.

Make sure that there is compliance of contrast ratio aka enough color contrast between the background and the text. Color contrast needs to be stronger for smaller or standard size typography and weaker for bigger font sizes or for bold characters.

#### 1. Small/standard text:

        Minimum compliance is achieved at 4.5:1

        Maximum compliance is achieved at 7:1

#### 2. Large/bold text:

        Minimum compliance is achieved at 3.1

        Maximum compliance is achieved at 4.5:1

There are websites that can help you in matching colors that are compliant.

The developer should create css variables to save their color palette

```
:root {
  --text-primary: #1a1a1a;
  --text-secondary: #555555;
  --bg-color: #ffffff;
}
```

They can add them then in the css rule like this:

```
body {
  background-color: var(--bg-color);
  color: var(--text-primary);
  font-family: 'Open Sans', sans-serif;
}
// Use var() method
```

Repeat this process if the web application has the night and day mode which could also help more users have better accessibility by choosing their preferred mode. Each mode should have its color palette

The developer shouldn't only rely on contrast ratio for readability, in case of color blindness.
They can use also error messages.
