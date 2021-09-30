## Component Lifecycle
A component in Angular has a life-cycle, a number of different phases it goes through from birth to death.We can hook into those different phases to get some pretty fine grained control of our application.<br/>

The hooks are executed in this order:<br/>
![image](https://user-images.githubusercontent.com/86051093/135412781-fd6f56d4-cd0f-4b0d-853b-d724b2ec55e3.png)

__constructor__<br/>
This is invoked when Angular creates a component or directive by calling new on the class.<br/>

__ngOnChanges__<br/>
Invoked every time there is a change in one of th input properties of the component.<br/>

__ngOnInit__<br/>
Invoked when given component has been initialized.This hook is only called once after the first ngOnChanges<br/>

__ngDoCheck__<br/>
Invoked when the change detector of the given component is invoked. It allows us to implement our own change detection algorithm for the given component.<br/>

__ngOnDestroy__<br/>
This method will be invoked just before Angular destroys the component.
Use this hook to unsubscribe observables and detach event handlers to avoid memory leaks.<br/>

__ngAfterContentInit__<br/>
Invoked after Angular performs any content projection into the component’s view (see the previous lecture on Content Projection for more info).<br/>

__ngAfterContentChecked__<br/>
Invoked each time the content of the given component has been checked by the change detection mechanism of Angular.<br/>

__ngAfterViewInit__<br/>
Invoked when the component’s view has been fully initialized.<br/>

__ngAfterViewChecked__<br/>
Invoked each time the view of the given component has been checked by the change detection mechanism of Angular.<br/>

