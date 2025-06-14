## 🔷 **SECTION 1: HTML, CSS, Browser (Q1–10)**

### **1. What is the difference between HTML and XHTML?**

**Answer:**

- **HTML (HyperText Markup Language)** is forgiving of syntax errors (e.g., missing end tags).
    
- **XHTML (Extensible HTML)** follows stricter XML rules: all tags must be closed, lowercase, properly nested.
    
- XHTML is stricter and better for data interchange; HTML is better supported by browsers.
    

---

### **2. Explain the CSS Box Model.**

**Answer:**  
Every HTML element is a box made of:

- **Content**: The actual text/image.
    
- **Padding**: Space inside the border.
    
- **Border**: Edge of the box.
    
- **Margin**: Space outside the box.
    

---

### **3. What is the difference between `display: none` and `visibility: hidden`?**

**Answer:**

- `display: none`: Hides the element completely — no layout space is reserved.
    
- `visibility: hidden`: Hides the element **but still reserves its space** in layout.
    

---

### **4. What are semantic HTML tags?**

**Answer:**  
Semantic tags like `<article>`, `<nav>`, `<header>`, `<section>` define the **meaning** of the content.  
They:

- Improve accessibility
    
- Aid SEO
    
- Help developers understand structure
    

---

### **5. How does `position: absolute` work in CSS?**

**Answer:**  
`position: absolute` positions the element **relative to its nearest positioned ancestor** (`relative`, `absolute`, or `fixed`). If no ancestor is positioned, it's relative to the document body.

---

### **6. What are media queries?**

**Answer:**  
Media queries apply CSS rules based on **device characteristics** (e.g., width).

css

CopyEdit

`@media (max-width: 768px) {   .container { flex-direction: column; } }`

Used for **responsive design**.

---

### **7. What is the difference between SSR and CSR?**

**Answer:**

- **Server-Side Rendering (SSR):** HTML is generated on the server (e.g., Next.js).
    
- **Client-Side Rendering (CSR):** JavaScript runs in the browser and builds HTML dynamically (e.g., React SPA).
    
- SSR is better for SEO; CSR is better for interactive apps.
    

---

### **8. What is CORS?**

**Answer:**  
CORS (Cross-Origin Resource Sharing) is a **security feature** that controls how one domain can access resources on another.  
Handled via response headers like:

http

CopyEdit

`Access-Control-Allow-Origin: https://example.com`

---

### **9. What is the DOM and how does it relate to JavaScript?**

**Answer:**  
DOM (Document Object Model) is a **tree-like structure** representing HTML in the browser.  
JavaScript can use it to:

- Modify structure (`createElement`, `removeChild`)
    
- Update styles
    
- Handle events
    

---

### **10. Explain Critical Rendering Path.**

**Answer:**  
The Critical Rendering Path is the sequence of steps the browser performs to render a page:

1. HTML → DOM
    
2. CSS → CSSOM
    
3. DOM + CSSOM → Render Tree
    
4. Layout
    
5. Paint
    
6. Composite