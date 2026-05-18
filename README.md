# Стамат Фитнес – Landing Page

Целева страница за безплатна индивидуална фитнес консултация.

## Структура
```
stamat-fitness/
├── index.html       ← целият сайт (снимката е вградена)
└── README.md
```

## Публикуване в GitHub Pages

1. Отвори терминал в VS Code (Ctrl + `)
2. Изпълни:
```bash
git init
git add .
git commit -m "Initial commit"
git remote add origin https://github.com/ТВОЯ_АКАУНТ/stamat-fitness.git
git push -u origin main
```
3. GitHub → Settings → Pages → Source: main / root → Save
4. Сайтът ще е на: https://ТВОЯ_АКАУНТ.github.io/stamat-fitness/

## Formspree (за получаване на имейли от формата)

1. Регистрирай се на https://formspree.io
2. Създай нова форма → копирай endpoint URL-а
3. В index.html намери коментара "Вариант 1: Formspree" и замени с:
```javascript
const res = await fetch('https://formspree.io/f/ТВОЯ_КОД', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({ name, phone, email, notes })
});
if (res.ok) { /* покажи success */ }
```
