
Slidev empowers you to create stunning, interactive presentations from plain Markdown files—without layers of complexity. Whether you're quickly drafting ideas or showcasing polished slides, Slidev keeps you focused on what truly matters: your content.

## Key Features

- **Instant Previews**  
  Make edits to your `.md` slides and see changes in real-time—no refreshing required.
- **Interactive Components**  
  Leverage built-in and custom Vue components, like the `Counter` (found in `components/Counter.vue`), to add dynamic functionality to your slides.
- **Theming & Customization**  
  Swap themes (e.g., `seriph`, `default`) with a single line in `slides.md`. Tailor styles, transitions, and layouts to fit any brand or storytelling style.
- **Easy Exports**  
  Export your slides to PDF or images, ensuring your content is accessible even outside the app.
- **Seamless Workflow**  
  Control dependencies with a straightforward `package.json`, and skip clutter by ignoring unneeded output folders in `.gitignore`.

## Quick Start

1. **Install Dependencies**  
   ```bash
   npm install
   ```
   (This uses the lockfile in `package-lock.json` to ensure consistent versions.)

2. **Start the Dev Server**  
   ```bash
   npm run dev
   ```
   Slidev's hot-reload launches an interactive view of your slides at a local development URL.

3. **Build for Production**  
   ```bash
   npm run build
   ```
   Outputs a highly optimized set of static files in the `dist` folder, ready to deploy anywhere.

4. **Export**  
   ```bash
   npm run export
   ```
   Export slides into a sharable PDF.

## Project Structure

- **`slides.md`**  
  Your main content. Slides are created simply by adding Markdown sections with frontmatter for layout or styling preferences.
- **`components/Counter.vue`**  
  Example of a Vue component integrated into slides, showcasing interactive functionalities.
- **`.gitignore`**  
  Keeps `dist` and other generated folders out of source control, ensuring a clean repository.
- **`package.json`** / **`package-lock.json`**  
  Manage dependencies and scripts consistently.  

## Additional Resources

- Full Slidev documentation: [https://sli.dev](https://sli.dev)  
- Learn more about the interactivity offered by Vue components: [https://vuejs.org](https://vuejs.org)

Enjoy crafting engaging, developer-friendly slide decks with Slidev in Memex!
