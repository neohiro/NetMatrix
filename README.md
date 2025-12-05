# NET_MATRIX // SYSTEM_OVERWATCH

"Wake up, Neo..."

NetMatrix Monitor is a Python-based network intelligence tool that transforms standard system monitoring into a high-tech, sci-fi "System Overwatch" experience. It provides real-time visualization of all active network connections, process associations, and geolocation data, wrapped in a sleek, "Matrix-style" terminal interface.

⚡ Features

Active Monitoring: Real-time stream of all TCP/UDP connections (PID, Protocol, Local/Remote Address, State).

Sci-Fi Aesthetic: Immersive dark-mode GUI with CRT-style greens, deep blacks, and monospace typography.

GeoIP Intelligence: automatically resolves and displays the Country of Origin for remote connections in the background.

Deep Trace Investigation: Select any connection to perform a deep lookup, revealing ISP, Organization, City, and Lat/Lon coordinates.

Search Matrix: Real-time filtering bar to instantly isolate connections by Process Name, PID, or IP.

Kill Switch: Terminate suspicious processes directly from the interface with a confirmation safeguard.

Context Actions: Right-click context menu to quickly copy IPs, PIDs, or Process Names to the clipboard.

Auto-Elevation: Automatically requests Administrator/Sudo privileges to ensure full visibility of system-level processes.

🛠️ Prerequisites

Python 3.x

Operating System: Windows, Linux, or macOS (UI is optimized for Windows).

Dependencies

The tool relies on psutil for system data and requests for the GeoIP API.

pip install psutil requests


🚀 Usage

Clone the Repository:

git clone [https://github.com/yourusername/net-matrix-monitor.git](https://github.com/yourusername/net-matrix-monitor.git)
cd net-matrix-monitor


Run the Script:

python net_matrix.py


Note on Privileges: NetMatrix Monitor requires Administrator (Windows) or Root/Sudo (Linux/Mac) privileges to:

View connections owned by system processes (not just your own).

Resolve Process Names for all PIDs.

Terminate processes.

The script includes a built-in check that will attempt to auto-elevate itself if run without sufficient permissions.

📡 API Usage

This tool uses the free API provided by ip-api.com for geolocation data.

Rate Limits: The script implements a background worker queue with delays to respect the API's rate limits (45 requests per minute).

Usage: Please use responsibly to avoid IP bans.

⚠️ Disclaimer

This tool allows for the termination of system processes. While safeguards are in place (confirmation dialogs, kernel protection checks), please exercise caution when terminating PIDs you do not recognize. The author is not responsible for system instability caused by misuse.

📄 License

Distributed under the MIT License. See LICENSE for more information.
