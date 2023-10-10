## 1. Structure a site using semantic HTML to aid accessibility
  Accessibility was one of the main requirements. We found out that it is not always possible to keep a perfect accessibility and also the design/technology decisions, so there is always a balance to mantain.
  Perfectly accessible sites may not have all the functionality or the looks that wew stated on the design phase.

### index.html:

* `<header>` : I used this for the header section of my website.
* `<nav>`: I wrapped the navigation menu with this element.
* `<ul>` and `<li>`: These were used to create an unordered list for navigation links.
* `<main>`: I encapsulated the main content of my webpage with this.
* `<section>`: I used this multiple times to structure different content sections.
* `<h1>`, `<h2>`, and `<h3>`: I used these headings to define content hierarchy.
* `<p>`: I used this for paragraphs of text.
* `<img>`: I used this to embed images with alt attributes for accessibility.
* `<form>`: I used this to create a contact form.
* `<label>`: I associated it with form fields for labeling.
* `<button>`: I used it for buttons within forms.
* `<footer>`: I used this for the footer section of my webpage.
  
### expert.html:

* `<main>`: I encapsulated the main content of my expert page with this element.
* `<div>` and `<article>`: I used these for structuring content about experts.
* `<label>`: I associated it with form fields for labeling.
* `<input>`, `<textarea>`, and `<button>`: These were the form elements I used for user interaction.
* `<h2>`: I used this for subheadings to organize content.
* `<button>`: I used it for navigation back to the expert list.
* `<div>`: I created a modal window for captcha with this element.
  

## 2. Ensure a web page is readable for screen readers

Utilizing proper semantic HTML elements, as mentioned earlier, is essential to ensure that our webpage is accessible to screen readers.

All the images on our site contain alt attributes with descriptions of the images. The only exception is the captcha modal window. While the captcha is fully functional and visually appealing, in a real-world scenario, we would use reCaptcha or a similar solution.

Additionally, we have incorporated ARIA attributes to enhance accessibility.

## 3. Ensure our UI has sufficient colour contrast so that everyone can perceive it comfortably

We have chosen a color palette that consists of dark fonts on light backgrounds and light fonts on dark backgrounds, as seen in our modal windows.

<img width="367" alt="modal" src="https://github.com/FAC29A/alex-portfolio/assets/94972293/cd40ef7d-e003-462c-a311-781bf231f49d">

These colors are defined as root variables, making it easy to modify the color palette by simply changing these values.
In the expert page we also used a dark colour to indicate that the "send" button from the contact form is disabled until all the fields are fulfilled.

## 4. Use various tools to check that our website meets accessibility criteria

## 5. Use CSS media queries to ensure our content is always presented effectively on screens of different sizes

## 6. Demonstrate a mobile-first approach to building a website

## 7. Use CSS variables to apply repeated colours to HTML elements

## 8. Use CSS Flexbox to style children in a single-direction layout (ie a row or a column)

## 9. Use CSS Grid to style children in two-direction layout

## 10. Ensure our Git commit history tells a coherent story

## 11. Use the appropriate input types in HTML forms for gathering different types of information
