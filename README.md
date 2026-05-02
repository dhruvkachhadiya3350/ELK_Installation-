⚙️ Complete Installation Walkthrough


📥 Step 1: Download the Script

git clone https://github.com/dhruvkachhadiya3350/ELK_Installation-.git
cd your-repo-name

🧩 Step 2: Create / Verify Script File

nano install_elk.sh
Paste the ELK installation script (if not already present)
Save and exit (CTRL + X, then Y, then ENTER)

🔐 Step 3: Give Execute Permission

chmod +x install_elk.sh
▶️ Step 4: Run the Script

sudo ./install_elk.sh

🌐 Step 5: Configure Kibana (Important)

Open Kibana configuration file:
sudo nano /etc/kibana/kibana.yml
Add/Update the following lines:
elasticsearch.username: "kibana_system"
elasticsearch.password: "elastic"

🔄 Step 6: Restart Kibana

sudo systemctl restart kibana

📊 Step 7: Check Kibana Logs

sudo journalctl -u kibana -f

✅ Step 8: Access Dashboard

Open in browser:
http://<YOUR_VM_IP>:5601

🔑 Step 9: Login Credentials

Username: elastic
Password: elastic
