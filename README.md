# PiAnsible

PiAnsible is an Ansible project designed to automate the setup of services on Raspberry Pi OS Lite. This repository includes playbooks to install and configure Docker, Docker Compose, and Apache2 within Docker containers.

## Getting Started

### Prerequisites

- Ansible installed on your local machine.
- Access to a Raspberry Pi running Raspberry Pi OS Lite.
- SSH access to the Raspberry Pi.

### Directory Structure

Your project should include the following directory structure:

```
PiAnsible/
├── tasks/
│   ├── update-upgrade.yml
│   ├── docker-compose.yml
│   ├── apache-docker.yml
├── inventory.example.ini
├── playbook.yml
└── index.html  # Create this file as described below
```

### Creating the `index.html` File

1. Navigate to the root directory of your `PiAnsible` repository.
2. Create an `index.html` file with the following command:

```bash
   touch index.html
```

3. Edit the `index.html` file to include your desired content. Here's a simple example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Welcome to PiAnsible!</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f9;
      color: #333;
      margin: 0;
      padding: 0;
      text-align: center;
    }
    .container {
      max-width: 800px;
      margin: 50px auto;
      padding: 20px;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
    h1 {
      color: #0056b3;
    }
    p {
      font-size: 1.2em;
      line-height: 1.6;
    }
    .footer {
      margin-top: 30px;
      font-size: 0.9em;
      color: #777;
    }
    a.button {
      display: inline-block;
      padding: 10px 20px;
      font-size: 1em;
      color: #fff;
      background-color: #0056b3;
      border: none;
      border-radius: 5px;
      text-decoration: none;
      transition: background-color 0.3s ease;
    }
    a.button:hover {
      background-color: #003d7a;
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Welcome to PiAnsible!</h1>
    <p>This is the default page served by your Apache2 Docker container. PiAnsible is an Ansible project designed to automate the setup of services on Raspberry Pi OS Lite.</p>
    <p>For more information and to get started, visit the project repository on GitHub.</p>
    <a href="https://github.com/wbreiler/PiAnsible" class="button">Visit GitHub Repository</a>
    <div class="footer">
      <p>&copy; 2024 PiAnsible. All rights reserved.</p>
    </div>
  </div>
</body>
</html>
```

### Using the Playbooks

1. **Set up the Inventory File**: Edit the `inventory.example.ini` to match your setup, and rename it to `inventory.ini`
    - Example:

    ```ini
    [all]
    pi.local ansible_user=pi
    ```

2. **Run the Playbook**
  
  ```bash
  ansible-playbook playbook.yml
  ```

## License
This project is licensed under the GNU General Public License v3.0 (GPL-3.0).

### What This Means

The GPL-3.0 is a free software license that guarantees end users the freedom to run, study, share, and modify the software. The key aspects of GPL-3.0 include:

- Freedom to Use: You can use the software for any purpose.
- Freedom to Study and Modify: You can study how the program works and change it to make it do what you wish. Access to the source code is a precondition for this.
- Freedom to Distribute Copies: You can redistribute copies of the original program so you can help others.
- Freedom to Distribute Modified Versions: You can distribute copies of your modified versions to others. By doing this you can give the whole community a chance to benefit from your changes. Access to the source code is a precondition for this.

If you distribute copies or modified versions of the software, you must pass on the same freedoms to others. That means you must distribute the source code and keep the GPL license intact.