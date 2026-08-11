DRAWLINE WEBSITE — Deploy to Vercel

WHAT'S HERE:
  index.html    — landing page (interactive trace-to-reveal hero)
  privacy.html  — privacy policy, matches the site's design

BEFORE DEPLOYING — fill in these placeholders:
  1. privacy.html: replace [DATE] and [YOUR_SUPPORT_EMAIL]
  2. index.html: the "Get it on Google Play" buttons currently link to "#"
     — once DrawLine is live on Play Store, replace href="#" with your
     real Play Store URL (search index.html for href="#" — 2 occurrences)
  3. index.html footer: replace support@example.com with your real email
  4. (Optional) Add a real favicon.png — currently referenced but not
     included; drop one in this folder, or just delete that <link> tag
     in index.html's <head> if you don't want one yet

DEPLOY — same flow as mindrivals-site.vercel.app:
  1. Push this folder to a new GitHub repo (or a subfolder of an existing
     one), OR just drag-and-drop the folder into vercel.com's dashboard
     ("Add New Project" → deploy without git for a quick static upload)
  2. No build step needed — this is plain HTML/CSS/JS, Vercel will
     serve it as-is. Framework preset: "Other" / static.
  3. Once deployed, your privacy policy URL for Play Console will be:
        https://<your-vercel-domain>/privacy.html
     (matches the pattern of mindrivals-site.vercel.app/delete-account/)

NOTES ON THE DESIGN:
  - Typography (Space Grotesk + Inter) deliberately matches MindRivals'
    own font choice — same studio family across both listings.
  - The hero's "signature element" is the trace-to-reveal mark: drag
    across it and it lights up neon, same mechanic as the actual game.
    It also auto-animates on a loop for visitors who don't interact,
    and respects prefers-reduced-motion (skips animation, shows the
    mark fully lit instead).
  - Colors, the boss-cadence dot row, the IQ tier scale, and the season
    swatches all pull real values from the actual game (theme.ts,
    seasons.ts, progressStore.ts) rather than generic marketing colors.
  - No screenshots section included yet — once you have real gameplay
    screenshots (recommended: mid-trace on a colorful level, a win
    screen, the level selector, a boss level), send them and I'll add
    a screenshots section to the page.
