# ALU GLOBE API Documentation

This repository contains the OpenAPI specifications for the ALU GLOBE application. The documentation is generated using Redoc.

## API Sections

The API is divided into the following sections:

- **Announcements API**: Manages announcements within the application. See the specification in [docs/annoucements.yaml](docs/annoucements.yaml).
- **Comments API**: Handles comments on various resources like posts, announcements, and icebreakers. See the specification in [docs/comments.yaml](docs/comments.yaml).
- **Icebreakers API**: Manages icebreaker questions and interactions. See the specification in [docs/icebreakers.yaml](docs/icebreakers.yaml).
- **Posts API**: Manages user posts within the ALU GLOBE platform. See the specification in [docs/posts.yaml](docs/posts.yaml).

## Building the Documentation

The documentation is built into HTML files using `redoc-cli`. The build process is defined in the [netlify.toml](netlify.toml) file.

To build the documentation locally, you can run the following command:

```sh
mkdir public && \
npx redoc-cli build docs/announcements.yaml -o public/announcements.html && \
npx redoc-cli build docs/comments.yaml -o public/comments.html && \
npx redoc-cli build docs/posts.yaml -o public/posts.html && \
npx redoc-cli build docs/icebreakers.yaml -o public/icebreakers.html
```

This will generate the following HTML files in the `public` directory:

- `public/announcements.html`
- `public/comments.html`
- `public/posts.html`
- `public/icebreakers.html`

## Dependencies

The main dependency for building the documentation is:

- [redoc-cli](https://www.npmjs.com/package/redoc-cli)
