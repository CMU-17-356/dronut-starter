# dronut-starter
In order to get ready to write productive code, complete the following steps during Sprint 0:

## Repository Setup

1. Create a new team and GitHub repository for your project using [GitHub classroom](https://classroom.github.com/a/eG2wmAqU).

   Your associated *cmu email* should show up in a listing and you can link your GitHub account.
   Subsequent members should choose to join an existing team using the same link.
   Message us on [Slack](https://cmu-17-776-s24.slack.com/) if you run into
   issues and we can add you directly.

   You may want to name your repository something like `foobarbaz`, which
   will end up as `dronuts-2024-foobarbaz`, aka your *$respository_name*.

   Your repository is made private to start, but we're ok with you making it
   public if you want. If you make it public, don't forget to add `.gitignore`
   and `License` files!

2. In addition, you should setup any tools needed for collaboration, issue
   tracking and project managment; Slack, Jira, GitHub Issues, ZenHub, Trello,
   whatever it is your team would like to use.

   If you're new to Git and GitHub, we highly recommend reading the
   [GitHub Documentation](https://docs.github.com/).

## Github Actions

Enable Github Actions. To do this, [these steps can be followed](https://docs.github.com/en/actions/quickstart).

## Initialize NodeJS/NPM

1. If you haven't already, install NodeJS and NPM on your computer.

2. Initialize your repository for NPM by running `npm init`. This will generate
   a `package.json` file in your repository.

### Web Framework

Within the NodeJS runtime, there a many frameworks for creating
server applications. For the purposes of this assignment, we recommend
the [Express Framework](https://expressjs.com/), which is a development
framework with widespread adoption

### QA/Helpful Tools

1. You should install a linter for your repository, to help manage code style.
   We highly recommend [eslint](https://eslint.org/docs/user-guide/getting-started)
   or [tslint](https://palantir.github.io/tslint/) if you decide to use typescript.

   To go a little further, we can use
   [eslint-watch](https://www.npmjs.com/package/eslint-watch) to automatically lint
   while we're programming:

   > Success Condition:
   > ```
   > $ npm run lint (## which is calling esw -w src test)
   > > ✓ Clean (10:12:27 AM)
   > ```

2. Because NodeJS projects have many dependencies, it is massively beneficial to
   use a tool to detect dependency updates and alert you as to potential
   vulnerabilities. Normally, we would recommend using a SaaS tool like
   [GreenKeeper](https://greenkeeper.io/) or [requires.io](https://requires.io/).
   However, if you're repository is private, these tools require payment. If
   that's the case, you should install [npm-check](https://www.npmjs.com/package/npm-check).

   > Success Condition:
   > ```
   > $ npm-check
   > > ❤️  Your modules look amazing. Keep up the great work. ❤️
   > ```

3. You should setup a test framework within your application to help with later
   test-driven development. We'd suggest [Jest](https://jestjs.io/) (especially for React
   development). Another option is to go with the [Mocha](https://mochajs.org/)
   framework along with [Chai](http://chaijs.com/). Once installed, write a
   single test, which doesn't actually test anything (besides that your tests run).

    > Success Condition:
    > ```
    > $ npm run test
    > > PASS test/routes.test.js
    > > GET /
    > > ✓ should render properly (853ms)
    > > GET /list
    > > ✓ should render properly with valid parameters (48ms)
    > > ✓ should error without a valid parameter (29ms)
    > > GET /404
    > > ✓ should return 404 for non-existent URLs (61ms)
    > > ...
    > ```

4. Verify that the above tools and targets can be executed by Github Actions.

5. Document the above tools in your README. Also update this boilerplate once
   it's no longer needed.

## Docker

Although Docker should already be configured (see `Dockerfile` and `docker-compose.yml`) as
necessary, you may need to install the Docker Daemon on your machine to properly
complete the assignment. Read the
[get-started](https://www.docker.com/get-started) guide for downloading Docker
locally. If you're on a Linux OS, starting
[here](https://docs.docker.com/machine/install-machine/) would be more helpful.
**MAKE sure you do not install docker via snap. Snap's version of docker is outdated**.

