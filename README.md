# 🌳 Linktree Clone

<p align="center">
  <img src="public/favicon.svg" alt="Linktree Logo" width="200">
</p>

A modern, customizable Linktree alternative built with Vue 3 and TypeScript. Features a clean design with dark/light mode support.

## ✨ Features

- 🎨 Light/Dark mode toggle
- 📱 Fully responsive design
- 🔗 Customizable social links
- 🎯 SEO friendly
- ⚡ Fast and lightweight
- 🛠️ Easy to customize

## 🚀 Technologies

- ![Vue.js](https://img.shields.io/badge/Vue.js-3-4FC08D?style=flat&logo=vue.js)
- ![TypeScript](https://img.shields.io/badge/TypeScript-4-3178C6?style=flat&logo=typescript)
- ![Vite](https://img.shields.io/badge/Vite-5-646CFF?style=flat&logo=vite)
- ![Bootstrap](https://img.shields.io/badge/Bootstrap-5-7952B3?style=flat&logo=bootstrap)
- ![Font Awesome](https://img.shields.io/badge/Font_Awesome-6-528DD7?style=flat&logo=fontawesome)

## 🛠️ Setup & Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/linktree-clone.git
```

2. Install dependencies:
```bash
npm install
```

3. Run development server:
```bash
npm run dev
```

4. Build for production:
```bash
npm run build
```

## 🔧 Configuration

Edit links in `src/config/links.ts` to customize your social links:

```typescript
export const links: Link[] = [
  {
    name: "Portfolio",
    url: "https://yourwebsite.com",
    icon: "globe"
  },
  // Add more links...
];
```

## 📝 License

MIT License © [Your Name]

---
<p align="center">
  Made with ❤️ by Ednei Trabach
</p>
