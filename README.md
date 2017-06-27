# \<scheduler-component\>

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/HaithemMosbahi/scheduler-component)


A Polymer 2.0 custom element for managing and scheduling events. A high level wrapper for the [FullCalendar](https://fullcalendar.io) library that uses Polymer version 2.0 and ES6.

## Properties and Methods
The scheduler component can be configured and customized like any custom element using properties and methods.

* Attributes

|   Attribute   |      Type      | Default |                                              Description                                               |
| ------------- | ----------------- | ------- | ------------------------------------------------------------------------------------------------------ |
| `header` | *Object* |         | customize the header of the scheduler component.                                                                                                      |
| `events` | *Array* |     []    |  list of events to be displayed on the scheduler.                                                                                                   |
| `default-view` | *String* |     month    | The default view to be displayed on the scheduler.                                                                                                    |

* Methods 

One of the feature of the scheduler component is to provides an easy to use API in order to access to different fuctionalities that are supported by the FullCalendar library.

The list below describes methods that can be used to manipulate the scheduler :

|   Methods   |      Return Type      |   Parameters |                                           Description                                               |
| ------------- | ----------------- | ------- | ------------------------------------------------------------------------------------------------------ |
| `today` | void | -- | Navigates to the current date.                                                                                                     |
| `next` | void | -- | Navigates to the next date based on the current view.
| `prev` | void | -- | Navigates to the previous date based on the current view.                                                                                                     |

## Events
The scheduler element dispatches the events below :
|   Event   |      Detail      |                                              Description                                               |
| ------------- | ----------------- | ------- | ------------------------------------------------------------------------------------------------------ |
| `day-click` | *Object* | customize the header of the scheduler component.                                                                                                      |


## Install
You can install this element using bower :

```
$ bower install scheduler-component --save
```


## Install the Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

## Viewing Your Element

```
$ polymer serve
```

## Running Tests

```
$ polymer test
```

Your application is already set up to be tested via [web-component-tester](https://github.com/Polymer/web-component-tester). Run `polymer test` to run your application's test suite locally.

## Contributing 
Comments, questions, suggestions, issues, and pull requests are all welcome.

* Fork it!
* Create your feature branch: git checkout -b my-new-feature
* Commit your changes: git commit -am 'Add some feature'
* Push to the branch: git push origin my-new-feature
* Submit a pull request :D

## History
TODO: Write history

## Credits
Credits goes to the creator of [FullCalendar](https://fullcalendar.io) library.

## License
MIT License
