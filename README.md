# Cookiecutter Ansible Template

This project is a Cookiecutter template for quickly creating Ansible projects. It helps you set up the basic structure of an Ansible project with pre-configured roles and files, allowing you to start your automation tasks faster.

## Project Structure

After running the template, the generated project will have the following structure:

```
{{cookiecutter.project_slug}}/
├── ansible.cfg
├── group_vars
│   └── all.yml
├── inventory
│   └── hosts
├── playbooks
│   └── nginx.yml
└── roles
    └── nginx
        ├── defaults
        │   └── main.yml
        ├── files
        ├── handlers
        │   └── main.yml
        ├── meta
        │   └── main.yml
        ├── tasks
        │   └── main.yml
        ├── templates
        └── vars
            └── main.yml
```

## Prerequisites

To use this template, you need to have the following installed:

- [Python](https://www.python.org/downloads/) (version 3.6 or higher)
- [Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/installation.html)

You can install Cookiecutter using the following command:

```bash
pip install cookiecutter
```

## How to Use

Follow these steps to create a new Ansible project using this template:

1. **Run the Cookiecutter template:**

   Open your terminal and run the command below. Replace `path/to/cookiecutter-ansible-template` with the actual path to your template:

   ```bash
   cookiecutter path/to/cookiecutter-ansible-template
   ```

2. **Answer the prompts:**

   You will be asked a series of questions to set up your project:

   - `project_name`: The name of your Ansible project.
   - `author_name`: The name of the author.
   - `remote_user`: The remote user that Ansible will use.
   - `server_ip`: The IP address of the server you want Ansible to connect to.

3. **Get started:**

   Once you've answered the prompts, a new project will be created with the name you specified. Navigate to the project folder and start managing and modifying as needed:

   ```bash
   cd {{cookiecutter.project_slug}}
   ansible-playbook playbooks/nginx.yml
   ```

## Customizing the Template

To customize this template further, you can modify the contents of the `roles`, `playbooks`, and configuration files like `ansible.cfg` to suit your specific needs.
