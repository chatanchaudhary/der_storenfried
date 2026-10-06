# der_storenfried

der_storenfried is a single file ai workspace frontend made to work on windows and android

## Concept

the app is basically a place where you can use ai in one workspace without having to jump between a bunch of different apps

it has stuff like

- ai chat
- switching between models and providers
- api key setup
- token and cost estimates
- monthly budget
- requests per hour
- max token limits
- local usage tracking
- recent chats
- file attachments
- voice input
- tools
- android friendly navigation
- desktop windows layout
- light and dark mode
- share and settings

the whole frontend is inside one html file

## Important architecture note

the single html file is only the frontend part

the normal setup should be

android or windows app
then the backend
then the provider api

the backend is where things like provider keys authentication user accounts quotas rate limits token tracking billing model permissions and abuse protection should be handled

stuff stored in localstorage is only for the frontend and should not be treated like real security because users can change browser storage and even the javascript

## Project name

der_storenfried

## Main source

index.html

## Demo behavior

the app can run without a backend right now because it has a small demo response system built in

this lets you test most of the interface without setting everything up first

when the real backend is ready the demo response part can be replaced with the real /api/chat request and the replies can be streamed into the chat

## Android + Windows packaging

the frontend is kept pretty simple on purpose

you can put the html file inside a webview based app or use something like tauri to package it for windows and android

the ui changes based on the device

windows has the desktop sidebar keyboard shortcuts and bigger workspace

android has touch controls bottom navigation safe area support and a smaller chat composer

## API pricing

the model list has some example prices in it for estimating token costs

before using this for real billing the prices should be replaced with current ones from the backend or the actual provider settings

## Running locally

you can open index.html directly in a browser

but for development its better to run it through a local web server because some browser features dont work the same way when opening files with file://

## File layout

```text
der_storenfried/
├── index.html
├── README.md
└── DESCRIPTION.md
