## Release notes

# Privacy Protection with Randomized User-Agent

HTTPRAF includes a built-in randomized User-Agent feature to enhance your privacy during scans. 
This ensures that your requests appear to originate from legitimate browsers, reducing the risk of detection or blocking by target servers.

## Key Features:
- Dynamic Rotation: Automatically rotates through a pool of realistic User-Agent strings.
- Customizable: Override with your own User-Agent using the --user-agent flag.
- Security: Prevents fingerprinting by mimicking real browser behavior.

## Set a custom User-Agent
httpraf urls.txt --user-agent "Mozilla/5.0 (Windows NT 10.0; Win64; x64)"

# Why Use This Feature?

- Anonymity: Avoid revealing your scanning tool's identity.
- Evasion: Bypass basic WAF (Web Application Firewall) rules.
- Flexibility: Test server responses under different client environments.
