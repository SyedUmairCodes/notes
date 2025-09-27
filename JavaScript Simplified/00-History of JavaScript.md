# History and Introduction to JavaScript
JavaScript is a high-level programming language for web development and is also popular in desktop and mobile development as well as for APIs using Node.js  

>[!NOTE ]
>JavaScript is currently being developer and new features and improvements are always being added into JavaScript. 

## History

In 1995, websites were just plain old html files, the Netscape Navigator was the Google Chrome of that time and more than 80% of market share. The creator of NN, Mark Andreessen, wanted the web to more than just simple documents and wanted to make it interactive for the users.

Netscape hired a developer named Brendan Eich, they tasked him with creating a programming language that was easy enough that even a designer or someone new can use.

> [!NOTE]
> The first version was called MOCA and was made in 10 days and was a mix of multiple languages.

Microsoft copied JavaScript and called it JScript when it launched IE. They were the same thing doing the same task from two different companies.

>[!IMPORTANT]
>Websites built using JavaScript worked best on Netscape Navigator and Websites built with JScript worked best on Internet Explorer. Developers had to add a best viewed in IE/NN badges to their websites who couldn't build for both platforms.

# ECMAScript

ECMA international is an industry association founded in 1961, which is dedicated to standardize the communication and information systems. In November 1996 Netscape handed over JavaScript to ECMA to build a standard implementation of the language. This led to other smaller implementors voicing their opinions on the evolution of the language and to keep every thing consistent with all browsers.

ECMA is governing body that standardizes JavaScript versions so that they are same across all web browsers. Each new specification comes with a standard and a committee. JavaScript has the ECMA-262 standard and the committee which works on ECMA-262 is called TC39. 

> [!IMPORTANT]
> Oracle owns the trademark for the name JavaScript, so to avoid any legal issues ECMA calls JavaScript ECMAScript. You will find this when search about the ECMA-262 standard.

> The name ECMAScript is used for the official standard of the ECMA-262 while JavaScript is used while talking about the language in practice.

TC39 stands for technical committee-39. Which consists of members who are generally browser vendors or companies who have invested highly into the language, such as Meta and PayPal.

Companies that are part of the TC39 send delegates who represents their companies at the TC39 meetings. These delegates are the ones who are responsible for creating, approving, or denying any feature that has been proposed to be added to the language. Whenever a new proposal is created, it has to go through certain stages before it can be a part of the official language.

- Stage zero proposals are those that are planned to be presented or don't meet the requirements to move forward.
- Stage one is where the proposal is defined, what problem it solves and how. You also need a high-level API example along with all of the drawbacks and ways to implement it.
- Stage two is where the proposal is ready to be added into the language but needs proper documentation and be production ready.
- Stage three is where the proposal should be finished and only requires feedback from implementors.
- Stage four is the final stage and the proposal now needs written tests and implementors should now have practical experience with it.

## Release schedule:

Since 2016 ECMAScript has been releasing new features that have passed the above criteria and adding them to the official spec. Each version is named with ES followed by the version number. ES6 was released in 2015 which added many new features to the language. Before 2015 the last update to ECMAScript was in 2011 which was called ES5.