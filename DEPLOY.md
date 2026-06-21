# Deploy: Signal lead dashboard

Same flow you used for the Headline site.

## Put it online (5 min, all clicks)
1. Unzip this folder. You get a "signal" folder with index.html.
2. Go to github.com/Artenvisage/Misc → Add file → Upload files.
3. Drag the whole "signal" folder in → Commit changes.
4. Go to vercel.com/new → Import "Misc" → set Root Directory to "signal" → Deploy.
   (If Misc is already a Vercel project, just push; it redeploys. You may want a
    second Vercel project pointed at the /signal folder so it gets its own URL.)
5. Rename the project to "signal" in Vercel settings for a clean URL.

## Using it
- Today's view already has 84 real businesses from Austin, Denver and Toronto.
- To run a fresh scan: paste your Apify API token (top-left field), pick categories
  and cities, hit "Run scan". Results score instantly and merge into the table.
- Your token is stored only in your browser, never sent anywhere but Apify.
- "Mark as contacted" and your token persist on your device.

## If "Run scan" is blocked by the browser
Some browsers block direct calls to Apify (CORS). The preloaded data still works.
For reliable live scanning at scale, the next step is the scheduled VPS job we
discussed: it runs the same scrape on a timer and writes results to Supabase, which
this dashboard then reads. Say the word and I'll build that piece.
