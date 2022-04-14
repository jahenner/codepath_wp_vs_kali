# codepath_wp_vs_kali

This repository is about finding and exploiting vulnerabilities in WordPress 4.2 using Kali Linux.

To begin, I ran a wpscan to see what vulnerabilities exists with version 4.2.
![Screen Shot 2022-04-14 at 9 37 53 AM](https://user-images.githubusercontent.com/76822904/163402506-ea6f35ed-3df7-4a19-8aa8-eb39e01c9c23.png)
The --url takes in the URL of the WordPress blog to scan. The --random-user-agent will randomly choose a different user agent for each scan. This allows us to be a little bit more discreet with our scan. The -o will allow us to save the scan in a file, so we don't have to run the scan multiple times if the terminal closes.

