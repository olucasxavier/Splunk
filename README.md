# Splunk | Exploring Security Information and Event Management (SIEM) with Splunk in My Homelab

Welcome to my Splunk project, where I dive into the world of Security Information and Event Management (SIEM) systems. In this repository, I'll take you on a journey through the powerful capabilities of Splunk as I deploy it in my homelab environment to enhance my skills and knowledge in the field of cybersecurity.

<h3>WHAT IS SPLUNK?</h3>

Splunk is a leading SIEM solution that enables organizations to collect, analyze, and visualize vast amounts of data from various sources in real-time. As a robust data analytics and security tool, Splunk helps businesses detect, investigate, and respond to security threats and incidents efficiently. Its flexibility and scalability make it a preferred choice for managing security and operational data.

<h3>WHY SPLUNK?</h3>

Understanding security threats and anomalies in a network is crucial in today's digital landscape. Splunk offers:

**1. Comprehensive Data Analysis:** Splunk can process and analyze diverse data types, providing valuable insights into security events, user behavior, and system performance.

**2. Real-time Monitoring:** Splunk allows real-time monitoring of network activities, enabling quick responses to security incidents and breaches.

**3. Custom Dashboards:** Users can create customized dashboards and reports, making it easier to interpret complex data and identify patterns or trends.

<h3>HANDS ON, TIME TO INSTALL SPLUNK</h3>

**Prerequisites:**

In my case, as I'm using Proxmox, I'm going to deploy Splunk using a container (LXC) running Ubuntu, you can follow these steps:

**Step 1: Create an Ubuntu LXC Container**

1. Log in to the Proxmox web interface.
2. Select the node where you want to create the LXC container.
3. Click on "Create CT" (Container).
4. In the "General" tab, provide a unique ID for the container (e.g., 100) and set a hostname.
5. Under "Template," select "ubuntu-20.04" or the Ubuntu version of your choice.
6. Set the "Root Password" and any other necessary options.
7. Click "Next" and review your settings. Then, click "Finish" to create the container.
8. Start the container by selecting it in the Proxmox web interface and clicking "Start."

**Step 2: Access the Ubuntu Container**

1. Once the Ubuntu container is running, you can access it via SSH or the Proxmox web terminal.
2. Open a terminal or SSH client and connect to the IP address of the LXC container. You'll need the root username and password you set during container creation.

**Step 3: Update & Upgrade your Container**

1. Update the package list inside the container:

````
sudo apt update
sudo apt upgrade
````

**Step 4: Install Splunk**

1. Download the Splunk Enterprise installation package. You can find the latest version at the Splunk website.

````
wget -O splunk-8.3.4-1fabulous-amd64.deb 'https://www.splunk.com/bin/splunk/DownloadActivityServlet?architecture=x86_64&platform=linux&version=8.3.4&product=splunk&filename=splunk-8.3.4-1fabulous-amd64.deb&wget=true'
````
Make sure to replace the URL with the correct link for the latest version.


2. Install the downloaded package:

````
sudo dpkg -i splunk-*.deb
````

3. Start Splunk:

````
sudo /opt/splunk/bin/splunk start --accept-license
````

Follow the prompts to set a password for the admin user and accept the license agreement.

4. Splunk is now running. You can access the Splunk web interface by opening a web browser and navigating to **http://<your_server_ip>:8000.**

5. Log in using the username admin and the password you set during installation.

6. Once logged in, you can configure data inputs, search data, and create dashboards to monitor and analyze your data.

Please note that this is a basic setup. For production environments or more complex setups, additional configurations and security measures are necessary. Always refer to the official Splunk documentation for detailed instructions and best practices.

**Contributions are more than Welcome**

I encourage contributions, feedback, and collaboration from the community. If you have suggestions, improvements, or questions, please feel free to open issues or submit pull requests.

Thank you,</br>
Lucas
