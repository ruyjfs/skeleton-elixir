# SkeletonElixir

    docker run -it --rm --name elixir -p 4000:4000 -v "$PWD":"/var/www" -w "/var/www" elixir:slim /bin/bash

    mix local.hex --force

    mix archive.install hex phx --force

    mix archive.install hex phx_new --force

    mix phx.new skeleton_elixir --no-html --no-webpack

    cd skeleton_elixir

    mix phx.server

    mix archive.install hex absinthe

    mix archive.install hex absinthe_plug absinthe_ecto --force

    mix ecto.create

    mix deps.get

Create DB
mix ecto.create

mix ecto.gen.migration create_people

mix ecto.migrate

## Run with docker

```
  docker-compose up
```

To start your Phoenix server:

- Install dependencies with `mix deps.get`
- Create and migrate your database with `mix ecto.setup`
- Start Phoenix endpoint with `mix phx.server`

Now you can visit [`localhost:4000`](http://localhost:4000) from your browser.

Ready to run in production? Please [check our deployment guides](https://hexdocs.pm/phoenix/deployment.html).

## Learn more

- Official website: http://www.phoenixframework.org/
- Guides: https://hexdocs.pm/phoenix/overview.html
- Docs: https://hexdocs.pm/phoenix
- Mailing list: http://groups.google.com/group/phoenix-talk
- Source: https://github.com/phoenixframework/phoenix
