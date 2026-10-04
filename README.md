# Ravi Seth Real Estate

Independent real estate website and backend. The homepage and server default to the estate view and estate content mode.

Includes sale and rental listings, property filters, photo and video galleries, amenities and connectivity in English and Telugu, maps, editorials, call requests and a mobile Content Studio.

## Run locally

Use Node.js 24 or newer. No dependency installation is required.

```sh
git clone https://github.com/Mukesh-004/ravi-seth-real-estate.git
cd ravi-seth-real-estate
npm run dev
```

Open `http://127.0.0.1:4173/`. Content Studio is at `/admin.html`. Listings are saved in `data/site.sqlite`, and uploaded media in `uploads/`.

## Configure and publish

Copy `.env.example` to `.env`, set a private `ADMIN_TOKEN`, and run `npm run dev:env`. Keep `SITE_VARIANT=estate`. Follow [SETUP.md](SETUP.md) for persistent hosting, Docker, Google Sheets delivery and search indexing. That guide documents the shared backend; this deployment enables the estate sections.

The [boutique and cars project](https://github.com/Mukesh-004/ravi-seth-boutique) has a separate repository and database.

```sh
npm run check
npm test
```

Generate the estate ZIP with `powershell -File scripts/build-packages.ps1`. Source code is directly browsable here. Private settings, local databases, uploaded media and generated ZIPs are ignored by Git.

Replace sample properties, prices, photos, articles and contact details before launch. Live Google Sheets delivery requires the Apps Script configuration in SETUP.md.
