# Checklist for Angular

* **Tight coupling**
    * is it hard to predict the behavior? (the method depends on a mutable global state which cannot be predicted by merely reading)
    * is it possible to reuse the method or it is implicitly connected to different source of data (it fetches inside other data)
    * possibly reverse direction of composition
* **Single responsibility**
    * services with a single responsibility that is encapsulated by its context.
    * create a new service once the service begins to exceed that singular purpose.
* **Delegate complex component logic to services**
    * limit logic in a component to only that required for the view. All other logic should be delegated to services.
* **Delegate logic from templates to component method**
    * writing `*ngIf="var === 1"` in template is ok, anything longer should be moved away
* **Delegate logic to directive**
    * are there any candidates to be extracted to directives
* **Component input changes**
    * what happens when the variables are loaded asynchronously (will it effect template, change subscribtion,...)
* **Testability**
    * is it hard to write tests ? (possible bad design, tight coupling,...)
    * are unit tests present ? if not, is there good reason
* **Variables/methods/code style**
    * is it clear upon initial reading (may be confusing or additional read needed)
    * no unnecessary/duplicated logic
    * all vars used, meaningful names
    * unused imports
* **What does it actually do ?**
    * last but not least, is it really doing what it what was required ?

***
