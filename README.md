# Greener Thumb

## Overview

Greener Thumb is a web application designed to help users select houseplants that best fit their lifestyle and home environment. It uses a form to capture user preferences and suggests plants that match their lifestyle based on those preferences.

## Features

### Plant Preference Form

The main feature is a form that collects user preferences regarding:

- Edibility of the plant.
- Safety for pets and children.
- Plant lifespan (annual or perennial).
- Watering schedule.
- Amount of sunlight.

### Dynamic Plant Display

The application dynamically displays plants based on user criteria. If no specific criteria are selected, the home page shows a default splash image of a plant. Matching plants are displayed with their common and scientific names, an image, and details about their lifecycle, watering needs, and sunlight requirements.

## HTML Structure

- **HTML5:** The document uses HTML5 semantics.
- **Form:** Preferences are submitted through a form that sends a GET request to `/getPlants`.
- **Dynamic Content:** Server-side scripting (EJS) displays content based on user selections.

## CSS

The layout and styling are defined in an external stylesheet located at `/style.css`.

## Server Setup

### Dependencies

- **Node.js** and **Express.js** for server management.
- **EJS** for templating.
- **dotenv** for environment variable management.

### Server.js

The server script configures the application and handles routes:

- **Static Files:** Serves static files from the `public` directory.
- **API Interaction:** Constructs a query string based on form inputs and fetches data from an external API.
- **Error Handling:** Manages errors during the API call process and provides user feedback.

### Routes

- **GET /**: Serves the main page.
- **GET /getPlants**: Handles the form submission, retrieves plant data based on user preferences, and renders the page with results.

### Environment Variables

- **PORT**: The server port (default is 3000).
- **PERENUAL_API_KEY**: API key for external plant data API.

## Getting Started

To run this application:

1. Ensure Node.js is installed.
2. Clone the repository and navigate into the project directory.
3. Install dependencies using `npm install`.
4. Set up the `.env` file with the required `PERENUAL_API_KEY`.
5. Start the server using `npm start` and access the app by navigating to `http://localhost:3000` in a web browser.

## License

This project is open-sourced under the MIT license. Feel free to use, modify, and distribute the code as you see fit.
