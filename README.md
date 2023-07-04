# Frontend Mentor - Stats preview card component solution

This is a solution to the [Stats preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [Reference](#reference)
  - [Font](#font)
  - [Color](#color)
  - [Typography](#typography)
- [Run Locally](#run-locally)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size

### Screenshot

![Stats preview card component desktop screenshot](https://devshaunb.github.io/fem-stats-preview-card-component/screenshots/desktop.png)

![Stats preview card component tablet screenshot](https://devshaunb.github.io/fem-stats-preview-card-component/screenshots/tablet.png)

![Stats preview card component mobile screenshot](https://devshaunb.github.io/fem-stats-preview-card-component/screenshots/mobile.png)

### Links

- Live Site URL: [https://devshaunb.github.io/fem-stats-preview-card-component/](https://devshaunb.github.io/fem-stats-preview-card-component/)

## Reference

### Font

- Family: [Inter](https://fonts.google.com/specimen/Inter)
- Weights: 400, 700
  <br>
- Family: [Lexend Deca](https://fonts.google.com/specimen/Lexend+Deca)
- Weights: 400

### Color

#### Primary

- ![hsl(233, 47%, 7%)](https://via.placeholder.com/10/090b1a?text=+) `Very dark blue (main background): hsl(233, 47%, 7%)`
- ![hsl(244, 38%, 16%)](https://via.placeholder.com/10/1b1938?text=+) `Dark desaturated blue (card background): hsl(244, 38%, 16%)`
- ![hsl(277, 64%, 61%)](https://via.placeholder.com/10/aa5cdb?text=+) `Soft violet (accent): hsl(277, 64%, 61%)`

#### Neutral

- ![hsl(0, 0%, 100%)](https://via.placeholder.com/10/ffffff?text=+) `White (main heading, stats): hsl(0, 0%, 100%)`

### Typography

#### Body Copy

- Font size (paragraph): 15px

## Run Locally

Clone the project

```bash
  git clone https://github.com/DevShaunB/fem-stats-preview-card-component.git
```

Go to the project directory

```bash
  cd fem-stats-preview-card-component/
```

Run `index.html`

```bash
  <browsername> index.html
```

E.g.

```bash
  firefox index.html
```

```bash
  google-chrome index.html
```

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- creating semantic list in HTML
- hiding elements from screen readers
- using grid to create equal columns

```css
.stats-preview-card {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}
```

- changing order of elements in a grid

```css
.stats-preview-card {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-auto-flow: dense;
}

.stats-preview-card__img-wrapper {
  grid-column: 2 / span 1;
}
```

- creating image overlay

```css
.stats-preview-card__img-wrapper {
  position: relative;
}

.stats-preview-card__img-wrapper::before {
  content: '';
  position: absolute;
  inset: 0;
  background-color: hsl(var(--clr-violet-400) / 0.6);
}
```

- working with images to take full (flex) parent height and width

```css
.stats-preview-card__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}
```

## Author

- Frontend Mentor - [@DevShaunB](https://www.frontendmentor.io/profile/DevShaunB)
- Twitter - [@DevShaunB](https://www.twitter.com/DevShaunB)

## Acknowledgments

- [Stats preview card component](https://www.frontendmentor.io/challenges/stats-preview-card-component-8JqbgoU62) by [Frontend Mentor](https://www.frontendmentor.io/)
