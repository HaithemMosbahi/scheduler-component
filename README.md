# \<scheduler-component\>

[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/HaithemMosbahi/scheduler-component)
[![Build Status](https://travis-ci.org/HaithemMosbahi/scheduler-component.svg?branch=master)](https://travis-ci.org/HaithemMosbahi/scheduler-component)
[![Bower version](https://badge.fury.io/bo/scheduler-component.svg)](https://badge.fury.io/bo/scheduler-component)
[![Gitter](https://img.shields.io/gitter/room/nwjs/nw.js.svg)](https://gitter.im/scheduler-component)


A Polymer 2.0 custom element for managing and scheduling events. A high level wrapper for the [FullCalendar](https://fullcalendar.io) library that uses Polymer version 2.0 and ES6.

The scheduler makes it easy to configure and customize the full calendar component
in a more declarative way and without worring about the implementation details.

Being a web component that follows custom elements V1 specifications, the scheduler
can be ineroperable with other JS frameworks such as Angular and Vue.js.

## Features 

* Manage and schedule events.
* Customize and configure the scueduler using properties.
* Build advanced calendar / scheduler in a declarative manner.
* Organize events using categories ( e.g Work, Holiday, Meeting)
* Show / Hide events by selecting / deselecting categories.

## Demo
A live [demo](https://www.webcomponents.org/element/HaithemMosbahi/scheduler-component/demo/demo/index.html) of the scheduler component is hosted on webcomponents.org.

![alt text](demo/scheduler.png "A simple scheduler with categories")

## Install
You can install this element using bower :

```
$ bower install --save HaithemMosbahi/scheduler-component
```

## Usage
1. Import scheduler-component

Once you have installed this element, you can import it in your project using HTML import :

```html
  <link rel="import" href="bower_components/scheduler-component.html">
```

2. Start using it :

Once the element is imported , you can start using the scheduler in your application :

```html
  <scheduler-component>
  </scheduler-component>
```


## Properties and Methods
The scheduler component can be configured and customized like any custom element using properties and methods.

* *Attributes* 

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
| `scroll-time` | *String* |     06:00:00    | Time on which the scroll becomes  enabled.               |
| `text-color` | *String* |   #FFFFFF     | Text color to be applied for each event. 
| `event-color` | *String* |    #3a87ad    | Background color to be applied for each event. 
| `show-categories` | *Boolean* |    false    | Wether to show categories in the bottom of the scheduler or not. This is linked to the categories property.    
| `categories` | *Array* |    []    | events's catgories. A Category has the following properties : label (required - string ), color (string) and hidden ( default is false, wether to show the events related to this category or not.)|        

* *Methods* 

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
| `incrementDate` | void | duration | Increments the date displayed on the scheduler by the given duration.                                                                                                    |

## Events
The scheduler element dispatches the events below :

|   Event   |      Detail      |                                              Description                                               |
| ----------------------- | -------------------- | ---------------------------------------------------------------------------------------- |
| `day-click` | *{ date, jsEvent, view }* | Fired when a day on the scheduler is clicked                                                                                                      |
| `event-click` | *{calEvent, jsEvent, view }* | Fired when an event on the scheduler is clicke                                                                                                      |
| `event-mouse-over` | *{ calEvent, jsEvent, view }* | Fired when a mouse over on event is detected                                                                                                      |
| `event-mouse-out` | *{ calEvent, jsEvent, view }* | Fired a mouse out on event is detected.                                                                              |
| `event-drag-start` | *{ event, jsEvent, ui, view }* | Fired when a drag start on event is detected.                                                                             |
| `event-drag-end` | *{ event, jsEvent, ui, view }* | Fired when a frag end on one event is detected.                                                                                   |
| `drop` | *{ date, jsEvent, ui, resourceId }* | Fired when an element is dropped on the scheduler. This is only dispatched when the droppable mode of the scheduler is set to true.                                                                                                     |
| `event-drop` | *{ event, delta, revertFunc, jsEvent, ui, view }* | Dispatched when an event element has been dropped on the scheduler.                                                                                   |
| `event-resize-start` | *{ event, jsEvent, ui, view }* | Fired when resize operation on one event is started.                                                                           |
| `event-resize-end` | *{ event, jsEvent, ui, view }* | Fired when resize operation on one event is ended.                                                                                                      |
| `event-resize` | *{ event, delta, revertFunc, jsEvent, ui, view }* | Fired when an event has been resized                                                                                   |
| `view-render` | *{ view, element }* | Dispatched when the view of the scheduler is rendered. A navigation between days, weeks or months will fire this event                                                                                    |
| `view-destroy` | *{ view, element }* | Dispatched when the view is destroyed.                                                                               |


## RoadMap

Scheduler V 1.x

- [x] A declarative web component that wraps the fullCalendar library 

- [x] Customize and configure the scheduler using properties

- [x] Dispatch events as they occur ( click on event, click on day, change view , etc )

- [x] Organize scheduler's events using categories 
    
   - [x] Show / Hide categories in the bottom of the scheduler

   - [x] Show / Hide events when select / deselect a category 

  - [x] Coloration of events based on categories


Scheduler V 2.x

- [ ] Add default view, create and edit templates

- [ ] Support overriding view, create and edit templates


## Development 

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your element locally.

* Viewing Scheduler Element

```
$ polymer serve
```

* Running Tests

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
