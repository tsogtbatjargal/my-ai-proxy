# Daily Automation Project

A Python script that automatically increments a number in a text file, commits the change to Git, and updates a cron job to run the script at a new random time daily. Perfect for maintaining a daily commit streak or tracking sequential values with a dynamic schedule.

## Setup

### Prerequisites

1. **Python**: Ensure Python is installed on your system. You can download it from [python.org](https://www.python.org/downloads/).
2. **Git**: Ensure Git is installed on your system. You can download it from [git-scm.com](https://git-scm.com/downloads).

### Steps

1. **Clone this repository**:

Open a Command Prompt or PowerShell and run:

```bash
git clone https://github.com/tsogtbatjargal/my-ai-proxy.git
cd my-ai-proxy
```

2. **Set up a virtual environment**:

Create a virtual environment to isolate your project's dependencies:

```bash
python -m venv venv
```

Activate the virtual environment:

- On Windows Command Prompt:

```bash
venv\Scripts\activate
```

- On Windows PowerShell:

```bash
.\venv\Scripts\Activate.ps1
```

3. **Install dependencies**:

Create a [requirements.txt](http://_vscodecontentref_/1) file with the following content:

```text
torch>=2.5.1
transformers>=4.47.1
```

Then, install the dependencies using `pip`:

```bash
pip install -r requirements.txt
```

4. **Run the script**:

The script can be run without dependencies besides the Python standard library, simply by running:

```bash
python update_number.py
```

You might want to run the script manually for the first time to verify it works before setting up a scheduled task.

### Using LLM-based Commit Message Generation

If you prefer to use LLM-based commit message generation, you need to set an environment variable and run the script:

1. **Set the environment variable and run the script**:

```bash
$env:FANCY_JOB_USE_LLM="true"; python update_number.py
```

### Setting Up a Scheduled Task on Windows

Since Windows does not support cron jobs, you can use Task Scheduler to run the script daily:

1. **Open Task Scheduler**:

   - Press `Win + R`, type `taskschd.msc`, and press `Enter`.

2. **Create a new task**:

   - Click on "Create Task" in the right-hand Actions pane.

3. **General Tab**:

   - Name your task (e.g., "Daily Number Incrementer").
   - Choose "Run whether user is logged on or not".
   - Check "Run with highest privileges".

4. **Triggers Tab**:

   - Click "New".
   - Set "Begin the task" to "On a schedule".
   - Set the schedule to daily and choose a start time.
   - Click "OK".

5. **Actions Tab**:

   - Click "New".
   - Set "Action" to "Start a program".
   - In the "Program/script" field, enter the path to your Python executable (e.g., `"C:\Users\YourUsername\my-ai-proxy\venv\Scripts\python.exe"`).
   - In the "Add arguments" field, enter the path to your script (e.g., `C:\Users\YourUsername\my-ai-proxy\update_number.py`).
   - Click "OK".

6. **Conditions Tab**:

   - Uncheck "Start the task only if the computer is on AC power".

7. **Settings Tab**:

   - Check "Allow task to be run on demand".
   - Check "Run task as soon as possible after a scheduled start is missed".
   - Click "OK".

## Usage

The script will increment the number in [number.txt](http://_vscodecontentref_/2) and commit the change to git. You can modify the script to increment by any value or use a different file to store the number.

By running this you will be able to get a fancy streak on your GitHub profile and potentially improve your job prospects.

![Good Luck!](evil-laughing.gif)

