# AI Interaction Rules for the Memex Slidev Project

This file defines the guidelines for how Memex should review, modify, or extend the code in this Slidev-based project. The project uses Slidev to create interactive presentations from Markdown and Vue components. For more information on Slidev features and configuration, please refer to the following guides:
- [Slidev Guide](https://sli.dev/guide/)
- [Syntax Guide](https://sli.dev/guide/syntax)
- [User Interface Guide](https://sli.dev/guide/ui)
- [Animations Guide](https://sli.dev/guide/animations)
- [Theme & Addons Guide](https://sli.dev/guide/theme-addon)
- [Component Guide](https://sli.dev/guide/component)
- [Layout Guide](https://sli.dev/guide/layout)
- [Exporting Guide](https://sli.dev/guide/exporting)
- [Hosting Guide](https://sli.dev/guide/hosting)
- [Build with PDF Feature](https://sli.dev/features/build-with-pdf)

---

## 1. Project Overview and Quick Start

- **Purpose:**  
  This repository uses [Slidev](https://sli.dev) to build interactive slideshows in Markdown with Vue-powered components. 

- **Key Commands:**  
  - **Install Dependencies:**  
    ```bash
    npm install
    ```  
    *(Uses the `package-lock.json` to lock versions.)*
    
  - **Start the Development Server:**  
    ```bash
    npm run dev &
    ```  
    *(Launches Slidev's hot-reload server in the background, allowing you to continue using the terminal.)*
    
  - **Build for Production:**  
    ```bash
    npm run build
    ```  
    *(Generates optimized static files in the `dist` folder.)*
    
  - **Export the Slides:**  
    ```bash
    npm run export
    ```  
    *(Exports the presentation as a sharable PDF.)*

---

## 2. Project Structure

- **`slides.md`**  
  The main Markdown file where slides are created using Slidev-specific frontmatter and syntax.  
  _Example:_  
  ```markdown
  ---
  theme: seriph
  background: https://source.unsplash.com/collection/94734566/1920x1080
  info: |
    ## Slidev Starter Template
    Learn more at [Sli.dev](https://sli.dev)
  ---
  
  # Welcome to Slidev
  Presentation slides for developers.
  ```

- **`components/Counter.vue`**  
  This folder contains example components provided as references (for instance, `Counter.vue`). These components serve purely as examples/demonstrations. Memex should primarily focus on making improvements or changes to the overall project based on user instructions, and only modify these sample components if explicitly requested.
  _Example snippet:_  
  ```vue
  <script setup lang="ts">
  import { ref } from 'vue'
  
  const props = defineProps({
    count: { default: 0 },
  })
  
  const counter = ref(props.count)
  </script>
  
  <template>
    <div class="flex w-min border border-gray-400 opacity-50 rounded-md">
      <button class="border-r border-gray-400 p-2 font-mono hover:bg-gray-400 hover:opacity-20" @click="counter -= 1">
        -
      </button>
      <span class="m-auto p-2">{{ counter }}</span>
      <button class="border-l border-gray-400 p-2 font-mono hover:bg-gray-400 hover:opacity-20" @click="counter += 1">
        +
      </button>
    </div>
  </template>
  ```

- **`.gitignore`**  
  Prevents tracking of generated files and folders.  
  _Excerpt:_  
  ```
  dist
  node_modules
  data/*
  !data/.gitkeep
  ```

- **`package.json` and `package-lock.json`**  
  Define dependencies and scripts such as `dev`, `build`, and `export`. The dependencies include the latest versions of `@slidev/cli`, `@slidev/theme-default`, and `@slidev/theme-seriph`.

- **Additional Files:**  
  Refer to the [README.md](./README.md) for a comprehensive project overview and usage instructions.

---

## 3. AI Interaction Guidelines

1. **Maintain Context and Comments:**  
   - Preserve existing inline comments unless they require correction.  
   - Maintain the file structure and naming conventions.

2. **Provide Inline Examples:**  
   When suggesting edits, show updated code in context using inline code blocks with proper file path annotations. For example:  
   ```vue:components/Counter.vue
   // Updated snippet here...
   ```

3. **Reference Documentation:**  
   Leverage the following Slidev resources to guide your changes:
   - [General Guide](https://sli.dev/guide/)
   - [Markdown Syntax Extensions](https://sli.dev/guide/syntax)
   - [Interactive UI Components](https://sli.dev/guide/ui) and [Animations](https://sli.dev/guide/animations)
   - [Themes and Addons](https://sli.dev/guide/theme-addon)
   - [Exporting Slides](https://sli.dev/guide/exporting) and [Building/Hosting](https://sli.dev/guide/hosting)
   - [Generating PDFs During Build](https://sli.dev/features/build-with-pdf)

4. **Quality and Consistency:**  
   - Ensure that every change is production-ready and adheres to the project's coding style.
   - Test changes using `npm run dev` to verify functionality interactively.

5. **Enhance Interactivity Thoughtfully:**  
   Use interactive components (e.g., `<Counter :count="10" />`) and motion or theme customizations as demonstrated in the `slides.md`. Your suggestions should enhance the user experience while keeping the project aligned with Slidev's documented standards.

---

## 4. Best Practices

- **Documentation:**  
  Update documentation and inline comments to reflect any code changes.
  
- **Consistent Styling:**  
  Follow the styles defined by UnoCSS and the theme settings in `slides.md`.
  
- **Testing:**  
  Verify your changes in development mode before proposing production builds.
  
- **Deployment:**  
  Keep in line with the instructions in the [Hosting Guide](https://sli.dev/guide/hosting) to ensure that any build or export modifications are correctly deployed.

---

## Summary

By following these AI interaction guidelines and referencing the [Slidev documentation](https://sli.dev/guide/), contributions will be consistent, clear, and maintain the high quality expected for interactive developer-friendly presentations. Happy coding and enhancing your slides!