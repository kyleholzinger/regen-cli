# regen-cli
An opinionated React CLI

##Installation

```bash
npm install --global regen-cli
```

##Usage

There are two commands:

```bash
regen project <project name>
regen component <component name>
```

###`regen project <project name>`
Generate a new React project with the name `<project name>`

To set up your project after generating all of the source and config files,
you will need to go into your new directory and run `yarn install` to install
all of your node modules. To start development, use `webpack-dev-server`, which
is a dev dependency of your new project, so you can now run
`./node_modules/.bin/webpack-dev-server`
- expects there to be no folder with name `<project name>`
in the current folder.

###`regen component <component name>`
Generate a new React component with the name `<component name>`
- will put a React component with the name `<component name>`
in `./src/client/app/javascripts/components/` if in the root directory of your project
or if there is a `/` in `<component name>`, otherwise it will put it in the current
folder. Regen expects this folder to exist, and not have a file with the name
`<component name>`.
- passing the `-f` flag to `regen component <component name>` will create a stateless
functional component instead.
