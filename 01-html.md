# 1. **HTML Basics – The Web’s Skeleton**

- Introduction to HTML (HyperText Markup Language) and its role in web development
- Understanding HTML tags and elements
- Building a simple webpage using HTML: `html`, `head`, `body`, `header`, `footer`
- Working with text elements: `h1`, `p`, `a`, `ul`, `ol`, `li`
- Structuring content with semantic HTML: `section`, `article`, `nav`, `main`, `aside`
- **Key Concepts:** Elements, Tags, Nesting, Attributes, Semantic HTML

# 2. **HTML Forms and Inputs – User Interaction**

- Creating forms with `form`, `input`, `textarea`, `select`, `button`
- Understanding form submission, `GET` and `POST` methods
- Using `input` types (text, email, number, password)
- Validating form data with attributes like `required`, `min`, `max`
- **Key Concepts:** Form elements, Input validation, Method types, Accessibility in forms

___

## What is HTML?

**HTML (HyperText Markup Language)** is the standard language used to create and structure web pages.

Think of a website like a human body:

| Part | Web Equivalent |
|--------|---------------|
| Skeleton | HTML |
| Skin & Appearance | CSS |
| Behavior & Actions | JavaScript |

HTML provides the structure and meaning of content on a webpage.

### Example

```html
<h1>Welcome to My Website</h1>
<p>This is my first webpage.</p>
```

Output:

```
Welcome to My Website
This is my first webpage.
```

---

## Understanding HTML Tags and Elements

### HTML Tag

A tag tells the browser what type of content it contains.

Example:

```html
<h1>
```

Opening tag

```html
</h1>
```

Closing tag

---

### HTML Element

An element consists of:

```html
<h1>Hello World</h1>
```

- Opening Tag → `<h1>`
- Content → `Hello World`
- Closing Tag → `</h1>`

Together they form an **HTML Element**.

---

## Basic Structure of an HTML Page

Every HTML document follows a standard structure.

```html
<!DOCTYPE html>
<html>
<head>
    <title>My First Page</title>
</head>
<body>

    <header>
        <h1>My Website</h1>
    </header>

    <main>
        <p>Welcome to my website.</p>
    </main>

    <footer>
        <p>Copyright 2026</p>
    </footer>

</body>
</html>
```

---

## Understanding Main HTML Sections

### `<html>`

Root element of the webpage.

```html
<html>
    ...
</html>
```

Contains all HTML content.

---

### `<head>`

Contains information about the page.

```html
<head>
    <title>My Website</title>
</head>
```

Examples:

- Title
- CSS links
- Meta tags
- Scripts

Not visible to users.

---

### `<body>`

Contains everything visible on the webpage.

```html
<body>
    <h1>Hello</h1>
</body>
```

---

### `<header>`

Top section of a page.

```html
<header>
    <h1>My Blog</h1>
</header>
```

Usually contains:

- Logo
- Navigation
- Site title

---

### `<footer>`

Bottom section of a page.

```html
<footer>
    <p>Copyright 2026</p>
</footer>
```

Usually contains:

- Copyright
- Contact details
- Links

---

# Working with Text Elements

---

## Headings (`h1` to `h6`)

Used for titles and headings.

```html
<h1>Main Title</h1>
<h2>Section Title</h2>
<h3>Subsection Title</h3>
```

Hierarchy:

```text
h1 → Main Heading
h2 → Section
h3 → Subsection
h4 → Smaller Section
h5 → Smaller
h6 → Smallest
```

---

## Paragraph (`p`)

Used for text content.

```html
<p>This is a paragraph.</p>
```

---

## Links (`a`)

Used to navigate to another page.

```html
<a href="https://google.com">
    Visit Google
</a>
```

### Important Attribute

```html
href
```

Specifies destination URL.

---

## Unordered List (`ul`)

Creates a bullet list.

```html
<ul>
    <li>HTML</li>
    <li>CSS</li>
    <li>JavaScript</li>
</ul>
```

Output:

- HTML
- CSS
- JavaScript

---

## Ordered List (`ol`)

Creates numbered lists.

```html
<ol>
    <li>Learn HTML</li>
    <li>Learn CSS</li>
    <li>Learn JavaScript</li>
</ol>
```

Output:

1. Learn HTML
2. Learn CSS
3. Learn JavaScript

---

## List Item (`li`)

Represents a single item.

```html
<li>HTML</li>
```

Must be inside:

- `ul`
- `ol`

---

# Semantic HTML

## What is Semantic HTML?

Semantic tags describe the meaning of content.

Instead of:

```html
<div>
```

We use:

```html
<header>
<nav>
<main>
<footer>
```

This makes code:

- Easier to read
- Better for SEO
- Better for accessibility

---

## `<section>`

Represents a logical section.

```html
<section>
    <h2>About Us</h2>
    <p>Company information.</p>
</section>
```

---

## `<article>`

Represents independent content.

```html
<article>
    <h2>Blog Post</h2>
    <p>Post content...</p>
</article>
```

Examples:

- Blog posts
- News articles
- Product reviews

---

## `<nav>`

Navigation links.

```html
<nav>
    <a href="#">Home</a>
    <a href="#">About</a>
</nav>
```

---

## `<main>`

Main content area.

```html
<main>
    <h1>Welcome</h1>
</main>
```

Only one `<main>` per page.

---

## `<aside>`

Secondary content.

```html
<aside>
    <h3>Related Articles</h3>
</aside>
```

Examples:

- Sidebar
- Advertisements
- Related posts

---

# Example Complete Webpage

```html
<!DOCTYPE html>
<html>
<head>
    <title>Tech Learning Hub</title>
</head>
<body>

<header>
    <h1>Tech Learning Hub</h1>
</header>

<nav>
    <a href="#">Home</a>
    <a href="#">Courses</a>
    <a href="#">Contact</a>
</nav>

<main>

    <section>
        <h2>HTML Course</h2>

        <article>
            <h3>Introduction to HTML</h3>
            <p>Learn the basics of web development.</p>
        </article>

    </section>

    <aside>
        <h3>Recommended Courses</h3>
        <ul>
            <li>CSS</li>
            <li>JavaScript</li>
        </ul>
    </aside>

</main>

<footer>
    <p>Copyright 2026</p>
</footer>

</body>
</html>
```

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Element | Complete HTML component |
| Tag | Opening or closing instruction |
| Nesting | Elements inside elements |
| Attribute | Additional information |
| Semantic HTML | Tags that describe meaning |

---

# Real-World Analogy

Imagine building a house:

| House Part | HTML Equivalent |
|------------|----------------|
| Foundation | html |
| Rooms | section |
| Main Hall | main |
| Entrance | header |
| Navigation Sign Boards | nav |
| Side Room | aside |
| Exit Area | footer |

HTML provides the structure of the entire house.

---

# Practice Exercise 1

Create a webpage containing:

- Website title
- Header
- Navigation
- About section
- Skills section
- Footer

Use:

```html
header
nav
main
section
footer
h1
h2
p
ul
li
```

---

# Mini Project

## Personal Portfolio Page

Build a webpage containing:

### Header

- Your Name
- Profession

### Navigation

- Home
- About
- Skills
- Contact

### Main Content

- About Me
- Skills List
- Projects Section

### Footer

- Copyright Text

---

# 2. HTML Forms and Inputs – User Interaction

## What are Forms?

Forms allow users to send data to a website.

Examples:

- Login page
- Registration form
- Contact form
- Search box

Think of a form as a paper application form that users fill and submit.

---

## Form Structure

```html
<form>
    <!-- Inputs -->
</form>
```

Example:

```html
<form>
    <input type="text">
    <button>Submit</button>
</form>
```

---

# Input Elements

## Text Input

```html
<input type="text">
```

Used for:

- Name
- City
- Company

---

## Email Input

```html
<input type="email">
```

Browser validates email format.

Example:

```html
john@gmail.com
```

---

## Password Input

```html
<input type="password">
```

Displays:

```text
*******
```

instead of actual text.

---

## Number Input

```html
<input type="number">
```

Only accepts numeric values.

---

# Textarea

Used for multi-line text.

```html
<textarea></textarea>
```

Example:

```html
<textarea>
Write your feedback
</textarea>
```

Useful for:

- Feedback
- Comments
- Messages

---

# Select Dropdown

```html
<select>
    <option>HTML</option>
    <option>CSS</option>
    <option>JavaScript</option>
</select>
```

Output:

```text
▼ HTML
```

---

# Button

```html
<button>Submit</button>
```

Used to:

- Submit forms
- Trigger actions

---

# Form Submission

When users click submit:

```html
<button type="submit">
```

Data is sent to a server.

---

## GET Method

```html
<form method="GET">
```

Data appears in URL.

Example:

```text
/search?name=John
```

### Characteristics

- Visible
- Bookmarkable
- Used for searching

---

## POST Method

```html
<form method="POST">
```

Data sent in request body.

### Characteristics

- More secure
- Not visible in URL
- Used for login and registration

---

# Form Validation

HTML provides built-in validation.

---

## Required Field

```html
<input type="text" required>
```

User cannot submit empty field.

---

## Minimum Value

```html
<input type="number" min="18">
```

Must be at least 18.

---

## Maximum Value

```html
<input type="number" max="60">
```

Cannot exceed 60.

---

# Complete Form Example

```html
<form method="POST">

    <label>Name</label>
    <input type="text" required>

    <br><br>

    <label>Email</label>
    <input type="email" required>

    <br><br>

    <label>Age</label>
    <input type="number" min="18" max="60">

    <br><br>

    <label>Message</label>
    <textarea></textarea>

    <br><br>

    <label>Course</label>
    <select>
        <option>HTML</option>
        <option>CSS</option>
        <option>JavaScript</option>
    </select>

    <br><br>

    <button type="submit">
        Submit
    </button>

</form>
```

---

# Accessibility in Forms

Accessibility ensures everyone can use forms, including people using screen readers.

---

## Use Labels

Good:

```html
<label for="email">Email</label>
<input id="email" type="email">
```

Bad:

```html
<input type="email">
```

Labels help users understand what each field is for.

---

# Key Concepts Summary

| Concept | Description |
|----------|-------------|
| Form | Collects user data |
| Input | Single data field |
| Textarea | Multi-line text |
| Select | Dropdown |
| Button | Performs action |
| GET | Sends data in URL |
| POST | Sends data in request body |
| Validation | Ensures correct input |
| Accessibility | Makes forms usable for everyone |

---

# Practice Exercise 2

Build a Student Registration Form containing:

- Name
- Email
- Password
- Age
- Course Dropdown
- Comments Textarea
- Submit Button

Requirements:

```html
required
min
max
POST method
```

---

# Mini Project

## Course Enrollment Form

Create a form for a training institute.

Fields:

- Full Name
- Email
- Mobile Number
- Age
- Course Selection
- Experience Level
- Comments

Validation:

- Required fields
- Age between 18 and 60
- Valid email

Submission Method:

```html
POST
```

This project combines all concepts from:
- Forms
- Inputs
- Validation
- Accessibility
- Semantic HTML
