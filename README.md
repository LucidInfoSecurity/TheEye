# The Eye Project

## Description

This is a fully featured adversary monitoring application based on the work done by various people on Ransomlook.io, it extends the functionality of their work by adding additional monitoring pages, such as; 

1. Darknet/TOR examination and surveillance
2. Newspaper indexing, ingestion and translation for breaches.
3. CVE registry monitoring
4. Realtime ingestion of IOCs (Domain/IPs)
5. Collection of documentation on APT/TA groups

The application has also been modified to make use of Cloudflare Workers, D1, R2. 

The current setup allows for an AI to translate text instead of using Google Translate, R2 is used for fast data delivery to the client and D1 replaces the Redis database used in Ransomlook.

The application is also fully dockerized, with the Website being contained seperately to the data collector.

## Installation

To install the project, follow these steps:

1. Clone this repo (A fresh installation of Ubuntu server 22.04 is recommended.)
2. Run the "install.sh" script as a normal user (not SUDO or ROOT, the account must have sudo permissions though.)
3. Modify the configuration file in TheEye/config/
4. The site should be live on http://localhost:8080

Some features will require additional configuration on your behalf to get this working. For example the API uses a Cloudflare Worker connected to a D1 database within Cloudflare.

## Contributing

If you want to contribute to the project, please fork the main branch and then create a pull request. Junk/spammy merge requests will just get you banned from contributing. 

## License

[GNU GENERAL PUBLIC LICENSE]
