# Development
To clarify, web development and in house development should be in the same category. We want to use the same set of standards and tools regardless if the app is public facing or an internally focused app.

## Styling

### Current
Should follow a design 

- [Sass](https://sass-lang.com/) (preferred)
- Latest CSS (rules must work in the current browswers we support)

### Roadmap
Each type of application should have their own design guide and when applicable have documented reusable components that can be quickly implmented within your application(s).

- TBD

## Javascript

### Current
- React
- [AngularJs](https://angularjs.org/)
- jQuery
- Vanilla Javascript (latest greatest with [BabelJs](https://babeljs.io/) for IE support)

### Roadmap
All apps should be built with the concept of [Atomic Design](http://bradfrost.com/blog/post/atomic-web-design/). Those components should focused and reusable.

- React
- Vanilla Javascript

## Running Tasks
We do things like minifying javacript, compiling sass, compiling es6 code. We use Gulp to manage those tasks, importing NPM packages to help us do what we need to do.

### Current
- Gulp
- Webpack (in react apps)

### Road
- TBD

## Managing Code
We use git with TFS to manage our code following a standard Microsoft [branching strategry](https://docs.microsoft.com/en-us/vsts/git/concepts/git-branching-guidance?view=vsts)

## Browser Support

### Current
We support all major browers and applications should be responsive (look good on a mobile device)

### Roadmap
We support all major browers and applications **MUST** be responsive (look good on a mobile device)

### Major Browsers
- Internet Explorer 11+
- Edge
- Chrome
- Firefox (IMPORTANT: we cannot exclude firefox for public facing applications because we cannot control what browsers constituents use, and firefox is still widely [used](https://www.stetic.com/market-share/browser/).)
- Safari
