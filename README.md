# Rails Store — Personal Learning

This is a personal learning project to take my first steps with Ruby on Rails. It provides a minimal base to explore a simple CRUD app (Products), authentication (Sessions/Users), subscriptions, and mailers using modern Rails defaults (Importmap, Turbo, Stimulus, Propshaft).

My goal is to get familiar with the Rails project structure, file-based conventions, and the most used CLI commands.

## Quick setup

Prerequisites:

- Ruby: 3.4.7 (see `.ruby-version`)
- Bundler installed
- SQLite3 (used by default for dev/test)

From the project root:

```bash
bin/setup
```

This installs gems, prepares the database, clears logs/tmp, and starts the dev server unless you pass `--skip-server`.

## Useful commands (from project root)

- Start dev server (Puma on http://localhost:3000):
	```bash
	bin/dev
	```

- Run Rails console:
	```bash
	bin/rails console
	```

- Run migrations / setup DB:
	```bash
	bin/rails db:prepare
	bin/rails db:migrate
	```

- Run tests:
	```bash
	bin/rails test
	bin/rails test:system
	```

- Code quality (optional):
	```bash
	bin/rubocop
	bin/brakeman
	```

## Project structure

Key areas of the app:

- `app/models/` — Active Record models (`Product`, `User`, `Session`, `Subscriber`, ...)
- `app/controllers/` — Controllers for products, sessions, passwords, subscribers, etc.
- `app/views/` — ERB views for pages and mailers
- `app/javascript/` — Importmap entrypoint and Stimulus controllers
- `app/assets/` — Propshaft-managed CSS and images
- `config/routes.rb` — Routes (root: `products#index`)
- `db/` — Migrations and schema (SQLite by default)
- `test/` — Minitest (unit, controller, system tests)

## Resources

- Rails Guides: https://guides.rubyonrails.org/
- Turbo: https://turbo.hotwired.dev/
- Stimulus: https://stimulus.hotwired.dev/
- Importmap: https://github.com/rails/importmap-rails
- Solid Queue: https://github.com/rails/solid_queue
- Solid Cache: https://github.com/rails/solid_cache

