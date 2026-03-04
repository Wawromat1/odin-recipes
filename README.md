# odin-recipes

Odin Recipes is a small static HTML website that contains a landing page and three recipe pages. The primary objective of the repository is to practice core HTML fundamentals in a clean, professional project structure. The focus is on building multiple pages, structuring readable content, using correct relative links, and separating assets from documents in a way that scales when the project grows.

The entry point of the site is index.html in the project root. From there, users can navigate to three recipe pages located in the recipes folder: Pizza.html, Kaiserschmarrn.html, and Popcornchicken.html. Each recipe page is a standalone HTML document with a consistent content layout. The recipe pages include a clear page title, a header image, a short description, an ingredients section, an instructions section, and a link back to the landing page. This structure is intentionally repetitive to build muscle memory and ensure the pages remain consistent as more recipes are added.

The repository uses a simple directory layout that keeps the root directory clean and groups related content together. All recipe pages live under the recipes folder, and all images are stored under recipes/images. This reduces clutter, makes the file system predictable, and supports future expansion without needing to restructure the project later.

Folder structure

.
├── index.html
├── recipes/
│   ├── Kaiserschmarrn.html
│   ├── Popcornchicken.html
│   └── Pizza.html
└── recipes/images/
    ├── Kaiserschmarrn_headingImg.jpeg
    ├── Popcornchicken_headingImg.jpeg
    └── Pizza_headingImg.jpeg

Navigation is implemented through relative paths. The landing page links to the recipe pages inside the recipes folder, and each recipe page links back to the landing page using a parent-directory reference. This is the key concept being practiced: controlling navigation with correct relative linking instead of hard-coded absolute URLs. Images are also loaded via relative paths. Since the recipe HTML files and the images folder are both located inside recipes, each recipe page can reference its header image through a short and consistent path that points into the images directory.

Running the project locally requires no installation steps, build process, or dependencies. The site can be opened by loading index.html in a browser and navigating through the links. Because it is a static site, the behavior is deterministic and easy to validate; if links or images fail to load, it usually indicates an incorrect relative path or a mismatch between file name and reference.

The project is designed to be extended. Adding a new recipe follows the same operating model: create a new HTML file under recipes, add its image to recipes/images, and include a link from index.html to the new page. Keeping naming consistent and preserving the same page structure ensures the repository stays maintainable and easy to understand for anyone reviewing it later.