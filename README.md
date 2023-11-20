# Try Docker Compose

From your project directory, start up your application by running `docker compose up`

If you want to run your services in the background, you can pass the `-d` flag (for "detached" mode) to docker `compose up` to see what is currently running:
`docker compose ps`

The `docker compose run` command allows you to run one-off commands for your services.
For example, to see what environment variables are available to the "web" service:
`docker compose run web env`

`docker image ls` to list local images

You can inspect images with `docker inspect <tag or id>`

If you started Compose with `docker compose up -d`, stop your services once you've finished with them:
`docker compose stop`

Stop the application, either by running `docker compose down` from within your project directory in the second terminal, or by hitting CTRL+C in the original terminal where you started the app.

You can bring everything down, removing the containers entirely, with the  `down` command. Pass `--volumes` to also remove the data volume used by the Redis container:
`docker compose down --volumes`
