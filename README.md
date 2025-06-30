## 🌙 Dark Mode Toggle with React & Tailwind CSS

In this project, I implemented a smooth and responsive **Dark Mode feature** using **React** and **Tailwind CSS**. The goal was to offer users a modern, visually pleasing interface that adapts to their theme preference in real time.

---

### 🛠️ How It Works

Tailwind CSS handles dark mode styling using the `dark:` variant. I configured Tailwind to use the **class-based strategy**, which toggles the `dark` class on the `<html>` element.

- **React State**: I used `useState` and `useContext` to manage the theme globally.
- **Theme Toggle**: A simple toggle switch updates the theme state and applies the `dark` class to the root.
- **Tailwind Integration**: Components use conditional classes like `bg-white dark:bg-gray-900` to apply styles based on the current theme.

---

### 🧠 Behind the Scenes

```js
useEffect(() => {
  document.querySelector('html').classList.remove('light', 'dark')
  document.querySelector('html').classList.add(theme)
}, [theme])

