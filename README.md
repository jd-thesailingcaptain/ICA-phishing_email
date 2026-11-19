<div align="center">

# EML Analyser

### Learn to spot phishing the way a security analyst does.

An Outlook-style practice inbox with 10 realistic emails. Investigate the headers, links and attachments, make the call, and see how you score.

[![Open the site](https://img.shields.io/badge/OPEN_THE_SITE-0f6cbd?style=for-the-badge)](https://jd-thesailingcaptain.github.io/ICA-phishing_email/)
[![Download](https://img.shields.io/badge/DOWNLOAD_ZIP-107c10?style=for-the-badge)](https://github.com/jd-thesailingcaptain/ICA-phishing_email/archive/refs/heads/main.zip)

![Single file](https://img.shields.io/badge/single_file-index.html-0f6cbd?style=flat-square)
![No install](https://img.shields.io/badge/install-none-555555?style=flat-square)
![Offline](https://img.shields.io/badge/works-offline-107c10?style=flat-square)
![Privacy](https://img.shields.io/badge/uploads-zero-c50f1f?style=flat-square)

</div>

---

## Get started

Pick whichever is easiest. Both give you the exact same app.

| | Visit the website | Download and run locally |
|---|---|---|
| **Best for** | Quick start, any device | No internet, or if the site is down |
| **How** | Click **OPEN THE SITE** above | Click **DOWNLOAD ZIP** above, unzip, double-click `index.html` |
| **Needs** | A web browser | A web browser |
| **Offline?** | No | Yes |

> **Tip:** you can also open `index.html` in this repo and use the download icon in the top right of the file view.

---

## What it does

EML Analyser puts you in front of an inbox full of emails and asks one question for each of them: **phishing or legitimate?**

- Read each email the way it would appear in a mail client.
- Dig into the evidence a real analyst would check.
- Lock in your verdict and find out whether you were right.
- Finish all 10 to get a final score and a breakdown of how you did.

Everything runs in your browser. Nothing is uploaded, and no account is needed.

---

## How to use it

1. **Open an email** from the inbox on the left.
2. **Investigate it** using the four tabs:

   | Tab | What to look for |
   |---|---|
   | **Message** | Greeting, tone, urgency, threats, requests for money or credentials |
   | **Headers** | From vs Reply-To vs Return-Path, and the SPF / DKIM / DMARC results (green is pass, red is fail, orange is none) |
   | **Links** | The text a link displays vs where it actually goes. Mismatches are flagged in red |
   | **Attachments** | Odd file types and double extensions such as `.pdf.html` |

3. **Decide.** Click **PHISHING** (red) or **LEGITIMATE** (green). You get one answer per email.
4. **Learn from the result.** After each answer you see whether it was a True Positive, True Negative, False Positive or False Negative.
5. **Finish all 10** to see your final results, then hit **Reset** to try again.

---

## Understanding the results

In phishing detection, a "positive" means you flagged an email as phishing.

| Outcome | What happened | Correct? |
|---|---|---|
| **True Positive** | A phishing email, and you flagged it | Yes |
| **True Negative** | A legitimate email, and you trusted it | Yes |
| **False Positive** | A legitimate email, but you flagged it | No (a false alarm) |
| **False Negative** | A phishing email, but you trusted it | No (the dangerous miss) |

### Final score messages

| Score | Message |
|---|---|
| 10 / 10 | Perfect score! |
| 9 / 10 | Awesome job! |
| 7 - 8 | Nice work, analyst |
| 5 - 6 | Not bad, keep going |
| 3 - 4 | Next time, champ |
| 0 - 2 | Rough round |

---

## Features

- **Outlook-style interface** with inbox list, reading pane and colored sender avatars
- **Header inspector** with the key authentication results highlighted
- **Link analyzer** that compares visible link text against the real destination
- **Safe attachment handling.** Files are listed, never opened
- **Live score** in the top bar, plus a full results screen at the end
- **Add your own `.eml` files** by drag-and-drop or the **Add .eml files** button
- **Remove** any email, **Restore samples** to bring them back, or **Reset** to start fresh
- **Animated** imports and transitions, with reduced-motion support

---

## Add your own emails

Have a suspicious email you want to examine? Export it as an `.eml` file from your mail client, then:

- **Drag and drop** the file anywhere on the page, or
- Click **Add .eml files** in the left pane.

Added emails are for practice and are not scored. They are stored only in your own browser.

---

## Safe by design

- **No uploads.** Emails are parsed locally in your browser.
- **Links are disabled.** You can hover to see the real destination, but you cannot click through.
- **Sandboxed rendering.** Email bodies run in a locked-down frame with scripts blocked and remote images off by default.
- **Attachments are never opened.** They are only listed and can be downloaded on request.
- **Fictional everything.** Every company, person and domain in the sample emails is made up, and all domains use the reserved `.example` and `.test` endings, so none can point to a real site.

---

## Host your own copy

The whole app is a single file, so hosting is easy.

1. Fork or copy this repo.
2. Go to **Settings, then Pages**.
3. Under **Source**, choose **Deploy from a branch**, select `main` and `/ (root)`, and save.
4. After a minute or two your site is live at `https://<your-username>.github.io/<repo-name>/`.

```
.
├── index.html   # the entire app, sample emails included
└── README.md
```

---

## Limitations

- Outlook `.msg` files are not supported, only `.eml`.
- Encrypted emails (S/MIME or PGP) cannot be read.
- The link check compares text to destination. It will not catch lookalike domains such as `paypa1.com`, so read carefully.
- Saved data (added emails, your answers) lives in your browser and may not persist if you clear site data or open the file in a private window.

---

<div align="center">

**For education and awareness only.** The sample emails are fictional and were written for training.

</div>
