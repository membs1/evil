README.txt
==========

Welcome to Evilginx! This guide will help you understand the basic commands and terms used in Evilginx for setting up phishing engagements.

1. **sudo ~/evilginx2/bin/evilginx -p ~/evilginx2/phishlets**
   - Opens the phishlets directory in command line.

: phishlets hostname gpt4 misorf-tg.top

sudo systemctl daemon-reload
sudo systemctl enable evilginx
sudo systemctl start evilginx
sudo systemctl status evilginx

cd ~/evilginx2
sudo ./bin/evilginx -p ./phishlets

membership@oca-sf.org

root@306517:~/evilginx2# sudo lsof -i :53
sudo lsof -i :443
COMMAND    PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
evilginx 93672 root    7u  IPv6 422284      0t0  UDP *:domain 
COMMAND    PID USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
evilginx 93672 root    8u  IPv6 422285      0t0  TCP *:https (LISTEN)
evilginx 93672 root   11u  IPv6 425769      0t0  TCP 23-227-196-78.static.hvvc.us:https->ec2-54-147-226-163.compute-1.amazonaws.com:44852 (ESTABLISHED)
root@306517:~/evilginx2# sudo kill -9 93672
root@306517:~/evilginx2# sudo lsof -i :443
root@306517:~/evilginx2# sudo lsof -i :53
root@306517:~/evilginx2# 



2. **nano ~/evilginx2/bin/evilginx -p ~/blacklists.txt**
   - Opens the blacklist file in a text editor to check blacklisted IPs.

3. **config domain <domain>**
   - Sets the base domain for all phishlets.
   - Example: `config domain evilsite.com`

4. **config ipv4 <ipv4_address>**
   - Sets the external IPv4 address of the current server.
   - Example: `config ipv4 192.168.1.1`

5. **config unauth_url <url>**
   - Changes the URL for all unauthorized requests.
   - Example: `config unauth_url https://www.unauthorized.com`

6. **config wildcards <true|false>**
   - Enables or disables the use of wildcard subdomains.
   - Example: `config wildcards true`

7. **phishlets hostname <phishlet> <hostname>**
   - Sets the hostname for a specific phishlet.
   - Example: `phishlets hostname google google.evilsite.com`

8. **phishlets enable <phishlet>**
   - Enables a specific phishlet.
   - Example: `phishlets enable google`

9. **phishlets disable <phishlet>**
   - Disables a specific phishlet.
   - Example: `phishlets disable google`

10. **lures create <phishlet> <name>**
    - Creates a lure for a specific phishlet.
    - Example: `lures create google login`

11. **lures get-url <id>**
    - Gets the URL of a specific lure.
    - Example: `lures get-url 1`

12. **sessions list**
    - Lists all active sessions.

13. **sessions remove <session_id>**
    - Removes a specific session.
    - Example: `sessions remove 1234abcd`

14. **certs list**
    - Lists all SSL certificates.

15. **certs create <domain>**
    - Creates a new SSL certificate for a domain.
    - Example: `certs create evilsite.com`

16. **blacklist add ip <ip_address>**
    - Adds an IP address to the blacklist.
    - Example: `blacklist add ip 192.168.1.100`

17. **blacklist remove ip <ip_address>**
    - Removes an IP address from the blacklist.
    - Example: `blacklist remove ip 192.168.1.100`

18. **log info**
    - Shows the information log.

19. **log warn**
    - Shows the warning log.

20. **log error**
    - Shows the error log.

21. **log clear**
    - Clears all logs.

22. **debug enable**
    - Enables debug mode.

23. **debug disable**
    - Disables debug mode.

24. **proxy start**
    - Starts the proxy server.

25. **proxy stop**
    - Stops the proxy server.

26. **proxy status**
    - Shows the status of the proxy server.

27. **hostnames list**
    - Lists all configured hostnames.

28. **hostnames add <hostname>**
    - Adds a new hostname.
    - Example: `hostnames add google.evilsite.com`

29. **hostnames remove <hostname>**
    - Removes a hostname.
    - Example: `hostnames remove google.evilsite.com`

30. **ips list**
    - Lists all IP addresses.

31. **ips add <ip_address>**
    - Adds a new IP address.
    - Example: `ips add 192.168.1.1`

32. **ips remove <ip_address>**
    - Removes an IP address.
    - Example: `ips remove 192.168.1.1`

33. **install update**
    - Updates Evilginx to the latest version.

34. **install clean**
    - Cleans up temporary installation files.

35. **uninstall**
    - Uninstalls Evilginx.

36. **backup create <name>**
    - Creates a backup with a specific name.
    - Example: `backup create backup_2024`

37. **backup restore <name>**
    - Restores a backup with a specific name.
    - Example: `backup restore backup_2024`

38. **update**
    - Checks for and applies updates.

39. **help**
    - Shows help for all commands.

40. **version**
    - Shows the current version of Evilginx.

41. **exit**
    - Exits the Evilginx interface.

42. **sessions show <session_id>**
    - Shows details of a specific session.
    - Example: `sessions show 1234abcd`

43. **config reload**
    - Reloads the configuration file.

44. **phishlets get-hosts <phishlet>**
    - Outputs host entries needed for local development.
    - Example: `phishlets get-hosts google`

45. **phishlets debug <phishlet>**
    - Enables debug mode for a specific phishlet.
    - Example: `phishlets debug google`

46. **lures update <id> <new_url>**
    - Updates the URL of a specific lure.
    - Example: `lures update 1 https://newphishinglink.com`

47. **lures delete <id>**
    - Deletes a specific lure.
    - Example: `lures delete 1`

48. **certs renew <domain>**
    - Renews the SSL certificate for a domain.
    - Example: `certs renew evilsite.com`

49. **sessions terminate <session_id>**
    - Terminates a specific session.
    - Example: `sessions terminate 1234abcd`

50. **sessions export <session_id>**
    - Exports session data to a file.
    - Example: `sessions export 1234abcd`

(Continue with more detailed commands and explanations up to 100 items)

For more detailed guidance, please visit:
- [Evilginx Documentation](https://help.evilginx.com/docs/guides)
README.txt
==========

(Continued from previous section)

51. **dns resolve <domain>**
    - Resolves the IP address of a domain.
    - Example: `dns resolve evilsite.com`

52. **dns cache clear**
    - Clears the DNS cache.

53. **dns cache show**
    - Shows the current DNS cache.

54. **phishlets import <url>**
    - Imports a phishlet from a URL.
    - Example: `phishlets import https://example.com/phishlet.yaml`

55. **phishlets export <phishlet> <path>**
    - Exports a phishlet to a specified path.
    - Example: `phishlets export google /path/to/google.yaml`

56. **certs delete <domain>**
    - Deletes the SSL certificate for a domain.
    - Example: `certs delete evilsite.com`

57. **certs list-expiring**
    - Lists all SSL certificates that are about to expire.

58. **logs enable <phishlet>**
    - Enables logging for a specific phishlet.
    - Example: `logs enable google`

59. **logs disable <phishlet>**
    - Disables logging for a specific phishlet.
    - Example: `logs disable google`

60. **alerts enable <type>**
    - Enables specific alert types (e.g., session, error).
    - Example: `alerts enable session`

61. **alerts disable <type>**
    - Disables specific alert types.
    - Example: `alerts disable session`

62. **firewall enable**
    - Enables the built-in firewall.

63. **firewall disable**
    - Disables the built-in firewall.

64. **firewall add rule <rule>**
    - Adds a firewall rule.
    - Example: `firewall add rule "allow from 192.168.1.1"`

65. **firewall remove rule <rule>**
    - Removes a firewall rule.
    - Example: `firewall remove rule "allow from 192.168.1.1"`

66. **lures activate <id>**
    - Activates a specific lure.
    - Example: `lures activate 1`

67. **lures deactivate <id>**
    - Deactivates a specific lure.
    - Example: `lures deactivate 1`

68. **geoip enable**
    - Enables GeoIP blocking.

69. **geoip disable**
    - Disables GeoIP blocking.

70. **geoip block <country_code>**
    - Blocks access from a specific country.
    - Example: `geoip block US`

71. **geoip unblock <country_code>**
    - Unblocks access from a specific country.
    - Example: `geoip unblock US`

72. **sessions import <file>**
    - Imports session data from a file.
    - Example: `sessions import /path/to/sessions.json`

73. **sessions export all <file>**
    - Exports all session data to a file.
    - Example: `sessions export all /path/to/sessions.json`

74. **config show**
    - Shows the current configuration.

75. **config reset**
    - Resets the configuration to default settings.

76. **install dependencies**
    - Installs all necessary dependencies.

77. **phishlets clone <phishlet> <new_name>**
    - Clones an existing phishlet with a new name.
    - Example: `phishlets clone google google_clone`

78. **certs auto-renew enable**
    - Enables automatic SSL certificate renewal.

79. **certs auto-renew disable**
    - Disables automatic SSL certificate renewal.

80. **auth list**
    - Lists all authentication tokens.

81. **auth add <token>**
    - Adds a new authentication token.
    - Example: `auth add mytoken123`

82. **auth remove <token>**
    - Removes an authentication token.
    - Example: `auth remove mytoken123`

83. **config backup <file>**
    - Creates a backup of the current configuration.
    - Example: `config backup /path/to/backup.conf`

84. **config restore <file>**
    - Restores the configuration from a backup file.
    - Example: `config restore /path/to/backup.conf`

85. **services restart**
    - Restarts all services.

86. **services start**
    - Starts all services.

87. **services stop**
    - Stops all services.

88. **users list**
    - Lists all users.

89. **users add <username> <password>**
    - Adds a new user with a username and password.
    - Example: `users add admin password123`

90. **users remove <username>**
    - Removes a user.
    - Example: `users remove admin`

91. **status system**
    - Shows the system status.

92. **status phishlets**
    - Shows the status of all phishlets.

93. **update check**
    - Checks for updates without applying them.

94. **update apply**
    - Applies available updates.

95. **alert notify <message>**
    - Sends a custom alert notification.
    - Example: `alert notify "Phishlet google activated"`

96. **debug log show**
    - Shows the debug log.

97. **debug log clear**
    - Clears the debug log.

98. **session timeout set <minutes>**
    - Sets the session timeout duration.
    - Example: `session timeout set 30`

99. **session timeout show**
    - Shows the current session timeout duration.

100. **session timeout reset**
    - Resets the session timeout to default.

For more detailed guidance, please visit:
- [Evilginx Documentation](https://help.evilginx.com/docs/guides)
