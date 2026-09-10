# STAR PAINTING WORKS — Single-Page Application (SPA)

Production-ready, responsive single-page application for **Star Painting Works** (Terdal), built for static hosting on **GitHub Pages** with **Supabase** database, authentication, and storage integration.

- **Live Website**: [https://tousifmahalingpur.github.io/star-painting-works/](https://tousifmahalingpur.github.io/star-painting-works/)
- **GitHub Repository**: [https://github.com/tousifmahalingpur/star-painting-works](https://github.com/tousifmahalingpur/star-painting-works)

---

## Features

- **Industrial Mechanical Aesthetic**: High-contrast Black, White, and Sky Blue theme (`#7dd3fc`, `#38bdf8`) with metallic panels and subtle scanline/grid textures.
- **Bilingual System (English & Kannada)**:
  - First-visit friendly language prompt modal.
  - Persistent preference in `localStorage` (`spw_language`).
  - Seamless header toggle (`EN | ಕನ್ನಡ`).
  - Natural automotive Kannada translations.
- **Interactive Before / After Comparison Slider**:
  - Accessible touch, mouse, and keyboard (Arrow keys) dragging.
  - Smooth sky-blue divider and handle.
- **Dynamic Portfolio & Live Shop Floor Log**:
  - Direct video playback (`mp4`, `webm`, `ogg`, `mov`, `m4v`).
  - Automatic YouTube & Vimeo video embeds.
  - Color-coded status badges (`IN QUEUE`, `IN PAINT BOOTH`, `IN REPAIR`, `COMPLETED`).
- **Admin Panel ("GARAGE OPS")**:
  - Single-page client-side switching (no page reload).
  - Secure email/password authentication using Supabase Auth.
  - Garage profile editor with live customer view synchronization.
  - Daily log publisher with direct media upload and URL fallback.
  - Portfolio manager with file upload and live delete capability.
- **Supabase Storage Integration**:
  - Direct upload to the `garage-media` bucket (folders: `portfolio/`, `feed/`).
  - 50MB file size limit with MIME validation.

---

## 1. Supabase Setup

1. Create a project at [supabase.com](https://supabase.com).
2. Open the **SQL Editor** in your Supabase project and execute `supabase-schema.sql`.
3. Create an admin user under **Authentication → Users** (e.g. `admin@starpainting.com`).
4. In **Storage**, create a new public bucket named:
   ```
   garage-media
   ```
   Ensure the bucket has public read access so uploaded images and videos can be rendered on the website.
5. In `index.html`, verify the `ENV` configuration:
   ```javascript
   const ENV = {
     SUPABASE_URL: "https://iuuyhzipcocceqdjlwbf.supabase.co",
     SUPABASE_ANON_KEY: "sb_publishable_4MV30zVNCTPvnbUG47tikg_DSGEbMbd"
   };
   ```
   > **Note**: Only the frontend publishable/anon key is used. Never include your `service_role` secret key in client-side code.

---

## 2. GitHub Pages Deployment

1. Commit and push `index.html` and `supabase-schema.sql` to your GitHub repository.
2. In your GitHub repository, navigate to **Settings → Pages**.
3. Under **Build and deployment → Source**, select **Deploy from a branch**.
4. Choose branch `main` (or `master`) and directory `/ (root)`.
5. Click **Save**. GitHub Pages will deploy your site at `https://<username>.github.io/<repo-name>/`.

---

## 3. Local Development

To run and test locally with an HTTP server:

```bash
# Python 3
python -m http.server 8080

# Or Node.js http-server
npx http-server -p 8080
```

Open `http://localhost:8080` in your browser.

---

## 4. Garage Details

- **Garage**: Star Painting Works
- **Location**: Rabkavi-Banahatti Road, Infront of SDM Trust's Danigond College of Commerce, Terdal
- **Plus Code / Maps**: `F3R6+2PM SDM Trust's Danigond College of Commerce (PU & B.com), Terdal, Karnataka 587315`
- **Owner**: Mujammil Jamadar
- **Phone / WhatsApp**: +91 88674 42645
- **Email**: jamadarmujammil9@gmail.com
- **Opening Hours**: 9:00 AM — 8:00 PM
