# Project setup

## Prettier

To install prettier for both the Ruby backend and the React front end, the configuration file needs to be in the prject root (i.e. in the directory above the front end and the backend). A `.prettierrc` file with the follow settings will have to be initialized:

```
{
"trailingComma": "es5",
"tabWidth": 2,
"semi": true,
"singleQuote": true
}
```

VSCode will let you choose prettier (inluding the rprettier plugin) as the default formatter in the settings. You may have to go intot the `settings.json` file and add the following lines:

```
{
  ...
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.formatOnSave": true,
}
```

This will initialize a new `package.json` file (in addition to the one in the front end folder), which we can use to run npm scripts from the project root, i.e. we can run `yarn start` from the root rather than have to go into the frontend folder.

## Foreman

To start the api and web server with one command we can use the `foreman` gem (needs to be added to the develoment group in the `Gemfile`.). We then need to add the following settings:

```
web: cd frontend && yarn start
api: cd backend && bundle exec rails s -p 3000
```
