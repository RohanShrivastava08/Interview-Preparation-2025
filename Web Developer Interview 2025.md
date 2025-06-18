
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
### 🟡 **JavaScript (JS)**

21. **What is JavaScript?**  
    JavaScript is a high-level, interpreted programming language used to create dynamic and interactive web pages.
    
22. **What is the difference between `var`, `let`, and `const`?**
    

- `var`: Function-scoped, hoisted
    
- `let`: Block-scoped, not hoisted
    
- `const`: Block-scoped, constant value
    

23. **What is hoisting in JavaScript?**  
    Variable and function declarations are moved to the top of their scope before code execution.
    
24. **What are closures in JavaScript?**  
    A closure is a function that remembers variables from its lexical scope even when executed outside that scope.
    
25. **What’s the difference between `==` and `===` in JavaScript?**
    
- `==`: Loose equality, converts types
    
- `===`: Strict equality, checks type and value
---
---
### 🟢 **DOM & Events**

26. **What is the DOM (Document Object Model)?**  
    The DOM is a programming interface that represents the structure of HTML documents as a tree of objects.
    
27. **How do you access elements in the DOM using JavaScript?**  
    Using methods like:
    

- `document.getElementById("id")`
    
- `document.querySelector(".class")`
    
- `document.querySelectorAll("div")`
    

28. **What is event delegation in JavaScript?**  
    Event delegation allows you to add a single event listener to a parent element to handle events from its children using `event.target`.
    
29. **What is event bubbling and capturing?**
    

- **Bubbling**: Event flows from the target element up to the root.
    
- **Capturing**: Event flows from the root down to the target.
    

30. **How to prevent event bubbling?**  
    Use `event.stopPropagation()` to stop the event from propagating further.
    
31. **What is `addEventListener` and its syntax?**  
    Adds an event listener to an element:
    

js

CopyEdit

`element.addEventListener('click', functionName);`

32. **How to remove an event listener?**  
    Use `removeEventListener()` with the same function reference:
    

js

CopyEdit

`element.removeEventListener('click', functionName);`

33. **What are different types of DOM events?**  
    Common events include:
    

- `click`
    
- `keydown`, `keyup`
    
- `submit`
    
- `change`
    
- `mouseover`, `mouseout`
    

34. **What is the difference between `innerHTML` and `textContent`?**
    

- `innerHTML`: Parses and renders HTML
    
- `textContent`: Only gets/sets plain text
    

35. **How to dynamically create an element in JavaScript?**
    `const div = document.createElement('div'); div.textContent = 'Hello'; document.body.appendChild(div);`

---
---
### 🔵 **Git & Version Control**

36. **What is Git?**  
    Git is a distributed version control system for tracking code changes during software development.
    
37. **What is GitHub?**  
    GitHub is a cloud-based hosting service that lets you manage Git repositories and collaborate on projects.
    
38. **What is the difference between `git fetch` and `git pull`?**
    

- `git fetch`: Gets changes from the remote but doesn’t merge
    
- `git pull`: Fetches + merges changes into current branch
    

39. **How do you resolve a merge conflict in Git?**
    

- Edit the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`)
    
- Save and stage the file
    
- Run `git commit`
    

40. **What is a Git branch?**  
    A branch is a lightweight movable pointer to a commit, used for parallel development.
    
41. **What is the purpose of `.gitignore` file?**  
    It tells Git which files/folders to ignore and not track (e.g., `node_modules/`, `.env`).
    
42. **How do you clone a Git repository?**
    `git clone https://github.com/user/repo.git`

43. **What is the command to initialize a Git repository?**
    `git init`

44. **How to stage and commit files in Git?**
    `git add .   git commit -m "Commit message"`

45. **What is `git status` used for?**  
    It shows the current state of the working directory and staging area.

---
---
