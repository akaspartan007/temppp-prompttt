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

## Error Handling and Defensive Coding

The website must fail gracefully and avoid broken layouts or unresponsive components. Ensure code accounts for:

* **Missing DOM Elements:** JavaScript modules must check for elements before assigning events to avoid console errors when pages lack specific UI components.
* **Failed Fetch Requests:** Network drops or missing JSON resources must fallback to reader-friendly UI alerts rather than rendering frozen loaders.
* **Corrupted Data:** Malformed or incomplete item arrays within the JSON catalog must skip rendering gracefully without stalling the script parsing engine.
* **localStorage Failures:** The product comparison dashboard must fall back to basic operational states without crashing if the browser restricts storage access.
* **Broken Image References:** Fallback images or text-labeled containers must replace broken media paths seamlessly to maintain card alignment.

Include clear inline programming comments that explain fundamental interaction blocks, routing updates, or validation steps without causing excessive code clutter.

---

## Explicit Constraints

* **Tech Stack Bound:** Use HTML5, CSS3, Tailwind CSS, and Vanilla JavaScript only.
* **Rendering:** All product displays must remain JSON-driven. Hardcoded HTML listings are banned.
* **Comparison Limits:** Enforce a maximum threshold of 3 products. Block extra additions with user alerts.
* **Zero Dependencies:** External AI models, compilation setups, backend routing engines, or framework plugins are strictly prohibited.
* **Pathing Integrity:** Use relative paths throughout the workspace to guarantee uncompromised performance when deployed over GitHub Pages subdirectories.

---

## Output Expectations

Deliver complete, production-grade, highly responsive web assets mapped neatly to the architectural blueprint. Code blocks must provide ready-to-run functionality, clear visual formatting, and complete architectural parity across every specified frontend system.
