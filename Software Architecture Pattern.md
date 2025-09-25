# Software Architecture Pattern

## Model-View-Controller

Our project will be utilising a Model-View-Controller (MVC) architecture, **React** will be used for views, **Express** will be our controller, and **Mongoose** will handle our models in our **MongoDB** database. By utilising "separation of concerns" of the applications business logic and display, MVC architecture allows for parallel development, and more granular maintenence. Newer methodologies like **Ajax** allow enhanced user experience while using the traditional MVC architecture, allowing for partial page updates and  asynchronous communication. Let's discuss the model, view and controller in detail.

---

### Model

The **Model** component of MVC, put simply, handles the data. Whichever database system is chosen in a project handles validation and sanitisation of any and all data associated with the aplication. In our case, using **Mongoose** to interact with a **MongoDB** noSQL database. Mongoose schemas and models will be used to create object data, which will be accessed by the **Express** controller component, and passed to the **React** view component.

### View

### Controller

The **Controller** component of MVC, well, it controls! The controller handles requests and responses made by the user from the view component, interacts and manipulates data from the model component, and responds to the view to display results of logic to the user. **Express** is our controller in this application, and consists of routing, error handling, business logic, and responses. It's the main gear-box of our application, which uses complex functions, authorisation and middleware to provide the building blocks of what is displayed to the user.