## Project 2: Serverless Solutions with Cloud Functions

### Project Overview

In this project, I designed and implemented serverless solutions using **Google Cloud Functions**. The main focus was on automating database updates for employee and vaccination records, making the process more efficient and error-free. I used **Logs Explorer** to monitor function invocations and analyze the system's performance, and I generated custom reports with **Stackdriver Trace** for deeper insights. Additionally, I've included screenshots of Cloud Functions, Logs Explorer, and the performance reports for better visualization.

### Use Cases

1. **Updating Employee Database:**
   This Cloud Function is triggered when the company provides an increment to an employee. It takes the employee ID (`empId`), the new salary (`salary`), and the employee's date of birth (`dob`) as input parameters. The function then connects to the employee database (using a connection string from environment variables) and updates the salary.

2. **Updating Vaccination Database:**
   This Cloud Function is triggered when a child receives a vaccination. The function takes the patient ID (`patientId`), vaccination date (`vaccinationDate`), and the child’s age (`age`) as input. It then updates the vaccination records in the database.

### Steps to Implement Cloud Functions

1. **Setting Up the Environment:**
   To begin, I created a **Google Cloud Project** and enabled the **Cloud Functions API**. For secure database connections, I set up environment variables that contained the database connection strings for both the employee and vaccination databases.

2. **Creating Cloud Functions:**
   I created separate Cloud Functions for each use case. The first function listens for employee salary increments and updates the corresponding database records with the provided `empId`, `salary`, and `dob`. The second function listens for vaccination events and updates the vaccination records in the vaccination database using the `patientId`, `vaccinationDate`, and `age`.

3. **Monitoring Performance:**
   I utilized **Logs Explorer** to track and monitor the performance of these Cloud Functions. The Logs Explorer provided insights into function invocations and helped analyze the frequency and timing of the function triggers. Additionally, I used **Stackdriver Trace** to generate detailed reports, enabling me to analyze the performance and latency of the functions.

4. **Deploying the Cloud Functions:**
   After implementing the Cloud Functions, I used the **gcloud CLI** and the **Google Cloud Console** to deploy them. I also made sure to thoroughly test each function with sample data to confirm that they were working as expected and accurately updating the employee and vaccination databases.

### Conclusion

Through this project, I successfully demonstrated how to build and deploy serverless solutions using **Google Cloud Functions**. By automating the process of updating employee and vaccination records, manual efforts were minimized, and efficiency was increased. The use of **Logs Explorer** and **Stackdriver Trace** allowed me to monitor the performance of the functions, ensuring that they operated smoothly and effectively.

### Next Steps

Moving forward, I plan to explore more use cases for Cloud Functions, such as automating more business processes. Additionally, I aim to implement more advanced monitoring and logging practices to further optimize the performance and scalability of the functions.
