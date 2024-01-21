## Flask Application Design

### HTML Files

1. **`index.html`**: This file serves as the landing page of the application. It should contain a user-friendly interface with instructions on how to upload a resume in PDF format. The HTML should include a file input field for selecting the resume and a submit button to initiate the analysis process.


2. **`results.html`**: This file displays the analysis results extracted from the uploaded resume. The design should include sections for presenting the extracted information, such as name, contact details, skills, education, and work experience. The HTML should also incorporate styling to make the results presentable and easy to read.


3. **`error.html`**: This file handles scenarios where errors occur during the analysis process. It should display a user-friendly error message explaining the nature of the error and providing potential solutions.

### Routes

1. **`/upload`**: This route handles the upload of the resume in PDF format. Upon receiving a POST request with the resume file in the request body, the route processes the file, extracts the necessary information, and saves it in the application's database. After successful processing, it redirects the user to the results page (`/results`).


2. **`/results`**: This route displays the extracted information from the uploaded resume. Upon receiving a GET request, the route retrieves the saved information from the database and passes it to the `results.html` template for rendering.


3. **`/error`**: This route handles error scenarios. Similar to the upload route, it handles POST requests. The route processes the error message, saves it in the application's logs, and redirects the user to the error page (`/error`).