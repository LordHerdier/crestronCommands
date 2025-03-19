# Commandset for the HD-PS401

> HD-PS401 [v1.4.4790.00038 (Mar 3 2022), %2350NEJ04549] @E-c442685306cb HD-
> PS401>
>
> 146 normal commands found. 0 hidden commands available.

8021XAUthenticate |  Enable/Disable 802.1x Authentication.  
---|---  
      
    
    8021xAuthenticate [ON |OFF]
            ON           - Enable 802.1x Supplicant Authentication
            OFF          - Disable 802.1x Supplicant Authentication
            No parameter - displays current setting
    
    HD-PS401>
      
  
8021XDOMain |  Configure/View 802.1x Domain Name.  
      
    
    8021xDomainName [Domain Name]
            DomainName   - Update Domain Name To Domain Specified
            No parameter - displays current setting
    
    HD-PS401>
      
  
8021XMEThod |  Configure/View EAP Method.  
      
    
    8021xMethod [Password |Certificate |List]
            Password     - 802.1x Suplicant Will Use Secured Password (EAP MSCHAP V2) EAP Method
            Certificate  - 802.1x Suplicant Will Use Certificate EAP Method
            List         - 802.1x Suplicant Will display the supported EAP Methods
            No parameter - displays current setting
    
    HD-PS401>
      
  
8021XPASsword |  Configure 802.1x Password.  
      
    
    8021xPassword [Password]
            {Password}      - Update Password To One Specified
            No parameter    - Echo back command
    
    HD-PS401>
      
  
8021XSENdpeapver |  Enable/Disable 802.1x Peap version reporting.  
      
    
    8021xSendPeapVer [ON |OFF]
            ON           - enable 802.1x peap version number report
            OFF          - disable 802.1x peap version number report
            No parameter - displays current setting
            Note: This setting only applies for 8021xMethod Password
            Does not work with Windows 2012 radius server
    
    HD-PS401>
      
  
8021XTRUStedcas |  Select/List 802.1x Trusted CA Certificates  
      
    
    8021xTrustedCAs [LIST|USE|DONTUSE] [|Name UID])
            LIST                 - List All Trusted Certificates
            LISTN                - List and number all Trusted Certificates
            LISTU                - List only Trusted Certificates marked use
            USE [#|Name UID]     - Add Specified Certificate To List Of Certificates Used To Validate The Server
            DONTUSE [#|Name UID] - Remove Specified Certificate From List Of Certificates Used To Validate The Server
            No parameter - Display this help message
    HD-PS401>
      
  
8021XUSERname |  Configure/View 802.1x User Name.  
      
    
    8021xUsername Password 
    
      
  
8021XVALidateserver |  Require Validation Of 802.1x Authentication Server's Certificate.  
      
    
    8021xValidateServer [OFF|ON]
            OFF - 802.1x supplicant will not validate authentication server's certificate
            ON - 802.1x supplicant will validate authentication server's sertificate
            No parameter - displays current setting
    
    HD-PS401>
      
  
ADDBLOCKEDip |  Add an IP Address to the blocked list  
      
    
    ADDBLOCKEDip [ipaddress]
            ipaddress - ip address to block
            No parameter - display current list of blocked ip addresses
    
    HD-PS401>
      
  
ADDDOMAINGroup |  Create a new domain group  
      
    
     ADDDOMAINGROUP -N:domaingroupname -L:accesslevel
            -N: specifies the domain group name (domain\group)
            -L: specifies one of the following access level:
                    A - as an Administrator
                    P - as a Programmer
                    O - as an Operator
                    U - as a User
                    C - for Connection only
    
    HD-PS401>
      
  
ADDDns |  Add an entry to DNS server List  
      
    
    ADDDns ip_address
            ip_address - IP address in dot decimal notation
    HD-PS401>
      
  
ADDGroup |  Create a new local group  
      
    
     ADDGROUP -N:groupname -L:accesslevel
            -N: specifies the domain group name (domain\group)
            -L: specifies one of the following access level:
                    A - as an Administrator
                    P - as a Programmer
                    O - as an Operator
                    U - as a User
                    C - for Connection only
    
    HD-PS401>
      
  
ADDLOCKEDUser |  Add user to the blocked list  
      
    
    ADDLOCKEDuser [username]
            username - user to block
            No parameter - display current list of blocked users
    
    HD-PS401>
      
  
ADDMaster |  Add an entry to IP table  
      
    
    Format: AddMaster cip_id ip_address/name [RoomId]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            RoomId - Optional.  Up to a 32 character Id. Valid characters are A-Z and 0-9.
                            - This is used for communication with a Virtual Control server
    HD-PS401>
      
  
ADDPUBKEYTouser |  Add a public key to an existing user account  
      
    
    ADDPUBKEYtouser -N:username -K:keyfilename
            -N: specifies name of a local user
            -K: specifies name of a public key file pre-uploaded to \user folder
    HD-PS401>
      
  
ADDPeer |  Add an entry to Peers IP table  
      
    
    ERROR: Command not supported on this product
    HD-PS401>
      
  
ADDREMOTeweb |  Add an entry to Remote Web Connections table  
      
    
    ADDENTRY Format: ADDREMOTEWEB RemoteId ModelName RemoteWebAddress UserName Password
            RemoteId - Id of the Remote Device. Valid Id: 1
            ModelName - Name of the Remote Device Model Name.
            RemoteWebAddress - Ipaddress/FQDN Name of the Remote Device.
            Username - UserName of the Remote Device.
            Password - Password of the Remote Device.
    HD-PS401>
      
  
ADDUSER |  Create a new local user  
      
    
    ADDUSER -N:username {-P:password}
            -N: specifies name of the local user to be created
            -P: specifies the password for the user
    HD-PS401>
      
  
ADDUSERTogroup |  Add an existing local or domain user to an existing local group  
      
    
    ADDUSERTOGROUP -N:username -G:groupname
            -N: specifies name of a local user or domain (domain\user) user
            -G: specifies name of a local group
    HD-PS401>
      
  
ADLOGIN |  Active Directory Login  
      
    
    ADLOGIN -D:domainname -N:username [-P:password]
            -D: specifies name of the domain
            -N: specifies name of the user
            -P: specifies the password for the user
            Prompts for password if not specified.
    HD-PS401>
      
  
ADLOGOUt |  Active Directory Logout  
      
    
    ADLOGOUT
            No parameters needed
    HD-PS401>
      
  
AUCHECKNOW |  Check for updates now.  
      
    
    AUCHECKNOW
             No Parameters - Checks for auto update actions now.
    
    HD-PS401>
      
  
AUDITLogging |  Display or Change the current audit logging operation.  
      
    
    AUDITLogging [ON|OFF] {[ALL]|[NONE]|{[ADMIN] [PROG] [OPER] [USER]} [REMOTESYSLOG]}
            ON - Enable Logging
            OFF - Disable Logging
            No parameter - Displays current setting
    NOTE: Logons, logoffs, & account management is always logged
    - optional, used to log commands by access level
            ADMIN - Administrator
            PROG - Programmer
            OPER - Operator
            USER - User
            ALL - All Access Levels
            NONE - No Command Logging
    Example: 'AUDITLOGGING ON ADMIN OPER'
            REMOTESYSLOG - Write to the remote syslog server only.
    HD-PS401>
      
  
AUENABLE |  Enable/disable automatic updates.  
      
    
    AUENABLE [ON|OFF]
             Enable/disable auto updates.
             No Parameters - Displays current setting
    
    HD-PS401>
      
  
AUFORCEUPDATENOW |  Force updates now.  
      
    
    AUFORCEUPDATENOW [COMPONENT]
             COMPONENT - ALL,FW,PROJECT,CONFIG,COPY.
             No Parameters - Forces all components to update now.
    
    HD-PS401>
      
  
AUMANIFESTURL |  Get or Set auto updater manifest URL.  
      
    
    AUMANIFESTURL [URL]
            URL - URL of manifest file.
            NONE- clear the of manifest url path.
            No Parameters - Displays current setting
    
    HD-PS401>
      
  
AUPASSWORD |  Get or Set auto updater password.  
      
    
    AUPASSWORD [password]
             password - Password for downloading auto update files.
                      - To clear password use keyword "none" as password.
             No Parameters - Displays current setting
    
    HD-PS401>
      
  
AUPOLLINTERVAL |  Set how long to wait before checking for updates again.  
      
    
    AUPOLLINTERVAL [interval_in_minutes]
             interval_in_minutes     - How many minutes to wait before checking for updates. (0 to disable)
                                             - Valid range (60 - 65535)
             No Parameters           - Displays current setting
    
    HD-PS401>
      
  
AUSTATUS |  Reports the auto update status.  
      
    
    AUSTATUS
             No Parameters - Displays current auto update status
    
    HD-PS401>
      
  
AUTHentication |  Authentication on/off  
      
    
    AUTHENTICATION [OFF | ON]
            ON - turns on authentication.
            OFF - is disabled. User cannot turn OFF Authentication.
            No parameter - displays current setting
    HD-PS401>
      
  
AUTIME |  Set a scheduled time for when to check for updates.  
      
    
    AUTIME [TIME]
             TIME - The day of week and time when a scheduled check for update should take place:
                    ie: monday 15:45 will schedule an update check every monday at 3:45 pm.
                    ie: 15:45 will schedule an update check every day at 3:45 pm.
                  - To clear time use keyword "NONE" as [TIME].
             No Parameters - Displays current setting
    
    HD-PS401>
      
  
AUTODiscovery |  Commands for Ethernet auto discovery  
      
    
    AUTODISCOVERY 
            ON - Turn autodiscovery on
            OFF - Turn autodiscovery off
            HOSTS - Show list of discovered nodes
    HD-PS401>
      
  
AUUSERNAME |  Get or Set auto updater username.  
      
    
    AUUSERNAME [username]
             username - Username for downloading auto update files.
                      - To clear username use keyword "none" as username.
             No Parameters - Displays current setting
    
    HD-PS401>
      
  
AUVERIFY |  Configure verification when negotiating TLS and SSL connections.  
      
    
    AUVERIFY [OFF | VERIFY]
             OFF - No verification.
             Verify - Verify certificate name against host and the peer's SSL ceritifcate.
             No Parameters - Displays current setting
    
    HD-PS401>
      
  
BROADcast |  Enable Error Broadcast  
      
    
    BROADCAST [ON | OFF]
            No parameter - displays current setting
    HD-PS401>
      
  
BYE |  Close user session  
      
    
    BYE - Closes the user session for the current connection
    HD-PS401>
      
  
CARDS |  Display Cards detected in system  
      
    
    CARDS
            No parameters
    HD-PS401>
      
  
CD |  Change directory  
      
    
    CD [directory]
            directory - string containing directory specification
            No parameter - display current setting
    HD-PS401>
      
  
CERTIFicate |  Add, Remove, List or View Certificates  
      
    
    CERTIFicate Cmd Certificate_Store   
            Where Cmd = [ADD|REM|LIST|LISTN|VIEW]
            Where Certificate_Store = [ROOT|MACHINE|INTERMEDIATE|SIP|STREAM|WEBSERVER]
    
      
  
CIPPORT |  Set port number for CIP  
      
    
    CIPPORT [portnumber]
            portnumber - desired port number > 4096 (in decimal).
            No parameter - displays current value
    HD-PS401>
      
  
CIPSERVERPORT |  Set port number for CIP Server  
      
    
    CIPSERVERPORT [portnumber]
            portnumber - desired port number > 4096 (in decimal).
    HD-PS401>
      
  
CIPTIMEOUT |  Set/Get CIP connection timeout  
      
    
    CIPTIMEOUT [value]
     alue - desired CIP connection establishment timeout (in decimal) second. Minimum 300s
    HD-PS401>
      
  
CLEARAUDITLOG |  Clear the audit log.  
      
    
    CLEARAUDITLOG
            No parameter - Clears the audit log
    HD-PS401>
      
  
CLEARCSAUTHENTICATIon |  Clear Control System Authentication  
      
    
    ClearCSAuthentication
    Clear Authentication parameters for CIP connect message.
    HD-PS401>
      
  
CLEARerr |  Clears the current error log  
      
    
    CLEARERR
            Clears the current error log.
    HD-PS401>
      
  
COPYfile |  Copy a file to a different directory  
      
    
    COPYfile sourcespec destspec
            sourcespec - source file name specification (could be relative to current dir)
            destspec - destination file name specification (could be relative to current dir)
            filenames with embedded spaces must be enclosed in double quotes("The File")
    HD-PS401>
      
  
CREATECsr |  Generate a CSR.  
      
    
    ERROR: CREATECSR is not supported on this type of device.
    HD-PS401>
      
  
DEFRouter |  Set default router  
      
    
    DEFROUTER [device_num ip_address]
            ip_address - IP address in dot decimal notation
            device_num - specified Ethernet device
            /now - take effect without a reboot
            No parameter - displays current value
    HD-PS401>
      
  
DELETEDOMAINGroup |  Delete an existing domain group  
      
    
    DELETEDOMAINGROUP groupname [/Y]
            domaingroupname - name of the domain group (domain\groupname) to be deleted.
    HD-PS401>
      
  
DELETEGroup |  Delete an existing local group  
      
    
    DELETEGROUP groupname [/Y]
            groupname - name of the group to be deleted.
    HD-PS401>
      
  
DELETEUser |  Delete an existing local user  
      
    
    DELETEUser username [/Y]
            username - name of the user to be deleted.
    HD-PS401>
      
  
DELete |  Remove File(s)  
      
    
    DELETE filesearchstring
            filesearchstring - search string which may contain wildcards
    HD-PS401>
      
  
DHCP |  Control dynamic IP addressing  
      
    
    DHCP [device_num  [ON | OFF | REL_RENEW]] [/now]
            ON - enables DHCP for device_num
            OFF - disables DHCP for device_num
            REL_RENEW - performs a DHCP release and renew for device_num
            /now - takes effect without a reboot
            No parameter - displays current setting
    
    HD-PS401>
      
  
DHCPEx |  Control dynamic IP addressing  
      
    
    DHCP [device_num  [ON | OFF | REL_RENEW]] [/now]
            ON - enables DHCP for device_num
            OFF - disables DHCP for device_num
            REL_RENEW - performs a DHCP release and renew for device_num
            /now - takes effect without a reboot
            No parameter - displays current setting
    
    HD-PS401>
      
  
DHCPOpt |  Use FQDN in DHCP Discover Request  
      
    
    DHCPOpt [HOSTNAME | FQDN]
            HOSTNAME - Send Local HostName in DHCP Discover Request - Default Option
            FQDN - Send the Fully Qualified Domain name in Discover Request
            No parameter - displays current setting
    HD-PS401>
      
  
DIR |  List files and directories in current directory  
      
    
    DIR filesearchstring
            filesearchstring - search string which may contain wildcards
    HD-PS401>
      
  
DOMAinname |  Set domain name  
      
    
    DOMAINNAME [string | /CLEAR] [/now]
            string - ASCII string containing domain name
            /CLEAR - clears the value
            /now - take effect without a reboot
            No parameter - current value
    HD-PS401>
      
  
ECHo |  Enable/disable character echoing  
      
    
    ECHO [ON | OFF]
            No parameter - displays current setting
    HD-PS401>
      
  
ERASE |  Remove file(s)  
      
    
    ERASE filesearchstring
            filesearchstring - search string which may contain wildcards
    HD-PS401>
      
  
ERRlog |  Prints the current error log  
      
    
    ERRLOG {SYS | PLOGCURRENT | PLOGPREVIOUS | PLOGALL | NOTICE | WARNING | ERROR | FATAL }
            No parameter:  Display the last 500 messages with Notice severity or greater
            SYS - Show the last 500 messages
            PLOGCURRENT - print persistent log for current session
            PLOGPREVIOUS - print persistent log for previous session
            PLOGALL - print persistent log for current and previous session
            NOTICE - print all notices and above (default)
            WARNING - print all warnings and above
            ERROR - print all errors and above
            FATAL - print all fatal errors and above
    HD-PS401>
      
  
FGETfile |  FTP file from a remote server  
      
    
    FGETfile [url] [local_path] {username:password}
            url - fully qualified URL to the file being downloaded from the server
            local_path - destination path to the file in the ROM
            username:password - access credentials to the server
    HD-PS401>
      
  
FORCEDREBOOT |  Forces system reboot  
      
    
    FORCEDREBOOT - reboot system
    HD-PS401>
      
  
FPUTfile |  FTP file to a remote server  
      
    
    FPUTfile [url] [local_path] {username:password}
            url - fully qualified URL to the file being uploaded to the server
            local_path - path to the source file in the ROM
            username:password - access credentials to the server
    HD-PS401>
      
  
FREE |  Show available file space  
      
    
    FREE - Indicates free disk space
            No parameter needed
    HD-PS401>
      
  
GETAUDITLOG |  Retrieve the audit log.  
      
    
    UPLOAD AUDITLOG via XMODEM
    GETAUDITLOG
            No parameter - retrieve the audit log file via xmodem
    HD-PS401>
      
  
GETPAsswordrule |  Display password rules  
      
    
    GETPASSWORDRULE
            No parameters needed.
    HD-PS401>
      
  
HEARTBEATtimeout |  Set/Get heartbeat timeout  
      
    
    HEARTBEATTIMEOUT [timeoutInMilliSeconds]
            timeoutInMilliSeconds - Timeout before sending a CIP heartbeat to the peer if no messages are received from the peer. Default value is 30
    seconds.
            No parameter - displays current setting
    HD-PS401>
      
  
HELP |  Display help screens  
      
    
    HELP [ALL|DEV|ETHER|SYS|BACNET|USER|CRESTIMERENG|DEVICE]
    HD-PS401>
      
  
HOSTname |  Set hostname  
      
    
    HOSTNAME [string | /clear] [/now]
            string - ASCII string containing host name
            /clear - clears the value
            /now - take effect without a reboot
            No parameter - current value
    HD-PS401>
      
  
ICMP |  Turn ON/OFF ICMP  
      
    
    ICMP [ON|OFF]
            ON:  will enable ICMP so the device replies to ping messages.
            OFF: will disable ICMP so the device will not replies to ping messages.
    HD-PS401>
      
  
INFO |  Print Software Capabilities  
      
    
    INFO
            No parameters
    HD-PS401>
      
  
INITIALIZE |  Clear file system  
      
    
    INITIALIZE
             No parameter
    HD-PS401>
      
  
IPAddress |  Set IP address  
      
    
    IPADDRESS [device_num ip_address] [/now]
            ip_address - IP address in dot decimal notation
            device_num - specified Ethernet device
            /now - take effect without a reboot
            No parameter - displays current value
    HD-PS401>
      
  
IPCONFIG |  Display/Configure IP Settings  
      
    
    usage: ipconfig [/all | /renew [adapter index] | /release [adapter index] ] /flushdns
             ?         Display this help message
             /release  Release the IP address of the specified adapter
             /renew    Renew the IP address of the specified adapter
             /flushdns Clean the name resolution client cache
    HD-PS401>
      
  
IPMask |  Set IP subnet mask  
      
    
    IPMASK [device_num ip_address]
            ip_address - IP address in dot decimal notation
            device_num - specified Ethernet device
            /now - take effect without a reboot
            No parameter - displays current value
    HD-PS401>
      
  
IPROUTE |  Print Kernel IP routing table  
      
    
    IPROUTE - display network routing table
    HD-PS401>
      
  
IPTable |  Display IP table  
      
    
    IPTABLE
            -T Display data in a tabular format
            -C Clears the IP Table.
    HD-PS401>
      
  
ISDIR |  Is the parameter a directory  
      
    
    ISDIR directory
            directory - string containing directory specification
    HD-PS401>
      
  
KILLSOCKET |  Close an active TCP console socket  
      
    
    KILLSOCKET [CTPx | SHELLx]
            CTPx - kill CTP console #x
            SHELLx - kill SHELL (SSH) console #x
    HD-PS401>
      
  
LISTBLOCKEDips |  List the blocked IP addresses  
      
    
    LISTBLOCKEDip
            No parameter - display current list of blocked ip addresses
    
    HD-PS401>
      
  
LISTDNS |  Display the list of DNS servers  
      
    
    LISTDNS
            shows current DNS servers - no parameters needed
    HD-PS401>
      
  
LISTDNSEx |  Display the list of DNS servers  
      
    
    LISTDNS
            shows current DNS servers - no parameters needed
    HD-PS401>
      
  
LISTGROUPS |  List existing local groups  
      
    
    LISTGROUPS [A] [P] [O] [U] [C]
            A: groups with administrator rights will be listed
            P: groups with programmer rights will be listed
            O: groups with operator rights will be listed
            U: groups with user rights will be listed
            C: groups with connection rights will be listed
            No parameter: all groups will be listed
    HD-PS401>
      
  
LISTGROUPUsers |  List all existing (local and domain) users in an existing  
      
    
    LISTGROUPUSERS groupname
    HD-PS401>
      
  
LISTLOCKEDUsers |  List blocked users  
      
    
    LISTLOCKEDuser
            No parameter - display current list of blocked users
    
    HD-PS401>
      
  
LISTPUBKEYFromuser |  List existing public key from an existing user account  
      
    
    LISTPUBKEYfromuser -N:username
            -N: specifies name of a local user
    HD-PS401>
      
  
LISTUSERS |  List of users authenicated on thus system  
      
    
    LISTUSERS
            No parameter - display current list of users
    HD-PS401>
      
  
LOGINSTAT |  Set time to count valid logins  
      
    
    LOGINSTAT [period]
            No parameter - Display login statistics period
            Period - time in days to count # of successful logins (1-30)
    HD-PS401>
      
  
LOGOFF |  Logs the currently authenticated user out of the system  
      
    
    Logs the currently authenticated user out of the system  
  
MAKEDIR |  Creates a directory  
      
    
    Creates a directory  
  
MOVEfile |  Move a file to a different directory  
      
    
    MOVEfile sourcespec destspec
            sourcespec - source file name specification (could be relative to current dir)
            destspec - destination file name specification (could be relative to current dir)
            filenames with embedded spaces must be enclosed in double quotes("The File")
    HD-PS401>
      
  
NVRAMREBOOT |  Print reboot information  
      
    
    NVRAMREBOOT [SHOW]
            SHOW - display the last reboot message in NVRAM
    HD-PS401>
      
  
PING |  Ping remote node  
      
    
    Usage: ping [-ncount] [-iTTL] [-wtimeout] address
    Options:
            -n count      Send count.
            -i TTL        Time to live.
            -w timeout    Timeout (in seconds)
            -S address    Source address to use (IPv6-only).
            -4            Force using IPv4.
            -6            Force using IPv6.
    Attention: This command has no space between option and option parameter.
    HD-PS401>
      
  
PRINTAUDITLOG |  Print the audit log.  
      
    
    PRINTAUDITLOG {[ALL]}
            All - Print the entire audit log
            No parameter - Print the last 50 entries from the log
    HD-PS401>
      
  
RAMFree |  Show available RAM file space  
      
    
    RAMFree [-x]
            -x - Attribute reclaimable memory to the reclaimable field and not to free memory.
    HD-PS401>
      
  
REBOOT |  Reboot the device  
      
    
    REBOOT - reboot system
    HD-PS401>
      
  
REMBLOCKEDip |  Remove an IP Address from the blocked list  
      
    
    REMBLOCKEDip [ALL|ipaddress]
            ipaddress - ip address of the blocked connection
            ALL - remove all blocked ip addresses
            No parameter - display current list of blocked ip addresses
    HD-PS401>
      
  
REMDns |  Remove an entry from DNS server List  
      
    
    REMDNS ip_address
            ip_address - IP address in dot decimal notation
    HD-PS401>
      
  
REMLOCKEDUser |  Remove user from the blocked list  
      
    
    REMLOCKEDuser [ALL|username]
            username - username of the blocked connection
            ALL - remove all blocked users
            No parameter - display current list of blocked users
    HD-PS401>
      
  
REMMaster |  Remove a master entry  
      
    
    Format: REMMaster cip_id ip_address/name [RoomId]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            RoomId - Optional.  Up to a 32 character Id. Valid characters are A-Z and 0-9.
                            - This is used for communication with a Virtual Control server
    HD-PS401>
      
  
REMOTEWEBConnections |  Display Remote Web Connections  
      
    
    REMOTEWEBCONNECTIONS
            No Argument: Display RemoteWebConnections data.
            -T:  Display RemoteWebConnections data in a tabular format.
            -C:   Clears the RemoteWebConnections.
    HD-PS401>
      
  
REMOVEDIR |  Remove a Directory  
      
    
    REMOVEDIR directory
            directory - string containing directory specification
    HD-PS401>
      
  
REMOVEPUBKEYFromuser |  Remove an existing public key from an existing user account  
      
    
    REMOVEPUBKEYfromuser -N:username
            -N: specifies name of a local user
    HD-PS401>
      
  
REMOVEUserfromgroup |  Remove an existing local or domain user from an existing local group  
      
    
    REMOVEUSERFROMGROUP -N:username -G:groupname
            -N: specifies name of a local or domain user
            -G: specifies name of a local group
    HD-PS401>
      
  
REMPeer |  Remove an entry from Peers IP table  
      
    
    ERROR: Command not supported on this product
    HD-PS401>
      
  
REMREMOTeweb |  Remove a Web connection Entry  
      
    
    REMENTRY Format: REMREMOTEWEB  RemoteId
            RemoteId - Id of the Remote Device.
    HD-PS401>
      
  
RESETPassword |  Reset an existing local user's password  
      
    
    RESETPASSWORD -N:username {-P:defaultpassword}
            -N: specifies name of the user to be reset
            -P: specifies the default password
    HD-PS401>
      
  
RESTORe |  Restore factory defaults  
      
    
    RESTORE
             No parameter
    HD-PS401>
      
  
RMLOGerr |  Enable logging errors to the file.  
      
    
    RMLOGERR
     [OFF|ON] -F: {Filename} -S:{MaxSize} -N:{MaxNumOfFiles} {OK | INFO | NOTICE | WARNING | ERROR | FATAL}
            -F:{Filename}: Filename is name of the Log file (must include the path and '.log' as file extension)
            -S{MaxSize}: MaxSize is between 262144 and 5242880 bytes
            -N{MaxNumOfFiles}: MaxNumOfFiles is between 1 and 10
            OK - log to file all OKs and above
            INFO - log to file all info messages and above
            NOTICE - log to file all notices and above
            WARNING - log to file warnings and above
            ERROR - log to file errors and above
            FATAL - log to file fatal errors and above
    
    HD-PS401>
      
  
SECURECIPport |  Set the secure (SSL) port number for CIP  
      
    
    SECURECIPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays the current value
    HD-PS401>
      
  
SECUREWebport |  Set Secure(SSL) port number for Web.  
      
    
    SECUREWEBPORT [portnumber]
            portnumber - desired port number  (in decimal).
            No parameter - displays the current value
    HD-PS401>
      
  
SETCSAUTHENTICATION |  Set Control System Authentication credentials.  
      
    
    SETCSAUTHENTICATION -N:Username -P:Password
            -N: specifies name of a local or domain (domain\user) user
            -P: specifies password.
    HD-PS401>
      
  
SETLOCKOUTTIME |  Set time that an IP is blocked from login  
      
    
    SETLOCKOUTTIME [number]
            number - number of hours (suffix 'h') or minutes (suffix 'm') to block an IP Address, 0 is indefinite, 750 hours or 45000 minutes max
            No parameter - display current setting.
    
    HD-PS401>
      
  
SETLOGINAttempts |  Set the number of login attempts before blocking IP  
      
    
    SETLOGINAttempts [number]
            number - number of login attempts a user will have before the console is blocked. 0 is infinite.
            No parameter - display current setting.
    
    HD-PS401>
      
  
SETLogoffidletime |  Set idle time allowed before current user is automatically logged off  
      
    
    SETLOGOFFIDLETIME [minutes]
            minutes - idle minutes passed before current user is logged off (Limit 60 minutes). 0 means user will NOT be logged off automatically.
            No parameter - display current transport setting.
    
    HD-PS401>
      
  
SETPAsswordrule |  Set password rules  
      
    
    SETPASSWORDRULE {-ALL | -NONE} | {-LENGTH:minPasswordLength} {-MIXED} {-DIGIT} {-SPECIAL}
            -ALL: all rules will be applied.
            -NONE no rule will be applied.
            -LENGTH: specifies minimum password length if greater than 6.  By default, the minimum length is 8. This parameter can't be combined with
    NONE.
            -MIXED: password must contain a lower and upper case character. This parameter can't be combined with NONE.
            -DIGIT: password must contain a number. This parameter can't be combined with NONE.
            -SPECIAL: password must contain a special character. This parameter can't be combined with NONE.
    
    HD-PS401>
      
  
SETUSERLOCKOUTTime |  Set time that a user is blocked from login  
      
    
    SETUSERLOCKOUTTIME [number]
            number - number of hours (suffix 'h') or minutes (suffix 'm') to block a User, 0 is indefinite, 750 hours or 45000 minutes max, or -1 to
    restore the default value
            No parameter - display current setting.
    
    HD-PS401>
      
  
SETUSERLOGINATtempts |  Set the number of login attempts before blocking User  
      
    
    SETUSERLOGINAttempts [number]
            number - number of login attempts a user will have before the console is blocked. 0 is infinite, or -1 to restore the default value.
            No parameter - display current setting.
    
    HD-PS401>
      
  
SHOWHW |  Display hardware configuration  
      
    
    SHOWHW
            No parameters
    HD-PS401>
      
  
SNTP |  Configure network time synchronization  
      
    
    SNTP [START|STOP|SYNC|DELETE {SERVER|SERVER2|SERVER3}|SERVER {args}|SERVER2 {args}|SERVER3 {args}]
            START  - start synchronization
            STOP   - stop synchronization
            SYNC   - force synchronization (one time)
            DELETE {SERVER|SERVER2|SERVER3}  - delete configuration for NTP server1 or server2 or server3
            SERVER:{address} [optional args] - address of primary NTP server with optional arguments
            SERVER2:{address} [optional args]- address of secondary NTP server to synchronize with optional arguments
            SERVER3:{address} [optional args]- address of secondary NTP server to synchronize with optional arguments
              optional args:
               PORT:{1-65535} - NTP Port (Default 123)
               AUTH:{MAC} - Secured NTP. MAC authentication.
               KEYTYPE:{MD5(less secured)|SHA1|SHA256} - Key Type for MAC authentication only. (Default SHA1).
               KEY:{shared key} - Pre-Shared key between NTP client and server. (MAC authentication only).
               KEYID:{1-65535} - Pre-Shared key index between NTP client and server. (MAC authentication only).
               Example:
                1. SNTP SERVER:macntp.example.com AUTH:mac KEYID:1 KEY:e5fa44f2b31c1fb553b6021e7360d07d5d91ff5e
                2. SNTP SERVER:pool.example.com
            No parameter - displays current setting
    HD-PS401>
      
  
SSHPORt |  Enable/Disable and configure SSH port number  
      
    
    SSHPORT [OFF | ON | port number]
            [OFF | ON ] - Disables/Enables SSH. Default is ON
            portnumber - desired port number (in decimal).
            no parameter - displays current value
    HD-PS401>
      
  
SSHSERVer |  User Configure the SSH server and the public keys  
      
    
    SSHSERVer 
    
      
  
SSL |  Display/Set SSL type  
      
    
    SSL [OFF | NOVERIFY | CA] {TLSSSL | TLSONLY | TLS1.2ONLY}
            where 'OFF' turns off SSL,
            where 'NOVERIFY' turns on SSL, but accepts any certificate from the control system without verifying it,
            where 'CA' turns on SSL, and sets SSL to verify server certificates,
            No parameter - displays the current setting
    HD-PS401>
      
  
SSLVERIFY |  Display/Set SSL certificate verification.  
      
    
    SSLVERIFY [ALL] | [[OFF|CA] | [-T:ON|OFF]] [-X:ON|OFF] [-C:ON|OFF] [-S:ON|OFF] [-H:ON|OFF]
            'ALL' enables all verification options,
            'OFF' disables server certificate trust check (allow both SELF and CA certificates),
            'CA' ensures that a server certificate is issued by a trusted CA,
            -T:ON|OFF enable/disable verification that a server certificate is issued by a trusted CA,
            -X:ON|OFF enable/disable required presence of extendedKeyUsage in server certs,
            -C:ON|OFF enable/disable required presence of CA in basicConstraints of
               installed server certs,
            -S:ON|OFF enable/disable required trusted signer on installed server certs,
            -H:ON|OFF enable/disable server certificate hostname checking,
            The OFF and CA parameters are deprecated; use the -T switch instead.
            The X option applies to outgoing TLS connections and to
               installed server certificates.
            No parameter - displays current setting
    HD-PS401>
      
  
SWRSTP |  ENABLE/DISABLE RSTP  
      
    
    SWRSTP ON/OFF
    Enables/disables RSTP, reboot required to take effect.
    
    HD-PS401>
      
  
SYSLOG |  Enable/disable system UI log.  
      
    
    SYSLOG [ON|OFF|CLEAR|PRINT|LOGNOTICEON|LOGNOTICEOFF|LOGEXTRAON|LOGEXTRAOFF]
             Enable/disable UI system logging.
             No Parameters - Displays current setting
    
    HD-PS401>
      
  
TASKSTAT |  Lists applications in system  
      
    
    TASKSTAT
            Usage:
              taskstat
              taskstat                - list processes with cpu & memory usage
              taskstat -t             - list processes, threads with cpu & memory usage
              taskstat -find:text     - list processes, threads filtered
    lists application in system.
    HD-PS401>
      
  
TESTDNS |  Test DNS Server  
      
    
    TESTDNS string
            string - ASCII string containing host name
    HD-PS401>
      
  
TIMEZone |  Get/Set the timezone  
      
    
    TIMEZONE [LIST | zone]
            LIST - print timezones
            zone - number of the timezone to set
            No parameter - displays current setting
    HD-PS401>
      
  
TIMEdate |  Get the time and date  
      
    
    TIMEdate [hh:mm:ss mm-dd-yyyy]
            hh:mm:ss - time in hours (use 24hr), mins and secs
            mm/dd/yyyy or mm-dd-yyyy - date in months(1-12), day(1-31) and year
            No parameter - displays current setting
    HD-PS401>
      
  
TLSVERsion |  Set the minimum TLS version.  
      
    
    TLSVERSION [TLS1.2]
            where 'TLS1.2' indicates that this is the minimum version for TLS connections.
            No parameter - displays the current setting
    HD-PS401>
      
  
TOP |  Lists proceseses and threads in system  
      
    
    TOP usage:
              lists processes and threads in system with cpu & memory usage
              top [-find:text] [-lines:#|ALL] [-col:#] [-sort:] [-rsort:sort options]  [-p:##|ALL]
                 -t        show threads, only with single columns
                 -p        filter crestron apps [##] or [ALL]
                 -lines    number of lines to display, default 25, all|ALL for all lines
                 -col      number of columns to display, default 1
                 -find     case insensitive filter, words can be quoted
                 -sort     ascending sort (default pid)
                 -rsort    desending sort
                    sort options: pid, cpu, time, mem, name, thread
              example: top -col:2
              example: top -t -lines:40 -col:2 -rsort:mem
              example: top -find:ctpd -lines:ALL -rsort:mem
              example: top -t -p:1
              example: top -p:ALL
    HD-PS401>
      
  
TYPE |  Display file contents  
      
    
    TYPE filename
            filename - the name of the file to display
    HD-PS401>
      
  
UPDATEPassword |  User Update current local user's password  
      
    
    UPDATEPASSWORD
            No parameters needed
    HD-PS401>
      
  
UPGRADERESULTS |  Print results of last upgrade command  
      
    
    UPGRADERESULT - show result of last upgrade
    HD-PS401>
      
  
UPTIME |  Display the time the system is running  
      
    
    UPTIME
            no parameters needed
    HD-PS401>
      
  
USBCOMMAND |  Executes commands from USB commands.txt  
      
    
             Executes commands from USB commands.txt
    
    HD-PS401>
      
  
USERInformation |  Show access information for a specific user  
      
    
    USERINFOrmation username
             username - Show the access information of the specified user.
    HD-PS401>
      
  
USERPAGEAUTH |  User page Authentication on/off  
      
    
    USERPAGEAUTH [OFF | ON]
            ON - turns on User Page Authentication.
            OFF - turns off User Page Authentication.
            No parameter - displays current setting
    HD-PS401>
      
  
VERsion |  Print version to console  
      
    
    VERSION [-v]
            -v : show extended version info
    HD-PS401>
      
  
WEBPORT |  Set port number for Webserver.  
      
    
    WEBPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays the current value
    HD-PS401>
      
  
WEBSERVER |  Enable/disable Webserver  
      
    
    WEBSERVER [ON | OFF | TIMEOUT  | MAXSESSIONSPERUSER ]
    WEBSERVER [TIMEOUT] will display current session timeout value
    WEBSERVER MAXSESSIONSPERUSER will display current max web sessions per user
            No parameter - displays current setting
    HD-PS401>
      
  
WHO |  Generate a report of the Ethernet consoles  
      
    
    WHO
             No Parameter necessary
    HD-PS401>
      
  
WHOAmi |  Display current user's identity  
      
    
    WHOAMI
            No parameter needed.
    HD-PS401>
      
  
XGETfile |  Use XMODEM to transfer file from ROM  
      
    
    XGET filename
            filename - name of the file
    HD-PS401>
      
  
XPUTfile |  Use XMODEM to transfer file to ROM  
      
    
    XPUT size date time name
            size - size of the file in bytes
            date - date of the file (MM-DD-YY)
            time - UTC time of the file (HH:MM:SS)
            name - name of the file
    HD-PS401>
    

