# All About You Astrology — policy site

The Privacy Policy and Terms of Service for the **All About You Astrology** Android app,
published by Beyond Animations. Served as a static site by GitHub Pages so that Google Play
has a public URL to link to.

## Why this is a separate repository

**This repository is public. The app's repository is private and must stay that way**,
because it contains real birth data for real people.

Nothing from the app repository belongs here. This repository holds four files and should
never hold anything else:

| File | What it is |
|---|---|
| `index.html` | Landing page, links to both documents and gives a support contact |
| `privacy.html` | Privacy Policy — the URL Google Play asks for |
| `terms.html` | Terms of Service — the URL the App content page asks for |
| `style.css` | Shared styling, light and dark |

No app source, no APK, no chart data, no birth data. Ever.

## The URLs

Once GitHub Pages is enabled on this repository:

- Privacy Policy — `https://beyondanimations.github.io/all-about-you-policies/privacy.html`
- Terms of Service — `https://beyondanimations.github.io/all-about-you-policies/terms.html`

Those are the two links to paste into Play Console.

## Enabling GitHub Pages

Settings → Pages → Source: *Deploy from a branch* → Branch: `main`, folder `/ (root)` →
Save. The site goes live in a minute or two.

## Keeping it accurate

The Privacy Policy describes the app as it actually behaves, not boilerplate. It was
written against the code and the following are verified facts about the shipped app:

- No Android permissions are declared in the manifest, including internet access
- No networking library, no analytics, no crash reporting, no advertising SDK
- Birth data is held in the app's private `SharedPreferences`
- `android:allowBackup="true"`, so Android Auto Backup may copy that data to the user's
  own Google Drive — this is disclosed in section 3 of the policy

**If any of those change, the policy has to change with them.** In particular, adding a
networking library, an analytics SDK, or a crash reporter would make section 2 false.

Update the "Last updated" date at the top of a document whenever its content changes.
