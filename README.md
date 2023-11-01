# meet - an events app

## Project Description
A serverless PWA built with React using test-driven development technique. It uses the Google Calendar API to fetch upcoming events in the city of the user's choosing.

## Features and User Stories

### Feature 1: Filter Events By City
As a user, I would like to be able to filter events by city so that I can see the list of events that take place in that city.

Scenario 1: When user hasn’t searched for a city, show upcoming events from all cities.
- Given the user hasn't searched for a city, when they open the app, then the user should see upcoming events from all cities.

Scenario 2: User should see a list of suggestions when they search for a city.
- Given the main page is open, when the user types into the city textbox, then the user should see a list of cities matching their query.

Scenario 3: User can select a city from the suggested list.
- Given user was typing “Berlin” in the city textbox AND the list of suggested cities is showing, when the user selects a city (e.g., “Berlin, Germany”) from the list, then their city should be changed to that city (i.e., “Berlin, Germany”) AND the user should receive a list of upcoming events in that city.

### Feature 2: Show/Hide Event Details
As a user, I would like to be able to show/hide event details so that I can see more/less information about an event.

Scenario 1: An event element is collapsed by default.
- Given the user has searched for an event, when they get the list of events, then the details will be collapsed by default.

Scenario 2: User can expand an event to see details.
- Given the user has searched for an event, when they click an event, then the details will be expanded.

Scenario 3: User can collapse an event to hide details.
- Given the user has expanded details of an event, when they click it again, then the details be collapsed.

### Feature 3: Specify Number of Events
As a user, I would like to be able to specify the number of events I want to view in the app so that I can see more or fewer events in the events list at once.

Scenario 1: When user hasn’t specified a number, 32 events are shown by default.
- Given the main page is open, when the user hasn't specified a number, then 32 events are shown by default.

Scenario 2: User can change the number of events displayed.
- Given the main page is open, when the user specifies a number, then that number of events are dsiplayed.

### Feature 4: Use the App When Offline
As a user, I would like to be able to use the app when offline so that I can see the events I viewed the last time I was online.

Scenario 1: Show cached data when there’s no internet connection.
- Given the app loaded events at the time it was online, when there is no internet connection, then cached data is shown.

Scenario 2: Show error when user changes search settings (city, number of events).
- Given the user is offline, when the user changes search settings, then show error message.

### Feature 5: Add an App Shortcut to the Home Screen
As a user, I would like to be able to add the app shortcut to my home screen so that I can open the app faster.

Scenario 1: User can install the meet app as a shortcut on their device home screen.
- Given the user wants to open the app faster, when the user installs as a shortcut, then a shortcut to the app will be created in the home screen.

### Feature 6: Display Charts Visualizing Event Details
As a user, I would like to be able to see a chart showing the upcoming events in each city so that I know what events are organized in which city.

Scenario 1: Show a chart with the number of upcoming events in each city.
- Given the user is looking at events, when they click a button to show comparisons, then a chart showing upcoming events in each city appears.

## Serverless
The meet App uses serverless architechture(FaaS) with the help of AWS Lambda and OAuth. This makes the app flexible to add more features and is cost-effective since there is no need to manage any complex server infrastructures. The app can scale based on the traffic.
