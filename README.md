# Utulo — Discover more

Utulo is a responsive travel and hospitality discovery marketplace designed to match the supplied mobile UI concept. It is a separate customer-facing experience intended to integrate with SifoHotel while remaining open to independent businesses.

## Included in this first UI build
- Responsive home/search screen and category discovery.
- Explore listings for hotels, lodges, apartments, resorts, guest houses, restaurants, car hire, safaris, parks and hourly/night rooms.
- Property detail view, gallery, room choices and booking/enquiry interaction.
- Map-style discovery view, saved listings, booking list, WhatsApp enquiry links and owner listing form.
- Animated Utulo AI travel helper (demo responses; not a live AI service yet).
- Accessible mobile bottom navigation, transitions, filters and search.
- Supabase client adapter that activates only when environment variables are supplied.

## Run locally
From this directory:

```bash
npm install
npm run dev
npm run build
```

## External Supabase later
Create `.env.local` in this folder when the separate Supabase project is ready:

```env
VITE_SUPABASE_URL=https://YOUR-PROJECT.supabase.co
VITE_SUPABASE_ANON_KEY=YOUR_PUBLIC_ANON_OR_PUBLISHABLE_KEY
```

Do not use a service-role key in browser code. The current experience uses clearly marked demo data and does not persist real bookings or listings. Before live launch, add database migrations, Auth, tenant-safe RLS policies, storage buckets, listing moderation, reservation conflict checks and server-side booking/payment integrations.

## SifoHotel integration plan
SifoHotel remains the source of truth for room inventory, rates and confirmed reservations for connected properties. Integrate through authenticated server-side endpoints or Supabase Edge Functions; do not trust browser-submitted availability or expose service credentials. Independent listings should continue to work without SifoHotel.

## Brand
Utulo — Discover places. Experience more. Stay smarter.
