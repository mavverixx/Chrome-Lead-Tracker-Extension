# Chrome Lead Tracker Extension

This project is a Chrome Extension built to help users track and save leads effectively. It offers a user-friendly interface to manually enter leads or capture the current tab's URL with a single click. Saved leads are displayed as clickable links, and you can delete all leads with a double-click.

## Table of Contents

- [Overview](#overview)
  - [The Challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My Process](#my-process)
  - [Built With](#built-with)
  - [What I Learned](#what-i-learned)
  - [Continued Development](#continued-development)
  - [Useful Resources](#useful-resources)
- [Installation & Running the Project](#installation--running-the-project)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The Challenge

The challenge was to create a Chrome Extension that allows users to:
- Capture the active tab's URL with a single click and save it as a lead.
- Manually enter and save leads using an input field.
- Display all saved leads as clickable links.
- Delete all leads through an intuitive user action.

This was accomplished using HTML, CSS, and vanilla JavaScript, taking advantage of Chrome’s Extension APIs (Manifest V3) and localStorage for data persistence.

### Screenshot

![Chrome Lead Tracker Extension Screenshot](./screenshot.jpg)

*Include a screenshot of your extension popup to showcase its design.*

### Links

- Repository URL: [Chrome Lead Tracker Extension](https://github.com/mavverixx/Chrome-Lead-Tracker-Extension)
- Live Demo: *(if available)*

## My Process

### Built With

- **HTML5 & CSS3:** For a responsive and clean UI
- **Vanilla JavaScript:** For handling user actions and interacting with the Chrome Tabs API
- **Vite:** As a modern development tool for building and serving the project
- **Chrome Extension APIs (Manifest V3):** Providing the necessary permissions and UI for the extension
- **localStorage:** To persist user data across sessions

### What I Learned

Working on this project increased my proficiency in:
- Developing Chrome Extensions using the latest Manifest V3 standards
- Utilizing the `chrome.tabs.query` API to capture the active tab's URL
- Implementing data persistence using localStorage
- Structuring a small, efficient project with Vite as a development server

Example snippet handling tab capture:
```js
chrome.tabs.query({ active: true, currentWindow: true }, function(tabs){
    myLeads.push(tabs[0].url)
    localStorage.setItem("myLeads", JSON.stringify(myLeads))
    render(myLeads)
})
```
Continued Development

Future enhancements may include:

Adding features to edit or categorize individual leads
Improving the UI/UX based on user feedback
Integrating additional data enrichment from external sources
Useful Resources
Chrome Extensions Documentation
Vite Documentation
MDN Web Docs on localStorage
Scrimba Frontend Developer Career Path
Installation & Running the Project

To get started locally:

Clone the repository:
git clone https://github.com/mavverixx/Chrome-Lead-Tracker-Extension.git

Navigate into the project directory:
cd Chrome-Lead-Tracker-Extension

Install the dependencies:
npm install

Start the development server:
npm start

Load the extension in Chrome:
Open Chrome and go to chrome://extensions/
Enable "Developer mode"
Click "Load unpacked" and select the project folder

Author

[LinkedIn](https://www.linkedin.com/in/rikkihenry/)

Acknowledgments

Special thanks to Scrimba for pushing me to build real-world projects that strengthen my development skills, and to the Chrome Extension community for providing excellent documentation and resources.

Happy Coding!

