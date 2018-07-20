# :newspaper: NY Times ReactJS App :statue_of_liberty:

A `NodeJS`, `MongoDB`, `Express`, and `ReactJS` application where users can query, display, and save articles from the [New York Times Article Search API](http://developer.nytimes.com/). Users can remove saved articles as well.

Please check out the deployed version in Heroku [here]!

Click on the headlines to be re-directed to the full New York Times articles.

## Functionality

On the backend, the app uses `express` to serve routes and `mongoose` to interact with a `MongoDB` database.

On the frontend, the app uses `ReactJS` for rendering components, `axios` for internal/external API calls, and `bootstrap` as a styling framework.

In order to transpile the JSX code, `webpack` and `babel` were utilized. All of the JSX code in the `/app` folder was transpiled into the `bundle.js` file located in the `/public` folder.

## Screenshots

#### Users are able to submit a topic, start year, and end year to query the New York Times

![Query Articles](/screenshots/query-articles.png)

#### Press the green, save button and the article is bookmarked via an `/api/saved` post route

![Article Content](/screenshots/add-bookmark.png)

#### Press the red, remove button and the bookmarked article is removed via an `/api/delete/:id` post route

![Add Comment](/screenshots/remove-bookmark.png)

#### Note that the get routes include an **internal route** to `/api/saved` for querying and displaying all the bookmarked articles from the Mongo database.

#### Note that the get routes also include an **external route** to `https://api.nytimes.com/svc/search/v2/articlesearch.json` for querying the New York Times.
