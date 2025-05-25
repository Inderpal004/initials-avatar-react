# 🧑‍🎨 react-username-avatar

A lightweight React component that generates a circular avatar with user initials and customizable background colors. Ideal for apps that need user identification when profile images are missing.

![React Username Avatar Demo](./demo.png)

---

## ✨ Features

- 🟣 Generates initials from full name
- 🎨 Deterministic background colors (custom or default)
- ⚙️ Fully customizable size and colors
- 💡 No dependencies other than React

---

## 📦 Installation

```bash
npm i initials-avatar-react
# or
yarn add initials-avatar-react


## 🚀 Usage

### 🧱 Basic Example

```jsx
import ReactAvatar from 'initials-avatar-react';

function App() {
  return (
    <div>
      <ReactAvatar name="Inderpal Singh" />
    </div>
  );
}
````

This will render a circular avatar showing `IS` with a default size of `50px` and an auto-selected background color.

---

### ⚙️ With Custom Props

```jsx
<ReactAvatar 
  name="Alice Bob" 
  size={80} 
  textColor="#000" 
  customColors={['#FF6F61', '#6B5B95', '#88B04B']} 
/>
```

This will:

* Show initials `AB`
* Set avatar size to `80px × 80px`
* Use black (`#000`) text
* Pull background color from your `customColors` array

---

### 📌 Props Reference

| Prop           | Type       | Default        | Required | Description                             |
| -------------- | ---------- | -------------- | -------- | --------------------------------------- |
| `name`         | `string`   | —              | ✅        | Full name used to generate initials     |
| `size`         | `number`   | `50`           | ❌        | Diameter of avatar in pixels            |
| `textColor`    | `string`   | `"#fff"`       | ❌        | Initials text color                     |
| `customColors` | `string[]` | Predefined set | ❌        | Custom array of background colors (hex) |

---

### ✅ Best Practices

* Always pass a **non-empty `name`** — it's required to generate initials.
* Keep `size` above `30` for readability.
* For consistent branding, use a fixed `customColors` array across your app.

---

### ⛔ Example of Bad Usage (missing name)

```jsx
<ReactAvatar /> // 🔴 Won’t render initials
```

Always pass a name string!
