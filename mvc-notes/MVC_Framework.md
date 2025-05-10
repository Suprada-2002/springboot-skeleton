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
