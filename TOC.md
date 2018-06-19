# AngularJS - A Retrospective

  + Introduction
    + Disclaimer AngularJS !== Angular
    + What is AngularJS
      + What is an SPA?
      + Why are SPAs significant?
    + Why a retrospective now?
  + History of AngularJS (and SPAs)
    + Who/What/When/Where/Why
    + The JavaScript application outlook before AngularJS
  + Timeline of AngularJS releases along with major features
    + Start timeline with jQuery
    + Include other influential libs/frameworks:
      + Batarang (July 2012)
      + Ember (Dec 2011)
      + Grunt (Jan 2012)
      + Gulp (July 2013)
      + Webpack (March 2012)
      + Express.js (Nov 2010)
      + Polymer (May 2015)
      + React (March 2013)
      + Vue.js (Feb 2014)
      + Electron (July 2013)
      + John Papa style guide (July 2014)
      + Karma (Testacular) (Jan-ish 2013)
      + Protractor (Jun-ish 2013)
      + Angular (2) (Announced Mar 2014, Released Sept 2016)
      + ui-router (May 2013)
      + ui-bootstrap (Feb 2013)
      + Todd Motto Style Guide (July 2014)
  + AngularJS 1.0
    + Show the classic "Hello World" example
    + Show the "adoption" graph from Mark's slides (extend it perhaps?)
    + Services / Templates / Controllers / Directives / Filters / Modules
    + $http / $scope / $compile
    + 2-way binding
  + The Rise and Fall of AngularJS
    + Brought a structure to Web Applications

## Timeline
  + August 2006
    + jQuery 1.0 released by John Resig
      + Massive improvements in
        + DOM selection and manipulation
        + Event handling
        + Ajax requests
        + Cross-browser compatibility
  + July 2010
    + Knockout Initial Release
  + October 2010
    + AngularJS 0.9.0 Released
      + Earliest public release in GitHub Repo
      + Includes jqLite
  + November 2010
    + Express.js Initial Release
  + March 2011
    + First Commits in "Traceur" repository
  + May 2011
    + ES6 "Proposal Freeze"
      + Includes "Classes"
  + December 2011
    + Ember.js Initial Release
  + January 2012
    + Grunt Initial Release
    + Initial Release of SlimJim (Later: Testacular) (Later: Karma)
  + March 2012
    + Webpack Initial Release
  + June 2012
    + AngularJS 1.0.0 Released
      + Most Base Concepts of the framework are in this release
      + Included mocks of most exposed functionality for easier testing.
      + AngularJS Project was compiled with `rake`
      + Tests were run from shell scripts
      + Repo had Eclipse `.project` files.
  + July 2012
    + Batarang Chrome Extension Announced
  + September 2012
    + Bower Initial Release
    + AngularJS 1.1.0 Released
      + Mostly bug fixes and API changes.
  + February 2013
    + Initial Release of UI-Bootstrap
  + March 2013
    + Initial React Release
      + Not a framework.  View layer only.
      + JSX outputs a representation of the DOM as it should appear, is diffed against last version. Minimal changes made to DOM.
  + May 2013
    + Initial Router-UI Release
  + June 2013
    + Initial Release of Protractor
  + July 2013
    + Gulp Initial Release
    + Electron Initial Release
  + November 2013
    + AngularJS 1.2.0 Released
      + Considered the first "non-experimental" release
      + Added support for transitions and animations
      + Added Strict Contextual Escaping
      + Track-By functionality added to `ng-repeat`
      + ngRoute split into it's own module
      + Tests moved to Karma
      + Build moved to Grunt
      + Eclipse files no longer in repository
  + February 2014
    + Vue.js Initial Release
  + March 2014
    + Angular 2 announced
  + July 2014
    + John Papa and Todd Motto each publish an AngularJS Style Guide
  + September 2014
    + First commit of Babel
  + October 2014
    + AngularJS 1.3.0 Released
      + Multiple performance improvements
      + Dropped support for IE8
      + One-time bindings
      + ngMessages - for better form validation message handling
      + ngModelOptions - Bound model customization (debounce input)
      + Improved support for minification
      + Improved support for writing accessible components
      + Repo now has protractor tests
  + May 2015
    + AngularJS 1.4.0 Released
      + More performance improvements
      + Was considered an "easy" upgrade
      + Lots of talk about "directives" vs "components", but component helpers weren't ready in time for 1.4 release.
    + Initial Polymer Release
  + June 2015
    + Initial Redux Release
    + ECMAScript 2015 Finalized
  + December 2015
    + Angular 2.0 Beta Released
      + Attempted to provide a migration path:
        + ngUpgrade - AngularJS Module that helps you mix Angular 2 in to your app
        + ngForward - Lets you write AngularJS applications using Angular 2 syntax
        + ngReact - AngularJS module that helps you mix React components in to your app
  + February 2016
    + AngularJS 1.5.0 Released
      + Mainly focused on better support for Components and migration to Angular 2+
      + Component helpers to make defining components easier
      + One-way binding syntax added to components / directives
      + Lifecycle hooks in components
      + Support for instantiation of native ES6 classes in `$injector`
  + September 2016
    + Angular 2 Released
  + December 2016
    + AngularJS 1.6.0 Released
      + Security & Usability Improvements
      + More form component improvements
  + May 2018
    + AngularJS 1.7.0 Released
      + Broke from 6 month release cycle
      + Last "minor" release of AngularJS 1.x
      + Mostly minor changes
  + July 2018
    + AngularJS 1.7.x enters long-term support
      + No breaking changes
      + Will only be updated when
        + Major security
        + Browser release that breaks current functionality

## Things to bring up
  + MEAN stack

## Things they got right
  + (Over-)Formalized conventions to bring MVW or MVVM to web application UI development using JavaScript
  + Up-front testing support
  + 2-way binding was easy to conceptualize.  Helped new developers make the leap into SPAs
  + $scope data binding clever solution to a complicated problem that led the way for modern alternatives
  + Built in event broadcasting across "components" using `broadcast`/`emit` methods on scope
    + Generic PubSub available with libs in other frameworks but not quite the same because it doesn't follow the component tree
  + Best form validation I've ever used
  + Design did not require a transpiler, pre-processor, etc to run production code
  + Browser plugins for additional debugging

## Things they didn't
  + Only so many optimizations you can do with the digest cycle
  + Tried to do too many things.  Learning curve very steep
    + Templates
    + Directives
    + Controllers
    + Views
    + Services
    + Filters
    + ...
  + Early on, little direction in terms of project layout / coding style.
    + Formal style-guide hard to find and not really followed
    + Competing style guides (John Papa / Todd Motto) confused matters more
  + Announcement of "Angular 2"
    + Should have named it something else
      + "Complete rewrite" does not make adopters feel good about their choice.
    + Should have made a beta release closer to announcing it
      + So much time between announcement and implementation gave people a lot of time to think about their next framework
    + Should have had a better migration path ready at announcement time
      + Did by time Angular 2 beta was released.

