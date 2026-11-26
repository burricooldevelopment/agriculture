# GreenHarvest Agriculture Portfolio Website

A responsive agriculture portfolio website built with HTML5, CSS3 and vanilla JavaScript.

## Project files

- `index.html` — semantic page structure and content
- `style.css` — colours, typography, layouts, responsive design and focus states
- `script.js` — mobile navigation, product filters, FAQ accordion, enquiry validation, back-to-top and active navigation

## Run the website

1. Extract the ZIP file.
2. Open the `agriculture-portfolio` folder in VS Code.
3. Open `index.html` in a browser, or use the VS Code Live Server extension.
4. Internet access is required for the Google Fonts, Bootstrap Icons CDN and remote sample photographs.

## Important customisation before publishing

Search `index.html` for `GreenHarvest`, `example.com`, `000 000 0000`, `Your farm location`, and sample content. Replace these with the real agricultural brand name, verified phone number, email, location, products, services, statistics and genuine testimonials.

Replace all sample Unsplash image URLs with photographs you own or are authorised to use. Product examples and service descriptions must reflect what the farm actually offers.

## Connect the enquiry form

The form validates in the browser, but HTML and JavaScript alone cannot securely store or email enquiries. Configure a backend endpoint that accepts JSON over HTTPS.

In `index.html`, find:

`<form class="contact-form" id="contactForm" data-endpoint="">`

Set `data-endpoint` to your real HTTPS endpoint, for example:

`data-endpoint="https://your-domain.com/api/enquiries/"`

The endpoint should:
- accept a POST request with JSON fields `name`, `email`, `subject`, and `message`;
- validate all values again on the server;
- apply spam protection/rate limiting and appropriate CSRF/CORS protections;
- store or deliver the enquiry securely;
- return a successful HTTP status only when the enquiry has actually been accepted.

Do not put database passwords, API secret keys or private credentials in frontend JavaScript. The page deliberately does not show a false success message when no backend endpoint is configured.

## Algorithm features implemented

- HTML semantic header, navigation, main sections and footer
- Hero, about, products, services, projects, impact, testimonial and contact sections
- Responsive desktop, tablet and mobile CSS layouts
- Mobile navigation with `aria-expanded` state and close-on-link behaviour
- Product category filtering and visible result count
- FAQ show/hide controls with accessible expanded state
- Enquiry form validation and configured secure endpoint submission
- Loading, success and failure form states
- Back-to-top button
- Keyboard focus visibility and reduced-motion preference support
