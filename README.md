<img width="1440" alt="dashboard_mockup" src="https://github.com/maybe-finance/maybe/assets/35243/a7763d0e-a942-42db-bde7-eb8d28106917">
<sup><i>(Note: The image above is a mockup of what we're working towards. We're rapidly approaching the functionality shown, but not all of the parts are ready just yet.)</i></sup>

# Maybe: The OS for your personal finances

<b>Get involved: [Discord](https://link.maybe.co/discord) • [Website](https://maybe.co) • [Issues](https://github.com/maybe-finance/maybe/issues)</b>

_If you're looking for the previous React codebase, you can find it at [maybe-finance/maybe-archive](https://github.com/maybe-finance/maybe-archive)._

## Backstory

We spent the better part of 2021/2022 building a personal finance + wealth management app called, Maybe. Very full-featured, including an "Ask an Advisor" feature which connected users with an actual CFP/CFA to help them with their finances (all included in your subscription).

The business end of things didn't work out, and so we shut things down mid-2023.

We spent the better part of $1,000,000 building the app (employees + contractors, data providers/services, infrastructure, etc.).

We're now reviving the product as a fully open-source project. The goal is to let you run the app yourself, for free, and use it to manage your own finances and eventually offer a hosted version of the app for a small monthly fee.

## Local Development Setup

### Requirements

- Ruby >3 (see `Gemfile`)
- PostgreSQL >9.3 (ideally, latest stable version)

After cloning the repo, the basic setup commands are:

```sh
cd maybe
cp .env.example .env
bin/setup
bin/dev
```

And visit http://localhost:3000 to see the app. You can use the following credentials to log in (generated by DB seed):

Email: `user@maybe.local`
Password: `password`

For further instructions, see guides below.

### Multi-currency support

If you'd like multi-currency support, there are a few extra steps to follow.

1. Sign up for an API key at [Open Exchange Rates](https://openexchangerates.org/signup). For now, you'll need the Developer plan, which is $12/mo.
2. Add your API key to your `.env` file.
3. Set the currencies you'd like to support in the `.env` file.
4. Run `rake currencies:seed`
5. Run `rake exchange_rates:sync`

### Setup Guides

#### Dev Container (optional)

This is 100% optional and meant for devs who don't want to worry about installing requirements manually for their platform. You can follow [this guide](https://code.visualstudio.com/docs/devcontainers/containers) to learn more about Dev Containers.

#### Mac

Please visit our [Mac dev setup guide](https://github.com/maybe-finance/maybe/wiki/Mac-Dev-Setup-Guide).

#### Linux

Please visit our [Linux dev setup guide](https://github.com/maybe-finance/maybe/wiki/Linux-Dev-Setup-Guide).

#### Windows

Please visit our [Windows dev setup guide](https://github.com/maybe-finance/maybe/wiki/Windows-Dev-Setup-Guide).

### Testing Emails

In development, we use `letter_opener` to automatically open emails in your browser. When an email sends locally, a new browser tab will open with a preview.

## Contributing

Before contributing, you'll likely find it helpful to [understand context and general vision/direction](https://github.com/maybe-finance/maybe/wiki).

Once you've done that, please visit our [contributing guide](https://github.com/maybe-finance/maybe/blob/main/CONTRIBUTING.md) to get started!

## Self Hosting

Our long term goal is to make self-hosting as easy as possible. That said, during these early stages of building the product, we are focusing our efforts on development.

We will update this section as we get closer to an initial release.

Please see our [guide on self hosting here](https://github.com/maybe-finance/maybe/wiki/Self-Hosting-Setup-Guide).

### Env Vars

| ENV Name | Default |
| --: | :-- |
| ASSUME_SSL | ? |
| FORCE_SSL | ? |
| RAILS_ENV | ? |
| SECRET_KEY_BASE | ? |
| SSL_ENABLE | ? |
| RAILS_MAX_THREADS | ? |
| HOSTED | ? |
| APP_DOMAIN | ? |
| SMTP_ADDRESS | ? |
| SMTP_PORT | ? |
| SMTP_USERNAME | ? |
| SMTP_PASSWORD | ? |
| TLS | ? |
| DB_HOST | ? |
| POSTGRES_PASSWORD | ? |
| POSTGRES_USER | ? |


## Repo Activity

![Repo Activity](https://repobeats.axiom.co/api/embed/7866c9790deba0baf63ca1688b209130b306ea4e.svg "Repobeats analytics image")

## Copyright & license

Maybe is distributed under an [AGPLv3 license](https://github.com/maybe-finance/maybe/blob/main/LICENSE). "Maybe" is a trademark of Maybe Finance, Inc.