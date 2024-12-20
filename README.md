# **Steam Workshop Item Stats Tracker**
A Python-based tool to monitor and log analytics for a specified Steam Workshop item. This application retrieves data such as views, subscriptions, and favorites, then displays the metrics in a live-updating graphical interface. You can also store the collected data in an Excel file for later analysis.

## Features
Configuration UI:
Easily set up your API key, Workshop Item ID, polling interval, and Excel output file path via a simple configuration GUI. No need to edit code or YAML files manually.

- **Multiple Configurations**
Specify which configuration file to use. Load and save different configurations to quickly switch between multiple Workshop items or environments.

- **Real-Time Updates**
Monitors the Workshop item's statistics at a fixed interval and updates the main UI with the latest values.

- **Data Logging to Excel**
Automatically logs collected stats to a time-stamped Excel file. Great for tracking trends over time.

- **Visual Graphing**
The integrated matplotlib graph updates in real-time, providing a visual snapshot of changes to subscriptions and other metrics.

### Requirements
Python: 3.6 or higher
Libraries:
- requests
- openpyxl
- matplotlib
- pyyaml
- tkinter (usually included with Python on most platforms)

### Getting Started
1. Install missing dependencies using:
`pip install requests openpyxl matplotlib pyyaml
`
2. Clone the Repository:
`git clone https://github.com/yourusername/steam-workshop-stats-tracker.git
cd steam-workshop-stats-tracker`
Install Dependencies: Ensure you have Python installed, then:
`pip install -r requirements.txt`
(If a requirements.txt is provided. Otherwise, install packages individually as shown above.)

3. Run the Application:
`python your_script_name.py`
When you first run the script:
- A configuration window will appear.
- Enter your API Key, the Workshop Item ID, the polling interval (in seconds), and the Excel file path.
- Specify or confirm the config.yaml file path if you want to use a custom config file.
- Click Apply to save your configuration.
- Click Start to begin monitoring.

4. Monitor Your Stats: After starting, the main UI will appear:

- The left side shows various metrics (timestamp, views, subscriptions, favorites, lifetime stats).
- A dynamic graph updates over time to visualize subscription trends.
- Data is periodically logged to an Excel file with a timestamped name based on the current month and year.

### Configuration Management
- **Changing Config Files**: You can switch to a different config file by entering its path in the Config File Path field and clicking Load Config in the configuration window.

- **Saved Settings**: The application remembers the last used configuration file path in last_used_config.txt, ensuring the same config is used next time you run the app.

### Notes & Limitations
- **API Key Security**:
Make sure to keep your API key private. Do not commit config.yaml or other sensitive files to your public repository.

- **Border Radius on Fields**:
Tkinter does not natively support rounded corners on widgets. The styling simulates a flat, modern look, but true rounded corners would require additional custom drawing or third-party widgets.

- **Data Availability**:
The quality and frequency of updates depend on the Steam API. Ensure you have a stable internet connection and a valid API key.

### Troubleshooting
- **No Data?**
Double-check that your API key is correct and that the Workshop Item ID is valid.

- **Connection Errors:**
Ensure you have internet access and no firewall is blocking the api.steampowered.com domain.

- **Visualization Issues:**
If the graph does not update, confirm that matplotlib is installed and that no exceptions are occurring in the console.

### Contributing
Feel free to submit pull requests, open issues, or contribute improvements. Whether it's code refactoring, UI enhancements, or new features, your contributions are welcome!

### License
This project is released under the MIT License. You are free to use, modify, and distribute this software as permitted by the license.

This README is a template. Adjust details such as repository URLs, file paths, or additional instructions as needed.
