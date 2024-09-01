# Threat Intelligence Powered SOC

This project demonstrates the integration of various open-source security tools to create an automated threat detection and incident response system. The key components include Wazuh, Graylog, MISP, Grafana, and DFIR IRIS, all interconnected using [SOCFortress CoPilot](https://github.com/socfortress/CoPilot) software. The setup enables the detection of Indicators of Compromise (IOCs) within logs and the seamless escalation of alerts to a case management system.

## Architecture Diagram

**Screenshot Placeholder:**  
*(Insert overall project architecture or workflow diagram here)*

## Project Overview

### 1. Wazuh & Graylog Integration

- **Wazuh** is configured as the primary security monitoring solution.
- A **Wazuh agent** is installed on a Windows server to monitor the system and collect security logs.
- **Graylog** is utilized as the centralized logging solution, receiving logs from the Wazuh manager.

### 2. MISP (Malware Information Sharing Platform)

- **MISP** is set up with various threat intelligence feeds to keep an updated list of IOCs.
- Graylog is configured to cross-reference its logs with the IOCs present in MISP.

### 3. IOC Detection & Alerting

- If any log in Graylog contains an IOC that matches an entry in MISP, an **alert** is automatically generated in Graylog.
- The generated alerts are crucial for early detection of potential threats within the monitored environment.

### 4. Grafana Dashboard

- A custom **Grafana dashboard** is built to visualize MISP-related alerts.
- The dashboard provides real-time insights into the IOC matches detected by the system.

**Screenshot Placeholder:**  
*(Insert Grafana dashboard screenshot here)*

### 5. DFIR IRIS Case Management

- Alerts generated in Graylog are sent to **DFIR IRIS** for case management and further investigation.
- This ensures that any detected threat is systematically managed and escalated as needed.

**Screenshot Placeholder:**  
*(Insert DFIR IRIS case management screenshot here)*

### 6. SOCFortress CoPilot Integration

- All these tools are connected using [**SOCFortress CoPilot**](https://github.com/socfortress/CoPilot), which simplifies the integration process and ensures smooth communication between the different components.

**Screenshot Placeholder:**  
*(Insert SOCFortress CoPilot configuration or connection screenshot here)*

## Getting Started

To replicate this setup, follow the steps below:

1. **Wazuh Setup**:
   - Install and configure Wazuh manager.
   - Install Wazuh agent on the Windows server.

2. **Graylog Setup**:
   - Install and configure Graylog.
   - Set up inputs to receive logs from Wazuh.

3. **MISP Setup**:
   - Install and configure MISP.
   - Subscribe to relevant threat feeds.

4. **Integration with Graylog**:
   - Configure Graylog to query MISP for IOC matching.
   - Set up alerting rules in Graylog for any IOC matches.

5. **Grafana Setup**:
   - Install and configure Grafana.
   - Create a dashboard to visualize MISP-related alerts.

6. **DFIR IRIS Setup**:
   - Install and configure DFIR IRIS.
   - Set up integration with Graylog for alert management.

7. **SOCFortress CoPilot Setup**:
   - Download and configure SOCFortress CoPilot.
   - Connect all tools using CoPilot for streamlined operations.

## Resources for Replication

Here are some useful resources that can help you replicate this project:

### Wazuh
- [Wazuh Documentation](https://documentation.wazuh.com/) - Official documentation for setting up and configuring Wazuh.
- [Wazuh YouTube Channel](https://www.youtube.com/c/Wazuh) - Tutorials and guides on Wazuh setup and usage.

### Graylog
- [Graylog Documentation](https://docs.graylog.org/) - Comprehensive guide to setting up and managing Graylog.
- [Graylog Marketplace](https://marketplace.graylog.org/) - Plugins, inputs, and more to enhance Graylog.

### MISP
- [MISP Project Documentation](https://www.misp-project.org/documentation/) - Official MISP documentation for installation and configuration.
- [MISP GitHub Repository](https://github.com/MISP/MISP) - Source code and additional resources for MISP.

### Grafana
- [Grafana Documentation](https://grafana.com/docs/) - Guides and tutorials for setting up Grafana and creating dashboards.
- [Grafana Labs YouTube Channel](https://www.youtube.com/c/Grafana) - Video tutorials on Grafana usage.

### DFIR IRIS
- [DFIR IRIS GitHub Repository](https://github.com/dfir-iris/iris-web) - Source code and setup instructions for DFIR IRIS.
- [DFIR Training](https://www.dfir.training/) - Training and resources for digital forensics and incident response.

### SOCFortress CoPilot
- [SOCFortress CoPilot GitHub Repository](https://github.com/socfortress/CoPilot) - The official repository for CoPilot with installation and configuration guides.
- [SOCFortress YouTube Channel](https://www.youtube.com/@taylorwalton_socfortress) - A series of tutorials and guides that were instrumental in deploying this project.

## Usage

- **Monitoring**: Use Wazuh and Graylog to monitor your environment continuously.
- **IOC Detection**: View alerts in Graylog for any detected IOCs.
- **Visualization**: Monitor MISP-related alerts in Grafana.
- **Case Management**: Manage detected threats in DFIR IRIS.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
