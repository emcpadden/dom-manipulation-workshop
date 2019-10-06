# DomManipulationWorkshop

* see on Youtube.com at: https://www.youtube.com/watch?v=vz9cNCkaPsY&list=PLw5h0DiJ-9PDyHiRwuP2c_kuxx1URzUMx

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 1.7.3.

# Tags 
note: s tags are the solutions txx tags are the clean version so you can try it out
## Modifying the DOM
* s1a : childRef to add an attribute using nativeElement
* s1b : using a custom directive to add an attribute using nativeElement
* s1c : using a custom directive to add an attribute using renderer making it platform independent also safe for web workers (https://youtu.be/vz9cNCkaPsY?t=2334)
## 
* 2s : Remove a child component DOM node (showing `checkAndUpdateView` method in `@angular/core` checkout `nodes` of the component to see the hierarchy  
* s3 : Using templateRef and viewContainer (ng-template and ng-container) to use to put the template into then remove the viewContainer
  * Questions?
    * Q: Why does the renderer have structural methods like removeChild, createDOM node, move node etc.
      * A: because Angular uses these internally to be cross platform
    * If you want to make structural changes to the DOM you should always use the view container (rather than the renderer)
    * If you want to make non-structural changes ot the DOM use the renderer.  For instance to add attributes, change attributes, update style etc.
  * NOTE: even though this example did rendering inside the component, it is always best to do rendering logic inside a directive
  * for solution, see: https://youtu.be/vz9cNCkaPsY?t=4977
* s4 : Dynamic components
  * Interesting article on Dynamic components: http://nataliesmith.ca/blog/dynamic-components-angular
  * NOTE!!! : make sure to add components that will be created dynamically to the entry Components so that they will not be optimized out during a production build
  
* s5 : optimized s4 example where we hold onto the components that are created and swap them so we don't have to keep creating the components over and over

* s6 : similar to s5 but it creates embedded views instead of components
  


## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `-prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
