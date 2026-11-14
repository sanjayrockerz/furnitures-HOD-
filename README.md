# Sky Furnitures

Production-oriented static furniture storefront refactored from the supplied Furniture Store HTML reference.

## Run locally

```powershell
python -m http.server 4173
```

Open http://localhost:4173. A static server is required because the app uses ES modules and JSON data.

## Structure

- `index.html` – home page shell
- `pages/` – catalogue, product, cart, wishlist, checkout, about and contact entry points
- `css/` – tokens, global layout and responsive styles
- `js/` – configuration, catalogue and storefront behavior
- `data/` – centralized product and category data
- `assets/images/` – copied product/category imagery from the source bundle

## Configuration

Set `whatsappBusinessNumber` in `js/config.js` with digits only. It is intentionally blank until Sky Furnitures supplies an official business number. Product availability, dimensions, material and warranty remain marked as confirmation-needed where the source did not specify them.

## Checkout

Checkout validates customer and delivery details in the browser, then creates a WhatsApp enquiry. It does not process payments or confirm orders. No card, UPI PIN or banking credentials are collected.

## Deployment

This is a buildless static site and can be deployed to Vercel by importing the repository with no build command and `index.html` as the output root.

## Current limitations

- WhatsApp ordering remains disabled until a verified business number is configured.
- Product specs and inventory are intentionally not fabricated.
- No backend, authentication, inventory system or payment gateway is included.
