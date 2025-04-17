# Grazioso Salvare Dashboard

Please see `README.docx` in this repository for full instructions, **screenshots**, and documentation.

# Grazioso Salvare Animal Outcomes Dashboard

This repository contains my final dashboard project for SNHU CS-340: Client/Server Development. It includes a fully interactive Dash app built with Python, Dash, Plotly, and MongoDB to support the mission of Grazioso Salvare by enabling the filtering, visualization, and geolocation of rescue dogs based on their suitability for specific rescue tasks.

---

##  Reflections on the Project

### Writing Maintainable, Readable, and Adaptable Code

Writing programs that are maintainable, readable, and adaptable requires clear structure, modularity, and consistent naming conventions. For this project, I used a **separate CRUD Python module** (from Project One) to isolate all database logic. This made the dashboard cleaner and easier to manage, as each widget and callback in the Dash app could simply call the appropriate CRUD method without duplicating logic. This separation of concerns is a key principle in software design, allowing future updates (e.g., changing database credentials or filtering logic) to be done in one place without disrupting the UI.

In the future, this same CRUD module could be reused for different dashboards, admin tools, or automation scripts that require access to the animal outcomes data. It provides a strong, reusable interface between the application and the MongoDB database.

---

### My Approach to Solving Problems as a Computer Scientist

I approached this project with a mindset of **incremental development and user-centric thinking**. First, I carefully reviewed the UI/UX specifications from Grazioso Salvare, then broke the project into small parts: data retrieval, filtering, table setup, and visualizations. I tested each part as I went, which made it easier to debug and refine the final dashboard.

Compared to earlier projects in other courses, this one required more careful planning and modular thinking. It also demanded integrating multiple technologies (MongoDB, Dash, Plotly, Leaflet) in a seamless way, which helped me think more like a full-stack developer. Going forward, I would continue using strategies like modularization, clear documentation, and separation of concerns when designing data-driven applications for clients.

---

### What Do Computer Scientists Do — and Why Does It Matter?

Computer scientists solve real-world problems by building reliable, scalable systems. This project reflects that perfectly. By transforming a raw dataset into a usable, interactive dashboard, I created a tool that could help a company like **Grazioso Salvare** make informed decisions faster. Instead of manually searching through data, staff can instantly filter dogs based on mission requirements and view their locations and breed trends at a glance.

Projects like this matter because they **bridge the gap between data and action**, empowering organizations to save time, reduce errors, and focus more energy on their core mission. Whether it's rescuing people or optimizing logistics, computer science provides the backbone for smarter, faster decision-making.

---

### Technologies Used

- Python 3
- Dash by Plotly
- MongoDB (Atlas)
- PyMongo
- Dash Leaflet
- JupyterDash
- Plotly Express

---

### Repository Structure

project-repo/ ├── assets/ │ └── GraziosoSalvareLogo.png ├── animal_shelter.py # CRUD module from Project One ├── ProjectTwoDashboard.ipynb ├── screenshots/ └── README.md


Screenshot Evidence (Please see word doc for screenshots)
The following screenshots are included as proof of functionality:
1.	Dashboard Default State (Reset)
 
 
2.	Water Rescue Filter Applied
 
 
3.	Mountain or Wilderness Rescue Filter Applied
 
 
4.	Disaster or Individual Tracking Filter Applied
 
 
Tools Used

Tool	Purpose

  MongoDB	Used as the backend database for storing and querying the Austin Animal Center Outcomes dataset.
  PyMongo	Enables the Python script to interact with MongoDB, handling all CRUD operations.
  Dash	Provides the framework to build the web-based dashboard with interactive components.
  Dash Leaflet	Used for embedding geolocation maps into the dashboard.
  Plotly Express	Used to generate the bar chart visualization for top dog breeds.
  Jupyter Notebook + JupyterDash	Simplifies development and debugging of the Dash app within an interactive environment.

Rationale for Tool Selection
  •	MongoDB was chosen for its flexible document model and ease of integration with Python via PyMongo. Its ability to handle complex queries with filters (e.g., by breed, age, and sex) made it ideal for the rescue-type filters.
  •	Dash was selected for its minimal boilerplate and integration of HTML, CSS, and JavaScript through Python. It simplifies the process of creating full-featured web dashboards.
  Resources & References
  •	Dash Documentation: https://dash.plotly.com/
  •	PyMongo Documentation: https://pymongo.readthedocs.io/en/stable/
  •	Plotly Express: https://plotly.com/python/plotly-express/
  •	Dash Leaflet: https://dash-leaflet.herokuapp.com/
  
Steps Taken
  1.	Reviewed the UI/UX specification document.
  2.	Imported and cleaned the AAC dataset using a MongoDB Atlas instance and PyMongo.
  3.	Developed CRUD functionality in a separate Python module.
  4.	Built the dashboard layout and added all visual components using Dash.
  5.	Implemented filtering logic and callback functions.
  6.	Added styling for responsive layout and branding.
  7.	Validated all functionality and took screenshots of each required state.
     
Challenges & Solutions
  •	Issue: Logo not displaying.
  o	Solution: Verified that the logo file was named correctly and placed in the assets/ folder, which Dash loads automatically.
  •	Issue: Bar chart was cut off in responsive view.
  o	Solution: Restructured the layout using display: flex and adjusted component sizing to ensure the bar chart remained visible and centered.
  •	Issue: Callback errors due to ID mismatches.
  o	Solution: Double-checked all component IDs and matched them with callback outputs and inputs.
  •	Issue: Error loading application after one time use.
  o	Solution: Clear stale outputs, and adjust the port the application runs in.
________________________________________
Author: Cody Adams
Course: SNHU CS-340
Client: Grazioso Salvare

