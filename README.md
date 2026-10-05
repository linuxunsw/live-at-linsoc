# Live@LNSC

This is the website for UNSW Linux Society's lightning talks series "Live@LNSC".

## Design

I am intentionally not creating a "reusable set of components" for the project.
This is because we want to give each instance of the event a unique aesthetic.
As we host more of these sessions, each session will end up with its own theme
that its promotional page is built around.

In addition, we want to facilitate a little bit of custom styling and layout for
each presenter as a way to make things more unique, so I also didn't take steps
to prevent duplication on that front.

## Updating to prep for a new event

1. Move the old page into a subdirectory (eg `26t3w4` for the one in 26t3, week 4).
2. Update the root page with a new aesthetic.
3. You should keep the aesthetic for the old page intact if possible.
4. At some point we need to create a "past events" list for the main page.

## Developing

Once you've created a project and installed dependencies with `npm install` (or `pnpm install` or `yarn`), start a development server:

```sh
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

In addition:

* Run linting: `npm run lint`
* Run type-checks: `npm run check`

## Building

To create a production version of the site:

```sh
npm run build
```

You can preview the production build with `npm run preview`.
