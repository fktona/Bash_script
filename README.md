

```markdown
# Linux User Creation Bash Script

This repository contains a bash script called `create_users.sh` that reads a text file containing usernames and groups, creates users and groups as specified, sets up home directories, generates random passwords, and logs all actions. The script is designed to be run on an Ubuntu machine.

## How to Run the Script

Follow these steps to clone the repository and run the `create_users.sh` script:

### Step 1: Clone the Repository

Open your terminal and run the following command to clone the repository:
```
```sh
git@github.com:fktona/Bash_script.git
```

Replace `yourusername` and `your-repo` with your actual GitHub username and repository name.

### Step 2: Navigate to the Repository Directory

Change into the repository directory:

```sh
cd your-repo
```

### Step 3: Make the Script Executable

Ensure the script has execute permissions:

```sh
chmod +x create_users.sh
```

### Step 4: Prepare the Input File

Ensure you have a text file with the usernames and groups formatted as `username;groups` where groups are comma-separated.

Example `user_list.txt` format:

```
user2;group2,group1,group3
user3;group3,group1
user4;group2,group1
```

### Step 5: Run the Script

Execute the script with the name of the text file as the first argument:

```sh
sudo ./create_users.sh user_list.txt
```

The script will create the users and groups, set up home directories, generate random passwords, log actions to `/var/log/user_management.log`, and store passwords securely in `/var/secure/user_passwords.csv`.

## Notes

- Ensure you run the script with `sudo` to have the necessary permissions for creating users and groups.
- The script handles error scenarios such as existing users and provides appropriate logging.

## Technical Article

For a detailed explanation of the script implementation, visit the [technical article](https://dev.to/fikan/tackling-a-tough-backend-challenge-building-a-distributed-task-scheduler-29i0).
