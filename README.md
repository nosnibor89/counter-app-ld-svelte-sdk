# Simple Counter App

Example app for LaunchDarkly Svelte SDK integration.

Important: This app was born out of the need to provide help and support for the Introduction to LaunchDarkly Svelte SDK blog post. Don't expect frequent updates or new features.

## Prerequisites

- Node.js (v14 or higher)
- npm or yarn

## Environment Variables

Before running the application, you need to set up the following environment variable:

```bash
LAUNCHDARKLY_CLIENT_ID=your_client_id_here
```

This client ID is required for feature flag management with LaunchDarkly.

## Getting Started

1.Clone the repository:

```bash
git clone https://github.com/nosnibor89/counter-app-ld-svelte-sdk.git
cd counter-app-ld-svelte-sdk
```

2.Install dependencies:

```bash
npm install
# or
yarn install
```

3.Set up environment variables:

- Create a `.env` file in the root directory
- Add your LaunchDarkly client ID as shown in the Environment Variables section

4.Start the development server:

```bash
npm run dev
# or
yarn dev
```

5.Open [http://localhost:3000](http://localhost:3000) in your browser to see the application.
