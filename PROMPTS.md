# Prompt Playbook — Build Your Portfolio with AI

> **How this works:** Follow the prompts below **in order**, from Phase 1 to Phase 7. Each prompt is something you paste into your AI assistant. After the AI gives you code, copy it into the correct file and save. Preview your site in the browser after each phase to see your progress.
>
> **Personalization:** Anywhere you see text inside `[brackets]`, replace it with your own info before pasting the prompt.

---

## Before You Start

Make sure you have already:

1. Pasted the **chatGPT-prompt-v2.md** content into your AI assistant to set up the conversation
2. Created the project folder and files as described in the **WORKSHOP-GUIDE.md**

---

## Phase 1 — Scaffolding (The Skeleton)

**Goal:** Get the basic HTML structure, a CSS reset, and the empty file setup.

### Prompt 1.1 — Create the base HTML

```
Create the complete index.html file for my portfolio website.
Include all the sections listed in the project context (hero, about, work, skills, contact, footer).
For now, just put placeholder text in each section — we will style and fill them in later.
Link to css/styles.css and js/main.js. Add a Google Font import for "Inter" and "Space Grotesk".
```

### Prompt 1.2 — Base styles and CSS reset

```
Create the complete css/styles.css file.
Start with a modern CSS reset, then define CSS custom properties using these exact design tokens:
- --bg-color: #0f172a
- --card-color: #111827
- --accent-color: #6366f1
- --accent-hover: #818cf8
- --text-primary: #f9fafb
- --text-secondary: #9ca3af
- Font families: "Inter" for body text, "Space Grotesk" for headings
- Spacing and border-radius variables
Then add base styles for the body, headings, links, and a container class.
Don't style the individual sections yet — we will do those one at a time.
```

**Checkpoint:** Open `index.html` in your browser. You should see plain text on a dark background with clean fonts. It won't look pretty yet — that's expected.

---

## Phase 2 — Hero Section (The First Impression)

**Goal:** A striking hero section with your name, tagline, and a CTA button.

### Prompt 2.1

```
Now style and enhance the hero section of my portfolio.

Update the HTML for the hero section to include:
- My name as a large heading: [Your Name]
- A tagline below it: [Your Tagline — e.g., "Designer. Animator. Creative Thinker."]
- A call-to-action button that smooth-scrolls to the work/projects section

Style it in CSS to be:
- Full viewport height (100vh), centered content
- Large typography with "Space Grotesk"
- The name should have a subtle gradient text effect or a creative typographic treatment
- The CTA button should have a hover animation (color shift + slight scale)
- Add a cursor glow effect that follows the mouse (subtle glowing circle)
- Add a subtle animated background (gradient shift, floating shapes, or particles — keep it lightweight and GPU-friendly)

Give me the complete updated index.html AND css/styles.css files.
```

**Checkpoint:** Your hero should now fill the screen and look impressive. The button should have a hover effect.

---

## Phase 3 — About Section (Who You Are)

**Goal:** A clean section with your bio and photo.

### Prompt 3.1

```
Now build out the About section.

Update the HTML to include:
- A section heading ("About Me" or similar)
- A profile photo (use https://placehold.co/400x400 as placeholder for now)
- A short bio paragraph: [Write 2-3 sentences about yourself, or use the placeholder from the project context]

Style it so the photo and text sit side-by-side on desktop and stack on mobile.
The photo should have a subtle border or creative shape treatment.
Add a fade-in-on-scroll animation class (we will wire up the JS later).

Give me the complete updated index.html AND css/styles.css files.
```

**Checkpoint:** You should see your bio and a placeholder photo in a nice layout.

---

## Phase 4 — Work / Projects Gallery (Show What You've Made)

**Goal:** A grid of project cards that look great and have hover effects.

### Prompt 4.1

```
Now build the Work/Projects section.

Update the HTML with a grid of project cards. Each card should have:
- A project image (use https://placehold.co/600x400 as placeholder)
- A project title
- A short 1-line description
- A hover overlay effect that reveals the description
- An image zoom effect on hover

Here are my projects (replace with your own or use these placeholders):
1. [Project 1 title] — [short description]
2. [Project 2 title] — [short description]
3. [Project 3 title] — [short description]
4. [Project 4 title] — [short description]
5. [Project 5 title] — [short description]
6. [Project 6 title] — [short description]

Style the grid to be:
- 3 columns on desktop, 2 on tablet, 1 on mobile
- Cards should have rounded corners and a box shadow
- On hover: subtle card elevation, shadow increase, image zoom, and show an overlay with the description text

Add the scroll-animation class to the cards.
Give me the complete updated index.html AND css/styles.css files.
```

**Checkpoint:** You should see a grid of cards. Hover over them — they should animate.

---

## Phase 5 — Skills Section

**Goal:** A visual display of your tools and skills.

### Prompt 5.1

```
Now build the Skills section.

Show my skills as a set of styled tags/badges or icon cards.
My skills are: [List your skills — e.g., Figma, After Effects, Photoshop, Illustrator, Blender, HTML/CSS, Premiere Pro]

Style them as:
- Pill-shaped badges or small cards arranged in a flex-wrap layout
- Each badge has a subtle background, border, and hover glow effect
- Center the whole section
- Add scroll-triggered animation

Give me the complete updated index.html AND css/styles.css files.
```

**Checkpoint:** Skills should appear as stylish badges.

---

## Phase 6 — Contact & Footer

**Goal:** A simple contact section with social links and a clean footer.

### Prompt 6.1

```
Now build the Contact section and footer.

The contact section should include:
- A heading like "Let's Connect" or "Get in Touch"
- A short line of text: [e.g., "I'm open to freelance work and collaboration."]
- Social media icon links for: [e.g., Behance, LinkedIn, Instagram, Email]
  (use # as placeholder URLs for now, use inline SVG icons or simple text labels)
- An email link: [your email or placeholder]

The footer should have:
- A simple copyright line: "© 2026 [Your Name]. Built with AI."

Style the contact section with centered text and icon links that have hover effects.
Give me the complete updated index.html AND css/styles.css files.
```

**Checkpoint:** Scroll to the bottom — you should see your contact links and footer.

---

## Phase 7 — Animations & Polish (Bring It to Life)

**Goal:** Wire up scroll animations and add final polish.

### Prompt 7.1 — Scroll animations

```
Now create the js/main.js file.

Add the following functionality:
1. Use the Intersection Observer API to detect when elements with the class "animate-on-scroll" enter the viewport, then add an "animated" class to trigger CSS animations (fade-in and slide-up).
2. Smooth scrolling for the navigation and CTA button links.
3. A simple active-nav-link highlight that updates based on scroll position.

Also update css/styles.css with the animation CSS:
- .animate-on-scroll elements start invisible and slightly translated down
- .animated elements transition to full opacity and original position
- Stagger the animation delay for grid children so cards animate in one after another

Give me the complete js/main.js AND updated css/styles.css files.
```

### Prompt 7.2 — Navigation bar

```
Add a fixed/sticky navigation bar to the top of the page.

It should include:
- My name or a logo on the left
- Navigation links to each section (About, Work, Skills, Contact) on the right
- Use a glassmorphism style: transparent background with backdrop-filter blur that becomes more visible when scrolled
- Mobile: collapse into an animated hamburger menu with smooth open/close transitions

Update the HTML, CSS, and JS as needed.
Give me the complete updated versions of ALL files that changed.
```

### Prompt 7.3 — Final polish

```
Do a final polish pass on my entire portfolio site:

1. Make sure all spacing and alignment is consistent
2. Ensure everything is responsive (test at 375px, 768px, and 1200px+ widths) using CSS Grid, Flexbox, clamp(), and fluid spacing — no fixed widths
3. Add smooth transition on ALL interactive elements
4. Make sure the page has a proper <title> and meta description for SEO
5. Add a favicon link (use a placeholder)
6. Check for accessibility: semantic HTML, proper alt text on images, focus states on buttons/links, readable contrast, and large enough clickable elements
7. Make sure all animations are GPU-friendly and the site loads instantly

Give me the complete final versions of ALL three files: index.html, css/styles.css, and js/main.js.
```

**Checkpoint:** Your full portfolio should now be polished, animated, and responsive. Test it on your phone!

---

## Phase 8 — Make It Yours (Personalization)

Now that the structure is complete, swap in your real content:

### Prompt 8.1

```
I want to personalize my portfolio. Here is my real information:

- Name: [Your full name]
- Tagline: [Your tagline]
- Bio: [Your bio — 2-3 sentences]
- Profile photo: [filename of your photo, e.g., "me.jpg" — place it in assets/images/]
- Projects:
  1. [Title] — [Description] — [image filename]
  2. [Title] — [Description] — [image filename]
  3. [Title] — [Description] — [image filename]
  4. [Title] — [Description] — [image filename]
- Skills: [Your skills list]
- Social links:
  - Behance: [URL]
  - LinkedIn: [URL]
  - Instagram: [URL]
  - Email: [your email]

Update the index.html with all this real content. Change the placeholder images to reference my actual image files in assets/images/. Give me the complete updated index.html.
```

---

## Phase 9 — Deploy to GitHub Pages

Follow the deployment steps in **WORKSHOP-GUIDE.md** to push your code and go live!

---

## Bonus Prompts (If You Have Extra Time)

### Theme Toggle (Light/Dark Mode)

```
Add a light/dark mode toggle button to the navigation bar.
Use CSS custom properties to swap the color scheme.
Save the user's preference in localStorage so it persists on reload.
Update all three files as needed and give me the complete versions.
```

### Custom Cursor

```
Add a custom animated cursor effect that follows the mouse.
Make it a small glowing circle that scales up when hovering over interactive elements.
Keep it CSS + minimal JS. Update the files as needed.
```

### Project Detail Modal

```
When a user clicks on a project card, show a modal/lightbox with:
- A larger image
- The project title
- A longer description
- A close button
Add smooth open/close animations. Update all files as needed.
```

### Typing Animation for Tagline

```
Make my tagline in the hero section appear with a typing animation effect.
After it finishes typing, show a blinking cursor.
Use JavaScript, no external libraries.
```
