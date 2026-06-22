# 3. **CSS Basics – Styling the Web**

- Introduction to CSS (Cascading Style Sheets) and its purpose
- Understanding the CSS box model: `margin`, `border`, `padding`, `content`
- Styling text, colors, and fonts with `color`, `font-family`, `font-size`, `line-height`
- Understanding the concept of specificity and how CSS selectors work
- Applying styles to HTML elements using selectors, classes, and IDs
- **Key Concepts:** Box model, Selectors, Specificity, Inline vs external CSS

# 4. **CSS Layouts – Building Responsive Pages**

- Introduction to layout techniques in CSS: `display`, `position`, `float`, `flexbox`, `grid`
- Building layouts with Flexbox: Aligning items, creating rows and columns
- Introduction to CSS Grid: Creating complex grid-based layouts
- Media queries: Making websites responsive to different screen sizes
- **Key Concepts:** Flexbox, Grid layout, Responsive design, Mobile-first approach

# 5. **Advanced CSS Styling**

- Using pseudo-classes and pseudo-elements: `:hover`, `:focus`, `:nth-child`
- Animations and transitions: Making elements move or change on user interaction
- Styling links, buttons, and forms for better UX
- **Key Concepts:** Pseudo-classes, Pseudo-elements, Animations, Transitions

# 6. **CSS Frameworks – Speeding Up Development**

- Introduction to popular CSS frameworks: Bootstrap, TailwindCSS
- How to use a CSS framework to quickly style pages
- Customizing and overriding default styles in a framework
- **Key Concepts:** Grid systems, Utility-first design, Responsive frameworks

___

# 3. CSS Basics – Styling the Web

## What is CSS?

**CSS (Cascading Style Sheets)** is used to control the appearance and presentation of HTML elements.

Think of a website like a house:

| Part | Technology |
|--------|------------|
| Structure of House | HTML |
| Paint, Furniture, Decoration | CSS |
| Electrical Systems & Automation | JavaScript |

HTML creates the structure, while CSS makes it beautiful.

---

## Why CSS is Important

Without CSS:

```html
<h1>My Website</h1>
<p>Welcome to my website.</p>
```

The webpage looks plain and unstyled.

With CSS:

```css
h1 {
    color: blue;
    font-size: 40px;
}
```

The page becomes visually appealing.

---

# Ways to Add CSS

There are 3 ways to apply CSS.

---

## 1. Inline CSS

Applied directly inside HTML elements.

```html
<h1 style="color:red;">Hello World</h1>
```

### Pros

- Quick testing

### Cons

- Difficult to maintain
- Not reusable

---

## 2. Internal CSS

Written inside `<style>` tag.

```html
<head>
    <style>
        h1 {
            color: blue;
        }
    </style>
</head>
```

---

## 3. External CSS (Recommended)

HTML:

```html
<link rel="stylesheet" href="styles.css">
```

CSS:

```css
h1 {
    color: green;
}
```

### Advantages

- Reusable
- Easy maintenance
- Industry standard

---

# CSS Syntax

```css
selector {
    property: value;
}
```

Example:

```css
h1 {
    color: blue;
}
```

Components:

| Part | Meaning |
|--------|---------|
| h1 | Selector |
| color | Property |
| blue | Value |

---

# Understanding the CSS Box Model

Every HTML element is treated as a rectangular box.

Think of receiving a gift package.

```text
+-------------------------+
|        Margin           |
|  +-------------------+  |
|  |      Border       |  |
|  | +-------------+   |  |
|  | |  Padding    |   |  |
|  | | +---------+ |   |  |
|  | | | Content | |   |  |
|  | | +---------+ |   |  |
|  | +-------------+   |  |
|  +-------------------+  |
+-------------------------+
```

---

## Content

Actual content of the element.

```html
<p>Hello World</p>
```

The text is the content.

---

## Padding

Space inside the element around content.

```css
padding: 20px;
```

Example:

```css
.card {
    padding: 20px;
}
```

---

## Border

Line surrounding the element.

```css
border: 2px solid black;
```

---

## Margin

Space outside the element.

```css
margin: 20px;
```

Creates distance between elements.

---

## Complete Example

```css
.card {
    width: 300px;
    padding: 20px;
    border: 2px solid black;
    margin: 30px;
}
```

---

# Styling Text

---

## Text Color

```css
color: blue;
```

Example:

```css
h1 {
    color: red;
}
```

---

## Font Family

Changes text style.

```css
font-family: Arial;
```

Example:

```css
body {
    font-family: Arial, sans-serif;
}
```

---

## Font Size

```css
font-size: 20px;
```

Example:

```css
p {
    font-size: 18px;
}
```

---

## Line Height

Controls spacing between lines.

```css
line-height: 1.6;
```

Example:

```css
p {
    line-height: 1.8;
}
```

Improves readability.

---

# CSS Selectors

Selectors determine which elements receive styles.

---

## Element Selector

```css
h1 {
    color: blue;
}
```

Targets all h1 elements.

---

## Class Selector

HTML:

```html
<p class="highlight">
    Important text
</p>
```

CSS:

```css
.highlight {
    color: red;
}
```

Can be reused many times.

---

## ID Selector

HTML:

```html
<h1 id="main-title">
    Welcome
</h1>
```

CSS:

```css
#main-title {
    color: green;
}
```

Used for unique elements.

---

# Specificity

Specificity determines which style wins when multiple styles apply.

Example:

```css
p {
    color: blue;
}

.highlight {
    color: red;
}
```

HTML:

```html
<p class="highlight">
    Hello
</p>
```

Output:

```text
Red
```

Because class selector is more specific.

---

## Specificity Hierarchy

```text
Inline CSS     → Highest
ID Selector    → High
Class Selector → Medium
Element        → Low
```

Example:

```css
p {
    color: blue;
}

.highlight {
    color: red;
}

#message {
    color: green;
}
```

Result:

```text
Green wins
```

---

# Example Website Styling

HTML:

```html
<h1 class="title">Tech Learning Hub</h1>
<p>Learn HTML, CSS, and JavaScript.</p>
```

CSS:

```css
.title {
    color: navy;
    font-size: 40px;
}

p {
    font-size: 18px;
    line-height: 1.6;
}
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| CSS | Styles HTML |
| Box Model | Content, Padding, Border, Margin |
| Selector | Chooses elements |
| Class | Reusable styling |
| ID | Unique styling |
| Specificity | Decides winning style |
| External CSS | Best practice |

---

# Practice Exercise 1

Create a webpage containing:

- Header
- Paragraph
- Button

Apply:

```css
color
font-size
font-family
padding
margin
border
```

---

# Mini Project

## Personal Profile Card

Create:

- Profile Picture
- Name
- Description
- Contact Button

Style using:

```css
padding
margin
border
font-size
color
```

---

---

# 4. CSS Layouts – Building Responsive Pages

## Why Layouts Matter

Imagine a newspaper.

Content is arranged into:

- Rows
- Columns
- Sections

CSS Layouts help organize webpage content similarly.

---

# Display Property

Controls how elements appear.

---

## Block Elements

Take full width.

```css
display: block;
```

Examples:

```html
div
p
h1
section
```

---

## Inline Elements

Only take required width.

```css
display: inline;
```

Examples:

```html
span
a
strong
```

---

## Inline-Block

Combines both behaviors.

```css
display: inline-block;
```

---

# Position Property

Controls element placement.

---

## Relative

Moves relative to original position.

```css
position: relative;
top: 20px;
```

---

## Absolute

Positions relative to nearest parent.

```css
position: absolute;
left: 50px;
```

---

## Fixed

Stays on screen during scrolling.

```css
position: fixed;
```

Example:

- Chat button
- Sticky support icon

---

# Float (Legacy Layout)

```css
float: left;
```

Used before Flexbox.

Today rarely used for layouts.

---

# Flexbox

Most commonly used layout system.

---

## Why Flexbox?

Makes alignment simple.

Example:

```html
[Logo]       [Menu]
```

---

## Enable Flexbox

```css
.container {
    display: flex;
}
```

---

## Row Layout

```css
display: flex;
flex-direction: row;
```

```text
Item1 Item2 Item3
```

---

## Column Layout

```css
display: flex;
flex-direction: column;
```

```text
Item1
Item2
Item3
```

---

## Horizontal Alignment

```css
justify-content: center;
```

Options:

```text
flex-start
center
flex-end
space-between
space-around
```

---

## Vertical Alignment

```css
align-items: center;
```

---

## Flexbox Example

```css
.container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

Used in:

- Navigation bars
- Dashboards
- Cards

---

# CSS Grid

Grid is designed for two-dimensional layouts.

Think of Excel.

```text
+----+----+
| A  | B  |
+----+----+
| C  | D  |
+----+----+
```

---

## Enable Grid

```css
.container {
    display: grid;
}
```

---

## Define Columns

```css
grid-template-columns: 1fr 1fr 1fr;
```

Creates:

```text
3 Columns
```

---

## Grid Example

```css
.container {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}
```

---

# Media Queries

Used for responsive design.

---

## Problem

Desktop:

```text
[Card][Card][Card]
```

Mobile:

```text
[Card]
[Card]
[Card]
```

---

## Media Query Example

```css
@media (max-width: 768px) {

    .container {
        grid-template-columns: 1fr;
    }

}
```

When screen width becomes smaller:

```text
3 columns → 1 column
```

---

# Mobile-First Approach

Design mobile first.

Example:

```css
.card {
    width: 100%;
}
```

Then enhance for larger screens.

```css
@media (min-width: 768px) {
    .card {
        width: 50%;
    }
}
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Display | Controls rendering |
| Position | Places elements |
| Float | Old layout method |
| Flexbox | One-dimensional layouts |
| Grid | Two-dimensional layouts |
| Media Query | Responsive design |
| Mobile First | Design for mobile first |

---

# Practice Exercise 2

Create:

- Navigation Bar
- Three Cards

Using:

```css
display:flex
justify-content
align-items
```

---

# Mini Project

## Responsive Product Dashboard

Features:

- Header
- Sidebar
- Content Area
- Product Cards

Requirements:

- Flexbox Navigation
- Grid Product Section
- Mobile Responsive Layout

---

---

# 5. Advanced CSS Styling

## Pseudo-Classes

Pseudo-classes apply styles based on state.

---

## :hover

Applies style when mouse hovers.

```css
button:hover {
    background: blue;
}
```

---

## :focus

Applies style when input is selected.

```css
input:focus {
    border: 2px solid blue;
}
```

---

## :nth-child()

Targets specific child elements.

```css
li:nth-child(2) {
    color: red;
}
```

Targets second item.

---

# Pseudo-Elements

Style specific parts of an element.

---

## ::before

Adds content before element.

```css
h1::before {
    content: "🔥 ";
}
```

---

## ::after

Adds content after element.

```css
h1::after {
    content: " 🚀";
}
```

---

# Transitions

Creates smooth changes.

Without transition:

```text
Instant change
```

With transition:

```text
Smooth change
```

---

## Example

```css
button {
    transition: 0.3s;
}

button:hover {
    background: blue;
}
```

---

# Animations

Allow continuous movement.

---

## Example

```css
@keyframes pulse {

    from {
        transform: scale(1);
    }

    to {
        transform: scale(1.1);
    }

}
```

Apply:

```css
.card {
    animation: pulse 2s infinite;
}
```

---

# Better UX Styling

## Links

```css
a {
    text-decoration: none;
}
```

---

## Buttons

```css
button {
    padding: 12px 20px;
    border-radius: 8px;
}
```

---

## Forms

```css
input {
    padding: 10px;
}
```

Improves usability.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| :hover | Mouse over |
| :focus | Active input |
| :nth-child | Target child |
| ::before | Content before |
| ::after | Content after |
| Transition | Smooth change |
| Animation | Continuous effect |

---

# Practice Exercise 3

Create:

- Animated Button
- Hover Effect
- Styled Form

---

# Mini Project

## Animated Landing Page

Features:

- Hero Section
- CTA Button
- Hover Effects
- Fade-in Animations

---

---

# 6. CSS Frameworks – Speeding Up Development

## What is a CSS Framework?

A CSS Framework provides prebuilt styles and components.

Instead of writing:

```css
button {
    padding: 10px;
}
```

You use predefined classes.

Benefits:

- Faster development
- Consistent design
- Responsive layouts

---

# Bootstrap

One of the most popular CSS frameworks.

Website:

```text
https://getbootstrap.com
```

---

## Example

```html
<button class="btn btn-primary">
    Submit
</button>
```

Bootstrap automatically styles it.

---

# Bootstrap Grid System

Uses 12 columns.

```text
|1|2|3|4|5|6|7|8|9|10|11|12|
```

Example:

```html
<div class="row">

    <div class="col-6">
        Left
    </div>

    <div class="col-6">
        Right
    </div>

</div>
```

---

# Tailwind CSS

A utility-first CSS framework.

Instead of writing custom CSS:

```css
padding: 20px;
color: blue;
```

Use utility classes.

Example:

```html
<button class="px-4 py-2 bg-blue-500 text-white">
    Submit
</button>
```

---

# Bootstrap vs Tailwind

| Feature | Bootstrap | Tailwind |
|-----------|------------|-----------|
| Learning Curve | Easy | Medium |
| Customization | Moderate | High |
| Ready Components | Yes | No |
| Flexibility | Medium | High |

---

# Customizing Framework Styles

Bootstrap:

```css
.btn-primary {
    background-color: green;
}
```

Overrides default styles.

---

# Responsive Framework Features

Both Bootstrap and Tailwind provide:

- Mobile responsiveness
- Grid systems
- Utility classes
- Layout helpers

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Framework | Prebuilt CSS tools |
| Bootstrap | Component-based framework |
| Tailwind | Utility-first framework |
| Grid System | Responsive columns |
| Utility Classes | Small reusable classes |

---

# Practice Exercise 4

Build a page using Bootstrap containing:

- Navbar
- Hero Section
- Three Cards
- Footer

---

# Mini Project

## Responsive Portfolio Website

Using Bootstrap or Tailwind:

### Features

- Navigation Bar
- About Section
- Skills Section
- Projects Grid
- Contact Form
- Mobile Responsive Layout

---

# CSS Learning Roadmap

```text
HTML Structure
      ↓
CSS Basics
      ↓
Box Model
      ↓
Selectors & Specificity
      ↓
Flexbox
      ↓
Grid
      ↓
Responsive Design
      ↓
Animations
      ↓
Bootstrap
      ↓
Tailwind CSS
      ↓
Modern Frontend Development
```

---

# Challenge Project

Build a complete "Learning Management System (LMS) Landing Page" using all concepts learned.

Requirements:

### HTML

- Semantic Layout
- Forms
- Navigation

### CSS

- Box Model
- Flexbox
- Grid
- Responsive Design
- Hover Effects
- Animations

### Framework

- Bootstrap or Tailwind

This single project will give hands-on experience with nearly every CSS concept covered in Sections 3–6.
