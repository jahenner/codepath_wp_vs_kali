# codepath_wp_vs_kali

This repository is about finding and exploiting vulnerabilities in WordPress 4.2 using Kali Linux.

To begin, I ran a wpscan to see what vulnerabilities exists with version 4.2.

![Screen Shot 2022-04-14 at 9 37 53 AM](https://user-images.githubusercontent.com/76822904/163402506-ea6f35ed-3df7-4a19-8aa8-eb39e01c9c23.png)

The --url takes in the URL of the WordPress blog to scan. The --random-user-agent will randomly choose a different user agent for each scan. This allows us to be a little bit more discreet with our scan. The -o will allow us to save the scan in a file, so we don't have to run the scan multiple times if the terminal closes.

![Screen Shot 2022-04-14 at 10 00 17 AM](https://user-images.githubusercontent.com/76822904/163406775-688da73b-bff2-4244-ab8b-777cb24855e5.png)

We see that we find 94 vulnerabilities that were identified (we are using an older version of WordPress for learning purposes)

Looking at the login page for WordPress we notice that the server is giving us too much information. We know when a username is incorrect and when a username exists in the database.

By running another wpscan to enumerate(-e) usernames (u) and check vulnerable plug-ins (-vp) we find a few users.

![ezgif com-gif-maker (12)](https://user-images.githubusercontent.com/76822904/163634276-71131bab-3b0c-4e40-9b67-f3c3a798e278.gif)

Afterwards we can use those found usernames to try brute force attacking the passwords for potential escalation. Again we can use wpscan to accomplish this. We will pass a password list for it to try. We could use rockyou password leaks to attempt this.

![ezgif com-gif-maker (13)](https://user-images.githubusercontent.com/76822904/163634653-d7305490-4e75-43bf-b126-c597cecdd1ef.gif)


