# In loving memory of Arleigh Patrick Todd

Memorial page for the candlelight vigil. Guests scan a QR code, browse the photos and videos, and light a candle with their name.

## Files

- `index.html` is the whole page (styles and script included)
- `media/` holds the 53 photos, 2 videos, and video posters, numbered in gallery order
- `config.js` holds the Supabase settings for the shared candle wall

## Shared candle wall

With `config.js` left blank, candles are saved only on the visitor's own phone.

To share candles with everyone, add your Supabase project URL and publishable (anon) key to `config.js`. The project needs a `candles` table with `id`, `name` and `created_at`, row level security on, and policies that let `anon` select and insert (names 1 to 40 characters). No update or delete access is given to visitors.

## Hosting

Any static host works: GitHub Pages, Netlify, or a folder on your own server. The page must be served over https, and every file must keep the same relative paths.
