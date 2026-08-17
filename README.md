# Word Weekend Registration · Gate Ministries Blouberg

Registration site for the **Word Weekend, 18 – 20 September 2026**.

* Pure HTML + CSS — runs on GitHub Pages with no build step.
* Submissions delivered to `info@gateministriesblouberg.co.za` via [Web3Forms](https://web3forms.com).
* Registrant sees a thank-you on the page and receives an email confirmation.

---

## Setup (2 minutes)

### Step 1 — Get a Web3Forms access key

1. Go to <https://web3forms.com>.
2. Click **Create Access Key**.
3. Enter **`info@gateministriesblouberg.co.za`** as the destination email.
4. Confirm the email you receive at that address.
5. You'll be given an **Access Key** — a long string like `abcd1234-ef56-7890-...`. Copy it.

### Step 2 — Paste the key into the site

Open **`index.html`** in any text editor and find this line:

```html
<input type="hidden" name="access_key" value="YOUR_ACCESS_KEY_HERE">
```

Replace `YOUR_ACCESS_KEY_HERE` with the key you just copied. Save.

### Step 3 — (Optional but recommended) Turn on the auto-reply

Go to your Web3Forms dashboard → your form → **Settings → Auto Response** and enable it.

Suggested content:

* **From name:** `Gate Ministries Blouberg`
* **Subject:** `Your Word Weekend attendance is confirmed`
* **Message:**

  > Dear {{First name}},
  >
  > Thank you for confirming your attendance for **Word Weekend**, taking place **18 – 20 September 2026**.
  >
  > **Sessions:**
  > • Friday · Session 1 · 7:00 PM
  > • Saturday · Session 1 · 9:30 AM
  > • Sunday · Final Session · 9:30 AM
  >
  > We look forward to gathering with you in the Word.
  >
  > For any queries, contact Pastor Amos James on 083 289 7627.
  >
  > *— Gate Ministries Blouberg*
  > www.gateministriesblouberg.co.za

Once saved, every registrant automatically gets this confirmation on the email address they provided.

### Step 4 — Push to GitHub & enable Pages

1. Create a new GitHub repo (any name — e.g. `word-weekend`).
2. Upload **all four files** — `index.html`, `styles.css`, `logo.png`, `README.md` — to the **root** of the repo (not inside a folder).
3. Repo → **Settings → Pages**. Under **Source**, pick branch `main` and folder `/ (root)`. Click **Save**.
4. After about a minute, the site is live at:
   `https://<your-username>.github.io/<repo-name>/`

Share that link with your community.

---

## What each registration email contains

You'll receive something like this:

> **📖 New Word Weekend Registration**
>
> From: Word Weekend · Gate Ministries Blouberg
> Reply-to: *[registrant's email]*
>
> First name: John
> Surname: Smith
> Cellphone: 082 555 1234
> Email: john@example.com

The registrant is automatically added as the reply-to, so you can just hit "Reply" in Gmail to get in touch with them directly.

---

## Customising

| What | Where |
| ---- | ----- |
| **Hero photo** | Save any beautiful worship / prayer / Bible / church photo as `hero.jpg` in the same folder as `index.html`. Recommended: at least 1600×900px, landscape. Without it, the warm gradient fallback shows. |
| Church logo | The white version is included as `logo.png`. To use a different version, just replace that file. |
| Event dates / session times | `index.html` — the `.hero-title`, `.hero-date`, and `.sessions` blocks |
| Email subject line | `index.html` — search for `subject` in the hidden fields |
| Colours | `styles.css` — the `:root` block at the top |
| Contact info in the footer | `index.html` — the `.site-footer` block |

---

## Limits

Web3Forms free plan: **250 submissions per month**. Plenty for a weekend event.

---

## Contact

For event queries: `info@gateministriesblouberg.co.za` · Pastor Amos James · 083 289 7627
Website: [www.gateministriesblouberg.co.za](https://www.gateministriesblouberg.co.za)
