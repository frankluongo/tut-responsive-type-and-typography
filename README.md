# Responsive Type & Typography
Modern web Typography with variable fonts
[Workshop Link](https://github.com/jpamental/rwt-vf-workshop-full)
[Slides](https://slides.com/frontendmasters/responsivetypography#/)


## 01 Introduction

### 01.01 Responsive Type Overview
- Performance: Don't block the page render
- Progressive: Plan for failure
- Proportion: Small screen / subtle scale
- Polish: Design is the detail
  - Drop caps, columns, quotes

Links
- [styleguides.io](http://styleguides.io/)


### 01.02 Responsive Type Q&A
- Add as many media queries as you need

### 01.03 Typography 101
- I went to art school... I know this

### 01.04 Anatomy of Letterforms
- [Type Anatomy Reference](https://slides.com/frontendmasters/responsivetypography#/37)
  - Similarities and differences in shape and width will help with pairing


### 01.05 Type Styles, Selection & Pairing
- [Type Styles and Classification](https://slides.com/frontendmasters/responsivetypography#/39)
- [Type Pairing Example](https://slides.com/frontendmasters/responsivetypography#/43)
- [Type Availability](https://slides.com/frontendmasters/responsivetypography#/48)

### 01.06 Web Fonts Performance
- Load only what you need
- Each font has a performance cost


### 01.07 Progressive Enhancement
- Load first with CSS, then use JavaScript
  - [Font Face Observer](https://fontfaceobserver.com/)


### 01.08 Flash of Unstyled Text
- Use classes `.wf-inactive` and `.wf-active`
```css
body {
  font-family: 'Trade Gothic', Helvetica, Arial;
}

.wf-inactive body {
  font-family: Helvetica, Arial;
}
```
- Adjust `font-size`, `line-height`, and `letter-spacing` to avoid jumpiness


### 01.09 Proportion
- [Modern CSS Scale](http://typecast.com/images/uploads/modernscale.css)
- [Responsive Typography Demo](http://hwdesignco.com/webtype/typecast/rwt/#)


### 01.10 Letter Spacing Polish
- Focus on orphans, widows and hyphens as well as letter spacing


### 01.11 Web Font Tips & Tricks
**Keep Text Readable**
This gets to around 65-70 characters
```css
@media (min-width: 58em) {
  p {
    max-width: 38em;
  }
}
```
- Don't use Pixels!
  - Use EM by just dividing whatever you were going to use in pixels by 16
  - This is great for accessibility


### 01.12 Web Fonts Demo
- [IBM Plex Font](https://fonts.google.com/specimen/IBM+Plex+Sans)
- Sample added to `course_files`


### 01.13 Responsive Variable Fonts
- Variable fonts condense all styles into one font


### 01.14 Variable Fonts Browser Support
- Works on iOS, Chrome, Edge, etc.


### 01.15 Variable Font Evolution
- Contribute to the Spec to W3C on Github


### 01.16 Variable Font Resources
- [Axis Praxis](https://www.axis-praxis.org/specimens/__DEFAULT__)
- [v-fonts](https://v-fonts.com/)
- [Microsoft Variable Font](https://developer.microsoft.com/en-us/microsoft-edge/testdrive/demos/variable-fonts/)
- [Open Source Variable Font](https://www.typenetwork.com/brochure/opentype-font-variations/#introduction)
- [MonoType Variable Fonts](https://www.monotype.com/fonts/variable-fonts)
- [Variable Web Typography](https://zeichenschatz.net/demos/vf/variable-web-typo/)
- [Variable Font Demo](https://codepen.io/jpamental/pen/MGEPEL/)




## 02 Implementing
[Implementation Slides](https://slides.com/frontendmasters/responsivetypography#/177)


### 02.01 Loading Web Fonts
- Use Font Face Observer


### 02.02 Common Font Issues
- Make sure your text fits the screen

**Preserve Meaning, Not Pixel Size**
- Communicate Ideas / Influence Behavior
- Use scale as a starting point


### 02.03 Coding Web Fonts
- Use `@font-face` declarations for fonts


### 02.04 Font Loading Stages
- Make sure to have a font fallback


### 02.05 Changing Type Faces
- This is very simple


### 02.06 Typography For Reading



### 02.07 Set Root Min & Max Font Size
```css
:root {
  /* Breakpoint variables */
  --bp-small: 24.15;  /* 386.4 */
  --bp-medium: 43.75; /* 700 */
  --bp-large: 60.25;  /* 964 */
  --bp-xlarge: 75;    /* 1200 */
  /* Paragraph variables */
  --p-line-height-min: 1.15;
  --p-line-height-max: 1.5;
  --p-font-size-min: 1.0;
  --p-font-size-max: 1.25;
  --p-vf-wght: 350;
  /* H1 variables */
  --h1-line-height-min: 1;
  --h1-line-height-max: 1.25;
  --h1-font-size-min: 5;
  --h1-font-size-max: 10;
  --h1-vf-wght-multiplier-s: 2.5;
  --h1-vf-wght-multiplier-m: 2.75;
  --h1-vf-wght-multiplier-l: 3;
  --wght-multiplier: 1; }
```


### 02.08 Variable Font Demo
- [Variable Fonts Codepen](https://codepen.io/jpamental/pen/MGEPEL/)


### 02.09 CSS Variables
- You can use CSS Variables to change font styles


### 02.10 Variable Fonts Fallback
- Use `@supports` to enhance the experience
```css
@supports (font-variation-settings: normal) {
  .no-support-message {
    display: none;
    position: absolute;
    text-indent: -999em;
    visibility: hidden;
  }
}

@supports not (font-variation-settings: normal) {
  .example-ampersand {
    display: none;
    position: absolute;
    text-indent: -999em;
    visibility: hidden;
  }
}
```


### 02.11 Variable Font Q&A




## 03 Future of Web Typography

### 03.01 Variable Font Features
### 03.02 Pulling From History
### 03.03 OpenType Features
### 03.04 Text-First Design
### 03.05 Adding Font Features
### 03.06 Editorial Design
### 03.07 Editorial Design With Variable Fonts



## 04 Wrapping Up
