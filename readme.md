# Popup JS

Popup.js is a lightweight JavaScript library that provides a simple way to create alerts for your web application. It's easy to use and customize, and works well with modern web browsers.

> [!NOTE]  
> Visit [this page](https://alphabrate.github.io/popupjs/code/showcase/) for sample.

## Features

* Alerts: Display customizable alert messages with icons and callbacks.
* Popups: Create modal popups with titles, messages, and buttons.
* Pull-Outs: Create pull-out notifications that can be swiped away.

## Usage

To use PopupJS in your web application, include the following CSS and JavaScript files in your HTML document:

```html
<head>
    <link rel="stylesheet" href="popup.css">
</head>
<body>
    <script src="popup.js"></script>
</body>
```

You can use our cdn-hosted files:

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/alphabrate/popupjs/pu.min.css">
<link rel="stylesheet" href="https://alb-cdn.web.app/popupjs/pu.min.css">

<script src="https://cdn.jsdelivr.net/gh/alphabrate/popupjs/pu.min.js"></script>
<script src="https://alb-cdn.web.app/popupjs/pu.min.js"></script>
```


You can then use the `pujs` object to create alerts, popups, and pull-outs in your application.

### Alerts

* `pujs.alert(message, type, timeout, selectable)`: Display an alert message with an icon and optional callback.
	+ `message` [String]: The alert message to display.
	+ `type` [String]: The type of alert (error, success, etc.).
	+ `timeout` [Integer]: The time in milliseconds to display the alert.
	+ `selectable` [Bool]: Whether the alert text is selectable.

### Popups

* `pujs.popup(title, message, buttons, buttonType, input)`: Create a modal popup with a title, message, and buttons.
	+ `title` [String]: The title of the popup.
	+ `message` [String]: The message to display in the popup.
	+ `buttons` [Array]: An array of button objects with text and callback properties.
        ```js
        [
            { text: 'Action 1', callback: function() { }, color: '[OPTIONAL]' },
            { text: 'Action 2', callback: function() { } }
        ]
        ```
	+ `buttonType` [String]: The type of buttons to display (vert or horiz).
	+ `input` [JSON]: An optional input field to include in the popup.
    ```js
    {
        type: 'text',
        placeholder: 'Enter your name',
        value: 'John Doe'
    }
    ```
    > The value will be stored on `pujs.popup.value` [String]

### Pull-Outs

* `pujs.pullOut(html, scroll, id)`: Create a pull-out notification with customizable HTML content.
	+ `html` [String]: The HTML content to display in the pull-out.
	+ `scroll` [Bool]: Whether the content of the pull-out should be scrollable.
	+ `id` [String]: An optional ID to assign to the pull-out element.

## Customization

PopupJS provides several options for customizing the appearance and behavior of alerts, popups, and pull-outs. You can modify the CSS styles and icons to fit your application's design.

### To-do

Before or after the alerts, you can add your own events using `pujs.setup.todo`

```js
todo: {
    alert: {
        start: () => { },
        end: () => { }
    },
    pullOut: {
        start: () => { },
        end: () => { }
    },
    popup: {
        start: () => { },
        end: () => { }
    }
},
```

## Browser Support

PopupJS is compatible with modern web browsers, including Chrome, Firefox, Safari, and Edge.

## Copyright

© AlphaBrate 2024. Released under the APEL.

## Credit

### Design Resources (Template)

* [Apple Design Resources](https://developer.apple.com/design/resources/)