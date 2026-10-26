# Reset password page

The page the "Reset Password" email opens. The person types the new password twice and saves; the link is used up
only when they press Save. Files: `index.html` and `supabase.js` (the Supabase browser library). No build step.

Host both files at the root of any static host (GitHub Pages, Netlify, Cloudflare Pages), then in Supabase:
- Authentication > URL Configuration > Site URL = the address of the page, without a trailing slash
  (for example https://gowtham-somu.github.io/poojai-reset).
- Authentication > Emails > Reset Password: paste `supabase/email-templates/reset-password.html`.

`index.html` holds the project's public anon key (the same key the app carries); data is protected by row level security.
