# The Rustique Restaurant — Exodus Dining (Nuwara Eliya, Sri Lanka)

A bespoke, single-file boutique website crafted for **The Rustique Restaurant — Exodus Dining**, an intimate four-table sanctuary tucked into the misty hills of Nuwara Eliya, Sri Lanka, serving authentic mom’s home-cooked breakfasts, lunches, and dinners.

---

## ✨ Overview & Design Philosophy

Built around a warm highland aesthetic of **antique linen (`#FCF8F0`)**, **deep roasted espresso (`#1A100B`)**, and **satin champagne brass (`#B89455`)**, the site pairs editorial typography (`Cormorant Garamond` & `Plus Jakarta Sans`) with lightweight interactive features—requiring zero build steps or backend servers.

### Key Highlights
* **Scroll-Reveal Sticky Header:** Keeps the top bar clean over the hero stage, smoothly revealing the circular crest emblem and brand title once the guest scrolls down.
* **Cinematic Hero Stage:** Features a soft-focus zoom entrance, subtle lantern glow, golden light sweep, floating bokeh sparkles, and an enlarged circular emblem badge.
* **Live Nuwara Eliya Telemetry & Weather:**
  * Real-time **Sri Lanka Standard Time (`Asia/Colombo`)** clock and live seating status banner (Breakfast, Lunch, or Dinner).
  * Live mountain weather conditions fetched directly from the **Open-Meteo API** (`6.9497° N, 80.7891° E`) displaying temperature, humidity, wind speed, precipitation, and rain probability.
* **Mom’s Home-Cooked Kitchen Philosophy:** Explains how daily menus are crafted from scratch around fresh Nuwara Eliya harvest and shared personally via WhatsApp or email rather than a rigid commercial menu.
* **Exodus in Motion & Interior Gallery:** Includes a cinematic video showcase (`GKWKE3340.mp4`) and a 5-photo interior gallery with a full-screen keyboard-accessible lightbox (`Esc`, `←`, `→`).
* **Ambient Highland Soundscape:** Built-in **Web Audio API** sound synthesizer generating gentle highland rain and mountain breeze audio with live volume control (silent until user interaction).
* **Dedicated `#reserve` Concierge View:** Instant hash-routed enquiry builder that formats a live preview card and dispatches directly to **WhatsApp (`+94 70 298 6611`)**, **Email (`reservations@therustiquerestaurant.com`)**, or clipboard copy.

---

## 📁 Project Structure & Required Media Assets

Because the entire application runs out of a single self-contained HTML file (`index.html`), keep all media assets in the **same root directory** with exact case-sensitive filenames:

```text
/
├── index.html               # Complete single-file website (HTML, CSS, Tailwind CDN, JS)
├── README.md                # Project documentation
├── image_ba9726.png         # Primary circular crest emblem (Hero & Sticky Header)
├── IMG_3964_beb93e.jpeg     # Favicon & fallback emblem asset
├── IMG_8895_beb93e.jpg      # Hero backdrop, video poster, Open Graph preview & gallery item
├── IMG_8896_beb93e.jpg      # Interior gallery: Mirrored shelves & woven rattan pendant
├── IMG_8892_beb93e.jpg      # Interior gallery: Slatted timber partition & crochet lace linen
├── IMG_8893_beb93e.jpg      # Interior gallery: Inner alcove teak tables & French doors
├── IMG_8894_beb93e.jpg      # Interior gallery: Warm evening sanctuary ambience
├── GKWKE3340.mp4            # Brand film (MP4 format)
└── GKWKE3340.MOV            # Brand film fallback (QuickTime format)
```

> **Note on Case Sensitivity:** Linux-based web servers (such as GitHub Pages, Netlify, Vercel, and cPanel hosts) are case-sensitive. Ensure uppercase extensions (`.JPG`, `.MOV`) vs. lowercase extensions (`.png`, `.jpg`, `.jpeg`, `.mp4`) match the filenames listed above.

---

## 🕰️ Service Hours & Concierge Contacts

* **Location:** Nuwara Eliya, Central Province, Sri Lanka (`1,868 m` elevation)
* **Capacity:** Four intimate tables only
* **Daily Seatings:**
  * **Highland Breakfast:** `7:30 AM – 10:30 AM`
  * **Highland Lunch:** `12:00 PM – 3:00 PM`
  * **Boutique Dinner:** `6:30 PM – 10:00 PM`
* **WhatsApp Availability Desk:** `+94 70 298 6611`
* **Reservations Email:** `reservations@therustiquerestaurant.com`

---

## 🚀 Local Preview & Deployment

### Running Locally
No Node.js, npm, or bundler installation is required:
1. Place `index.html` and all image/video files in a single folder.
2. Open `index.html` directly in any modern browser, or run a lightweight local server (e.g., VS Code **Live Server** or `python3 -m http.server 8080`).

### Deploying to Production
1. Upload `index.html` along with all media files in the root folder to your static web host (**GitHub Pages**, **Cloudflare Pages**, **Netlify**, **Vercel**, or standard shared hosting).
2. Ensure HTTPS is enabled so the Open-Meteo weather API and Web Audio API run without mixed-content restrictions.
3. Update the `og:url`, `og:image`, and JSON-LD `url` fields in `<head>` if you point a custom domain to the deployment.

---

## 🛠️ Customization Quick Reference

* **WhatsApp Phone Number:** Update `const WHATSAPP_NUMBER = '94702986611';` in the `<script>` block (international format without `+` or spaces).
* **Reservations Email:** Update `const RESERVATIONS_EMAIL = 'reservations@therustiquerestaurant.com';` in the `<script>` block and the `mailto:` links in the header, location section, and footer.
* **Weather Coordinates:** Configured in `loadHighlandWeather()` using Nuwara Eliya coordinates (`latitude=6.9497&longitude=80.7891`, `timezone=Asia/Colombo`).