# React Boilerplate V2

### Overview

Boilerplate for React Development with Redux, Firebase, SCSS, Webpack, Babel 7, Polyfill, Express, Jest, Enzyme, ESLint, Prettier, and more.

### Requirements
Node 10.14.1 LTS due to Firebase dependency.

### Dependencies

Yarn add will install the following dependencies. Modify to taste.

```
  "dependencies": {
    "@babel/cli": "^7.1.0",
    "@babel/core": "^7.1.6",
    "@babel/plugin-proposal-class-properties": "^7.1.0",
    "@babel/plugin-proposal-object-rest-spread": "^7.0.0",
    "@babel/preset-env": "^7.1.6",
    "@babel/preset-react": "^7.0.0",
    "@firebase/app-types": "^0.3.2",
    "babel-core": "^7.0.0-bridge.0",
    "babel-loader": "^8.0.2",
    "babel-polyfill": "^6.26.0",
    "css-loader": "^1.0.1",
    "dotenv": "^6.2.0",
    "enzyme": "^3.7.0",
    "enzyme-adapter-react-16": "^1.7.0",
    "enzyme-to-json": "^3.3.4",
    "express": "^4.16.4",
    "firebase": "^5.6.0",
    "history": "^4.7.2",
    "moment": "^2.22.2",
    "node-sass": "^4.10.0",
    "normalize.css": "^8.0.1",
    "numeral": "^2.0.6",
    "prop-types": "^15.6.2",
    "raf": "^3.4.1",
    "react": "^16.6.3",
    "react-dates": "^18.2.2",
    "react-dom": "^16.6.3",
    "react-modal": "^3.6.1",
    "react-redux": "^5.1.1",
    "react-router-dom": "^4.3.1",
    "react-with-direction": "^1.3.0",
    "redux": "^4.0.1",
    "redux-mock-store": "^1.5.3",
    "redux-thunk": "^2.3.0",
    "sass-loader": "^7.1.0",
    "style-loader": "^0.23.1",
    "uuid": "^3.3.2",
    "validator": "^10.8.0",
    "webpack": "^4.25.1"
  },
  "devDependencies": {
    "babel-eslint": "^10.0.1",
    "babel-jest": "^23.6.0",
    "cross-env": "^5.2.0",
    "eslint": "^5.9.0",
    "eslint-config-airbnb": "^17.1.0",
    "eslint-config-prettier": "^3.3.0",
    "eslint-plugin-import": "^2.14.0",
    "eslint-plugin-jsx-a11y": "^6.1.2",
    "eslint-plugin-prettier": "^3.0.0",
    "eslint-plugin-react": "^7.11.1",
    "extract-text-webpack-plugin": "^4.0.0-beta.0",
    "jest": "^23.6.0",
    "prettier": "^1.15.2",
    "react-test-renderer": "^16.6.3",
    "regenerator-runtime": "^0.12.1",
    "webpack-cli": "^3.1.2",
    "webpack-dev-server": "^3.1.10"
  }
  
```
  
## Firebase
	
Add a firebase/firebase.js file in the src folder with your own firebase configuration object:
	
```firebase.js
import firebase from 'firebase/app';
import 'firebase/database';
	
const config = {
  apiKey: '<apiKey>',
  authDomain: '<authDomain>',
  databaseURL: '<databaseURL>',
  projectId: '<projectId>',
  storageBucket: '<storageBucket>',
  messagingSenderId: '<messagingSenderId>'
};
	
firebase.initializeApp(config);

const database = firebase.database();hero

export { firebase, database as default };
```

``` .env.development / .env.test
	
FIREBASE_API_KEY=<apiKey>
FIREBASE_AUTH_DOMAIN=<authDomain>
FIREBASE_DATABASE_URL=<databaseURL>
FIREBASE_PROJECT_ID=<projectId>
FIREBASE_STORAGE_BUCKET=<storageBucket>
FIREBASE_MESSAGING_SENDER_ID=<messagingSenderId>
	
```
