
### 🟠 **HTML (HyperText Markup Language)**

1. **What is HTML?**  
    HTML (HyperText Markup Language) is the standard language used to create and structure content on the web.
    
2. **What are HTML tags?**  
    Tags define elements in HTML, usually with an opening (`<tag>`) and closing (`</tag>`) syntax.
    
3. **What is the difference between HTML4 and HTML5?**  
    HTML5 introduced new semantic elements (`<article>`, `<section>`), multimedia support (`<audio>`, `<video>`), and APIs like localStorage and geolocation.
    
4. **What is semantic HTML?**  
    Semantic HTML uses meaningful tags like `<nav>`, `<main>`, `<footer>` to improve readability and accessibility.
    
5. **What are void (self-closing) elements in HTML?**  
    Tags that don’t need a closing tag, e.g., `<img>`, `<br>`, `<input>`, `<hr>`.
    
6. **What is the purpose of the `alt` attribute on images?**  
    It provides alternative text if the image fails to load and helps with accessibility.
    
7. **What is the difference between `<div>` and `<span>`?**  
    `<div>` is a block-level element, while `<span>` is an inline element.
    
8. **What is the DOCTYPE in HTML?**  
    It tells the browser the version of HTML being used. Example: `<!DOCTYPE html>` for HTML5.
    
9. **Can you nest block-level elements inside inline elements?**  
    No. Block-level elements like `<div>` should not be placed inside inline elements like `<span>`.
    
10. **How do you make a hyperlink open in a new tab?**  
    Use `target="_blank"` in the `<a>` tag:
    `<a href="https://example.com" target="_blank">Visit</a>`

---
---
### 🟣 **CSS (Cascading Style Sheets)**

11. **What is CSS?**  
    CSS is used to style HTML elements, controlling layout, colors, fonts, and spacing.
    
12. **What is the difference between ID and Class in CSS?**  
    `ID` is unique (`#id`) and used once; `Class` (`.class`) can be reused across elements.
    
13. **What is the Box Model in CSS?**  
    It includes:  
    `Content → Padding → Border → Margin`
    
14. **What are pseudo-classes in CSS?**  
    Pseudo-classes define special states:  
    Example: `:hover`, `:first-child`, `:nth-child(n)`
    
15. **Difference between absolute, relative, fixed, and sticky positioning?**
    

- `relative`: Positioned relative to its normal position
    
- `absolute`: Relative to the nearest positioned ancestor
    
- `fixed`: Relative to the viewport
    
- `sticky`: Sticks within a scroll range
    

16. **What is specificity in CSS?**  
    It determines which style is applied when multiple rules match. Inline > ID > Class > Tag
    
17. **How can you apply the same style to multiple elements?**  
    Use a common class name and apply styles using `.classname { ... }`.
    
18. **How to import a CSS file into another?**  
    Use `@import 'style.css';` or link both in HTML.
    
19. **What is the difference between `inline`, `block`, and `inline-block`?**
    

- `inline`: No new line, can’t set width/height
    
- `block`: Starts on new line, can set width/height
    
- `inline-block`: Like inline, but can set dimensions
    

20. **What is a media query in CSS?**  
    Used for responsive design to apply styles conditionally:
    `@media (max-width: 600px) { ... }`

---
---
