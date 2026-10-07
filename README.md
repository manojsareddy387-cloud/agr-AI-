# AgriSmart AI — Professional Full-Stack Starter

## Frontend
The frontend is now a **single self-contained `index.html`** with embedded CSS and JavaScript. This avoids the CSS-loading problem seen when opening the page directly from a phone/file manager.

Open `index.html` directly in Chrome, or use VS Code Live Server.

No personal name is displayed in the interface.

## Backend
The project also contains the FastAPI/PostgreSQL starter backend from the previous version.

See `requirements.txt`, `database.sql`, `docker-compose.yml`, and `backend/`.

## Important
Crop disease detection and weather values in the frontend are demo values until the backend/model and weather API are configured.


## New Access Features
- Login and Register screens
- Frontend logout with session state stored in browser localStorage
- Browser location permission using the Geolocation API
- Location status shown on Login and Weather pages
- Update Location button
- Location coordinates are used only in the frontend demo; connect them to the backend/weather API for live personalized weather.


## Crop AI update
The previous hard-coded `Rice/Paddy -> Rice Blast` response has been removed.
The UI now supports multiple crop types (Rice, Tomato, Potato, Maize, Cotton, Chilli, Grape and Apple), an Auto/AI Detect option, and crop-specific demo guidance.

For genuine image-based automatic detection, connect the frontend to the FastAPI `/api/crop/analyze` endpoint and load a trained crop-disease computer-vision model (for example a PlantVillage/custom model). The demo deliberately does not claim to diagnose an arbitrary photo without a real trained model.


## Multilingual Support
The website now includes a language selector for:
- English
- Hindi (हिन्दी)
- Telugu (తెలుగు)
- Kannada (ಕನ್ನಡ)
- Tamil (தமிழ்)
- Malayalam (മലയാളം)

The selected language is saved in browser localStorage so it remains selected after reopening the page.


## Andhra Pradesh Location Update
Added a district selector for Andhra Pradesh with 28 current districts, including Markapuram and Polavaram. Selecting a district updates the demo weather display and the crop recommendation cards. The location selection is saved in the browser. Live weather/soil values should be connected to the backend APIs for production use.
