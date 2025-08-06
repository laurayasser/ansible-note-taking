# ansible_note_taking

## Note-Taking App with Ansible Deployment

This project is a simple Python Flask web application for note-taking, deployed on an AWS EC2 instance using Ansible automation.

---

## Project Structure

- `app.py` — The main Flask application file.
- `templates/index.html` — The HTML template rendered by Flask.
- `roles/` — Ansible roles containing tasks, files, and templates for deployment.
- `site.yml` — The main Ansible playbook to configure the EC2 instance and deploy the app.
- `.gitignore` — Specifies files to ignore in Git.
- `README.md` — This file.

---

## Prerequisites

- AWS EC2 instance with Amazon Linux or similar
- Python 3 installed on the EC2 instance
- Ansible installed on your control machine
- Access to AWS security group allowing port 5000 inbound traffic
- Git installed (optional for cloning this repo)

---

## Setup Instructions

1. **Clone the repository**

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
Run the Ansible playbook

This will configure your EC2 instance, install dependencies, and deploy the app files.

bash
Copy
Edit
ansible-playbook -i hosts site.yml
Start the Flask app on the EC2 instance

SSH into your EC2:

bash
Copy
Edit
ssh -i your-key.pem ec2-user@your-ec2-ip
Run:

bash
Copy
Edit
python3 /home/ec2-user/app.py
Access the app

Open your browser and visit:

arduino
Copy
Edit
http://your-ec2-public-ip:5000
Notes
The Flask app listens on port 5000. Make sure your EC2 security group allows inbound traffic on this port.

The Ansible playbook deploys index.html and other config files to /home/ec2-user/templates/.

You can modify the UI by editing templates/index.html and redeploying.

License
This project is open source and free to use.

Contact
For any questions, feel free to contact Your Name.

yaml
Copy
Edit

---

You can save this as `README.md` in your project root and commit it to GitHub:

```bash
git add README.md
git commit -m "Add project README"
git push origin main
