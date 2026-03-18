# КПДІ PWA

Progressive Web App для Кам'янець-Подільського державного інституту.

## Можливості

- **Розклад дзвінків** — живий годинник, поточна пара з прогрес-баром, дві зміни (Коледж / Інститут)
- **Moodle** — швидкий перехід до навчальної платформи
- **Їдальня** — демо-меню по днях тижня + підключення Google Таблиці
- **Контакти** — картки з tap-діями (карта, дзвінок, email) + форма зворотного зв'язку
- **PWA** — встановлюється на Android та iOS, працює офлайн

## Структура

```
├── index.html        # SPA (React 18 via CDN, без збірки)
├── manifest.json     # PWA manifest
├── sw.js             # Service Worker (cache-first / network-first)
├── icons/            # Іконки 192×192 та 512×512
├── .nojekyll         # Для GitHub Pages
└── .github/workflows/deploy.yml  # Автодеплой
```

## Деплой

1. Запушити репозиторій на GitHub
2. Settings → Pages → Source: **GitHub Actions**
3. Перший пуш у `main` запустить workflow — сайт з'явиться за хвилину

## Розробка

Відкрийте `index.html` у браузері. Немає npm, немає збірки — просто файли.

> Service Worker потребує HTTPS або `localhost`. Для локального тестування PWA-функцій використовуйте `python3 -m http.server 8080`.
