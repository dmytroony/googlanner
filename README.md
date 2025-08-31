# Weekly Scheduler

This is a single-page web application designed to help you manage your weekly tasks by integrating with your Google Tasks and Google Calendar. You can add pre-defined tasks directly to your Google accounts with a single click.

## Getting Started

To use this application, you need to set up the necessary credentials in the Google Cloud Console and deploy the single `index.html` file to a web server. GitHub Pages is a great free option for this.

### Prerequisites

*   A Google account with access to the Google Cloud Console.
*   A GitHub account to host the project.

### Step 1: Set up Google APIs

You need to enable the required Google APIs and get your unique API credentials.

1.  Go to the [Google Cloud Console](https://console.cloud.google.com/) and create a new project.
2.  In the API Library, search for and enable the **Google Tasks API** and the **Google Calendar API**.
3.  Navigate to the **Credentials** page and click **Create Credentials**.
4.  Choose **OAuth 2.0 Client ID**.
5.  Select **Web application** as the application type.
6.  Under **Authorized JavaScript origins**, add two new URIs:
    *   `http://localhost:8000` (for local testing)
    *   `https://[your-github-username].github.io` (your future GitHub Pages URL)
7.  Click **Create** and copy the **Client ID** that is generated.
8.  While still on the **Credentials** page, click **Create Credentials** again and select **API Key**. Copy this key as well.

### Step 2: Deploy to GitHub Pages

1.  Save the `index.html` file to your computer.
2.  Create a new public repository on GitHub.
3.  Upload the `index.html` file to the root of your new repository.
4.  Go to the **Settings** tab of your repository, then navigate to the **Pages** section.
5.  Under **Build and deployment**, select the `main` branch and the `/ (root)` folder, then click **Save**.
6.  Wait a few moments for GitHub to deploy your site. You will see a green checkmark next to the branch, and a live URL will be provided.

## How to Use the App

1.  Open your newly deployed GitHub Pages URL in a web browser.
2.  A pop-up modal will appear asking for your **Google API Key** and **Client ID**. Paste the credentials you copied earlier and click **Save and Continue**.
3.  Click the **Tasks** button to add a task to your default Google Tasks list.
4.  Click the **Calendar** button to add a 30-minute event to your primary Google Calendar.

Your API credentials are saved securely in your browser's local storage and will not be shared with anyone else.
