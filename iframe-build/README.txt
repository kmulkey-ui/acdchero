NOLA Skyline Shader — iframe build
====================================

Folder contents:
  index.html            the shader page (loads parallel assets, no unpacking splash)
  assets/               skyline + logo images referenced by index.html

Deploy
------
1. Upload this entire folder to a static host. Easy options:
     • Netlify Drop   https://app.netlify.com/drop   (drag the folder in)
     • Cloudflare Pages
     • GitHub Pages
   You'll get a public URL like https://your-site.netlify.app/
2. In vFairs, add a Custom HTML / iframe widget to the hero section with:

     <iframe
       src="https://YOUR-HOST/index.html"
       style="display:block;border:0;width:100%;height:100vh;"
       allow="fullscreen"
       loading="eager"
       title="ACDC 2026">
     </iframe>

   Adjust the height to taste — 60vh / 80vh / 100vh all work.

Notes
-----
• Tweaks panel is hidden by default on a public page. If you want it visible,
  open index.html and search for `class="tweaks"` — change it to `class="tweaks on"`.
• All interactivity (mouse = sun, click = lightning) works inside the iframe.
• No external fonts / CDNs are loaded; the page is fully self-contained
  once the 4 files are hosted together.
