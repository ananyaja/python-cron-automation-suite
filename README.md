# Python Cron Automation Suite

A modular collection of Python and Linux automation utilities designed to streamline local system administration, file management, telemetry monitoring, and background logging on any Linux environment.

## 🚀 Key Features

* **Automated File Organiser:** Cleanly sorts messy directories into structured categories (Documents, Images, Archives, Code, Media) using `pathlib` and `shutil` with collision handling.
* **System Telemetry Inspector:** Lightweight monitoring tool utilising `psutil` to track CPU, RAM, and disk utilisation.
* **Robust Cron Wrapper (`cron_wrapper.py`):** Intercepts scheduled background scripts, manages execution time, captures stdout/stderr, and logs detailed error tracebacks.
* **Cron Log Parser (`parse_cron_log.py`):** Scans master logs, summarises success/error rates, and triggers native Linux desktop alerts (`notify-send`) upon failure.
* **Local Command Centre (`local_dashboard.py`):** Interactive terminal dashboard uniting system stats, thought logging, and cron health checks.

---

## 📂 Repository Structure

```text
.
├── file_organizer.py      # Automated file classification and sorting utility
├── cron_wrapper.py        # Centralised error-handling wrapper for cron jobs
├── parse_cron_log.py      # Log parser and desktop notification alert utility
├── local_dashboard.py     # Interactive terminal command centre
├── requirements.txt       # Project dependencies (e.g., psutil)
└── README.md              # Project documentation
```

##🛠️ Installation & Setup
1. Clone the repository:

```Bash
git clone [https://github.com/ananyaja/your-repo-name.git](https://github.com/ananyaja/your-repo-name.git)

cd your-repo-name
```

2. Install dependencies:

```Bash
pip install -r requirements.txt
```
3. Run the local command dashboard:

```Bash
python3 local_dashboard.py
```
##⏱️ Automation & Cron Integration
To run scripts automatically in the background using Linux cron:

1. Open your crontab editor:

```Bash
crontab -e
```
2. Add your scheduled wrapper command (using absolute paths):

```Bash
0 9 * * 0 /usr/bin/python3 /home/ananyaja/your-repo-name/cron_wrapper.py /home/ananyaja/your-repo-name/file_organizer.py
```

##💡 Author
Developed as part of an ongoing systems engineering and automation workflow.
