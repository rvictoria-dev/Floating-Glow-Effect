# Floating Glow Effect

### ₊⊹ About

A pure HTML and CSS button effect featuring a vibrant, neon-like rainbow glow on hover. The animation uses a blurred, gradient-shifting pseudo-element layered behind the button to achieve a dynamic pulsing border. 

https://github.com/user-attachments/assets/6b7a9efd-e32b-43a8-aec4-2c74a9c5ed6e

---

### ★ Features

- **Pure CSS Architecture:** Built entirely using semantic HTML5 and CSS3, eliminating the need for JavaScript or external libraries.
- **Dynamic Hover Effect:** Triggers a smooth, 3-second fade-in transition (`opacity: 1`) revealing a vibrant multi-color gradient border on hover.
- **Fluid Shifting Animation:** Utilizes a custom `@keyframes` animation that seamlessly loops a 400% scaled gradient backdrop horizontally for a fluid, liquid-like motion.
- **Layered Pseudo-Elements:** Leverages a precise `:before` and `:after` structural stacking context (`z-index`) to isolate the blur effect (`filter: blur(5px)`) safely behind the button surface.
- **Tactile Click Feedback:** Implements a reactive `:active` state that smoothly inverts text color to black for immediate visual confirmation upon user click.
- **Responsive Layout Alignment:** Designed using CSS Flexbox on the parent container to guarantee perfect centering on any screen size.

---

### ⚙️ Tech Stack

- **HTML5**
- **CSS3**

---

### 🖿 Project structure

```
floating-glow-effect/
├── index.html
├── style.css
└── README.md
```

---

### .ᐟ.ᐟ How It Works

1. **The Top Layer (The Text)**
* **What it is:** The actual `<button>` element itself (`z-index: 0`).
* **The Mechanics:** It holds the interactive text surface. When clicked (`:active`), the text dynamically shifts from white to black to trigger a tactile, satisfying click response.

2. **The Middle Layer (The Shield)**
* **What it is:** The `:after` pseudo-element.
* **The Mechanics:** Positioned immediately behind the text (`z-index: -1`) with a solid dark background (`#111`). This layer acts as a visual shield. It hides the chaotic rainbow gradient moving directly underneath it, ensuring only the outer edges are exposed.

3. **The Bottom Layer (The Rainbow Glow)**
* **What it is:** The `:before` pseudo-element.
* **The Mechanics:** This is where the magic happens. It is sized slightly larger than the button using `calc(100% + 4px)` and offset by `-2px`.
* **The Animation:** It holds a huge, 400%-scaled multi-color `linear-gradient` that continuously shifts horizontally via a `@keyframes` animation loop.
* **The Glow Effect:** By applying `filter: blur(5px)`, the harsh edges of the moving gradient soften into a smooth, vibrant neon glow radiating outward from behind the button.
 **The Interaction:** On `:hover`, this layer seamlessly transitions from `opacity: 0` to `opacity: 1` over 3 seconds, fading the active engine into view.
