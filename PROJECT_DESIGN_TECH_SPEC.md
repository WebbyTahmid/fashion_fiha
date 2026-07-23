# ✦ FIHA — Web Design, Tech Stack & AI Agent Steering Master Guide

এই ডকুমেন্টটি তৈরি করা হয়েছে যাতে আপনি এবং যেকোনো AI Agent (বা Developer) খুব সহজেই বুঝতে পারেন এই ওয়েবসাইটে **কী কী Technology, Design Pattern, Animations এবং Sections** ব্যবহার করা হয়েছে, **কেন ব্যবহার করা হয়েছে**, এবং **কীভাবে এটি কাজ করে**।

এছাড়াও ভবিষ্যতের কাজের জন্য **AI Agent-দের সঠিক Command দেওয়ার ও ভুল ধরার Complete Blueprint** নিচে দেওয়া হলো।

---

## 1. 🛠️ Tech Stack & Dependencies (কী কী টেকনোলজি ব্যবহার করা হয়েছে)

এই সাইটটিতে কোনো ভারী Framework (যেমন React/Vue) ব্যবহার না করে **Pure High-Performance Vanilla Web Stack** ব্যবহার করা হয়েছে, যাতে সাইটটি দ্রুত লোড হয় এবং ৬০ FPS (Frames Per Second) মসৃণ অ্যানিমেশন দেয়।

| Technology / Library | Purpose (কেন ব্যবহার করা হয়েছে) | Technical How-To (কীভাবে কাজ করে) |
| :--- | :--- | :--- |
| **HTML5 & CSS3** | পুরো ওয়েবসাইটের Structure, Layout এবং Visual Styling | CSS Grid, Flexbox, CSS Custom Properties (CSS Variables) এবং BEM Layout Architecture। |
| **Canvas Video Engine (Custom JS)** | Hero Section-এ ৬০ FPS Smooth Saree & Kundan Jewelry Video Loop | HTML5 `<canvas>` Elements, `requestAnimationFrame`, image crossfade interpolation & gold particle system. |
| **Studio Freight Lenis (`lenis.min.js`)** | Sofi Health Style Inertia Smooth Scrolling | Browser-এর ডিফল্ট Wheel/Touch Scroll-কে ইন্টারসেপ্ট করে Smooth Momentum Animation তৈরি করে। |
| **GSAP (`gsap.min.js`)** | High-Performance Animation Engine | DOM Elements, Opacity, Smooth Transformations এবং Physics Timelines হ্যান্ডেল করার জন্য। |
| **GSAP ScrollTrigger (`ScrollTrigger.min.js`)** | Pinned Scroll, Dynamic Color Scrubbing & Reveal Effects | স্ক্রিনের Scroll Position ট্র্যাকিং করে Horizontal Scrolling এবং Background Theme Color Scrubbing পরিচালনা করে। |
| **Google Fonts** | Luxury Aesthetic Typography Hierarchy | `Playfair Display` (Headings), `Cormorant Garamond` (Subheadings/Quotes), `Inter` (Body & Tags)। |

---

## 2. 🎨 Design Architecture & Aesthetics (ডিজাইন গাইডলাইন)

### 🔴 Color Palette (কালার প্যালেট)
- **Primary Background:** `#faf6f0` (Warm Ivory / Warm Linen — প্লাস্টিক বা জেনেরিক সাদা নয়, এটি লাক্সারি ফিল দেয়)
- **Secondary Background:** `#f3ece2` (Soft Sand Linen — কার্ড ও সেকশন বিভাজনের জন্য)
- **Dark Theme Scrub:** `#0e1f17` (Deep Emerald Forest Green — রিচ ও প্রিমিয়াম বিডি ফ্যাশন থিম)
- **Gold Accent:** `#9a7b4f` (Antique Muted Gold — লেখার হাইলাইট ও বোতামের জন্য)
- **Text Primary:** `#1a1409` (Deep Charcoal — একদম ১০০% কালো নয়, সফট ডার্ক)

### ✒️ Typography Hierarchy (টাইপোগ্রাফি স্কেল)
- **Display Headings (`--fs-display`):** `Playfair Display` serif font, fluid sizing `clamp(3.2rem, 6.5vw + 0.5rem, 6.2rem)`।
- **Subheadings / Quotes (`--ff-accent`):** `Cormorant Garamond` italic accent font।
- **Body & Controls (`--ff-sans`):** `Inter` clean sans-serif font for readability.

### 🔮 Micro-Animations & Reveal Effects
1. **Line-Mask Split Reveal (`.line-outer` & `.line-inner`):** লেখাগুলো নিচে থেকে উপরে মাস্ক খুলে উঠে আসে (Sofi Health Style)।
2. **Gold Sparkle Particle Dust Overlay:** ক্যানভাস ভিডিওর উপরে সফট সোনার কণা ভেসে বেড়ায়।
3. **Gold Selection Highlight:** সাইটের যেকোনো টেক্সট সিলেক্ট করলে গোল্ডেন ব্যাকগ্রাউন্ড ও ডার্ক টেক্সট শাইন করে।

---

## 3. 🧩 Section-by-Section Complete Breakdown (কয়টা সেকশন, কেন ও কীভাবে)

### ① Preloader (প্রিলোডার সেকশন)
- **কী:** ওয়েবসাইট ওপেন হওয়ার সাথে সাথে একটি গোল্ডেন পালসিং লোগো ও প্রোগ্রেস বার।
- **কেন:** ভারী হাই-রেজোলিউশন ইমেজ ও ফন্ট ব্যাকগ্রাউন্ডে লোড হওয়ার সময় ইউজারকে একটি লাক্সারি ব্র্যান্ডের ফিল দেওয়া।
- **কীভাবে:** CSS `@keyframes fill` এবং JS-এর `window.onload` ইভেন্ট দিয়ে সাইট লোড হলে `.hidden` ক্লাস যুক্ত হয়ে ফেইড আউট হয়ে যায়।

---

### ② Navbar (ন্যাভবার)
- **কী:** ফিক্সড হেডার লোগো, নেভিগেশন লিংক এবং গোল্ডেন "Shop Now" CTA বাটন।
- **কেন:** ইউজার যেকোনো সময় সহজেই সাইটের সেকশনে যেতে পারে অথবা ফেসবুক পেজে কেনাকাটা করতে পারে।
- **কীভাবে:** JS Lenis Scroll Listeners ব্যবহার করে ৮০px স্ক্রোল হলে `backdrop-filter: blur(24px)` সহ গ্লাস মোর্ফিজম স্টাইলে ছোট হয়ে যায়। ডার্ক ব্যাকগ্রাউন্ড সেকশনে এটি ডার্ক থিমে শিফট করে।

---

### ③ Hero Section — 60fps Canvas Video Engine (হিরো সেকশন)
- **কী:** শাড়ি, সোনার কুণ্ডন গহনা এবং অ্যাকসেসরিজের ৬০ FPS ভিডিও লুপ, যার উপর গোল্ডেন পার্টিকেল ভাসছে।
- **কেন:** প্রথম দর্শনেই ইউজার যাতে ব্র্যান্ডের লাক্সারি ও প্রিমিয়াম বিডি ফ্যাশন ফিল পেয়ে মুগ্ধ হয়ে যায় (Wow Effect)।
- **কীভাবে:** HTML5 `<canvas id="heroCanvas">`-এ ৩টি হাই-রেজোলিউশন ফ্রেম এবং পার্টিকেল অ্যারে `requestAnimationFrame`-এর মাধ্যমে মসৃণ ক্রসফেড এবং Ken-Burns জুম এফেক্ট তৈরি করে।

---

### ④ Brand Ticker (ব্র্যান্ড ট্র্যাকার / মার্কি)
- **কী:** অনবরত বাম দিকে স্ক্রোল হওয়া গোল্ডেন টেক্সট লাইন (যেমন: *Handcrafted BD Sarees ✦ Kundan & Gold Accessories*)।
- **কেন:** দ্রুত ব্র্যান্ডের ট্রাস্ট ফ্যাক্টর, ফ্রি ডেলিভারি ও প্রধান ফিচারগুলোকে ইউজারের চোখে তুলে ধরা।
- **কীভাবে:** CSS `@keyframes ticker` অ্যানিমেশন ব্যবহার করে Infinite Loop আকারে `transform: translateX(-50%)` করা হয়।

---

### ⑤ Story / About Section (আওয়ার স্টোরি)
- **কী:** ব্র্যান্ডের গল্প, "24K+ Happy Customers" ফ্ল্যাটিং ব্যাজ এবং ৪টি কোর ফিচারের গ্রিড।
- **কেন:** ব্র্যাণ্ডের বিশ্বাসযোগ্যতা (Credibility) এবং বাংলাদেশী কারুশিল্পের ঐতিহ্য তুলে ধরা।
- **কীভাবে:** IntersectionObserver ব্যবহার করে স্ক্রোল করে স্ক্রিনে আসলে `reveal-up` ক্লাসের মাধ্যমে উপাদানগুলো সুন্দরভাবে ফেইড-ইন হয়ে উঠে আসে।

---

### ⑥ Pinned Horizontal Collections Section (সোফি হেলথ স্টাইল কালেকশনস)
- **কী:** ইউজার মাউস দিয়ে সোজা নিচে স্ক্রোল করবে (Vertical Scroll), কিন্তু কালেকশন কার্ডগুলো বাম থেকে ডান দিকে স্লাইড করবে (Horizontal Scroll)।
- **কেন:** এটি আধুনিক ওয়েবসাইটের অন্যতম প্রিমিয়াম ও আকর্ষণীয় এফেক্ট, যা ইউজারকে এঙ্গেজড রাখে।
- **কীভাবে:** GSAP `ScrollTrigger`-এর মাধ্যমে `#collectionsPinned` সেকশনটি স্ক্রিনে `pin: true` করে লক করা হয় এবং স্ক্রোলের দূরত্বের অনুপাতে `#horizontalWrapper`-কে বামে সরান হয় (`x: -scrollWidth`)।

---

### ⑦ Dynamic Theme Color Scrub Banner (ডার্ক থিম স্ক্রোল ব্যানার)
- **কী:** স্ক্রোল করার সাথে সাথে পুরো ব্রাউজারের ব্যাকগ্রাউন্ড কালার লাইট ক্রিম থেকে ডিপ এমারেল্ড গ্রিন (`#0e1f17`) হয়ে যায় এবং আবার লাইটে ফিরে আসে।
- **কেন:** ভিজ্যুয়াল ভ্যারাইটি তৈরি করা এবং ড্রামাটিক লাক্সারি অনুভূতি দেওয়া।
- **কীভাবে:** GSAP `ScrollTrigger`-এর `scrub: 0.6` প্রপার্টি দিয়ে `body`-র `background-color` ইন্টারপোলেট করা হয়।

---

### ⑧ Live Counter Stats Section (পরিসংখ্যান সেকশন)
- **কী:** 24,000+ গ্রাহক, 500+ ডিজাইন, 4.9 রেটিং এবং 64 জেলার লাইভ কাউন্টিং নম্বর কার্ড।
- **কেন:** সোশাল প্রুফ (Social Proof) দিয়ে কাস্টমারের কনফিডেন্স বাড়ানো।
- **কীভাবে:** JS IntersectionObserver স্ক্রিন সনাক্ত করার পর `requestAnimationFrame` দিয়ে সংখ্যাগুলোকে ০ থেকে টার্গেট সংখ্যা পর্যন্ত কাউন্ট করে দেখায়।

---

### ⑨ Testimonials (গ্রাহকদের রিভিউ)
- **কী:** স্টার রেটিং সহ কাস্টমার রিভিউ কার্ডের গ্রিড।
- **কেন:** ফেসবুক কাস্টমারদের আসল ইতিবাচক অভিজ্ঞতার প্রমাণ।
- **কীভাবে:** সফট ব্যাকড্রপ ব্লার ও বর্ডার সহ থ্রি-কলাম রেসপন্সিভ গ্রিড।

---

### ⑩ Social Feed Grid (ফেসবুক লাইভ ফটো গ্রিড)
- **কী:** ফেসবুক পেজের ৬টি অরিজিনাল প্রোডাক্ট ফটো দিয়ে তৈরি গ্রিড, যাতে হোভার করলে ডার্ক হয় এবং গোল্ড স্টার ফুটে ওঠে।
- **কেন:** প্রোডাক্টের বাস্তব ছবি দেখানো ও সরাসরি ফেসবুক পেজে ট্রাফিক পাঠানো।
- **কীভাবে:** CSS Grid `repeat(6, 1fr)` এবং হোভার স্কেল অ্যানিমেশন।

---

### ⑪ Newsletter Section (নিউজলেটার স্পেশাল অফার)
- **কী:** "Subscribe For Exclusive Offers" পিল-শেপ ইনপুট ফিল্ড ও সাবস্ক্রাইব বাটন।
- **কেন:** ইমেইল লিড কালেকশন করা এবং পরবর্তীতে অফার পাঠানো।
- **কীভাবে:** JS Form Submit Intercept করে তাৎক্ষণিক "✓ Subscribed!" ফিডব্যাক মেসেজ দেখানো।

---

### ⑫ Footer & Back-to-Top Button (ফুটার ও ব্যাক-টু-টপ)
- **কী:** ৪-কলাম ডার্ক ফুটার, সোশাল লিংক, ক্যাটাগরি ও কুইক লিংক এবং স্মুথ রিটার্ন বাটন।
- **কেন:** অল-ইন-ওয়ান সাইট নেভিগেশন ও কপিরাইট ইনফরমেশন।
- **কীভাবে:** JS Lenis integration দিয়ে ক্লিক করলে ১.২ সেকেন্ডে স্মুথভাবে স্ক্রিনের একদম উপরে নিয়ে যায়।

---

## 4. 🧠 Future AI Agent Prompting & Control Blueprint (অন্য Agent-কে দিয়ে নতুন ওয়েবসাইট বানানোর গাইড)

আপনি যখন ভবিষ্যতের যেকোনো AI Agent-কে (যেমন Antigravity, Claude, ChatGPT, Gemini, etc.) কোনো নতুন ওয়েবসাইট তৈরি করতে বলবেন, তখন কীভাবে কমান্ড দেবেন এবং কীভাবে ভুল ধরবেন — তার প্রম্পটিং স্ট্র্যাটেজি নিচে দেওয়া হলো:

### 📋 Rule 1: Always Enforce Design System First (ডিজাইন সিস্টেম নির্ধারণ করা)
Agent-কে কাজ শুরুর আগেই এই ইনস্ট্রাকশন দেবেন:
> *"Before writing HTML/JS, write a comprehensive CSS Design System using CSS Variables (`:root`). Define custom HSL/Hex color tokens, custom Google Fonts (`Playfair Display` + `Inter`), smooth transitions, and responsiveness tokens. Do NOT create basic or generic blue/red/white MVPs."*

---

### 📋 Rule 2: Demand Specific Smooth Scroll & Motion Engines (অ্যানিমেশন প্রম্পট)
যদি আপনি Sofi Health বা অনুরূপ লাক্সারি স্ক্রোল চান, তবে সরাসরি এই লাইব্রেরিগুলো স্পেসিফাই করুন:
> *"Implement Studio Freight Lenis for smooth inertia scrolling. Sync Lenis with GSAP and GSAP ScrollTrigger. Use line-mask split text reveals (`.line-outer` & `.line-inner`) for titles, and pinned horizontal scrolling for feature showcases."*

---

### 📋 Rule 3: Ban Generic Text & Placeholder Buzzwords (টেক্সট সাইজ ও কপি কন্ট্রোল)
Agent-কে জেনেরিক লেখা থেকে বিরত রাখতে বলুন:
> *"Do NOT use generic corporate buzzwords like 'Signature Edit', 'Stay in the loop', 'Lorem Ipsum', or location errors. Use real, high-converting retail/boutique copy tailored specifically for our brand."*

---

### 📋 Rule 4: Zero External Broken CDNs for Hero Media (মিডিয়া হ্যান্ডলিং)
যদি হিরো সেকশনে ভিডিও বা পিকচার লোড না হয় বা লিংক ভেঙে যায়, তবে বলবেন:
> *"If external video CDNs return 403 Forbidden or session timeouts, build an HTML5 Canvas 60fps frame-interpolation video engine with particle overlays so that the hero visual loops smoothly under all network conditions without failing."*

---

### 📋 Rule 5: Checklist for Catching Agent Errors (Agent-এর ভুল ধরার নিয়ম)
Agent কাজ শেষ ঘোষণা করলে আপনি নিচে উল্লেখিত ৫টি জিনিস পরীক্ষা করে ভুল ধরবেন:

1. **Text Overlap / Dark Theme Leak:** ডার্ক থিম স্ক্রোল হওয়ার পর কি নিচের কোনো লেখার কালার টেক্সট ও ব্যাকগ্রাউন্ডের সাথে মিশে গায়েব হয়ে যাচ্ছে? (যদি হয়, Agent-কে বলুন: *"Explicitly set section-level backgrounds so body-scrub doesn't hide text."*)
2. **Missing Media:** ছবিতে কি ৩০০০x২০০০ পিক্সেলের খালি ফোল্ডার বা ব্রোকেন লিংক দেখা যাচ্ছে? (বলুন: *"Replace broken image links with responsive, working compressed images."*)
3. **Broken Scroll Engine:** জেনুইন মাউস হুইল দিয়ে স্ক্রোল করার সময় কি ধাক্কা খাচ্ছে বা লাফ দিচ্ছে? (বলুন: *"Ensure Lenis.raf is added to GSAP ticker without conflicting native scroll events."*)
4. **Mobile Layout Overlap:** মোবাইল ভিউতে কি টেক্সট ভেঙে বাইরে চলে যাচ্ছে বা বাটন ওভারল্যাপ করছে? (বলুন: *"Fix media queries for max-width 768px, wrap flex containers, and adjust font clamps."*)
5. **Console Errors:** ব্রাউজার Inspect-এর Console ট্যাবে কি লাল রঙের Error দেখা যাচ্ছে? (বলুন: *"Fix all uncaught TypeError or undefined element references in console."*)

---

## 📌 Summary Cheat-Sheet for Your Commands

যখনই কোনো নতুন পেজ বানাবেন, এই শর্ট প্রম্পটটি কপি-পেস্ট করে দিতে পারেন:

```text
Build a modern, luxury web app using standard HTML, CSS, and JS.
Follow these specifications:
1. Core Palette: Warm Linen (#faf6f0), Dark Forest Emerald (#0e1f17), Muted Antique Gold (#9a7b4f).
2. Typography: Playfair Display for headings, Cormorant Garamond for italics/accents, Inter for body text.
3. Motion & Scroll: Implement Studio Freight Lenis for smooth inertia scroll, synced with GSAP & ScrollTrigger.
4. Hero Visual: 60fps Canvas video/photo engine with gold sparkle particle dust overlay.
5. Interactive Sections: Pinned horizontal scroll track for collections, split-text line masks for headings, live counting numbers for stats.
6. Execution Quality: Zero placeholder text, zero broken links, responsive layout across desktop and mobile, zero console errors.
```
