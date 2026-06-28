# Nelluvellil Curtains — Online Store

A complete, ready-to-use online store with a customer-facing shop and an admin
panel to manage products and view orders.

## 📁 Files
```
nelluvellil-store/
├── index.html        → Customer storefront
├── admin.html        → Admin panel (products + orders)
├── css/
│   ├── style.css      → Storefront styling
│   └── admin.css      → Admin panel styling
├── js/
│   ├── products.js     → Default product catalog (edit to change starting products)
│   ├── store.js         → Data layer (cart, products, orders)
│   ├── app.js            → Storefront behaviour
│   └── admin.js          → Admin panel behaviour
```

## 🚀 How to use
1. Unzip the folder.
2. Open `index.html` in any browser — that's your live store.
3. Open `admin.html` to log in to the admin panel.
   - Default password: `admin123`
   - **Change this** in `js/admin.js` (line: `const ADMIN_PASSWORD = "admin123"`)

To put it online, upload the whole folder to any web host (e.g. Netlify,
GitHub Pages, Hostinger, etc.) — no server setup required, it's plain HTML/CSS/JS.

## 🛍️ Adding / removing products
Two ways:

**Option A — Admin Panel (recommended, no coding):**
- Go to `admin.html` → Products tab
- Click "+ Add Product" to add a new curtain (name, price, category, image, stock status)
- Click "Edit" or "Delete" on any row to update/remove products
- Changes are saved automatically and reflected instantly on the storefront

**Option B — Edit the code (sets the default catalog for all visitors):**
- Open `js/products.js`
- Add/remove items in the `DEFAULT_PRODUCTS` array following the existing format

## 📦 Viewing customer orders
- Go to `admin.html` → Orders tab
- Every order placed on the storefront (name, phone, address, items, total) appears here
- Update order status: Pending → Processing → Shipped → Delivered (or Cancelled)
- "Overview" tab shows total orders, revenue, pending orders, and product count

## 🎨 Customizing the look
- Colors/fonts: edit the `:root` variables at the top of `css/style.css`
- Logo text, hero text, contact info, about section: edit directly in `index.html`
- Categories: edit the filter buttons in `index.html` and the `<select>` in
  `admin.html`'s product form to match (`living-room`, `bedroom`, `door`, `sheer`)

## ⚠️ Important note on data storage
This store uses the browser's `localStorage` to save products, cart, and
orders — meaning data is stored per-browser/device, with no server needed.
This is great for a demo, a small local business, or testing. For a larger
production store (multiple staff viewing the same orders, payment gateway
integration, etc.) you would connect this front-end to a real backend
database — let me know if you'd like help with that next step.
