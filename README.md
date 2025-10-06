Cybersecure Digital Wallet - Backend Server
This guide explains how to set up and run the Python backend for your digital wallet project on your laptop.

Where and How To Do It
Goal: Create a dedicated folder for your backend code. This keeps your project organized.

Location: You can create this folder anywhere you like on your laptop. A good place is your Documents folder or a dedicated Projects folder.

Step 1: Project Setup
Create the Project Folder:

Open your file explorer and create a new folder. Name it DigitalWallet_Backend.

Place the app.py and requirements.txt files you just downloaded inside this DigitalWallet_Backend folder.

Open in VS Code:

Open the Visual Studio Code application.

Go to File > Open Folder... and select the DigitalWallet_Backend folder.

You should now see app.py and requirements.txt in the file explorer panel on the left.

Step 2: Install Required Packages
Open the Terminal in VS Code:

In VS Code, go to the top menu and click Terminal > New Terminal.

A command line will open at the bottom of the editor, already inside your project folder.

Create a Virtual Environment (Highly Recommended):

A virtual environment keeps your project's Python packages separate from your computer's global packages. It's a best practice for any Python project.

In the terminal, run this command:

python -m venv venv

Now, activate the environment:

On Windows:

.\venv\Scripts\activate

On macOS/Linux:

source venv/bin/activate

You'll know it's active because you'll see (venv) at the beginning of your terminal prompt.

Install the Packages:

With your virtual environment active, run the following command in the terminal. This command reads the requirements.txt file and installs the exact versions of the packages needed.

pip install -r requirements.txt

Step 3: Run the API Server
Start the Server:

Make sure you are still in the VS Code terminal with the (venv) active.

Run the main Python file with this command:

python app.py

Check the Output:

You should see output in the terminal that looks like this:

Initializing the database...
Creating 'users' table.
Table 'users' created successfully.
 * Serving Flask app 'app'
 * Running on [http://127.0.0.1:5000](http://127.0.0.1:5000)
 * Running on http://YOUR_LAPTOP_IP:5000
Press CTRL+C to quit

A new file named wallet.db will also appear in your project folder. This is your SQLite database file!

Congratulations! Your API server is now running on your laptop. It is listening for requests on port 5000. You can now proceed to test it with Postman or connect your mobile app to it.