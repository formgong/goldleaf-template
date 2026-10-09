# Goldleaf: an interior design and architecture studio site with a Formgong form

**Live demo:** https://goldleaf.formgong.com · Download: the [latest release](https://github.com/formgong/goldleaf-template/releases/latest) zip.

[![Deploy to Cloudflare](https://deploy.workers.cloudflare.com/button)](https://deploy.workers.cloudflare.com/?url=https://github.com/formgong/goldleaf-template) [![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fformgong%2Fgoldleaf-template&project-name=goldleaf&repository-name=goldleaf)

Each button copies the site to your GitHub and publishes it. Then replace every `fk_your_access_key` in `index.html` of your copy with your Formgong access key (free at https://formgong.com/new) and commit: the host republishes on its own.

Сайт студії дизайну й архітектури з формою Формгонг

A one-page template for an interior design or architecture studio that sells fixed-price services, in a single `index.html`. The demo studio, Goldleaf, its prices, address and reviews are fictional.

- **Grid.** Thin lines divide the page into three columns between two side margins. Every block sits on the same lines.
- **Header.** The wordmark, the menu, a round "call us" badge that turns slowly, the phone number and messenger links.
- **Hero.** Spaced lines "Design / architecture / decorating" and the wordmark, whose bar is the "l" of both words. A bouncing arrow sits beside a drawn plant and two open blue doors that show a photo of a hallway. The doors and plant are SVG line art you can recolour.
- **Running line.** A black band with "Design project – $99" moving slowly across.
- **Service cards.** Nine cards in pink, cream, blue and white, each with a serif title, a short text or list, and a large pill button.
- **Client reviews from Formgong.** A rating block and a review card that changes every 6 seconds, with dots to pick one. A "Leave a review" button opens a form with 1–5 stars, a name and the review text. Once you approve reviews in Formgong (Dashboard → Reviews), they replace the sample reviews, together with the real average and count.
- **Footer.** A dark footer with the address, contacts and messenger icons. On phones, a sticky bar keeps "Write to us" at hand.

Every button ("Sample", "Learn more", "Start drawing", the call badge and "Write to us") opens one "Write to us" window. It fills the topic in for the visitor and sends it as a hidden `topic` field.

## English

**Set up the form**

1. Create a form in the Formgong dashboard and copy its access key.
2. In `index.html`, replace every `fk_your_access_key` with that key (the write-to-us form and the review form).
3. The form sends `name`, `phone`, `email`, `message` and `topic`. It shows thanks only when Formgong answers `success: true`. If the answer is anything else, it shows the error and keeps what was typed.

**Reviews**

1. In the Formgong dashboard, open Reviews (https://formgong.com/dashboard/reviews) and turn reviews on for a form. It can be the same form as the one above, or a separate one. You approve or hide each review there.
2. Put that form's access key in the review form (`<form id="f-review">`). If you use one form for everything, it is already there after find and replace.
3. A submission with a `rating` from 1 to 5 becomes a pending review. When you approve it, the slider loads it from `https://formgong.com/reviews/<your key>.json` and shows the real average and count. Until then the five sample reviews stay, so replace or delete them before you launch.

**Edit**

- Colours are at the top of the styles: `--bg` for the page, `--pink`, `--sky` and `--white` for the cards, `--door` for the doors, and `--blue` for the wordmark.
- The side margins are `--m`. The three middle columns share the rest of the width.
- To change the running line, edit the text of the two `[data-run]` paragraphs. The script repeats it.
- Point the messenger links (Viber, Telegram, WhatsApp, Instagram) at your accounts.

**Image.** The hallway photo was generated for this template with ChatGPT image generation (OpenAI) and saved as WebP (43 KB). The doors, plant and icons are drawn in SVG. You may use them in your own site.

## Українська

Односторінковий шаблон для студії дизайну інтер'єру чи архітектури з послугами за фіксованою ціною. Студія Goldleaf, ціни, адреса й відгуки вигадані.

На сторінці:

- сітка з тонких ліній;
- шапка з бейджем «call us», що обертається;
- перший екран з логотипом, рослиною і блакитними дверима, намальованими в SVG, з фото коридору всередині;
- чорна стрічка з текстом, що біжить;
- дев'ять кольорових карток послуг із кнопками-«пігулками»;
- відгуки з Formgong, що змінюються кожні 6 секунд: відвідувач залишає відгук із зірками, ви схвалюєте його в кабінеті, і він з'являється замість прикладів разом зі справжнім середнім балом;
- темний футер.

Усі кнопки відкривають одне вікно «Write to us» з уже вписаною темою.

**Налаштування.** Створіть форму в кабінеті Formgong і замініть `fk_your_access_key` у `index.html` на свій ключ. Подяка з'являється лише тоді, коли Formgong відповідає `success: true`.

MIT license.
