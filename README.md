# Radio4000

The main front-end web application for Radio4000.

See the continous integration: https://gitlab.com/internet4000/radio4000/pipelines

## How to develop

Make sure Ember CLI is installed globally, then clone this project and install it's dependencies:

```
npm install -g ember-cli
git clone git@gitlab.com:internet4000/radio4000.git
cd radio4000
npm install; bower install
npm start
```

## Testing

```
npm run lint
npm test
```

## Deployment

To deploy to staging aka http://much.radio4000.com, run:

`npm run deploy`

To deploy to production aka https://radio4000.com, run:

1. `git checkout master; git pull --rebase; git merge develop --no-ff`
2. (make sure all branches you want are merged in)
3. `release-it`
4. `npm run deploy-production`

## Icons

Add .svg icons to `public/assets/images/icons` and run `gulp icons`.

## Building native apps

Run `npm run build-app`, make some coffee and then check the `dist-electron` folder.

## Important if you use Sublime Text

Sublime automatically watches all files in a folder. Because ember-cli is so huge your PC will slow down. To solve this, tell Sublime to ignore the `tmp` and `node_modules` folder: http://www.ember-cli.com/#sublime-text

## Emberfire

We use Firebase as our backend through Ember Data and [Emberfire](https://github.com/firebase/emberfire).

## Google API

We're using the YouTube API so you might run into trouble with permissions, domains etc. If so, check here https://console.developers.google.com/project/much-play/

## Firebase security rules

Firebase rules are a bitch but see the `rules` folder.
