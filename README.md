# Nodebase

A modern web application built with **Next.js**, designed for scalability, maintainability, and efficient development.

## Overview

This project is built using the Next.js framework and bootstrapped with [`create-next-app`](https://nextjs.org/docs/app/api-reference/cli/create-next-app). It leverages modern web development practices and integrates database management, authentication, billing, background task processing, and error monitoring.

## Tech Stack

- **Framework:** Next.js
- **Language:** TypeScript
- **Database:** PostgreSQL
- **ORM:** Drizzle ORM
- **Authentication:** Better Auth
- **Billing:** Polar
- **Background Jobs:** Trigger.dev
- **Error Monitoring:** Sentry
- **Font Optimization:** `next/font` with Geist

## Prerequisites

Before getting started, ensure you have the following installed:

- [Node.js](https://nodejs.org/) — compatible with your project's dependencies
- npm, Yarn, pnpm, or Bun
- Access to a PostgreSQL database
- Credentials for any external services you intend to use

## Getting Started

Follow these steps to set up and run the project locally.

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd <your-project-directory>
```

Replace the placeholders with your repository URL and project directory.

### 2. Install Dependencies

Using npm:

```bash
npm install
```

Alternatively, use Yarn, pnpm, or Bun according to your preferred package manager.

### 3. Configure Environment Variables

Create your local environment file from the provided example:

```bash
cp .env.example .env.local
```

Open `.env.local` and configure the required environment variables.

| Variable | Description |
|---|---|
| `DATABASE_URL` | PostgreSQL connection string used by Drizzle ORM and Better Auth |
| `POLAR_ACCESS_TOKEN` | Access token for Polar billing |
| `POLAR_PRODUCT_ID` | Identifier of the Polar product |
| `POLAR_SUCCESS_URL` | URL users are redirected to after a successful billing flow |
| `TRIGGER_PROJECT_ID` | Trigger.dev project identifier |
| `NEXT_PUBLIC_SENTRY_DSN` | Public Sentry DSN for client-side error monitoring |
| `SENTRY_DSN` | Sentry DSN for server-side error monitoring |
| `SENTRY_ORG` | Sentry organization identifier |
| `SENTRY_PROJECT` | Sentry project identifier |

**Note:** Polar, Trigger.dev, and Sentry configurations should be provided according to the integrations enabled in your project. Sentry can be disabled by leaving its configuration values blank, as supported by the application.

### 4. Start the Development Server

Run the following command:

```bash
npm run dev
```

Alternatively:

```bash
yarn dev
# or
pnpm dev
# or
bun dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser to access the application.

## Development

### Project Customization

- Modify `app/page.tsx` to update the application's main page.
- Update components and layouts to customize the user interface.
- Configure environment variables for external services and integrations.
- Follow the existing project structure and coding conventions when introducing new features.

Next.js supports hot reloading during development, allowing changes to appear in the browser automatically.

## Environment and Security

To protect sensitive information:

- Never commit `.env.local` or other files containing secrets.
- Keep API keys, access tokens, and database credentials private.
- Use `.env.example` to document the required environment variable names without exposing actual credentials.
- Configure production environment variables securely through your deployment platform.

## Learn More

Explore the following resources to learn more about the technologies used in this project:

- [Next.js Documentation](https://nextjs.org/docs) — Framework documentation and API references.
- [Learn Next.js](https://nextjs.org/learn) — Interactive learning resources.
- [Drizzle ORM Documentation](https://orm.drizzle.team/) — Database queries, schemas, and migrations.
- [Better Auth Documentation](https://www.better-auth.com/) — Authentication setup and configuration.
- [Polar Documentation](https://docs.polar.sh/) — Billing and payment integration.
- [Trigger.dev Documentation](https://trigger.dev/docs) — Background jobs and task orchestration.
- [Sentry Documentation](https://docs.sentry.io/) — Application monitoring and error tracking.

## Deployment

The application can be deployed on [Vercel](https://vercel.com/), which provides native support for Next.js applications.

Before deploying:

1. Configure all required production environment variables.
2. Verify the database connection and authentication configuration.
3. Configure the relevant billing and background task integrations.
4. Set up error monitoring if required.
5. Run a production build and resolve any errors before release.

For additional guidance, refer to the [Next.js deployment documentation](https://nextjs.org/docs/app/building-your-application/deploying).

## License

Add the applicable license information here if the project is intended for public distribution.
