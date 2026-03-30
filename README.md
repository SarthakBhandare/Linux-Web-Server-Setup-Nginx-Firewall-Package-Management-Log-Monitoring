🔧 Project Overview :
This project simulates the responsibilities of a junior Linux engineer by setting up a production-style web server from scratch. The tasks include installing and configuring Nginx, managing packages with YUM/APT, securing the system with a firewall, monitoring logs with rsyslog, and automating server health checks using a shell script scheduled via cron. The goal is to build a resilient, secure, and monitored environment similar to what is used in real-world production systems.

🖥️ Project Architecture Breakdown :
• 	Linux Web Server (EC2 or VM)
The foundation of the project, providing the operating system and environment for hosting services.
• 	Nginx Web Server
• 	Hosts a default site on port 80.
• 	Serves a custom HTML page, demonstrating configuration and deployment skills.
• 	Nginx is chosen for its efficiency and scalability compared to Apache.
• 	Firewall (firewalld)
• 	Configured to allow HTTP (80) for web traffic.
• 	Allow SSH (22) for secure remote administration.
• 	Block all other ports, minimizing attack surface and enhancing security.
• 	Log Monitoring
• 	Tracks activity in  for user requests.
• 	Monitors  for issues and failures.
• 	Provides visibility into server performance and potential problems.
• 	Shell Script (server_health_check.sh)
• 	Runs automatically every 5 minutes via cron.
• 	Checks if Nginx and other critical services are running.
• 	Can restart services or send alerts if issues are detected, reducing downtime risk.

📊 Production-Style Monitoring :
This setup ensures the server is functional and secure, but to make it fully production-ready, you would add:
• 	Centralized monitoring tools (Prometheus + Grafana) for metrics visualization.
• 	Log aggregation (ELK stack) for deeper analysis and troubleshooting.
• 	Automated alerts (Alertmanager, email/SMS notifications) for proactive response.
• 	Intrusion detection systems (like Fail2Ban or Snort) for enhanced security.
• 	Automated backups to protect against data loss.

✅ In summary, this project combines web server deployment, firewall configuration, log monitoring, and automated health checks into a cohesive production-style environment. It builds a strong foundation for understanding how real-world Linux servers are managed and maintained.

