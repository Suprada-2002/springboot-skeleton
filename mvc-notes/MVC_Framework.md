# MVC
- Model-View-Controller architectural design pattern which works around Front Controller, i.e Dispatcher Servlet.
- Dispatcher Servlet handles and dispatches all incoming request to appropiate controllers.
- it uses ```@Controller``` and ```@RequestMapping``` as default handlers.

### Model
- encapuslate application data.

### View
- renders model data
- generate HTML output that client can interpret.

### Controller
- processese user request and passes them to view to render.

## JpaRespository
- contains the full API for ```CrudRepository``` & ```PagingAndSortingRepository```.
- contains API for basic CRUD operations and also API for pagination & sorting.


### Important methods
1. saveAll() : save all entities
- returned Iterable same size as passed argument Iterable
- returns the saved entities but never null.
- throws ```IllegalArgumentException``` in case given entities/one of entities is null.
2. getById()
- return reference to the entity with given identifier.
- likely return an instance or throw ```EntityNotFoundException``` on first access.
3. flush(): flushes all pending changes to database.
