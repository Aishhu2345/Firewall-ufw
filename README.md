UFW Firewall Configuration – Full Command Flow

# 🔁 Step 1: Reset UFW to start fresh (clears all existing rules and disables firewall)
sudo ufw reset

# ✅ Step 2: Enable UFW firewall
sudo ufw enable

# ⛔ Step 3: Block Telnet (port 23) - considered insecure
sudo ufw deny 23

# 🔓 Step 4: Allow SSH (port 22) - needed for secure remote access
sudo ufw allow 22

# 📜 Step 5: Show all active rules with numbers (helps in rule management)
sudo ufw status numbered

# 🔍 Step 6: Show detailed firewall status (useful for documentation/reporting)
sudo ufw status verbose

# 💾 Step 7: Save current firewall config to a text file for submission
sudo ufw status verbose > ufw_rules.txt

# ❌ Step 8: (Optional) Delete the rule blocking Telnet (port 23)
# First, find the rule number for port 23 by rechecking the list
sudo ufw status numbered

# Then replace X below with the actual rule number for port 23 and run:
# Example: sudo ufw delete 2
# Only run this step if you want to restore the original state
# sudo ufw delete X
