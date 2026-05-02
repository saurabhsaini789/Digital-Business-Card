# Digital Business Card

A minimal, ultra-fast, mobile-first digital business card designed to be accessed via QR code.

## Key Features
- **Ultra-Lightweight**: No external libraries or frameworks. Pure HTML, CSS, and minimal JS.
- **Blazing Fast**: Uses inline CSS to avoid extra network requests and ensure instant rendering (target Lighthouse score: 99-100).
- **Mobile-First App Feel**: Fills exactly one screen height (`100dvh`), avoiding scrolling, and disables mobile tap highlights.
- **Native Dark Mode Support**: Automatically adapts to the user's system preferences using CSS variables.
- **Save to Contacts**: Includes a lightweight JS function to dynamically generate a `.vcf` file, allowing users to instantly save your contact details directly to their phonebook.

---

## 🛠️ How to Customize

All code is contained within the `index.html` file.

### 1. Update Profile Image
Find the `<img class="profile-img">` tag inside `index.html`.
Replace the `src` attribute with the path to your image.
*Pro-tip: Compress your image to WebP or JPEG format (under 50KB) and place it in the same folder as `index.html` (e.g., `<img src="profile.webp" alt="Profile">`).*

### 2. Update Personal Info
Search for the following classes inside the HTML and update the text:
- `<h1 class="name">Jane Doe</h1>` -> Change to your Full Name
- `<div class="title">Product Designer</div>` -> Change to your Title
- `<p class="value-prop">...</p>` -> Change to your 1-line value proposition
- `<div class="micro-proof">...</div>` -> Change to your micro-proof (e.g., "Shipped 10+ Apps")

### 3. Update Action Button Links
Find the `href="..."` attributes on the `<a>` tags in the HTML and replace them with your actual URLs:
- **Portfolio**: `href="https://yourportfolio.com"`
- **LinkedIn**: `href="https://linkedin.com/in/yourprofile"`
- **Email/WhatsApp**: For email, use `href="mailto:your@email.com"`. For WhatsApp, use `href="https://wa.me/YOUR_PHONE_NUMBER"` (e.g., `https://wa.me/1234567890`).

### 4. Update the "Save Contact" (vCard) Info
Scroll to the very bottom of `index.html` to the `<script>` section.
Update the `contact` object with your actual details. This is what will be saved to the user's phone when they tap "Save Contact":
```javascript
const contact = {
    firstName: "Jane",
    lastName: "Doe",
    phone: "+1234567890", // Important for Save Contact
    email: "hello@example.com",
    title: "Product Designer",
    url: "https://yourportfolio.com",
    linkedin: "https://linkedin.com/in/yourprofile"
};
```

---

## 🚀 How to Host on GitHub Pages (Free)

1. Create a GitHub account at [github.com](https://github.com) if you don't have one.
2. Create a new repository (e.g., `my-business-card`). Make sure it is set to **Public**.
3. Upload your customized `index.html` (and your profile image file, if you have one) to the repository.
4. Go to the repository **Settings** tab.
5. In the left sidebar, click on **Pages**.
6. Under the **Build and deployment** section, select **Deploy from a branch**.
7. Under the **Branch** dropdown, select `main` (or `master`) and leave the folder as `/ (root)`. Click **Save**.
8. Wait a couple of minutes, and GitHub will provide you with a live URL (e.g., `https://yourusername.github.io/my-business-card/`).
9. Generate a QR code using your new GitHub Pages URL and place it on your physical card or lock screen!
