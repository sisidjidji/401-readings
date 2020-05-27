#read 17


- In the Model-View-Controller (MVC) pattern, the view handles the app's data presentation and user interaction. A view is an HTML template with embedded Razor markup. Razor markup is code that interacts with HTML markup to produce a webpage that's sent to the client.

- Benefits of using views:

1. The app is easier to maintain because it's better organized. Views are generally grouped by app feature. This makes it easier to find related views when working on a feature.

2. The parts of the app are loosely coupled. You can build and update the app's views separately from the business logic and data access components. You can modify the views of the app without necessarily having to update other parts of the app.

3. It's easier to test the user interface parts of the app because the views are separate units.

4. Due to better organization, it's less likely that you'll accidentally repeat sections of the user interface.


- The term partial view is used when developing either an MVC app, where markup files are called views, or a Razor Pages app, where markup files are called pages. This topic generically refers to MVC views and Razor Pages pages as markup files.


- When to use partial views

1. Break up large markup files into smaller components.

2. In a large, complex markup file composed of several logical pieces, there's an advantage to working with each piece isolated into a partial view. The code in the markup file is manageable because the markup only contains the overall page structure and references to partial views.

3. Reduce the duplication of common markup content across markup files.

4. When the same markup elements are used across markup files, a partial view removes the duplication of markup content into one partial view file. When the markup is changed in the partial view, it updates the rendered output of the markup files that use the partial view.


- Tag Helpers enable server-side code to participate in creating and rendering HTML elements in Razor files. For example, the built-in ImageTagHelper can append a version number to the image name
