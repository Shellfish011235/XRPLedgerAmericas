# Email signup form (Formspree)

The **Join the movement** button scrolls to an email signup section. Submissions are stored via [Formspree](https://formspree.io) so you can collect emails and send news later.

## Setup (one-time)

1. Go to **[formspree.io](https://formspree.io)** and create a free account.
2. Click **New form** and name it (e.g. "XRPLedgerAmericas signups").
3. Formspree gives you a form endpoint like:  
   `https://formspree.io/f/xxxxxxxx`
4. In **index.html**, find the join form and replace `YOUR_FORM_ID` with your form ID:
   - Find: `action="https://formspree.io/f/YOUR_FORM_ID"`
   - Replace with: `action="https://formspree.io/f/your-actual-id"`  
   (e.g. if your URL is `https://formspree.io/f/abc123xy`, use `abc123xy` as the ID.)
5. Save, commit, and push. New signups will appear in your Formspree dashboard.

## What you get

- **Formspree dashboard:** View every submission (email, optional name).
- **Export:** Download submissions as CSV for use in a newsletter tool (Mailchimp, etc.).
- **Notifications:** Optional email alert for each new signup (Formspree settings).
- **Later:** Use the exported list to send news and updates when you’re ready.

No backend or database is required on your site; Formspree stores the data.
