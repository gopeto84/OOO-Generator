# Out of Office Message Generator

A lightweight, client-side web app to generate clear and professional Out-of-Office (OOO) email messages with optional cover contacts, templates, and a downloadable Outlook calendar event.

## Features

* **Responsive web app** built with HTML, TailwindCSS (via CDN), and vanilla JavaScript.
* **Lineage branding colors** applied (Blue, Green, Gray, Light Gray).
* **Templates** for different OOO contexts:

  * General OOO
  * Travel (mentions limited availability)
  * Conference (mentions delayed responses)
* **Quick date ranges** for convenience:

  * Rest of today
  * Today (9–5)
  * Tomorrow (9–5)
  * Next week (Mon–Fri)
* **Time zone selector** (defaults to your local zone).
* **Primary cover person** details (name, email, reason).
* **Support portal link** (default: `https://lineage.service-now.com/esc`, included as clickable link).
* **Generated outputs:**

  * Subject line
  * Plain text message
  * HTML preview (with clickable links)
* **Copy buttons** for subject, message, and HTML.
* **Downloadable Outlook calendar event (.ics)** that sets OOO status.
* **Dark mode toggle** for user preference.

## Getting Started

### Prerequisites

* Modern browser (Chrome, Edge, Firefox, Safari).
* No build tools required — runs directly in the browser.

### Usage

1. Clone this repository:

   ```bash
   git clone https://github.com/your-org/ooo-generator.git
   cd ooo-generator
   ```
2. Open `index.html` in your browser.
3. Fill out the form with your dates, time zone, and primary cover contact.
4. Select a template if desired.
5. Review the **Preview** panel for subject and message.
6. Use the copy buttons or download an `.ics` calendar event.

### Calendar Event (.ics)

* Clicking **Download Calendar Event (.ics)** generates an Outlook/Google Calendar event.
* The event:

  * Uses the generated subject as the title.
  * Contains the OOO message in the description.
  * Blocks your calendar for the selected duration.
  * Sets the status to **Out of Office (OOF)** for Outlook compatibility.

## Project Structure

```
/ooo-generator
│── index.html        # Main app (all HTML, CSS, and JS inline)
│── README.md         # Documentation (this file)
```

## Customization

* **Branding:** Edit the `:root` CSS variables in `index.html` to change colors.
* **Default portal link:** Update the value in the `support-link` input element.
* **Templates:** Add or modify options in the `<select id="template">` dropdown.

## Roadmap

* [ ] Add support for multiple secondary cover persons with remove/edit.
* [ ] Save/load user preferences via localStorage (partially implemented).
* [ ] Export to Slack/Teams short message format.
* [ ] Additional templates (e.g., parental leave).

## License

MIT License. See LICENSE file for details.

---

### Example Screenshot

![Screenshot](docs/screenshot.png)

---

**Maintainer:** Your Name
**Contact:** [your.email@example.com](mailto:your.email@example.com)
