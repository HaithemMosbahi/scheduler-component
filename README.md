# \<scheduler-component\>

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/HaithemMosbahi/scheduler-component)
[![Build Status](https://travis-ci.org/HaithemMosbahi/scheduler-component.svg?branch=master)](https://travis-ci.org/HaithemMosbahi/scheduler-component)


A Polymer 2.0 custom element for managing and scheduling events. A high level wrapper for the [FullCalendar](https://fullcalendar.io) library that uses Polymer version 2.0 and ES6.

## Properties and Methods
The scheduler component can be configured and customized like any custom element using properties and methods.

* Attributes

|   Attribute   |      Type      | Default |                                              Description                                               |
| ------------- | ----------------- | ------- | ------------------------------------------------------------------------------------------------------ |
| `header` | *Object* |         | customize the header of the scheduler component.                                                                                                      |
| `events` | *Array* |     []    |  list of events to be displayed on the scheduler.                                                                                                   |
| `default-view` | *String* |     month    | The default view to be displayed on the scheduler.   
| `weekends` | *Boolean* |     true    | Whether to show the weekends or not.
| `rtl` | *Boolean* |     false    | RTL mode.
| `hidden-days` | *Array* |     []    | List of days to be hidden.  
| `week-numbers` | *Boolean* |     false    | Whether to show week numbers or not    
| `business-hours` | *Object* |     {}    | Object that describes scheduler business hours. 
| `height` | *string* |     {}    | Calendar's height.
| `default-date` | *Object* |     {}    | Default date to be displayed when the scheduler is opened.
| `editable` | *Boolean* |     false    | Enable or disable edit mode.
| `droppable` | *Boolean* |     false    | Whether to allow dropping elements on the scheduler or not.
| `event-start-editable` | *Boolean* |     false    | Whether to allow changing event's start date.
| `event-duration-editable` | *Boolean* |     false    | Whether to allow changing event's end date
| `all-day-slot` | *Boolean* |    true   | Whether to display the all day slot.
| `all-day-text` | *String* |     all-day    | Text to be displayed on the all day slot.
| `slot-duration` | *String* |     00:30:00    | Default slot duration. This duration will be used when a new event is added without specifing its duration. 
| `min-time` | *String* |     00:00:00    | The min time to be displayed on the scheduler.
| `max-time` | *String* |     24:00:00    | The max time to be displayed on the scheduler.
| `scroll-time` | *String* |     06:00:00    | Time on which the scroll becomes  enabled.                                                                        |

* Methods 

One of the feature of the scheduler component is to provides an easy to use API in order to access to different fuctionalities that are supported by the FullCalendar library.

The list below describes methods that can be used to manipulate the scheduler :

|   Methods   |      Return Type      |   Parameters |                                           Description                                               |
| ------------- | ----------------- | ------- | ------------------------------------------------------------------------------------------------------ |
| `today` | void | -- | Navigates to the current date.                                                                                                     |
| `next` | void | -- | Navigates to the next date based on the current view.
| `prev` | void | -- | Navigates to the previous date based on the current view. 
| `getView` | string | -- | Returns the current view of the scheduler.
| `changeView` | void | viewName | Changes the view of scheduler.
| `getDate` | date | -- | Return the current date displayed on the scheduler.
| `goToDate` | void | targetDate | Navigates to the given date.
| `prevYear` | void | -- | Navigates to the next year.
| `nextYear` | void | -- | Navigates to the previous year.
| `incrementDate` | void | duration | Increments the date displayed on the scheduler by the given duration.
                                                                                                    |

## Events
The scheduler element dispatches the events below :

|   Event   |      Detail      |                                              Description                                               |
| ----------------------- | -------------------- | ---------------------------------------------------------------------------------------- |
| `day-click` | *Object* | Fired when a day on the scheduler is clicked                                                                                                      |
| `event-click` | *Object* | Fired when an event on the scheduler is clicke                                                                                                      |
| `event-mouse-over` | *Object* | Fired when a mouse over on event is detected                                                                                                      |
| `event-mouse-out` | *Object* | Fired a mouse out on event is detected.                                                                              |
| `event-drag-start` | *Object* | Fired when a drag start on event is detected.                                                                             |
| `event-drag-end` | *Object* | Fired when a frag end on one event is detected.                                                                                   |
| `drop` | *Object* | Fired when an element is dropped on the scheduler. This is only dispatched when the droppable mode of the scheduler is set to true.                                                                                                     |
| `event-drop` | *Object* | Dispatched when an event element has been dropped on the scheduler.                                                                                   |
| `event-resize-start` | *Object* | Fired when resize operation on one event is started.                                                                           |
| `event-resize-end` | *Object* | Fired when resize operation on one event is ended.                                                                                                      |
| `event-resize` | *Object* | Fired when an event has been resized                                                                                   |
| `view-render` | *Object* | Dispatched when the view of the scheduler is rendered. A navigation between days, weeks or months will fire this event                                                                                    |
| `'view-destroy` | *Object* | Dispatched when the view is destroyed.                                                                               |


## Install
You can install this element using bower :

```
$ bower install --save HaithemMosbahi/scheduler-component
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
