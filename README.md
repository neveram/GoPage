# GoPage

This is a simple web application built in Go that allows users to view, edit, and save text files as pages. The application uses the `net/http` package to handle HTTP requests and the `html/template` package to render HTML templates. The pages are stored as individual text files on the server.

## Prerequisites

To run this application, you need to have Go installed on your system.

## How to Use

1. Clone or download this repository to your local machine.

2. Navigate to the project directory.

3. Build and run the application:

```bash
go run main.go
```

4. The application will start a local server at `[http://localhost:8080](http://localhost:8080/view/ANewPage`.

## File Structure

- `main.go`: Contains the main logic of the web application, including the handlers for view, edit, and save actions, as well as the server setup.

- `edit.html` and `view.html`: HTML templates used to render the edit and view pages, respectively.

## Endpoints

1. **View Page**: To view an existing page or create a new one.

   - URL: `/view/{page_title}`
   - Method: GET
   - Action: If the page exists, it will be displayed. If the page does not exist, it will redirect to the edit page.

2. **Edit Page**: To edit an existing page or create a new one.

   - URL: `/edit/{page_title}`
   - Method: GET
   - Action: If the page exists, it will be displayed in the editable format. If the page does not exist, a new page will be created with the given title.

3. **Save Page**: To save changes made to a page or create a new page.

   - URL: `/save/{page_title}`
   - Method: POST
   - Action: The data from the form will be saved as a text file with the given title. If the page already exists, it will be updated with the new content.

## Important Notes

- This application uses a very basic file-based storage system for simplicity. In a real-world scenario, a more robust and secure data storage mechanism, like a database, would be recommended.
