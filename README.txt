E-LIQUID // MIX.CORE – PWA
==========================

OBSAH SLOŽKY
  index.html              aplikace (výpočet, UI)
  app.css                 předkompilovaný Tailwind (žádné CDN)
  sw.js                   service worker – offline režim
  manifest.webmanifest    název, ikony a barvy instalované aplikace
  icons/                  ikony pro Android, iOS a prohlížeč

JAK APLIKACI ZPROVOZNIT
  PWA musí běžet z webu přes HTTPS. Otevřený soubor z disku (file://) se jako aplikace nainstalovat nedá.
  Nejrychlejší možnosti zdarma:
    • Netlify Drop (app.netlify.com/drop): přetáhni celou tuto složku do okna, během chvilky dostaneš adresu.
    • GitHub Pages / Cloudflare Pages: nahraj obsah složky do repozitáře a zapni Pages.
  Všechny soubory musí zůstat ve stejné struktuře vedle sebe.

INSTALACE DO TELEFONU
  Android (Chrome): otevři adresu, klepni na tlačítko „↓ Instalovat“ v hlavičce,
                    nebo v menu ⋮ zvol „Přidat na plochu / Instalovat aplikaci“.
  iPhone (Safari):  otevři adresu, klepni na Sdílet ⬆ a zvol „Přidat na plochu“.

OFFLINE
  Po prvním otevření s internetem se aplikace uloží do telefonu a dál funguje i bez připojení.
  Písma (Chakra Petch, JetBrains Mono) se stahují z Google Fonts při prvním spuštění a pak se drží v cache.
  Bez nich aplikace funguje stejně, jen se zobrazí systémovým písmem.

AKTUALIZACE
  Když upravíš soubory, zvyš v sw.js hodnotu VERSION (např. 'mixcore-v2'),
  aby si telefony stáhly novou verzi. Projeví se při druhém otevření aplikace.
  Pokud do index.html přidáš nové Tailwind třídy, je potřeba znovu vygenerovat app.css.
