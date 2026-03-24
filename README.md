# Edge Functions - APIs Podai

This repository contains all Supabase Edge Functions used in the project. These functions are deployed across staging and production environments.

---

## Prerequisites

Make sure you have the following installed:

- [Node.js (v18 or above)](https://nodejs.org/)  
  Required to run JavaScript and install dependencies.

- [Supabase CLI](https://supabase.com/docs/guides/cli)  
  Used to run and deploy edge functions.

- [Git](https://git-scm.com/downloads)  
  Required to clone and manage the repository.

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/artefaxrudralabs/apis_podai.git
cd apis_podai
```

### 2. Install dependencies

```bash
npm install
```

### 3. Install Supabase CLI

```bash
npm install -g supabase
```

### 4. Verify Installation

```bash
supabase --version
```

### 5. Login to Supabase

```bash
supabase login
```

A browser window will open for authentication. Copy the code provided and return to the CLI to complete the login.

![Supabase Login](images/supabase-login.png)

### 6. Link your project

```bash
supabase link --project-ref YOUR_PROJECT_ID
```

To find your `YOUR_PROJECT_ID`, visit your [Supabase Dashboard](https://app.supabase.com/) and copy the project reference from your project settings.

![Project Reference](images/project-ref.png)

### 7. Start local development

```bash
npx supabase start
```

---

## Running Edge Functions Locally

Serve all edge functions:

```bash
supabase functions serve
```

Run a specific function:

```bash
supabase functions serve FUNCTION_NAME
```

---

## Environment Variables

Create a `.env` file in the root directory and add:

```bash
SUPABASE_URL=your_url
SUPABASE_ANON_KEY=your_key
```

Obtain these values from your Supabase project settings.

---

## Deployment

Deploy all edge functions:

```bash
supabase functions deploy
```

Deploy a specific function:

```bash
supabase functions deploy FUNCTION_NAME
```

---

## Project Structure

```
apis_podai/
├── supabase/
│   ├── functions/
│   │   ├── address/
│   │   ├── analytics/
│   │   ├── assets/
│   │   ├── cart/
│   │   ├── orders/
│   │   ├── products-dashboard/
│   │   └── [other functions...]
│   ├── migrations/
│   └── config.toml
├── images/
├── arch_docs/
├── .env
├── package.json
└── README.md
```

---

## Stopping Local Development

```bash
supabase stop
```

---









