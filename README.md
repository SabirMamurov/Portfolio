# Портфолио — Сабир Мамуров

Премиальный двуязычный (RU/EN) сайт-портфолио. Один самодостаточный файл `index.html` (стили, скрипты и данные внутри), шрифты — с Google Fonts.

## Локальный запуск

```bash
node server.js
# → http://localhost:4321
```

`server.js` нужен только для локального просмотра — на хостинг он не идёт (см. `.vercelignore`).

## Деплой на Vercel

1. **Создать репозиторий на GitHub** (пустой, без README), например `portfolio`.
2. **Привязать и запушить** (из папки проекта):
   ```bash
   git remote add origin https://github.com/<username>/portfolio.git
   git branch -M main
   git push -u origin main
   ```
3. **Импорт в Vercel:** [vercel.com/new](https://vercel.com/new) → Import репозиторий → Framework Preset: **Other** → Deploy.
4. Готово — сайт на `https://<project>.vercel.app`. Каждый `git push` в `main` обновляет сайт автоматически.

### Как обновлять сайт

```bash
git add -A
git commit -m "update"
git push
```

## Правки контента

- Тексты и кейсы — в объектах `I18N`, `SERVICES`, `PROJECTS`, `STACK`, `FLOW` внутри `<script>` в `index.html`.
- Telegram — константа `TG_HANDLE` в конце `<script>`.
