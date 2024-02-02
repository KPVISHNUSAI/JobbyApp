# Jobby App

I have successfully implemented the Jobby App, a web application that allows users to explore and apply for jobs. The app has various routes, each serving a different purpose, and it's designed to provide a seamless experience for users.

## Screenshots and Videos

### Login Route
- #### Extra Small (Size < 576px) and Small (Size >= 576px)
![Login - Extra Small/Small](https://assets.ccbp.in/frontend/content/react-js/jobby-app-login-sm-outputs.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px)
![Login - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-login-lg-output.png)

### Home Route
- #### Extra Small (Size < 576px) and Small (Size >= 576px)
![Home - Extra Small/Small](https://assets.ccbp.in/frontend/content/react-js/jobby-app-home-sm-output.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px)
![Home - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-home-lg-output.png)

### Jobs Route
- #### Extra Small (Size < 576px) and Small (Size >= 576px)
![Jobs - Extra Small/Small](https://assets.ccbp.in/frontend/content/react-js/jobby-app-jobs-sm-outputs.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px) - Jobs Success
![Jobs Success - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-jobs-success-lg-output-v0.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px) - No Jobs
![No Jobs - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-no-jobs-lg-output-v0.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px) - Profile Failure
![Profile Failure - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jooby-app-profile-failure-lg-output-v0.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px) - Jobs Failure
![Jobs Failure - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-jobs-failure-lg-output-v0.png)

### Job Item Details Route
- #### Extra Small (Size < 576px) and Small (Size >= 576px) - Job Details Success
![Job Details Success - Extra Small/Small](https://assets.ccbp.in/frontend/content/react-js/jobby-app-job-details-success-sm-output-v0.png)
- #### Extra Small (Size < 576px) and Small (Size >= 576px) - Job Details Failure
![Job Details Failure - Extra Small/Small](https://assets.ccbp.in/frontend/content/react-js/jobby-app-job-details-failure-sm-output.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px) - Job Details Success
![Job Details Success - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-job-details-success-lg-output-v0.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px) - Job Details Failure
![Job Details Failure - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-job-details-failure-lg-output.png)

### Not Found Route
- #### Extra Small (Size < 576px) and Small (Size >= 576px)
![Not Found - Extra Small/Small](https://assets.ccbp.in/frontend/content/react-js/jobby-app-not-found-sm-output-v0.png)
- #### Medium (Size >= 768px), Large (Size >= 992px), and Extra Large (Size >= 1200px)
![Not Found - Medium/Large/Extra Large](https://assets.ccbp.in/frontend/content/react-js/jobby-app-not-found-lg-output-v0.png)

## Set Up Instructions
- Download dependencies by running `npm install`
- Start up the app using `npm start`

## Functionalities Implemented
### Login Route
- Handles authentication with valid and invalid credentials.
- Navigates to Home Route on successful login.
- Redirects unauthenticated users to the Login Route when accessing other routes.

### Home Route
- Clicking on "Find Jobs" navigates to the Jobs Route.

### Jobs Route
- Fetches and displays profile details.
- Fetches and displays job listings.
- Supports filtering by employment type, salary range, and search.
- Displays loader while fetching data.
- Handles retry functionality on API failure.
- Shows "No Jobs" view when the job list is empty.
- Navigates to Job Item Details Route on clicking a job item.

### Job Item Details Route
- Fetches and displays detailed information about a job.
- Displays a list of similar jobs.
- Opens the company website on clicking "Visit."

### Not Found Route
- Redirects to the Not Found Route for unknown paths.

### Header
- Navigates to Home, Jobs, and Login Routes.
- Logs out and navigates to the Login Route.

## API Requests & Responses
- **Login API**
  - POST: `https://apis.ccbp.in/login`
  - Sample Success Response:
    ```json
    {
      "jwt_token": "<token>"
    }
    ```
  - Sample Failure Response:
    ```json
    {
      "status_code": 404,
      "error_msg": "Username is not found"
    }
    ```

- **Profile API**
  - GET: `https://apis.ccbp.in/profile`
  - Sample Response:
    ```json
    {
      "profile_details": {
        "name": "Rahul Attuluri",
        "profile_image_url": "https://assets.ccbp.in/frontend/react-js/male-avatar-img.png",
        "short_bio": "Lead Software Developer and AI-ML expert"
      }
    }
    ```

- **Jobs API**
  - GET: `https://apis.ccbp.in/jobs`
  - Sample Response:
    ```json
    {
      "jobs": [...],
      "total": 25
    }
    ```

- **Job Details API**
  - GET: `https://apis.ccbp.in/jobs/:id`
  - Sample Response:
    ```json
    {
      "job_details": { ... },
      "similar_jobs": [...]
    }
    ```

## Additional Notes
- User credentials for testing:
  - Username: rahul
  - Password: rahul@2021

- Ensure proper implementation of alt attributes
