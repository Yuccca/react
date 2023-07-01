# [React](https://reactjs.org/) &middot; [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE) [![npm version](https://img.shields.io/npm/v/react.svg?style=flat)](https://www.npmjs.com/package/react) [![CircleCI Status](https://circleci.com/gh/facebook/react.svg?style=shield&circle-token=:circle-token)](https://circleci.com/gh/facebook/react) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://reactjs.org/docs/how-to-contribute.html#your-first-pull-request)

React is a JavaScript library for building user interfaces.

* **Declarative:** React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes. Declarative views make your code more predictable, simpler to understand, and easier to debug.
* **Component-Based:** Build encapsulated components that manage their own state, then compose them to make complex UIs. Since component logic is written in JavaScript instead of templates, you can easily pass rich data through your app and keep the state out of the DOM.
* **Learn Once, Write Anywhere:** We don't make assumptions about the rest of your technology stack, so you can develop new features in React without rewriting existing code. React can also render on the server using Node and power mobile apps using [React Native](https://reactnative.dev/).

[Learn how to use React in your project](https://reactjs.org/docs/getting-started.html).

## Installation

React has been designed for gradual adoption from the start, and **you can use as little or as much React as you need**:

* Use [Online Playgrounds](https://reactjs.org/docs/getting-started.html#online-playgrounds) to get a taste of React.
* [Add React to a Website](https://reactjs.org/docs/add-react-to-a-website.html) as a `<script>` tag in one minute.
* [Create a New React App](https://reactjs.org/docs/create-a-new-react-app.html) if you're looking for a powerful JavaScript toolchain.

You can use React as a `<script>` tag from a [CDN](https://reactjs.org/docs/cdn-links.html), or as a `react` package on [npm](https://www.npmjs.com/package/react).

## Documentation

You can find the React documentation [on the website](https://reactjs.org/).  

Check out the [Getting Started](https://reactjs.org/docs/getting-started.html) page for a quick overview.

The documentation is divided into several sections:

* [Tutorial](https://reactjs.org/tutorial/tutorial.html)
* [Main Concepts](https://reactjs.org/docs/hello-world.html)
* [Advanced Guides](https://reactjs.org/docs/jsx-in-depth.html)
* [API Reference](https://reactjs.org/docs/react-api.html)
* [Where to Get Support](https://reactjs.org/community/support.html)
* [Contributing Guide](https://reactjs.org/docs/how-to-contribute.html)

You can improve it by sending pull requests to [this repository](https://github.com/reactjs/reactjs.org).

## Examples

We have several examples [on the website](https://reactjs.org/). Here is the first one to get you started:

```jsx
import { createRoot } from 'react-dom/client';

function HelloMessage({ name }) {
  return <div>Hello {name}</div>;
}

const root = createRoot(document.getElementById('container'));
root.render(<HelloMessage name="Taylor" />);
```

This example will render "Hello Taylor" into a container on the page.

You'll notice that we used an HTML-like syntax; [we call it JSX](https://reactjs.org/docs/introducing-jsx.html). JSX is not required to use React, but it makes code more readable, and writing it feels like writing HTML. If you're using React as a `<script>` tag, read [this section](https://reactjs.org/docs/add-react-to-a-website.html#optional-try-react-with-jsx) on integrating JSX; otherwise, the [recommended JavaScript toolchains](https://reactjs.org/docs/create-a-new-react-app.html) handle it automatically.

## Contributing

The main purpose of this repository is to continue evolving React core, making it faster and easier to use. Development of React happens in the open on GitHub, and we are grateful to the community for contributing bugfixes and improvements. Read below to learn how you can take part in improving React.

### [Code of Conduct](https://code.fb.com/codeofconduct)

Facebook has adopted a Code of Conduct that we expect project participants to adhere to. Please read [the full text](https://code.fb.com/codeofconduct) so that you can understand what actions will and will not be tolerated.

### [Contributing Guide](https://reactjs.org/docs/how-to-contribute.html)

Read our [contributing guide](https://reactjs.org/docs/how-to-contribute.html) to learn about our development process, how to propose bugfixes and improvements, and how to build and test your changes to React.

### Good First Issues

To help you get your feet wet and get you familiar with our contribution process, we have a list of [good first issues](https://github.com/facebook/react/labels/good%20first%20issue) that contain bugs that have a relatively limited scope. This is a great place to get started.

### License

React is [MIT licensed](./LICENSE).



# My design portfolio
#### Video Demo:  https://youtu.be/gktFpr10dT4
#### Description:
I've recreated my design portfolio using HTML, CSS, Python, SQL, Flask and Jinja templating.
Since I had created a version with the4 no-code platfrom Webflow, there might be some similarities as I follow the same structure and have added the same case studies.

#### Portfolio
I've added 3 main case studies and 3 playground projects that are real on the index page.
In the About page, you can find a summary of who I am along with a PDF of my Résumé.
Last, in the Contact page, you can leave a message for me to reach out to you! I created a contact.db database to keep track of the person's name, their email along with their message. Here, I do some checls with Python: (1) I check if users inputted content and, if they did (2) I check the email's validity thanks to the robust email address syntax and deliverability validation library for Python 3.7+ by **Joshua Tauberer**. More info on how to install thge library below.

### Files and structure
I leveraged the structure from the Finance project.
I have a directory called ```/templates``` for all my HTML files.
The directory ```/static``` contains all images used and the CSS files.
The file ```app.py``` contains the Python code that I used to create the server.


#### Tech used
I used Flask and Python to build aa web application. It also includes support for Jinja2 templating, which I used since I needed to re-create varios case studies with similar structure of their content.
I used SQL to create my contacts.db database.


# Installation
## Jinja templating
Get details from: https://github.com/pallets/jinja
Install and update using pip:
```
$ pip install -U Jinja2
```

### Example from my code
Contact page:
```
{% extends "layout.html" %}

{% block title %}
    Contact
{% endblock %}

{% block main %}
<section>
    <div class="container-contact">
        <div class="title">
            <h1 class = "title">Want to connect? Say hi!</h1>
        </div>
        <form action="/contact" method="post">
            <div class="form-grid">
                <div class="form-item">
                    <label for="name">Name</label>
                    <input id="name" name="name" type="text" class="input-style">
                </div>
                <div class="form-item">
                    <label for="email">Email</label>
                    <input id="email" name="email" type="email" class="input-style">
                </div>

            </div>
            <div class="form-item">
                <label for="message">Message</label>
                <textarea id="message" name="message" type="text" class="input-style"></textarea>
            </div>
            <input type="submit" class="submit-btn input-style">
        </form>

    </div>
</section>
{% endblock %}
```

## Email validator
Install email-validator from https://pypi.org/project/email-validator/.
This package is on PyPI, so:

```
pip install email-validator
```
(You might need to use pip3 depending on your local environment.)


### Example from my code
Verify validity of email in my Contact page

```
#Check email validity
try:
    val = validate_email(email)
except EmailNotValidError as e:
    return apology("must provide valid email", 403)
```
