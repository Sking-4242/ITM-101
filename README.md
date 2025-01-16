# ITM-101
Creating a **universal university grad planner app** that leverages AI to scrape bachelor degree requirements and build a personalized academic path for a student is an ambitious but very impactful project. Below, I'll guide you through brainstorming the **core features**, **technology stack**, and **development path** for such an app.

### Key Features to Consider:

1. **University Selection:**
   - Allow users to choose their university from a list.
   - For universities not on the list, let users manually input course data.

2. **Degree Program Selection:**
   - Provide a list of degree programs (e.g., Computer Science, Psychology, Engineering).
   - Include options for minors, double majors, and specializations.

3. **AI-Powered Requirement Scraping:**
   - Use AI or web scraping techniques to gather degree program requirements from the university's website or course catalog (e.g., general education, core courses, electives).
   - Regularly update the program requirements to accommodate any curriculum changes.

4. **Personalized Path Generation:**
   - Based on the selected program, the app generates a personalized degree plan.
   - Factor in prerequisites, course sequences, and suggested course load per semester.
   - Consider options for summer courses, online courses, and off-campus programs.
   
5. **Progress Tracking:**
   - Track which courses the student has taken, which are in-progress, and which remain.
   - Display progress toward graduation (e.g., percent completed, upcoming requirements).

6. **Course Scheduling:**
   - Recommend course schedules that avoid conflicts, balance workloads, and meet prerequisites.
   - Integrate with academic calendars to align course offerings by semester.
   - Account for course availability (e.g., full, prerequisites not met, or offering every other semester).

7. **Course Recommendations:**
   - Suggest electives based on the student’s interests and career goals.
   - Incorporate AI-driven recommendations that take into account trends in the job market or emerging fields of study.

8. **Notifications & Reminders:**
   - Set reminders for course registration deadlines, application deadlines, and important dates.
   - Notify the student when new course options or updates are available.

9. **Integration with University Systems:**
   - Allow the app to integrate with the university's existing student portal (if possible) to fetch real-time data about courses, grades, and prerequisites.
   
10. **Social & Collaborative Features:**
   - Provide features to connect with other students in similar programs or who are taking the same courses.
   - Add a discussion board, course review system, or study group functionality.

---

### Steps to Build the App:

#### 1. **Research and Planning**
   - **Gather Requirements**: Understand the specific requirements of various universities’ degree programs and their course catalogs.
   - **Legal and Privacy Concerns**: Make sure to comply with regulations such as FERPA (Family Educational Rights and Privacy Act) and ensure privacy when handling student data.
   - **Feasibility Study**: Determine the feasibility of scraping data from multiple universities. Some universities may have restrictions or APIs for accessing their course catalogs.

#### 2. **AI-Powered Scraping/Parsing of Degree Programs**
   - **Data Collection**: Use a web scraping tool like **Puppeteer** or **Cheerio** for scraping university websites or course catalogs.
   - **AI Integration**: For more complex data extraction, implement an NLP model that can parse and understand course descriptions, degree requirements, prerequisites, etc.
     - Use models such as **spaCy** or **OpenAI's GPT** for text extraction and understanding.
   - **Data Structuring**: Clean and structure scraped data into a standardized format (e.g., JSON or SQL) for use across multiple universities.

#### 3. **Core App Development**
   - **Platform Choice**: Decide whether the app will be mobile-first (Android/iOS) or web-based. You can use:
     - **Web**: React.js (frontend), Node.js (backend), MongoDB or SQL for databases.
     - **Mobile**: React Native, Flutter, or native development (Swift for iOS, Kotlin for Android).
   - **Backend**:
     - Build a RESTful API to manage course data, user progress, and generate degree plans.
     - Use Node.js, Express, or Django (Python) for the backend. Implement OAuth for user authentication.
   - **Database**: Use **MongoDB** for flexible, document-based storage (if using unstructured or semi-structured data). Alternatively, use **PostgreSQL** or **MySQL** for more relational data like course sequences.

#### 4. **Frontend and User Interface**
   - **User Registration and Profiles**: Students should be able to sign up, select their university, and input their degree program.
   - **Dashboard**: A clean dashboard where students can see their academic progress, upcoming courses, and degree requirements.
   - **Planner Interface**: Drag-and-drop or calendar-based interface to plan out semester schedules.
   - **Course Recommendations**: Use AI to suggest electives and customize course recommendations based on student interests.

#### 5. **AI for Course Path Optimization**
   - **Prerequisite Handling**: Build an algorithm that intelligently recommends a path, ensuring prerequisites are met and course availability is factored in.
   - **Machine Learning (optional)**: Use machine learning models to suggest course optimizations based on historical data from students or university trends.
   
#### 6. **Integrations**
   - **University Data Integration**: If possible, integrate the app with universities’ APIs (e.g., course catalogs, grades, and academic calendars).
   - **Google Calendar**: Sync deadlines, courses, and reminders with Google Calendar or similar services.

#### 7. **Testing & Feedback**
   - **User Testing**: Conduct usability testing with students from various universities. Gather feedback on the app's usability, course suggestions, and progress tracking.
   - **Iterative Development**: Implement feedback and improve the app in iterations. Focus on polishing the AI-powered features like course recommendations and path generation.

#### 8. **Launch & Support**
   - **Marketing**: Collaborate with universities, student organizations, and educational influencers to promote the app.
   - **Customer Support**: Provide resources (FAQ, chatbot, help desk) for students needing assistance with the app.

---

### Technology Stack Suggestion:

1. **Frontend**: 
   - **React.js** (Web), **React Native** (Mobile), or **Flutter**.
   - **TailwindCSS** or **Material-UI** for styling.
   - **Redux** for state management.

2. **Backend**:
   - **Node.js** with **Express** for API development.
   - **GraphQL** for efficient data fetching.
   - **Python** with **Flask** or **Django** for AI and NLP-related tasks.

3. **Database**:
   - **MongoDB** for flexible data storage or **PostgreSQL** for structured data.
   - **Redis** for caching (for faster data retrieval, especially when scraping).

4. **AI/NLP Tools**:
   - **spaCy**, **NLTK**, or **OpenAI GPT** for natural language processing.
   - **TensorFlow** or **PyTorch** for machine learning (optional).

5. **Web Scraping**:
   - **Puppeteer** or **Cheerio** for scraping HTML content from university sites.

6. **Cloud/Hosting**:
   - **AWS**, **Google Cloud**, or **Azure** for hosting.
   - Use **Firebase** for authentication and real-time database needs.

---

### Next Steps:
1. **Prototype**: Create an MVP (Minimum Viable Product) with one or two universities and a basic degree path.
2. **Expand**: Gradually add more universities and degree programs, refine the AI, and integrate more features like course scheduling.
3. **Market & Iterate**: Market to students and universities, gather feedback, and keep improving.

This could be an extremely useful tool for students, making university planning easier and more organized, and giving them a clear path to graduation!
