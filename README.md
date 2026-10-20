# Caloria

A tiny bilingual (Spanish/English), offline-first food diary PWA. It uses no framework, build step, backend, analytics, or paid API.

## Included

- Responsive layout suitable for mobile and desktop.
- Spanish and English interface.
- Photo picker/camera capture with a local preview.
- Sample food catalogue and editable portion sizes.
- Approximate calorie and macronutrient calculations.
- Food diary persisted in browser `localStorage`.
- Service worker for a basic offline app shell.
- GitHub Pages-ready static files.

## Important: photo recognition is not implemented

The selected image is only previewed; this version does not identify food from an image and does not estimate portion size automatically. Choose a food from the sample list and adjust grams manually. This is intentional: the UI does not pretend a photo preview is AI recognition.

## Run and deploy

No build command is required. Serve this directory from a static HTTPS host. For GitHub Pages, open **Settings → Pages**, select **Deploy from a branch**, choose **main** and **/(root)**, then save. After deployment, open the published HTTPS URL and use your browser's Add to Home Screen option.

## Privacy and limitations

- Photos are previewed locally and are not uploaded.
- Diary entries are saved on this device in browser storage.
- Clearing site data will delete the local diary.
- Offline availability depends on the browser's service-worker and storage behaviour.
- Sample nutrition values are approximate and for demonstration only.

## Next steps

1. Evaluate a genuinely on-device food recognition model and its licence.
2. Add model download consent, caching, and mobile performance tests.
3. Improve portion estimation and communicate uncertainty clearly.
4. Replace sample values with a documented nutrition dataset.

MIT License.