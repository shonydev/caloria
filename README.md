# Caloria

> **🚀 Open the app:** https://shonydev.github.io/caloria/  
> Anyone can use it directly in the browser; no installation is required.

A tiny bilingual (Spanish/English), offline-first food diary PWA. It uses no framework, build step, backend, analytics, or paid API.

## Included

- Responsive layout suitable for mobile and desktop.
- Spanish and English interface.
- Photo picker/camera capture and on-device Food-101 dish classification (model downloaded on first use, about 93 MB).
- Sample food catalogue and editable portion sizes.
- Approximate calorie and macronutrient calculations.
- Food diary persisted in browser `localStorage`.
- Service worker for a basic offline app shell.
- GitHub Pages-ready static files.

## Photo recognition and nutrition limits

Use **Identify food with AI** after selecting a photo. The Food-101 model runs in the browser on your device; the first use downloads roughly 93 MB from Hugging Face, and needs an internet connection. The photo itself is not uploaded to a Caloria backend. It recognizes one dish from a fixed set of 101 categories, not every ingredient in a mixed plate. For some common dishes, Caloria selects a matching sample nutrition entry; confirm the food and portion before logging. This prototype does **not** reliably estimate serving weight, hidden ingredients, sauces, or oil from a photo, so calorie and macro values remain rough estimates.

## Run and deploy

No build command is required. Serve this directory from a static HTTPS host. The app is published with GitHub Actions at **https://shonydev.github.io/caloria/**. To redeploy, push changes to `main`; the workflow in `.github/workflows/pages.yml` publishes the static files. Open the HTTPS URL and use your browser's Add to Home Screen option to install it as a PWA.

## Privacy and limitations

- Food photos are processed in the browser and are not uploaded to a Caloria backend; the model files are downloaded from Hugging Face on first use.
- Diary entries are saved on this device in browser storage.
- Clearing site data will delete the local diary.
- Offline availability depends on the browser's service-worker and storage behaviour.
- Sample nutrition values are approximate and for demonstration only.

## Next steps

1. Improve mapping from the model's 101 dish labels to nutrition data.
2. Add serving-size estimation and mobile performance tests.
3. Replace sample values with a documented nutrition dataset and clearer uncertainty estimates.

MIT License.