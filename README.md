# Harmoni
Harmoni is a website to manage events. The website allows organizers to create events and link artists to them. Users who interested in these events can read about them, buy tickets or volunteer.

##Libraries
The website was developed using TypeScript. For all the libraries that were used, in some cases it was also necessary to download type libraries to inform TypeScript about types that were not originally defined in JavaScript.

###Client
In the client, React used to develop and manage user interfaces. Of the components that has been developed, some were largely reusable and in the form of widgets. An example is eventGrid.tsx, which is used on the front page to show current and upcoming events, and is also used on the user's profile to show events it is associated with. Other components are more specific. Examples of these are those located in the Pages folder. An example is pageNotFound.tsx, which is used if the user arrives at a non-existent url.
Library used for the design of the components are styled-components, which gave the opportunity to create simple css-components. In this way, all styling was reserved for a component placed in the same file.
To make the website a one-page application it has been used react-router. It automatically checks with regard to the url which page components to display. Then the website does not have to retrieve each and every page from the server.

Other libraries worth noting:


* React bootstrap:

Used to construct navigation bar, lists and dropdown.

* Material UI:

Used to construct forms, eg login, registration and creation of events.
* React-loading-skeleton:

Used to achieve lazy-loading. Lazy-loading is that instead of having a blank white page while data is being retrieved from the server, it has empty, animated gray boxes where the data will be displayed later.
* Google Map React:

Offers a component that makes it easier to implement google maps into the react application.
* React-big-calendar:

Offers a calendar component that takes in custom date objects to easily view them.
* React bootstrap typeahead:

Works as a search field and is used to search for artists when these are to be linked to an event.
* React icons:

Library with several icons.

In order for the components to talk to the database, they use Service Classes. These classes import the axios library, which simplifies HTTP requests.
JEST and enzyme are used For testing the reusable components. JEST is a framework for setting up test files and writing easy-to-understand tests. Enzyme makes it possible to simulate inputs on the components to ensure that they behave as expected.

###Server
For the server part of the project,Express is used to set up an API. The API is made up of different http routers, which return data based on any parameters. From the section above, axios were mentioned. The Axios calls communicate directly with these routes. The HTTP routes use methods from the classes located in the DAO folder. DAO stands for Data-Access-Object and creates an interface to the database. Dao classes use the mysql library to query a mysql database. The JEST test library was used to test the dao classes.

Other libraries worth noting:

* Nodemailer

Library for sending mail. Used, for example, to send links for resetting passwords to users.


* Geocoder-free

Free service for translating addresses into coordinates.



* SJCL (Stanford JavaScript Crypto Library)

Used for hashing user passwords.



* Dotenv

Used to load environment variables from file.



* Jsonwebtoken

Library to generate tokens that can be used to verify users.



* Body-parser

Provides access to the body attribute in http requests.