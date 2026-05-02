# ELK_Installation

⚙️ Complete Installation Walkthrough
🧩 Step 1: Create Script File
nano install_elk.sh
Paste the ELK installation script inside the file
Save and exit (CTRL + X, then Y, then ENTER)
🔐 Step 2: Give Execute Permission
chmod +x install_elk.sh
▶️ Step 3: Run the Script
sudo ./install_elk.sh
🌐 Step 4: Configure Kibana (Important)
Open Kibana configuration file:
sudo nano /etc/kibana/kibana.yml
Add/Update the following lines:
elasticsearch.username: "kibana_system"
elasticsearch.password: "elastic"
🔄 Step 5: Restart Kibana
sudo systemctl restart kibana
📊 Step 6: Check Kibana Logs
sudo journalctl -u kibana -f
✅ Step 7: Access Dashboard
Open in browser:
http://<YOUR_VM_IP>:5601
🔑 Step 8: Login Credentials
Username: elastic
Password: elastic
