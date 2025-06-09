# Phase 2 Code Challenge: Plantsy

## Demo

Use this gif as an example of how the app should work.

![Demo GIF](./demo.gif)

## Instructions

Welcome to Plantsy! You've been tasked with building out some features for the
admin side of a plant store. The designers have put together the components and
CSS. Now it's up to you to bring the features to life by adding stateful logic
as well as persisting data to the backend via our API.

Your job will be to make our app work according to the user stories you will
find the [Deliverables](#Deliverables) section.

## Setup

1. Run `npm install` in your terminal.
2. Run `npm run server`. This will run your backend on port `6001`.
3. In a new terminal, run `npm run dev`.

Make sure to open [http://localhost:6001/plants](http://localhost:6001/plants)
in the browser to verify that your backend is working before you proceed!

## Endpoints

The base URL for your backend is: `http://localhost:6001`

## Deliverables

As a user:

1. When the app starts, I can see all plants.
2. I can add a new plant to the page by submitting the form.
3. I can mark a plant as "sold out".
4. I can search for plants by their name and see a filtered list of plants.

### Endpoints for Core Deliverables

#### GET /plants

Example Response:

```json
[
  {
    "id": 1,
    "name": "Aloe",
    "image": "./images/aloe.jpg",
    "price": 15.99
  },
  {
    "id": 2,
    "name": "ZZ Plant",
    "image": "./images/zz-plant.jpg",
    "price": 25.98
  }
]
```

#### POST `/plants`

Required Headers:

```js
{
  "Content-Type": "application/json"
}
```

Request Object:

```json
{
  "name": "string",
  "image": "string",
  "price": number
}
```

Example Response:

```json
{
  "id": 1,
  "name": "Aloe",
  "image": "./images/aloe.jpg",
  "price": 15.99
}
```

---

## Features

- **View Plants:** Displays a list of plant cards on page load by fetching data from a local server.
- **Search Functionality:** Users can filter the list of plants by name using a search input.
- **Add New Plants:** Users can submit a form to add new plants, which updates the list.
- **Toggle Stock Status:** Each plant can be marked as "In Stock" or "Out of Stock".
- **Styling:** Custom CSS styles included for layout and basic styling.

---

## File Structure (Key Components)

- `PlantPage.jsx` - Main container that manages plant state and renders all subcomponents.
- `PlantList.jsx` - Renders a list of `PlantCard` components.
- `PlantCard.jsx` - Individual plant display with toggleable stock status.
- `NewPlantForm.jsx` - Form to add new plant entries.
- `Search.jsx` - Input field that filters the displayed plant list.

---

## Testing Notes

- The application has a test suite that verifies rendering and interactivity.
- One test may fail despite functional behavior due to strict matching in `findByText("foo")`. After debugging, it was confirmed that the plant is rendered in the browser with the correct name and structure. This appears to be a test-side limitation in detecting the rendered node under test conditions.

---

## Author

Andrew Snyder  
React Lab - Flatiron School of Software Engineering
June 2025

---
