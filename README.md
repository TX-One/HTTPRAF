# HTTPRAF - HTTP Status Scanner 🚀

A high-performance HTTP scanner designed for cybersecurity teams. Key features:

- **Massive Parallelism**: 10K+ URLs/min via libcurl-multi
- **Smart Filtering**: Regex-based status code matching
- **SOC Integration**: JSON/CSV output formats
- **Zero-Dependency**: Single binary deployment

# Quick Start
## Install Dependencies
```bash
sudo apt install libcurl4-openssl-dev
```
## Download & Install
```bash
# Clone The Repo
git clone https://github.com/TX-One/HTTPRAF
# Make executable
chmod +x httpraf
# Install globally
sudo mv httpraf /usr/local/bin/httpraf
```
## Usage
```bash
# Basic Scan

httpraf urls.txt --2xx --output live_targets.txt

# Advanced Usage

httpraf urls.txt --201 --user-agent "Mozilla/5.0 (Red Team / HTTPRAF)" --verbose |tee -a output.txt
```
## --help/--h
```bash
Options:
  --1xx/2xx/3xx/4xx/5xx  Filter by status category
  --<code>               Filter by specific status code (e.g., --404)
  --all                  Show all responses
  --output FILE          Save results to file
  --user-agent STR       Set custom User-Agent
  --silent               Disable all non-essential output
  --verbose              Show detailed processing info
```
# Development Guidelines
## 🏗️ Architecture

```mermaid
flowchart TD
    A[("fa:fa-terminal CLI Parser")]
    B[["fa:fa-search Scan Engine"]]
    C[("fa:fa-cogs libcurl-multi")]
    D[["fa:fa-file-export Output Formatter"]]
    
    A -->|Processes input files<br>and command flags| B
    B -->|Manages parallel HTTP requests<br>using| C
    B -->|Formats filtered results| D
    
    style A fill:#4a90e2,color:white
    style B fill:#7ed321,color:white
    style C fill:#f5a623,color:white
    style D fill:#9013fe,color:white
```
## Security Practices
- Validate all user inputs
- Sanitize output buffers
- Implement rate limiting
- Use CSPRNG for nonce generation

---

# 🤝 Contributing to the Project

🔹 Have improvements? Submit a Pull Request.

🔹 Encountered an issue? Report it in GitHub Issues.


---

# 📞 Support & Contact

📢 Have questions? Reach out through:

🔹 Telegram : https://t.me/TXpOne

🔹 GitHub Issues

---
