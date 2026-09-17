# GiftMatcher 🎁

GiftMatch AI is a lightweight, single-page gift recommendation prototype that helps users discover gift ideas based on a recipient's occasion, budget, interests, and personalization clues.

The current MVP runs entirely in the browser with no backend, database, build process, or external service dependencies. It uses a small simulated gift catalog and client-side JavaScript filtering to demonstrate the core recommendation flow.

## Application Description

GiftMatch AI captures a recipient's basic profile through a simple form and returns gift suggestions tailored to the selected hobby and budget tier. Users can provide additional clues, such as a favorite color or previously successful gifts, which are used to add personalization guidance to the results.

The current application supports:

- Birthday, anniversary, and holiday occasions
- Any/unisex, female, or male recipient selections
- Budget tiers up to $25, $25–$100, and premium gifts over $100
- Cooking, technology/gaming, and fitness/outdoor interests
- Favorite-color personalization clues
- Past successful gift notes
- Product and experience recommendations
- Simulated vendor links and store information
- Responsive desktop and mobile layouts

> **Current status:** Phase 1 MVP prototype. The gender and occasion fields are captured by the interface but are not yet used by the matching algorithm. The catalog, prices, vendor information, and links are simulated demonstration data.

## Features

### Recipient profile form

The onboarding form collects:

- Occasion
- Gender preference
- Maximum budget
- Primary interest or hobby
- Favorite color
- Past successful gifts

### Matching engine

When the user submits the form, the browser filters the local `giftDatabase` array by:

1. Selected hobby
2. Selected budget tier

Matching gifts are rendered immediately in the results panel without a page reload or network request.

### Recommendation cards

Each match displays:

- Gift name
- Product or experience category
- Suggested store or provider
- Estimated price tier
- Favorite-color customization tip, when provided
- Vendor outlet link

## Getting Started

### Requirements

No installation or development environment is required. You only need a modern web browser.

### Run locally

1. Clone the repository:

   ```bash
   git clone https://github.com/DeveloperWe/Gift-Matcher.git
   cd Gift-Matcher
   ```

2. Open `gift.html` directly in a browser.

Alternatively, start a simple local web server:

```bash
python3 -m http.server 8000
```

Then visit [http://localhost:8000/gift.html](http://localhost:8000/gift.html).

## Project Structure

```text
Gift-Matcher/
└── gift.html    # UI, styles, simulated catalog, and matching logic
```

## Technology Stack

- HTML5
- CSS3
- Vanilla JavaScript
- Browser DOM APIs

There are currently no frameworks, packages, databases, APIs, or cloud services required to run the application.

## Roadmap

### Phase 1: MVP — Current

- Build a functional single-page prototype
- Capture recipient preferences
- Provide a simulated local gift catalog
- Filter gift recommendations in the browser

### Phase 2: Hosting and infrastructure

- Provision an AWS Free Tier environment
- Create a secured IAM administrator account
- Deploy an Ubuntu Linux EC2 instance
- Configure security groups for HTTP, HTTPS, and restricted SSH access
- Serve the application with Nginx or Apache

### Phase 3: Dynamic data and storage

- Replace the hardcoded catalog with a managed database
- Save multiple recipient profiles, such as “Mom” or “Best Friend”
- Add an admin dashboard for gifts, tags, budgets, and vendor links

### Phase 4: Third-party integrations

- Retrieve live products, prices, images, and affiliate links
- Add local experience recommendations using services such as Yelp or Google Places
- Use location or ZIP code to suggest nearby activities

### Phase 5: AI personalization — “The Vibe Generator”

- Add a natural-language recipient description field
- Use a serverless backend function to call an AI service
- Convert descriptions into semantic tags and recommendation queries
- Match gifts to personality, mood, and lifestyle clues

## Limitations

This prototype intentionally uses simulated data. It does not currently provide:

- User accounts or authentication
- Persistent recipient profiles
- A backend or database
- Live prices, inventory, images, or vendor URLs
- Location-based recommendations
- AI-generated recommendations
- Production security, monitoring, or deployment configuration

## Contributing

Contributions and ideas are welcome. For larger changes, consider opening an issue first to discuss the proposed feature or implementation.

## License

No license has been specified yet.
