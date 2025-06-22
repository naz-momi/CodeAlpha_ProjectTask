#  Task 4: Network Intrusion Detection System – Suricata (CodeAlpha Internship)

This project was completed during my internship at **CodeAlpha** under the role of **Cybersecurity Intern**.  
The objective was to set up and configure a Network-Based Intrusion Detection System (NIDS) using **Suricata**, implement custom alert rules, and visualize the alerts using **EveBox**.

---

##  Objective

- Install and configure Suricata on Kali Linux.
- Create and test custom rules.
- Trigger real alerts using malicious traffic simulations.
- Visualize alerts in JSON and web dashboard format.

---

##  Tools & Technologies

- Suricata (IDS engine)
- EveBox (alert dashboard)
- `jq` (JSON parsing)
- `iptables` (response automation)
- curl / testmynids.org (attack simulation)
- bash scripting

---

##  Key Configuration Steps

- Installed Suricata using `apt-get install suricata`.
- Enabled rule sets in `/etc/suricata/suricata.yaml`.
- Created custom rules in `/etc/suricata/rules/local.rules`.
- Used `testmynids.org` and curl to generate alerts.
- Verified alerts in:
  - `fast.log`
  - `eve.json` (with `jq`)
- Configured **EveBox** to visualize alerts via web UI.
- Implemented bash script to block malicious IPs using `iptables`.

---

##  Custom Rules Example

```plaintext
alert http any any -> any any (msg:"CodeAlpha Test Rule"; content:"root"; sid:1000001; rev:1;)

````

## Learning Outcomes

Gained deep knowledge of how IDS engines inspect traffic.

Learned to write and test detection rules.

Practiced log parsing and JSON alert filtering.

Integrated dashboard (EveBox) for visual security analysis.
