Supabase Dev Platform
This project is a simple, single-file web application designed to act as a development platform or dashboard for viewing data from a Supabase backend. It's built with HTML, Tailwind CSS, and vanilla JavaScript.

🚀 How to Use
This platform is designed to be incredibly simple to set up. Follow these steps to get it running with your own Supabase project.

1. Set Up Your Supabase Backend
Make sure you have a Supabase project created.

Inside your project, you should have tables with data you want to view (e.g., bookings, forms).

Important: Ensure you have Row Level Security (RLS) policies in place if this data is sensitive. For a simple read-only internal dashboard, you might create a policy that allows select operations for authenticated users.

2. Configure the Application
Get Your Supabase Credentials:

In your Supabase project, go to Project Settings > API.

Find your Project URL.

Find your Project API Keys and copy the anon public key.

Update index.html:

Open the index.html file.

Find the <script> section at the bottom.

Locate these lines:

const SUPABASE_URL = 'YOUR_SUPABASE_URL';
const SUPABASE_ANON_KEY = 'YOUR_SUPABASE_ANON_KEY';

Replace 'YOUR_SUPABASE_URL' and 'YOUR_SUPABASE_ANON_KEY' with the credentials you just copied.

3. Running Locally
Simply open the index.html file in your web browser. It will connect to your Supabase instance and fetch the data.

4. Setting up the GitHub Repository
Create a New Repository:

Go to GitHub and create a new repository. You can make it private if it's for internal use.

Upload Your Files:

Upload the index.html and README.md files to your new repository.

5. Deploying with GitHub Pages (Optional)
You can host this platform for free using GitHub Pages, making it accessible to your team via a URL.

Enable GitHub Pages:

In your GitHub repository, go to Settings > Pages.

Under "Build and deployment", select the source as Deploy from a branch.

Choose the main (or master) branch and the /(root) folder.

Click Save.

Access Your Platform:

GitHub will provide you with a URL (e.g., https://your-username.github.io/your-repo-name/). It may take a few minutes for the site to become live.

⚠️ Security Warning: The Supabase anon key is designed to be public and safe to use in a browser, provided you have Row Level Security (RLS) enabled on your tables. Without RLS, the anon key would allow anyone to access your data. For an internal tool, ensure your RLS policies are strict and only allow access to the intended users.
