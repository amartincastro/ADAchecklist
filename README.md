# ADAchecklist
An ADA and accessibility checklist for web developers

## ADA Checklist:
-	Improve legibility for visually-impaired and colorblind users by ensuring all text meets contrast ratio requirements. Web Content Accessibility Guidelines (WCAG) recommend at least a 4.5 to 1 contrast ratio for normal text. 
-	All multimedia (`<img>`, `<audio>`, `<video>`) elements should have alt text describing the content for the visual- or audio-impaired to access via screen-reader or other assistive technologies.
-	Descriptive link text (“Click here to see search results”) instead of generic link text (“Click here”) because some screen readers have settings to only read the links available on a page.
-	HTML5 section elements are used for applicable content types to enable browser accessibility tools & screen readers
  - `<header>` once per page inside of <body> tag, denotes header. Different from the <head> tag with page title, meta info, etc.
  - `<nav>` once per page, denotes navigation bar. Should not be a standard “div”.
  - `<main>` once per page, denotes main body for “jump to Main” accessibility features
  - `<article>` many times per page, denotes independent, self-contained content (eg. Location Search result). Does it make sense without surrounding context?
  - `<section>` many times per page, denotes related content (eg. Each column within a data table)
  - `<footer>` once per page, denotes footer
-	Headings (`<h1>`, `<h2>`, etc) used to represent information hierarchy
-	`<figure>` used where data visualization elements necessary, and <figcaption> provides description
-	`<input>` fields have appropriate <label>s to indicate expected data type and parameters, id="" and name="" fields. Example date input:
  - `<input type="date" id="pickdate" name="date"></input>`
-	Radio button forms are surrounded by `<fieldset>`, include a `<legend>` description (not a `<p>`), and each `<input id="">` option has a corresponding `<label for=””>` that matches the `<input>`’s id. 
-	Standardized times / dates with HTML5 “datetime” attribute, e.g.:
  - `<time datetime="2020-03-20">Thursday, March 12th</time>`
## Usability & Accessibility Improvements:
-	Add keyboard shortcuts to navigation items 
  - E.g., make nav items keyboard accessible `<nav><button accesskey="l">Home</button></nav>` 
-	Make navigations tab accessible
  - E.g. When navigating to site for the first time, hit TAB to focus an item on the nav bar 
  - `<nav><button tabindex="1">Home</button><button tabindex="2">Menu</button></nav>`
  - Tip: adding tabindex attribute enables the CSS pseudoclass ":focus" to apply styles to the currently-focused item, like a highlight.
-	Glossary of terms and acronyms accessible from app footer
-	FAQ/Info/Tooltips available to describe specific functionalities that may not be obvious to naïve user

## Additional Resources:
- https://www.w3.org/TR/WCAG20/
- https://accessible.org/wcag-20-guide/
