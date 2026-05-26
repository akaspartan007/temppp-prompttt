# Smart IT Product Discovery & Quote Management System

## Context and Role

You are a Frontend Web Developer and Digital Commerce Experience Engineer specializing in modern product showcase platforms, responsive web systems, and lightweight e-commerce experiences.

You have been contracted to design and develop a high-performance, visually engaging, and production-quality frontend platform for a company providing teleprompters, IT products, laptops, and technology accessories.

The project must function as a modern IT product discovery and quotation platform that enables visitors to browse, compare, and explore technical products through an intuitive and professional interface.

The platform should not behave like a basic classroom website or static brochure. Instead, it must resemble a lightweight e-commerce product catalogue and business showcase platform designed for real customers and commercial use cases.

The website must support a unified customer experience model where individual users and business clients alike can:

* Explore professional equipment and enterprise products while evaluating specifications and pricing before making purchasing decisions.
* Compare multiple technical products simultaneously so they can identify suitable equipment for organizational or personal deployment.
* Submit quotation requests for single or bulk purchases and specialized technical requirements.
* Search products using natural language or category-based navigation.

The platform must therefore balance professional presentation, modern UI design, smooth user experience, fast navigation, frontend maintainability, and a scalable product architecture.

The final system should communicate trust, technical expertise, brand professionalism, and digital credibility.

---

## Objective

Develop a complete multi-page IT Product Discovery and Quote Management Website titled: **Smart E-Commerce Product Discovery & Quote Management System**

The purpose of the platform is to improve how customers discover and evaluate technical products online. The application must function as a frontend-only e-commerce catalogue system that delivers an experience similar to modern e-commerce websites while remaining lightweight and easy to deploy.

The system must:

* Present products through visually organized catalogue pages that make technical products easier to browse and understand.
* Provide intelligent discovery systems that reduce friction during product exploration and help customers locate suitable products quickly.
* Support side-by-side comparisons so customers can evaluate competing products before requesting quotations.
* Offer responsive interaction patterns and reusable UI systems that improve usability across desktop, tablet, and mobile devices.
* Deliver a professional and trustworthy online experience that strengthens the digital brand presence.

The completed project should function as a commercial-grade frontend showcase platform. All product cards, detail pages, and listings must be generated dynamically using JSON-driven frontend logic. Hardcoded product rendering is prohibited.

---

## Business and User Context

The e-commerce platform provides a range of technology products and professional solutions. The company specializes in:

* Teleprompter systems
* Laptop devices
* IT accessories and hardware

Customers interacting with the platform may have different browsing intentions. Some users may already know the exact product they want, while others may need recommendations, compare alternatives, explore compatible devices, search within a budget, or request technical guidance.

Because of these varied use cases, the platform must support multiple discovery methods rather than relying on static navigation alone. The website should therefore behave like a smart product discovery system.

The visual identity and interaction patterns should communicate reliability, simplicity, technical sophistication, and business credibility. The interface should help reduce information overload and guide users toward informed product decisions.

---

## Core System Requirements

### Product Showcase and Discovery System

Develop a centralized product showcase experience that organizes products clearly and supports efficient navigation.
Users must be able to:

* Browse category-based product collections through structured catalogue pages that separate teleprompters, laptops, and accessories into intuitive navigation groups.
* Open dedicated product detail pages where users can review descriptions, specifications, pricing, and additional information without cluttered layouts.
* Explore visually rich product cards that summarize important information while encouraging deeper product interaction.
* Move between related products and categories without losing navigation context, helping users continue exploration smoothly.
* Filter and search products dynamically to reduce browsing effort and improve decision-making efficiency.
* Submit quotation requests whenever purchase intent or product interest is identified.

All listing data must load dynamically from `data/products.json`. This file functions as the single source of truth and must control catalogue rendering, product metadata, category grouping, and dynamic frontend updates. Manual duplication of product data in HTML is not allowed.

### Product Categories

The catalogue must support multiple technology categories while preserving clean organization and intuitive navigation.

#### 1. Teleprompters

The teleprompter section represents a major offering and should receive professional visual treatment. The teleprompter catalogue must support:

* **Studio teleprompters:** Designed for professional recording and production environments where screen size and readability are critical.
* **Broadcast teleprompters:** Intended for media and television workflows where reliability and clarity are essential.
* **Portable teleprompters:** Designed for mobile content creators and lightweight recording environments.

The interface should visually distinguish professional and portable product use cases so users quickly understand product purpose, deployment scenario, and equipment category.

#### 2. Laptop Categories

The laptop section should support technical comparison and specification-focused browsing. Supported laptop types include:

* **Business laptops:** Optimized for productivity, enterprise work, and professional use cases.
* **Consumer laptops:** Intended for casual users, personal productivity, and general computing tasks.

Laptop pages should emphasize hardware specifications, performance-related information, pricing visibility, and comparative browsing. Users should be encouraged to compare devices rather than relying solely on isolated product viewing.

#### 3. IT Products and Accessories

The accessories section should provide broader browsing flexibility. Supported accessory categories include:

* Wireless mouse
* Keyboard
* USB hubs
* Monitor accessories and peripheral devices

This category should be designed for scalability. The architecture should support future additions without requiring major frontend restructuring, and accessories should remain easy to browse despite potentially larger catalogue sizes.

### Product Listing Requirements

Each product listing must include:

* Product image that visually represents the item for immediate identification.
* Product title and category labels to organize listings clearly.
* Brand information so customers can identify manufacturers.
* Short descriptive summaries that communicate product purpose without overwhelming users.
* Technical specifications highlighting key differentiators and purchasing considerations.
* Pricing information displayed clearly and consistently across the catalogue.
* Ratings or review indicators that provide social validation.
* Promotional badges such as “New,” “Best Seller,” or “Featured” to highlight product importance.

Users interacting with product listings must be able to open product pages, add products to comparison directly from listings, and request quotations without navigating through unnecessary interaction layers.

### AI Product Finder Requirements

Develop a rule-based AI Product Finder that simulates intelligent product discovery without relying on external machine learning services or third-party AI APIs. The purpose of this feature is to help users discover suitable products through conversational or natural-language-style search rather than relying entirely on manual browsing.

The AI finder must:

* Accept natural language input so users can describe what they need using conversational or everyday language.
* Detect category intent by identifying whether users are searching for laptops, teleprompters, accessories, or related products.
* Identify price-based conditions so users can search according to affordability and budget preferences.
* Detect feature-related keywords that indicate technical requirements or intended use cases.
* Recognize brand preferences whenever users specify manufacturers or preferred technology providers.
* Rank and prioritize relevant results rather than displaying unrelated or randomly ordered products.
* Display recommendations dynamically within a clean and visually understandable UI.

> **Examples of User Queries and Expected Behavior:**
> * *User Query:* "Laptop under $700" $\rightarrow$ *Expected Result:* Display affordable laptop recommendations sorted by closest matching criteria.
> * *User Query:* "Wireless mouse for office work" $\rightarrow$ *Expected Result:* Filter accessories matching both category and workflow flags.
> * *User Query:* "Portable teleprompter" $\rightarrow$ *Expected Result:* Directly isolate lightweight teleprompter entries.
> 
> 

The AI finder should improve product discovery while remaining fast, explainable, maintainable, and rule-driven. External AI APIs and backend recommendation services are prohibited.

### Live Search Requirements

Develop a shared global search system that behaves similarly to modern e-commerce search experiences. Search functionality must remain available across the entire website via a shared navbar-based search input.

Search must:

* Work across all pages so users can search products without losing their current browsing context.
* Match product names, descriptions, summaries, and brand information to help users locate specific items quickly.
* Display live dropdown suggestions that update dynamically while users type.
* Navigate users directly to product detail pages when search results or suggestions are selected.

> **Examples of Live Search Behavior:**
> * *Typing:* "tele" $\rightarrow$ *Expected Suggestions:* Studio Teleprompter, Broadcast Teleprompter, Portable Teleprompter
> * *Typing:* "mouse" $\rightarrow$ *Expected Suggestions:* Wireless Mouse, Gaming Mouse, Bluetooth Mouse
> 
> 

Search results should update instantly to reduce friction and encourage exploration.

### Product Comparison Requirements

Develop a dynamic side-by-side product comparison system that helps users evaluate products more confidently before requesting quotations.

The comparison experience must:

* Allow users to add products directly from product cards or product detail pages without unnecessary navigation.
* Display specifications and pricing side-by-side so differences become immediately visible and easier to understand.
* Highlight specification differences visually rather than presenting raw text tables alone.
* Allow users to remove products individually or clear comparison lists completely.
* **Maximum supported products: 3 products.** This limitation preserves readability and prevents UI clutter.
* Prevent duplicate comparison entries so the same product cannot appear multiple times.
* Display validation or feedback messages whenever comparison limits are exceeded.
* Persist comparison selections using `localStorage` so users do not lose progress during navigation or refresh.

### Quote and Inquiry System Requirements

Develop a quotation and inquiry workflow that captures customer intent and encourages business communication.

#### Quote Modal Requirements

Implement a reusable quote request modal that can open from product cards, product detail pages, CTA sections, and comparison pages.
The modal must:

* Animate smoothly during open and close interactions to create a modern user experience.
* Prevent page confusion by maintaining clear modal focus and interaction hierarchy.
* Require fields: Name, Email, Phone number, and Inquiry details.
* Prevent empty form submission, validate email structure, and validate phone number formatting.
* Display inline validation feedback so users understand errors immediately.
* Show confirmation feedback and clear form data safely upon successful submission to avoid accidental duplicates.

#### Contact Page Requirements

Develop a dedicated Contact Page that strengthens communication and improves company credibility. The page must include:

* Company information that introduces the brand and reinforces business legitimacy.
* Contact forms that allow customers to submit inquiries conveniently.
* Email, phone communication details, and social media links.
* Optional Google Maps integration to communicate physical business presence.

### Chatbot Requirements

Develop a rule-based chatbot widget designed to guide users and improve product discovery. The chatbot functions as a lightweight digital assistant rather than a full conversational AI.

The chatbot must:

* Float persistently across pages so assistance remains accessible throughout browsing.
* Include open and close animations that feel modern and non-disruptive.
* Accept predefined product and navigation queries from users.
* Return mapped responses that help guide users toward relevant pages or product categories.

> **Example Dialogue:**
> * *User:* "Show laptops" $\rightarrow$ *Bot:* "Opening laptop catalogue..."
> * *User:* "Compare products" $\rightarrow$ *Bot:* "Opening comparison dashboard..."
> 
> 

Backend chatbot services and AI APIs are prohibited. All chatbot behavior must remain frontend and rule-driven.

---

## UI and Design Requirements

The interface should communicate professionalism, technical credibility, product clarity, and modern e-commerce digital branding. The design should support both information discovery and business conversion.

### Brand Identity Requirements

* **Brand Name:** E-Commerce IT Showroom
* **Logo Asset:** `images/Logo.png`
* **Primary Colors:** Primary Sky Blue (`#0ea5e9`), Secondary Slate (`#64748b`), Deep Dark Blue (`#0f172a`)
* **Typography:** Body Font: Inter; Heading Font: Poppins

### Required UI Components

* **Fixed Navbar:** Sticky navigation system supporting desktop and mobile layouts, containing navigation links and the global search input.
* **Hero Section:** Attention-grabbing homepage layout with headline messaging, CTA buttons, and strong visual hierarchy.
* **Category Cards:** Clickable, responsive cards using icons or imagery to provide clear summaries of major product groups.
* **Product Cards:** Clean grid items presenting images, pricing, ratings, badges, and action paths for comparison and quotes.
* **Product Detail Layout:** Pages that separate technical specifications logically, highlight pricing, and offer clean quote pathways.
* **Comparison Dashboard:** A dedicated interface that visually organizes product rows, highlights structural differences, and stays readable.
* **Quote Modal:** A reusable overlay layout with smooth transitions, error alerts, and focus lock rules.
* **Chatbot Widget:** A non-obstructive overlay styled matching the brand colors to navigate users to relevant collections.
* **Footer:** A clean structural component tracking navigation links, direct corporate contact details, and copyright data.

---

## Frontend Technology Requirements

Develop the application using lightweight frontend technologies that prioritize portability and maintainability.

* **Required Stack:** HTML5, CSS3, Tailwind CSS CDN (`<script src="[https://cdn.tailwindcss.com](https://cdn.tailwindcss.com)"></script>`), and Vanilla JavaScript ES6+.
* **Supporting Tools:** Feather Icons, Google Fonts, and local JSON files.
* **Prohibited Stack Elements:** Do **NOT** use React, Vue, Angular, Svelte, backend frameworks, bundlers (Vite, Webpack), or Node-based frontend tooling. The project must remain fully static and deployable without compilation steps.

### Required Pages

* `index.html` — Homepage
* `teleprompters.html` — Teleprompter catalogue
* `laptop_categories.html` — Laptop catalogue
* `it-products.html` — Accessories catalogue
* `product.html` — Product detail layout
* `compare.html` — Comparison dashboard
* `contact.html` — Contact experience
* `navbarhtml.txt` — Reusable component snippet

### JavaScript Architecture Requirements

Develop modular JavaScript systems that separate concerns. The following specific architectural modules must be delivered:

* `script.js` — Primary initialization and core global UI logic
* `search.js` — Navbar search and live autocomplete suggestions
* `ai-product-finder.js` — Rule-based query evaluation parser
* `chatbot.js` — Overlay micro-bot navigation helper
* `comparison.js` — Matrix logic and localStorage state syncing
* `quote-modal.js` — Modal form validation and processing interactions
* `index-products.js` — Homepage collection filters
* `teleprompters.js` — Teleprompter catalog UI generator
* `laptop_categories.js` — Laptop catalog UI generator
* `it-products.js` — Accessories catalog UI generator
* `product.js` — Dedicated deep-dive detail renderer

All dynamic components must use `fetch()` to parse data from `data/products.json` synchronously or asynchronously at runtime.

---

### Performance and Scalability Requirements

The application should prioritize performance, responsiveness, and long-term maintainability.

The frontend must:

* Load quickly and minimize unnecessary rendering operations so users experience smooth browsing and reduced waiting time.

* Avoid excessive DOM manipulation or deeply nested structures that may degrade rendering performance as product catalogues grow.

* Use lightweight transitions and animations that improve interaction quality without blocking scrolling or navigation.

* Optimize repeated data access patterns to avoid redundant fetch operations and inefficient filtering logic.

* Maintain responsive behavior as new products, categories, and JSON entries are introduced.

The platform should remain optimized for:

* Mobile devices where screen space and performance limitations require efficient rendering.

* Tablet environments where responsive layouts and touch interactions must remain intuitive.

* Desktop environments where denser catalogue layouts and broader navigation experiences may appear.

Performance should be treated as a core engineering requirement rather than a post-development optimization task.

---

## Testing Requirements

Perform structured frontend testing before final deployment to ensure functionality, UI consistency, and reliable interaction behavior.

Testing should validate both technical execution and user experience quality.

Required testing includes:

### Chrome Browser Testing

* Perform Chrome testing to validate rendering behavior, JavaScript execution, and primary interaction flows.

* Confirm functionality for search systems, product rendering, chatbot interactions, modal behavior, and comparison logic.

### Firefox Browser Testing

* Perform Firefox testing to ensure layout consistency and styling reliability across browser engines.

* Validate CSS behavior, navigation systems, and dynamic rendering stability.

### Mobile Responsiveness Testing

* Test layouts across mobile screen sizes to confirm responsive behavior and touch-friendly interaction patterns.

* Validate navigation menus, chatbot placement, product grids, and quote modal usability.

### Form Validation Testing

* Test quote and contact forms to ensure validation logic behaves correctly and rejects invalid or incomplete submissions.

* Confirm email validation, phone validation, and confirmation feedback.

### Console and Runtime Testing

* Inspect browser consoles to identify JavaScript errors, missing assets, failed fetch requests, or broken logic.

* The final deployment should not contain unresolved console errors.

### Cross-Browser Verification

* Compare behavior across multiple browsers to identify rendering inconsistencies and interaction differences.

* The application should remain visually stable and functionally reliable across environments.

---

## Deployment Requirements

Deploy the project using static hosting infrastructure compatible with frontend-only applications.

Supported deployment targets include:

* GitHub Pages
* Netlify
* Other static hosting providers

Deployment must:

* Use relative paths so assets, navigation systems, and scripts remain functional across hosting environments.

* Avoid server-side dependencies, backend routing, or compilation pipelines.

* Remain deployable without bundlers, build tools, or backend configuration.

Expected deployment examples:

```text
https://username.github.io
https://goldenresponsetraining.netlify.app
```

After deployment validate:

* Navigation links
* Product rendering
* Search systems
* Comparison persistence
* Quote modal behavior
* Chatbot interactions
* Responsive layouts

Deployment should represent a stable and production-ready frontend experience rather than a partially functional prototype.

---

## Output Expectations

The final solution must deliver a production-quality frontend experience that aligns with the architectural blueprint and business requirements.

Deliverables must include:

* A multi-page responsive website supported by shared navigation and reusable UI components.

* JSON-driven catalogue rendering that supports maintainable and scalable product architecture.

* A functional live search system with autocomplete suggestions and cross-page accessibility.

* A rule-based AI Product Finder that supports natural-language-style product discovery.

* A dynamic product comparison dashboard supporting side-by-side evaluation workflows.

* A quotation workflow with reusable modal interactions, validation logic, and confirmation feedback.

* A lightweight chatbot system that guides users toward navigation paths and product discovery.

* Modular JavaScript architecture with reusable logic, maintainable code structure, and clear separation of concerns.

* Production-ready deployment compatible with GitHub Pages, Netlify, or equivalent static hosting infrastructure.

The completed system should resemble a commercial IT showcase and quotation platform rather than a classroom prototype or static brochure website.

---

## Tailwind CDN Configuration Correction

Use the following CDN implementation:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

Do not use malformed markdown or mixed hyperlink syntax inside HTML tags.
