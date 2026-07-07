# Language Course

A modern, responsive landing page for a language school. Visitors can browse courses, sign up for classes, subscribe to a newsletter, and explore events, news, and instructors in Hungarian or English, with light or dark theme support.

## Features

- **Image slider**: auto-rotating hero section with key messages
- **Course catalog**: English, German, French, and kids courses with pricing and duration
- **Course finder form**: language, name, phone, email, and date fields with validation
- **Newsletter signup**: email validation included
- **Events calendar**: interactive calendar and upcoming events list
- **Countdown timer**: time remaining until the next course starts
- **Statistics**: animated counters (students, programs, instructors, and more)
- **News and articles**: blog-style cards
- **Testimonials**: feedback from happy students
- **Instructors**: featured teachers section
- **Language progress bars**: visual language proficiency display
- **Bilingual UI**: Hungarian and English switching via Transloco, preference saved in localStorage
- **Dark and light mode**: theme toggle, saved in localStorage
- **Responsive design**: mobile, tablet, and desktop layouts

## Tech Stack

| Category | Technology |
| --- | --- |
| Framework | [Angular 19](https://angular.dev/) |
| Language | TypeScript |
| Styling | [Tailwind CSS 4](https://tailwindcss.com/), SCSS |
| UI Components | [Angular Material](https://material.angular.io/) |
| i18n | [@jsverse/transloco](https://jsverse.github.io/transloco/) |
| Reactive Programming | RxJS |
| Date Handling | date-fns |
| Build Tool | Angular CLI (`@angular-devkit/build-angular`) |
| Lint / Formatting | ESLint, Prettier |

## Local Setup

### Prerequisites

- [Node.js](https://nodejs.org/) (LTS recommended)
- npm

### Steps

```bash
git clone https://github.com/lali1998/language-course-front-end.git
cd language-course-front-end
npm install
npm start
```

The dev server runs at **http://localhost:4200/** by default. The app reloads automatically when source files change.

### Production Build

```bash
npm run build
```

Build output goes to `dist/lang-course/`. The production build is configured with a `/lang-course/` base href for GitHub Pages.

### Other Commands

```bash
npm run lint                  # Run ESLint
npm run test                  # Unit tests (Jest, watch mode)
npm run generate-translations # Generate i18n keys from source
```

## Usage

1. **Switch language**: select the Hungarian or English flag in the top-right header area.
2. **Switch theme**: toggle light or dark mode in the header.
3. **Browse courses**: scroll to the "Choose your language" section to view available courses.
4. **Sign up for a course**: fill in the "Find your course" form (language, name, phone, email, date), then click **Send message**.
5. **Newsletter**: enter your email in the subscription section.
6. **Events**: browse dates in the events calendar; events for the selected day appear below.
7. **Next course**: the countdown shows time remaining until the next course begins.

> **Note:** Forms currently work on the front end only (mock data, no backend API).

## Project Structure

```
src/
├── app/
│   ├── pages/
│   │   └── home/              # Home page and section components
│   └── shared/
│       ├── components/        # Reusable UI components
│       ├── layouts/           # Header, navbar, footer
│       ├── services/          # Theme and language services
│       ├── mocks/             # Mock data (courses, events, etc.)
│       ├── interfaces/        # TypeScript interfaces
│       └── core/              # App config, routing, Transloco loader
├── styles.scss                # Global styles
public/
├── i18n/                      # Translation files (hu.json, en.json)
└── images/                    # Static images
scripts/
└── generate-translations.ts   # i18n key generator script
```
