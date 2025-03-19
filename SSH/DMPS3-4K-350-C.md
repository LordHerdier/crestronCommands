# Commandset for the DMPS3-4K-350-C

> DMPS3-4K-350-C Cntrl Eng [v1.502.3224.17519 (Oct 30 2017), #87C2404A]
> @E-00107faddaf7
>
> 199 normal commands found. 110 hidden commands available.

8021XAUthenticate |  Enable/Disable 802.1x Authentication.  
---|---  
      
    
    8021xAuthenticate [ON |OFF]
            ON  - Enable 802.1x Supplicant Authentication
            OFF - Disable 802.1x Supplicant Authentication
            No parameter - displays current setting
    
      
  
8021XDOMain |  Configure/View 802.1x Domain Name.  
      
    
    8021xDomainName [Domain Name]
             DomainName - Update Domain Name To Domain Specified
            No parameter - displays current setting
    
      
  
8021XMEThod |  Configure/View EAP Method.  
      
    
    8021xMethod [Password |Certificate |List]
            Password - 802.1x Suplicant Will Use Secured Password (EAP MSCHAP V2) EAP Method
            Certificate - 802.1x Suplicant Will Use Certificate EAP Method
            List - 802.1x Suplicant Will display the supported EAP Methods
            No parameter - displays current setting
    
      
  
8021XPASsword |  Configure 802.1x Password.  
      
    
    8021xPassword [Password]
            {Password} - Update Password To One Specified
            No parameter - Echo back command
    
      
  
8021XSENdpeapver |  Enable/Disable 802.1x Peap version reporting.  
      
    
    8021xSendPeapVer [ON |OFF]
            ON  - enable 802.1x peap version number report
            OFF - disable 802.1x peap version number report
            No parameter - displays current setting
    
      
  
8021XTRUStedcas |  Select/List 802.1x Trusted CA Certificates.  
      
    
    8021xTrustedCAs [LIST|USE|DONTUSE] )
            LIST -                               List All Trusted Root Certificates
            USE {Certificate Name and UID} -     Add Specified Certificate To List Of Certificates Used To Validate The Server
            DONTUSE {Certificate Name and UID} - Remove Specified Certificate From List Of Certificates Used To Validate The Server
            No parameter -                      Display this help message
    
      
  
8021XUSERname |  Configure/View 802.1x User Name.  
      
    
    8021xUsername Password 
             Password - Displays current settings
             Password {Name} - Update User Name To Name Specified
             No parameter - Displays Help Menu
    
      
  
8021XVALidateserver |  Require Validation Of 802.1x Authentication Server's Certificate.  
      
    
    8021xValidateServer [ON |OFF]
            ON  - 802.1x Suplicant Will Validate Authentication Server's Certificate
            OFF - 802.1x Suplicant Will Not Validate Authentication Server's Certificate
            No parameter - displays current setting
    
      
  
ADDBLOCKEDip |  Add an IP Address to the blocked list  
      
    
    No help available for this command.  
  
ADDDOMAINGroup |  Add a domain group to this control system  
      
    
    No help available for this command.  
  
ADDDns |  Add an entry to DNS server List  
      
    
    ADDDNS ip_address
            ip_address - IP address in dot decimal notation
    
      
  
ADDGroup |  Create a new local group  
      
    
    No help available for this command.  
  
ADDLICense |  Add application license.  
      
    
    ADDLICENSE [License] {Name} - add license
            License - license key
            Name - license name string (optional)
    
      
  
ADDMaster |  Add a master entry to IP table  
      
    
    Format: ADDMaster cip_id ip_address/name
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
    
      
  
ADDPOrtmap |  Add a port map to the port forwarding table.  
      
    
    ADDPOrtmap {-d} ext_port int_port ip_address/hostname protocol
            -d   - Option for port forwarding from the LAN side to the CS side or from the CS side to the DMNET side of Router
            ext_port   - port number on the LAN side of Router when {-d} is not selected. Otherwise it is a port number on the CS side of Router
            int_port   - port number on the CS side of Router when {-d} is not selected.  Otherwise it is a port number on the DMNET side of Router
            ip_address - IP address (in dot decimal notation) of the device on the CS side of Router when {-d} is not selected. Otherwise the device is on
    the DMNET side of Router
            hostname   - Hostname of the device on the CS side of Router when {-d} is not selected. Otherwise the device is on the DMNET side of Router
            protocol   - IP protocol for the portmap service (TCP | UDP | Both)
    
      
  
ADDPeer |  Add a peer(slave) entry to IP table  
      
    
    Format: ADDPeer cip_id ip_address/name [-D:device_id] [-C:cipport] [-P:program]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            device_id       - ID in device redirection table (in hex) (must be < 256)
            port number     - port number for the connection (in dec) (must be > 256)
            program         - program number which uses device (in dec) (default 1)
    
      
  
ADDUSER |  Create a new local user  
      
    
    No help available for this command.  
  
ADDUSERTogroup |  Add an existing local or domain user to an existing local group  
      
    
    No help available for this command.  
  
ADLOGIn |  Login to Active Directory server  
      
    
    No help available for this command.  
  
ADLOGOut |  Logout from Active Directory server  
      
    
    No help available for this command.  
  
APPSTATs |  Dumps out Registered App Stats  
      
    
     APPSTATS {-P:ALL | -P:Specific Program Identifier}
             -P:  Dump app info for a specific program or ALL.  If not present, ALL assumed.
    
    
      
  
AUCANCEL |  Cancel the auto update in progress.  
      
    
    AUCANCEL
             No Parameters - Cancels any pending auto update.
    
      
  
AUCHECKNOW |  Check for updates now.  
      
    
    AUCHECKNOW
             No Parameters - Checks for auto update actions now.
    
      
  
AUDEVCONNECTPASS |  Get/Set the password used by auto update to login to Crestron devices.  
      
    
    AUDEVCONNECTPASS [password]
             password - Password for connecting to remote devices.
                      - To clear password use keyword "none" as password.
             No Parameters - Displays current setting
    
      
  
AUDEVCONNECTUSER |  Get/Set the username used by auto update to login to Crestron devices.  
      
    
    AUDEVCONNECTUSER [username]
             username - Username for connecting to remote devices.
                      - To clear username use keyword "none" as username.
             No Parameters - Displays current setting
    
      
  
AUDITLogging |  Display or Change the current audit logging operation.  
      
    
    No help available for this command.  
  
AUENABLE |  Enable/disable automatic updates.  
      
    
    AUENABLE [ON|OFF]
             Enable/disable auto updates.
             No Parameters - Displays current setting
    
      
  
AUFORCEUPDATENOW |  Force updates now.  
      
    
    AUFORCEUPDATENOW
             No Parameters - Forces manifest file to be processed now.
    
      
  
AUMANIFESTURL |  Get or Set auto updater manifest URL.  
      
    
    AUMANIFESTURL [URL]
            URL - URL of Manifest file.
            NONE- clear the of Manifest url path.
            No Parameters - Displays current setting
    
      
  
AUPASSWORD |  Get/Set the password used by auto update to login to the update server.  
      
    
    AUPASSWORD [password]
             password - Password for downloading auto update files.
                      - To clear password use keyword "none" as password.
             No Parameters - Displays current setting
    
      
  
AUPLUGINCATALOGURL |  Get or Set auto updater plugin catalog URL.  
      
    
    AUPLUGINCATALOGURL [URL]
            URL - URL of Plugin Catalog file.
            NONE- To go back to the Default Plugin Catalog URL which is http://www.crestron.com/autofwupdates/AU-Plugin-Catalog.txt.
            No Parameters - Displays current setting
    
      
  
AUPOLLINTERVAL |  Set how long to wait before checking for updates again.  
      
    
    AUPOLLINTERVAL [interval_in_minutes]
             interval_in_minutes - How many minutes to wait before checking for updates.
                                   Will be rounded up to the nearest hour.  0 to disable.
             No Parameters - Displays current setting
    
      
  
AUSTATUS |  Reports the auto update status.  
      
    
    AUSTATUS
             No Parameters - Displays current auto update status
    
      
  
AUTHentication |  Authentication on/off  
      
    
    AUTHENTICATION [ON|OFF]
            ON - turns on authentication.
            OFF - turns off authentication.
            No parameter - displays current setting.
    
      
  
AUTIME |  Set a scheduled time for when to check for updates.  
      
    
    AUTIME [TIME]
             TIME is [SUNDAY|MONDAY|TUESDAY|WEDNESDAY|THURSDAY|FRIDAY|SATURDAY] HH:MM
                HH:MM:  24 hour time when the manifest file should be read.
                Specifying only HH:MM will make the update run every day at that time.
                Specifying the day in addition HH:MM will make the update run only at that day and time each week.
             To clear time use keyword "none" as [TIME].
             No Parameters - Displays current setting
    
      
  
AUTODIScovery |  Commands for Ethernet auto discovery  
      
    
    AUTODISCOVERY [ON | OFF | QUERY | LIST | HOSTS | LIGHTBYIP ipaddress | LIGHTBYTYPE type {NOFORCEALL}| STOPLIGHT | SETNEXTID id | SQUAWK | SETHOSTNAME
    ipaddress hostname | CLEARBYIP ipaddress | CLEARBYTYPE type | FORCEBYTYPE type | SETNUMTIMESQUERYMSGSENT times | SETDELAYBETWEENQUERYMSGINMS delayInMs
    | OPTION autodiscoveryqueryoption | ADAPTER autodiscoveryadapteroption]
            on : enables autodiscovery functions
            off : disables autodiscovery functions
            query : runs the discovery query
            list : displays the list of nodes discovered
            hosts : displays the list of hostnames
            lightbyip : puts in the device at the specified IP address into light-n-poll mode.
            lightbytype : puts in the devices of the specified type into light-n-poll mode.
                    NoForceAll : Will not force all the devices into light-n-poll mode if the specified device type is not found.
            stoplight : removes all devices from light-n-poll mode.
            setnextid : indicates that the next ID to set is id.  Entered in hex.
            squawk : simulates pressing the SW-R button in light and poll mode.
            sethostname: assigned the given hostname to the device at specified ip address.
            clearbyip : clears the IP table in the device at the specified IP address.
            clearbytype : clears the IP table in the devices of the specified type.
            forcebytype : force the device of the specified type to the previous chosen ID.
            setnumtimesquerymsgsent : Set the number of times the query message is sent.
            setdelaybetweenquerymsginms : Set the delay (in msec) between sending each query message.
            option : Sets autodiscovery query message option [HOSTNAME | IPADDRESS | HOSTNAME_IPA].
            adapter : Sets autodiscovery adapter option [LAN | CS | BOTH].
    
      
  
AUTONEGot |  Set auto negotiation for Ethernet Device  
      
    
    AUTONEGOT [device_num (ON | 10HALF | 10FULL | 100HALF | 100FULL)]
            device_num - number of device to set (0 or 1)
            ON - autonegotiation is ON
            10HALF - autonegotiation is OFF, use 10mps, half duplex.
            10FULL - autonegotiation is OFF, use 10mps, full duplex.
            100HALF - autonegotiation is OFF, use 100mps, half duplex.
            100FULL - autonegotiation is OFF, use 100mps, full duplex.
            No parameter - displays current setting
    
      
  
AUUSERNAME |  Get/Set the username used by auto update to login to the update server.  
      
    
    AUUSERNAME [username]
             username - Username for downloading auto update files.
                      - To clear username use keyword "none" as username.
             No Parameters - Displays current setting
    
      
  
BACNETADAPTER |  Configure BACnet operation for running on LAN, Control Subnet, or USB Ethernet  
      
    
    BACNETADAPTER [0 | 1 | 3]
            No parameters - Current status of BACnet configuration. Default is '0' LAN
            0 - BACnetAdapter is LAN
            1 - BACnetAdapter is Control Subnet
            3 - BACnetAdapter is USB Ethernet
    
      
  
BASICAUthentication |  Enable web server basic authentication.  
      
    
    BASICAUTHENTICATION [ON | OFF]
            ON - Enable basic authentication for web server.
            OFF - Disable basic authentication for web server.
            No parameter - Display current setting.
    
      
  
BLACKBIRD |  Console command to enable OOTBF debug data  
      
    
    
      
  
BROADcast |  Enable/disable broadcasting of errors.  
      
    
     BROADCAST [ON|OFF]
         No parameter - displays current setting
    
      
  
BYE |  Close user session for this connection  
      
    
    BYE - Closes the user session for the current connection
    
      
  
CARDS |  Display Cards Detected in System  
      
    
     CARDS
     No parameters
    
      
  
CD |  Change Directory  
      
    
    CD [directory]
            directory - string containing directory specification
            No parameter - display current setting
    
      
  
CERTIFicate |  Add, Remove, List or View Certificates  
      
    
    CERTIFicate Cmd Certificate_Store {Certificate_Name} {Certificate_UID} {Password}
             Where Cmd = [ADD|REM|LIST|VIEW]
             Where Certificate_Store = [ROOT|MACHINE|USER|INTERMEDIATE]
             ADD  Certificate_Store -                  Add Certificate(from known location) To Specified Certificate Store (MACHINE store requires
    password)
             REM  Certificate_Store Certificate_Name Certificate_UID -  Remove Specified Certificate From Specified Certificate Store
             LIST Certificate_Store -                  List All Certificates In Specified Certificate Store
             VIEW Certificate_Store Certificate_Name Certificate_UID -  View Details Of Specified Certificate In Specified Certificate Store
             No parameter -                            Lists Usage
    
      
  
CIPHER |  Set/Get the class of ciphers/algorithms used for the encryption  
      
    
    CIPHER [STRONG/ALL]
            parameter - desired set of ciphers/algorithms SSH server will use for encryption
            No parameter - displays current value
    
      
  
CIPPORT |  Set port number for CIP  
      
    
    CIPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current value
    
      
  
CLEARAUDITLOG |  Clear the audit log.  
      
    
    No help available for this command.  
  
CLEARCSAUTHENTICATION |  Clear Control System Authentication credentials.  
      
    
    ClearCSAuthentication
    Clear Control System Authentication parameters for CIP connect message.
    
      
  
CLEAREVents |  Clear application timer events  
      
    
    Clear all timer events for specified event group within application program id.
    CLEAREVENTS -I:ProgramTag -G:GroupEventName
             -I: ProgramTag/UserDefinedTag
             -G: Group Event Name
    
      
  
CLEARerr |  Clears the current error log.  
      
    
     CLEARERR
         Clears the current error log.
    
      
  
CLOUDPROXYAUTH |  Sets the authentication method for connecting to a proxy  
      
    
    Sets the specified authentication methods to try when connecting to a proxy, the methods must be space delimited
    CLOUDPROXYAUTH: [None | Basic | Digest | Digest_IE | NTLM | ANY | ANYSAFE | ONLY]
            None - no authentication
            Basic - Most commonly used and supported, username/password are sent in clear text (DEFAULT)
            Digest - More secure than BASIC, username/password are NOT sent in clear text
            Digest_IE - Digest authentication with an IE flavor
            NTLM - A proprietary protocol invented and used by Microsoft. It uses a challenge-response and hash concept similar to Digest, to prevent the
    password from being eavesdropped
            ANY - Automatically selects whatever is suitable, the most secure option is preferred
            ANYSAFE - Automatically selects whatever is suitable except 'BASIC', the most secure option is preferred
            ONLY - Specifies that if authentication is required only the seleced method is acceptable
    
      
  
CLOUDPROXYURL |  Sets the url of the proxy used to make requests  
      
    
    Sets the url of the proxy used to make requests
    CloudProxyUrl: [scheme://][username:password@][hostname | ipAddress][:port]
            scheme - The scheme of the request: http, socks4, socks5, etc
            username - The username used to connect to the proxy server (OPTIONAL)
            password - The password used to connect to the proxy server (OPTIONAL)
            hostname - The hostname of the proxy server
            ipAddress - The ip address of the proxy server
            port - The port number the proxy server is listening on (OPTIONAL, default '1080')
    Use 'clear' to clear the current url
    
      
  
COPYfile |  Copy a file to a different directory  
      
    
    COPYFILE sourcespec destspec
            sourcespec - source file name specification (could be relative to current dir)
            destspec - destination file name specification (could be relative to current dir)
            filenames with embedded spaces must be enclosed in double quotes("The File")
    
      
  
CORE3XPANELWEB |  Configure the core3 XPanel Flash policy server  
      
    
    Core3XpanelWeb [ON | OFF] [DOMAIN] [PORT(s)] [SECURE_OFF | SECURE_ON]
            ON - enables Smart Graphics XPanel Web
            OFF - disables Smart Graphics XPanel Web
            DOMAIN - sets Smart Graphics XPanel Web domain
            PORT(s) - sets Smart Graphics XPanel Web port(s) (0 to use default port, * to open all ports. Other valid input examples: "64232" or
    "64232,6700-8900")
            SECURE_OFF - Smart Graphics XPanel Web can only connect to control system using an unencrypted connection
            SECURE_ON - Smart Graphics XPanel Web can only connect to control system using encrypted TLS/SSL. Note: SSL must be ON and CA Signed
            No parameter - displays current setting
    
      
  
CREATECsr |  Generate a CSR.  
      
    
    CREATECSR CN:SN:LN:ON:OUN:DN:EA [-P:password] [-I:option]
            where CN = 2 letter country code
            where SN = Full state or province name
            where LN = Locality or city name
            where ON = Organization or company name
            where OUN= Organizational Unit name or division
            where DN = site name or domain name
            where EA = Email address
            where -P: sets password for the private key file being generated
            where -I: Ignore blank parameters. Options are True or False.
    
      
  
CSINAutomode |  Display if the router is in the automatic/Manual mode  
      
    
    CSINAutoMode
             No parameter - Displays if the control subnet is in the automatic or manual mode
    
      
  
CSIODebug |  Set/View run-time CSIO debug options.  
      
    
    CSIODEBUG
    View incoming and outgoing packets on the CSIO interface
    [ON/OFF] Turns on and off debug trace.
             No Parameters - Displays current debug settings
    
      
  
CSROUTerprefix |  Display or Configure Control Subnet's Static Router Prefix.  
      
    
    CSRouterPrefix [IP_Address/Prefix_Size]
             IP_Address - IP Address
             Prefix_Size - Number of leading bits of the routing prefix.
             No parameter - Displays Current Control Subnet Prefix Configuration
    
      
  
CTPPORT |  Set/Get the CTP Port  
      
    
    CTPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current value
    
      
  
DATASTOREDELete |  Clear the Logs for the Specified Program  
      
    
    DATASTOREDELETE [-T:DAYS OLD] [-P:ALL | -P:Specific OWNER ID] [-L | -G]
            -T: Delete older than xxx days
            -P: Clear DATASTORE for a specific owner or ALL.
            -L: Operate on Local Store
            -G: Operate on Global Store
    
      
  
DATASTOREEXPORT |  Export to XML file  
      
    
    DATASTOREEXPORT [-F:filename] [-P:ALL | -P:Specific OWNER ID] [-L | -G]
            -F:\filepath\filename for result. Default is Console
            -P: Export DATASTORE records for a specific owner or ALL.
            -L: Operate on Local Store
            -G: Operate on Global Store
    
      
  
DATASTOREIMPORt |  Import from XML file  
      
    
    DATASTOREIMPORT [-F:filename] [-L | -G]
            -F:\filepath\filename to import. Default is Console
            -L: Operate on Local Store
            -G: Operate on Global Store
    
      
  
DATASTORESTATus |  The Data Store Status  
      
    
    DATASTORESTATUS
    Gives Information on All data Store databases.
    
      
  
DBGDEVice |  (*) Simulate incoming packets for the selected device  
      
    
    DBGDEVICE[:program#] {devnum} {packet} {-L}  - Simulate an incoming packet {packet} for device {devnum}
            program#: number of program to execute. (default=1)
              {devnum} is a Hex number (i.e. 0x0014) or a decimal number (i.e. 20)
              {packet} is a Quoted string representation of a packet without an ID or count
                    (i.e. "\x00\x01\x80" represents a digital low for join 1)
              -L means the packet should be treated as a long packet.
    
      
  
DBGPKTRX |  (*) Show/hide all packets received by the device symbol layer  
      
    
    DBGPKTRX[:program#] {Parameters}
            program#: number of program to execute. (default=1)
            -S:ON|OFF       Turn ON or OFF display of Incoming packets
            -N:C|E|S|A      Show for Cresnet, Ethernet, Slot, or All [All assumed if not present]
            -I:ID           ID to debug; Preface with 0x for Hex.  Assumes all ID's if not present.
            -H:ON|OFF       Show packets as hex only
            -T:ON|OFF       Timestamp
            Current Status:  OFF
    
      
  
DBGPKTTX |  (*) Show/hide all packets sent by the device symbol layer  
      
    
    DBGPKTTX[:program#] {Parameters}
            program#: number of program to execute. (default=1)
            -S:ON|OFF       Turn ON or OFF display of Outgoing packets
            -N:C|E|S|A      Show for Cresnet, Ethernet, Slot, or All [All assumed if not present]
            -I:ID           ID to debug; Preface with 0x for Hex.  Assumes all ID's if not present.
            -H:ON|OFF       Show packets as hex only
            -T:ON|OFF       Timestamp
            Current Status:  OFF
    
      
  
DBGSIGnal |  Sets or clears Debug flag for signal processing  
      
    
    Sets or clears Debug flag for signal processing  
  
DBGTRANSMITTER |  (*) Sets or clears Debug flag for IR/RF Transmitter  
      
    
    Sets or clears Debug flag for IR/RF TransmitterCustomizable help. See the text file donotexec.upc  
  
DEBug |  Set/View run-time debug options  
      
    
    Valid options are:
     CONsole - via current console
     DISable - all debugs OFF
     ASCII -  ASCII only
     MIXED -  ASCII and hex
     HEX_ONLy -  hex, no ACSII
     HEX -  hex with space
     NO_ZERoes -  skip zeroes
     ALL_HEX -  all hexadecimal
     SER_DATa -  serial data only
     SINGLe_id - single cresnet ID
     POWERUP - powerup ON|OFF
     ON - all or powerup
     OFF - all or powerup
     SAVE - save in EEPROM
     LEVel - set debug level(0-3)
            syntax: debug # ON|OFF [lev #]
     HELP - show levels bitmap
       Status if no arguments
     #0 bitmap:
    To use debug:
       - enable debug output: DEBUG [CONSOLE]
       - specify what to debug(run DEBUG with no parameters for opt#): DEBUG opt# [ON|OFF]
       - to kill all debugs: DEBUG OFF
       - to restore or clear settings after powerup(does autosave): DEBUG POWERUP [ON|OFF]
       - to save manually debug conf(DEBUG OFF does not autosave): DEBUG SAVE
    
    
      
  
DEFRouter |  Set default router.  
      
    
    DEFROUTER [device_num ip_address]
            device_num - specified Ethernet device  [0 - 3]
            ip_address - IP address in dot decimal notation
            No parameter - displays current value
    
      
  
DELETEDOMAINGroup |  Delete a domain group that was previously added to this control system  
      
    
    No help available for this command.  
  
DELETEGroup |  Delete an existing local group  
      
    
    No help available for this command.  
  
DELETEUser |  Delete an existing local user  
      
    
    No help available for this command.  
  
DELLICense |  Delete application(s) license.  
      
    
    DELLICENSE {[VENDORID] [MODULEID]} | [ALL] - delete license key
            VENDORID - vendor id, valid range (1...65535)
            MODULEID - module id, valid range (0...65535)
            ALL - delete all license keys
    
      
  
DELete |  Remove file(s)  
      
    
    DELETE filesearchstring
            filesearchstring - search string which may contain wildcards
    
      
  
DHCP |  Enable/disable dynamic IP addressing.  
      
    
    DHCP [device_num [ON | OFF | REL_RENEW]]
            ON - enables DHCP for device_num
            OFF - disables DHCP for device_num
            REL_RENEW - performs a DHCP release and renew for device_num
            No parameter - displays current setting for all devices
    
      
  
DHCPLeases |  Display Control Subnet's DHCP Leases.  
      
    
    DHCPLeases
             No parameter - Displays Current Control Subnet DHCP leases in tabular format
    
      
  
DHCPOPT |  Sets DHCP Server Options  
      
    
    DHCPOPT [HOSTNAME | FQDN]
            HOSTNAME - Send Local HostName in DHCP Discover Request - Default Option
            FQDN - Send the Fully Qualified Domain Name in DHCP Discover Request
            No parameter - displays current setting
    
      
  
DIR |  List files and directories in current directory  
      
    
    DIR filesearchstring
        filesearchstring - search string which may contain wildcards
    
      
  
DOMAINNAMEEx |  Set the domain name for multiple adapters  
      
    
    DOMAINNAMEEX [device_num domain | /CLEAR ]
            device_num - Specified ethernet device[0..3]
            domain - ASCII string containing domain name
            /CLEAR - clears the value
            No parameter - displays current value
    
      
  
DOMAinname |  Set the domain name for DNS environment  
      
    
    DOMAINNAME [string | /CLEAR ]
            string - ASCII string containing domain name
            /CLEAR - clears the value
            No parameter - current value
    
      
  
DUMPCOMCAPS |  Dumps comp port HW capabilities  
      
    
    DUMPCOMCAPS [COMPORTNUMBER]
    Dumps HW capabilities for the specified COMPORT.
    
      
  
DUMPDMIPCOnfig |  Dump DM Device IP Config  
      
    
    TableStart: DM IP Config
    Slot#         |Device_Name             |FW_Version      |Ext_IP_Address |TCP_Port|Int_IP_Address |LINK |MAG
    -----------------------------------------------------------------------------------------------------------
    8             |C2I-DMPS3-4K-200-300-AUDIO|1.3209.00033    |0.0.0.0        |50003   |169.254.0.3    |UP   |N
    9             |C2I-DMPS3-4K-350-VIDEO  |1.3458.0032     |0.0.0.0        |50004   |169.254.0.4    |UP   |N
    9.1           |DMPS3-4K-300-HDMI-RX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.2           |DMPS3-4K-300-HDMI-RX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.3           |DMPS3-4K-300-HDMI-RX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.4           |DMPS3-4K-300-HDMI-RX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.5           |DMPS3-4K-300-HDMI-RX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.6           |DMPS3-4K-300-HDMI-RX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.7           |DMPS3-4K-300-DM-RX      |1.3458.00032    |               |00000   |               |DOWN |N
    9.8           |DMPS3-4K-300-DM-RX      |1.3458.00032    |               |00000   |               |DOWN |N
    9.9           |DMPS3-4K-STR            |1.3459.00079    |0.0.0.0        |50009   |169.254.0.9    |UP   |N
    9.11          |DMPS3-4K-300-HDMI-TX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.12          |DMPS3-4K-300-HDMI-TX    |1.3458.00032    |               |00000   |               |DOWN |N
    9.13          |DMPS3-4K-300-DM-TX      |1.3458.00032    |               |00000   |               |DOWN |N
    9.13.1        |DM-RMC-4K-SCALER-C      |1.2911.00057    |0.0.0.0        |50007   |169.254.0.7    |UP   |N
    9.14          |DMPS3-4K-300-DM-TX      |1.3458.00032    |               |00000   |               |DOWN |N
    9.14.1        |DM-RMC-4K-SCALER-C      |1.2911.00057    |0.0.0.0        |50008   |169.254.0.8    |UP   |N
    
      
  
ECHO |  Enable/disable character echoing  
      
    
    ECHO [ON | OFF]
            No parameter - displays current setting
    
      
  
EDEBUG |  Set/View run-time ethernet debug options  
      
    
    Valid options are:
    GATEWAY [ON/OFF] - turns Gateway Server extended debugs on and off
    ZPANEL [ON/OFF] - turns ZPanel Server extended debugs on and off
    ESLAVE [ON/OFF] - turns eslave client debug on and off
    [ON/OFF] - turns all debug on and off
    To use debug:
             - enable all debug outputs: EDEBUG ON
             - Specify what Logic App to debug: AENTRY [Application ID]
             - Specify what Logic App and IPTable Entry to debug: SENTRY [Application ID] [CIP ID]
             - Specify what Logic App to remove from debug: RAENTRY [Application ID]
             - Specify what Logic App and IPTable Entry remove from debug: RSENTRY [Application ID] [CIP ID]
             - To kill debugs: EDEBUG OFF
    
      
  
ENABLEFEature |  Enable/disable optional features  
      
    
    ENABLEFEATURE  [ON, OFF]
            FEATURE - Feature to be enabled/disabled or ALL
            ON - start feature when system boots
            OFF - do not start feature when system boots
            feature by itself shows current state for next boot
    
      
  
ERASE |  Remove file(s)  
      
    
    ERASE filesearchstring
            filesearchstring - search string which may contain wildcards
    
      
  
ERRlog |  Prints the current error log.  
      
    
     ERRLOG {OK | NOTICE | WARNING | ERROR | FATAL}
         OK - print all OKs and above
         NOTICE - print all notices and above  (default)
         WARNING - print all warnings and above
         ERROR - print all errors and above
         FATAL - print all fatal errors and above
         No parameter:  Same as "ERRLOG NOTICE"
         PLOGALL - print persistent log for both previous and current session
         PLOGCURRENT - print persistent log for current session
         PLOGPREVIOUS - print persistent log for previous session
    
      
  
ETHWdog |  Enable/disable Ethernet Watchdog.  
      
    
    ETHWDOG [ON | OFF]
            ON - turn on Ethernet watchdog
            OFF - turn off Ethernet watchdog
            No parameter - display current watchdog status
    
      
  
EWDGCONFIG |  Configure Ethernet Watchdog.  
      
    
    EWDGCONFIG [-SA:SampleInterval] [-SD:ShutdownInterval] [-RC:RxPacketTripCount] [-MS:MaxShutdownIntervalCount]
            -SA: - watchdog sample interval in millisecond
            -SD: - RX shutdown interval in millisecond
            -RC: - minimum RX packet received per watchdog sample interval before trip
            -MS: - maximum number of shutdown intervals allowed per shutdown
            No parameter - display current watchdog settings
    
      
  
FGETfile |  Uses built-in (S)FTP/HTTP(S) client to transfer file from the server to ROM  
      
    
    FGETfile [url] [local_path] {username:password} {proxy}
            url - fully qualified URL to the file being downloaded from the server
            local_path - destination path to the file in the ROM
            username:password - optional access credentials to the server
            proxy - optional proxy in the form of url
    
      
  
FORCEDREBOOT |  Forces system reboot  
      
    
    FORCEDREBOOT - reboot system
    
      
  
FPUTfile |  Uses built-in (S)FTP/HTTP(S) client to transfer file from ROM to the server  
      
    
    FPUTfile [url] [local_path] {username:password} {proxy}
            url - fully qualified URL to the file being uploaded to the server
            local_path - path to the source file in the ROM
            username:password - optional access credentials to the server
            proxy - optional proxy in the form of url
    
      
  
FREE |  Show available file space  
      
    
    FREE - Indicates free disk space
    
      
  
FTPSERVer |  Enable/disable the FTP Server  
      
    
    FTPserver [OFF | ON ]
            No parameter - displays current state
    
      
  
GETANALOGJOIN |  Get a analog join value  
      
    
    Get an analog join value.
    GETANALOGJOIN [join#]]
            [join#] - positive integer
    
      
  
GETAUDITLOG |  Retrieve the audit log.  
      
    
    No help available for this command.  
  
GETCODE |  Retrieve code needed for eControl2 activation  
      
    
    GETCODE
             Retrieves code needed for eControl2 activation.
    
      
  
GETDIGITALJOIN |  Get a digital join value  
      
    
    Get a digital join value.
    GETDIGITALJOIN [join#]
            [join#] - positive integer
    
      
  
GETIPTABLE |  Transfer the IP table from Internal flash  
      
    
    GETIPTABLE [program]
            program - which program the table is for (default = 1)
    
      
  
GETPAsswordrule |  Get password rules for local users  
      
    
    GETPASSWORDRULE
            No parameters needed.
    
      
  
GETSERIALJOIN |  Get a serial join value  
      
    
    Get a serial join value.
    GETSERIALJOIN [join#] [join value]
            [join#] - positive integer
    
      
  
HEARTBEATtimeout |  Set TCP Socket Send Timeout value in Milliseconds  
      
    
    HEARTBEATTIMEOUT [timeoutInMilliSeconds]
            timeoutInMilliSeconds - Timeout before sending a CIP heartbeat to the peer if no messages are received from the peer. Default value is 30
    seconds.
            No parameter - displays current setting
    
      
  
HELP |  Display help screens  
      
    
    HELP - Detailed help available.  Type a command followed by
           a space and '?' to see options for that command
           (i.e. HELP ?)
    HELP ALL will display a list of all commands.
    HELP DEVice will display a list of commands specific to this device.
    HELP ETHERnet will display a list of Ethernet commands.
    HELP FILE will display a list of commands for file operations.
    HELP SYStem will display a list of general system commands.
    HELP RF will display a list of commands for the radio chip if available.
    HELP OSD will display a list of commands for the on-screen-display if available.
    HELP RAVA will display a list of commands for RAVA VOIP if available.
    HELP BACNET will display a list of commands for the BACNET stack if available.
    HELP USER will display a list of commands added to the system by user programs.
    HELP CRESTIMERENG will display a list of commands for the Crestron Timer Engine.
    HELP xxx* will display a list of commands starting with xxx.
    
      
  
HOSTname |  Set the host name for DNS environment  
      
    
    HOSTNAME [string | /CLEAR ]
            string - ASCII string containing host name (max 15 chars)
            /CLEAR - clears the value
            No parameter - current value
    
      
  
ICMP |  Enable/disable ICMP ping  
      
    
    ICMP [ON | OFF]
            No parameter - displays current setting
    
      
  
ICMPREDIRECT |  Enable/disable ICMP Redirect  
      
    
    ICMPREDIRECT [Enable | Disable]
            Enable Disable ICMP Redirect.
            No parameter - displays current setting
    
      
  
INFO |  Print Software Capabilities  
      
    
    INFO
            No parameters
    
      
  
INITIALIZE |  Clear file system  
      
    
    INITIALIZE
            No parameter
    
      
  
INTERNALCNETDebug |  Set/View run-time Internal Cresnet debug options.  
      
    
    INTERNALCNETDEBUG
    View incoming and outgoing packets on the Internal cresnet
    [ON/OFF] Turns on and off debug trace.
             No Parameters - Displays current debug settings
    
      
  
IPAddress |  Set IP address.  
      
    
    IPADDRESS [device_num ip_address]
            device_num - specified Ethernet device  [0 - 3]
            ip_address - IP address in dot decimal notation
            No parameter - displays current value
    
      
  
IPCONFIG |  Display/Configure IP Settings  
      
    
    usage : ipconfig [/all | /renew [adapter index] | /release [adapter index] ] /flushdns
        ?    Display this help message.
        /all  Display full configuration information.
        /release   Release the IP address for the specified adapter
        /renew     Renew the IP address for the specified adapter
        /flushdns  Clear the name resolution client cache
     The default is to display only the IP address, subnet mask and default gateway for each adapter bound to TCP/IP.
    
      
  
IPLINKDebug |  Set/View run-time OSD IPLink Server debug options.  
      
    
    IPLINKDEBUG
    View incoming and outgoing packets on the OSD IPLink Server.
    [ON/OFF] Turns on and off debug packets.
    [ENABLEREMOTEDEBUG/DISABLEREMOTEDEBUG] Enables or disables flash remote debugging
    [DISABLEIPLINKTIMEOUT/ENABLEIPLINKTIMEOUT] Enables or disables the iplink inactivity timeout
    [SENDDIGITALJOIN] [Join Number] [JoinValue] Sends a digital join over IPLink
             No Parameters - Displays current debug settings
    
      
  
IPLINKStatus |  View run-time OSD IPLink Server connection status.  
      
    
    IPLINKSTATUS
    Displays the OSD  IPLink connection status.
             No Parameters
    
      
  
IPMask |  Set IP Subnet Mask.  
      
    
    IPMASK [device_num ip_address]
            device_num - specified Ethernet device  [0 - 3]
            ip_address - IP address in dot decimal notation
            No parameter - displays current value
    
      
  
IPTable |  Display IP Table  
      
    
    IPTABLE  [-P:program] [-T] [-I:id] [-C] [-O]
            -I:id:  ID to display entry for
            -P:program: ALL or # of programs's IP table to show
            -T Display data in a tabular format
            -C Clears the IP Table for the specified program. Requires -P option
            -O Displays only offline devices
            No Arguments shows IP Table for program 1
    
      
  
ISDIR |  Is the parameter a directory  
      
    
    ISDIR directory
            directory - string containing directory specification
    
      
  
ISOLATENETworks |  Isolate The LAN and Control Subnet Networks.  
      
    
    ISOLATENETWORKS [state]
             state          - {ON|OFF}
             No parameter   - displays current value
    
      
  
ISTAT |  (*) Check Internal Status of Program  
      
    
    ISTAT[:program#] {Parameters}
            program#: number of program to execute. (default=1)
            ISTAT SIG                   - Show internal status on signals.
            ISTAT PROG [-Q]             - Show internal status on program, -Q=Do Not List Symbols
            ISTAT SYM {number}          - Show internal status of specified symbol
            ISTAT DEV                   - Show devices in system only.
            ISTAT REGDEV                - Show successfully registered devices in system only.
            ISTAT LIST {number}         - List all occurances of compiler code {number} in the program.
            ISTAT SHOWDEBUG {number}    - Show Debug Info for symbol {number} in the program.
            ISTAT SYMQUE                - Show number of entries in symbol input queue for devices that have them.
            ISTAT PSTRINGS              - Show size of each perm. string & total space for all fixed strings.
            ISTAT TREE {number}         - Show children and helpers of this symbol.
            ISTAT ABILITY {number}      - Show abilities of this symbol.
            ISTAT MAINLOOP              - Show main loop counter.
            ISTAT OVERHEAD              - Show some symbol data overhead.
            ISTAT SCHED                 - Scheduler Dump.
            ISTAT FINDSIG {number}      - Find Signal Index in Scheduler.
            ISTAT FINDSYM {number}      - Find Symbol Index in Scheduler.
            ISTAT ERSLEEPY              - Show Unconfigured ErSleepy devices in program.
            ISTAT WAVELIST              - Show last 0 symbols processed
                    (Use LOGICDEBUG WAVESTORE       command to change size)
    
      
  
JOINGETINANalog |  Read Analog Input Joins to Console  
      
    
    Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETINDIgital |  Read Digital Input Joins to Console  
      
    
    Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETINSErial |  Read Serial Input Joins to Console  
      
    
    Xact# slot#[.subslot#...] join#
    
      
  
JOINGETINTparam |  Read Integer Params to Console  
      
    
    [type]
    Xact# slot#[.subslot#...] join#1...[join#N]
    
    
      
  
JOINGETOUTANalog |  Read Analog Output Joins to Console  
      
    
    Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETOUTDIgital |  Read Digital Output Joins to Console  
      
    
    Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETOUTSErial |  Read Serial Output Joins to Console  
      
    
    Xact# slot#[.subslot#...] join#
    
      
  
JOINGETSERparam |  Read Serial Params to Console  
      
    
    Xact# slot#[.subslot#...] join#1...[join#N]
    
    
      
  
JOINMONITORSlot |  Start/Stop TJI monitor  
      
    
    JoinMonitorSlot - Valid Options are
    JoinMonitorSlot ? - Display this help
    JoinMonitorSlot - Display current list of slots being monitored
    JoinMonitorSlot [transactionId] #slot[.subslot]...
    JoinMonitorSlot STOP ALL - Remove all slots
    JoinMonitorSlot STOP [transactionId]  - Remove Specified slot
    
    
      
  
JOINSETANALOG16 |  Set Analog Joins from Console for 16 bit Ethernet Id Devices  
      
    
     JOINSETANALOG16 -  Direct Signal Write.
     [type] slot#[.subslot#...] join#1=val#1 ...[join#N=val#N]
      Type could be
     TYPE01 - Sends Analog Packet
      TYPE14 - Sends New Analog Packet
      Only for 16 bit ethernet IP Id's
    
      
  
JOINSETANalog |  Set Analog Joins from Console  
      
    
     JOINSETANALOG -  Direct Signal Write.
     [type] slot#[.subslot#...] join#1=val#1 ...[join#N=val#N]
      Type could be
     TYPE01 - Sends Analog Packet
      TYPE14 - Sends New Analog Packet
    
    
      
  
JOINSETDIGITAL16 |  Set Digital Joins from Console for 16 bit Ethernet Id Devices  
      
    
     JOINSETDIGITAL16 -  Direct Signal Write.
     slot#[.subslot#...] join#1=val#1 ...[join#N=val#N]
     Only for 16 bit ethernet IP Id's
    
      
  
JOINSETDIgital |  Set Digital Joins from Console  
      
    
     JOINSETDIGITAL -  Direct Signal Write.
     slot#[.subslot#...] join#1=val#1 ...[join#N=val#N]
    
      
  
JOINSETINTparam |  Send Integer Parameter from Console  
      
    
     JOINSETINTPARAM -  Direct Signal Write.
     [type] slot#[.subslot#...] param#1=val#1 ...[param#N=val#N]
     Type could be
     TYPE09 - Sends 16 bit Parameters
     Default are 32 bit parameters
    
      
  
JOINSETPAcket |  Send Any Packet from Console  
      
    
     JOINSETPACKET -  Direct Signal Write.
     slot#[.subslot#...]["[ASCII_string]"] | [hex_byte_1...hex_byte_N]
    
      
  
JOINSETSERIAL16 |  Send Any Packet from Console for 16 bit Ethernet Id Devices  
      
    
     JOINSET16XXX Command failed
    
      
  
JOINSETSERParam |  Send Serial Parameter from Console  
      
    
     JOINSETSERPARAM -  Direct Signal Write.
     slot#[.subslot#...] param# ["[ASCII_string]]  | [hex_byte_1...hex_byte_N]
    
    
      
  
JOINSETSErial |  Send Any Packet from Console  
      
    
     JOINSETSERIAL -  Direct Signal Write.
     [type] slot#[.subslot#...] ["[ASCII_string]"] | [hex_byte_1...hex_byte_N]
     Type could be
     TYPE12/ type12 - Sends Multi Serial Packet
     TYPE15/ type15 - Sends Extended Serial Packet
    
      
  
KILLSOCKET |  Close an active TCP console socket  
      
    
    KILLSOCKET [CTPx | TELNETx | SCTPx | SHELLx]
            CTPx - kill CTP console #x
            TELNETx - kill Telnet console #x
            SCTPx - kill SCTP console #x
            SHELLx - kill SHELL (SSH) console #x
    
      
  
LIGHTBYPPN |  start squack mode  
      
    
    Valid options are:
       Status if no arguments
    Syntax: LIGHTBYPPN [4 byte Hex Adr]|ALL
    
      
  
LISTACTIVEMODULES |  (*) Get a list of active S+ Modules.  
      
    
    LISTACTIVEMODULES[:program#]
            View running S+ modules.
            No arguments necessary.
    
      
  
LISTBLOCKEDip |  List the blocked IP addresses  
      
    
    No help available for this command.  
  
LISTDNS |  Display the list of DNS servers  
      
    
            shows current DNS servers - no parameters needed
    
      
  
LISTDOMAINGroups |  List domain groups that were added to this control system  
      
    
    No help available for this command.  
  
LISTENSTAT |  Generate a report of the Ethernet listen sockets  
      
    
    LISTENSTAT
             No Parameter neccessary
    
      
  
LISTGROUPS |  List existing local groups  
      
    
    No help available for this command.  
  
LISTGROUPUsers |  List all existing (local and domain) users in an existing local group  
      
    
    No help available for this command.  
  
LISTUSERS |  List of users authenticated on this system  
      
    
    No help available for this command.  
  
LOCATION |  Location latitude, longitude and city country.  
      
    
    Location for astronomical events
    LOCATION -LAT:Latitude -LON:Longitude -LOC:CityCountry
             -LAT: Latitude north <##.###> or latitude south <-##.###>
             -LON: Longitude east <##.###> or longitude west <-##.###>
             -LOC: City country
    
      
  
LOGGER |  (*) Turn the logger on, off, or change the operation mode  
      
    
    LOGGER[:program#] {ON|OFF|STANDBY} {DEBUGLEVEL} {ONLY} {LOGGERMODE}
            Turn the Logger on or off
            program#: number of program to execute. (default=1)
            ON - Initialize the Logger; must specify DEBUGLEVEL.
            OFF - Disable the Logger
            STANDBY - Silence the Logger temporarily. No messages will be printed/logged.
            {DEBUGLEVEL}- Desired Debug Level if turning Logger on. (excepted range 1-10)
            {ONLY}- Optional parameter if only one Debug Level is to be handled.
            {LOGGERMODE} = {RM, CONSOLE, DEFAULT, RM/CONSOLE}- Optional parameter to specify the mode of the Logger.
    
      
  
LOGGERBuffersize |  (*) Set or show the Logger Buffer Size  
      
    
    LOGGERBUFFERSIZE[:program#] {BUFFERSIZE}
            View or change the Logger Buffer Size
            program#: number of program to execute. (default=1)
            BUFFERSIZE - Desired Logger Buffer Size in Kilobytes(KB).
            Maximum Buffer Size Allowed: 500KB
    
      
  
LOGGERClear |  (*) Clear the Logs for the Specified Program  
      
    
    LOGGERCLEAR[:program#] {ALL}
            Clear the log for the specified program.
            program#: number of program to execute. (default=1)
            {ALL} - Optional parameter to clear all the logs, including all backup logs.
    
      
  
LOGGERDebuglevel |  (*) Set or show Logger debug level  
      
    
    LOGGERDEBUGLEVEL[:program#] [DEBUGLEVEL] {ONLY}
            View or change the Logger Debug Level
            program#: number of program to execute. (default=1)
            [DEBUGLEVEL] - Desired Logger Debug Level(1-10)
            {ONLY} - Include after DEBUGLEVEL to Log only this level.
    
      
  
LOGGERFlush |  (*) Flush the current buffer to RM  
      
    
    LOGGERFLUSH[:program#]
            Flush the current buffer to RM
            program#: number of program to execute. (default=1)
            {No Parameters}
    
      
  
LOGGERMode |  (*) Set or show the Number of Backup Logs desired  
      
    
    LOGGERMODE[:program#] {DEFAULT | RM | CONSOLE | RM/CONSOLE}
            View or change the Logger Mode
            program#: number of program to execute. (default=1)
            BUFFERSIZE - Desired Logger Buffer Size in Kilobytes(KB).
            Maximum Buffer Size Allowed: 500KB
    
      
  
LOGGERNumbackuplogs |  (*) Set or show the Number of Backup Logs desired  
      
    
    LOGGERNUMBACKUPLOGS[:program#] {NUMBACKUPLOGS}
            View or change the desired number of backup logs for the Logger
            program#: number of program to execute. (default=1)
            NUMBACKUPLOGS - Desired number of Backup logs to keep
            Maximum number of backup files (*.bac) allowed: 10
    
      
  
LOGGERPrint |  (*) Print the current log to the console  
      
    
    LOGGERPRINT[:program#] {ALL}
            Print recent messages in the Log to the console.
            program#: number of program to execute. (default=1)
            ALL - Optional parameter to print the entire log.
    
      
  
LOGICDebug |  (*) Set Logic Debug Options  
      
    
    LOGICDEBUG {Parameters}
                                                Current State
            LOGICDEBUG LOGIC ON|OFF                (     OFF) - Logic info
            LOGICDEBUG SKEDDER ON|OFF              (     OFF) - Event Scheduler info
            LOGICDEBUG ANSKEDDER ON|OFF            (     OFF) - Analog Event Scheduler info
            LOGICDEBUG VALIDATESKED ON|OFF         (N/A) - Validate Scheduler Nodes (Requires Custom Firmware)
            LOGICDEBUG SYMPROC ON|OFF              (     OFF) - Show Symbols as Processed
            LOGICDEBUG TXTIME ON|OFF               (     OFF) - Show time before/after packet transmission to driver
            LOGICDEBUG SYMSIGPROC ON|OFF           (     OFF) - Show signals changed for symbols being processed
            LOGICDEBUG UPREQ ON|OFF                (     OFF) - Debug update request
            LOGICDEBUG SHOWREG ON|OFF              (     OFF) - Show extended registration info
            LOGICDEBUG SHOWBOOT ON|OFF             (     OFF) - Show extended logic startup/shutdown info
            LOGICDEBUG PAGEUPDATE ON|OFF           (     OFF) - Show info about Page update requests
            LOGICDEBUG BUILDIFOFFLINE ON|OFF       (     OFF) - Ignore m_uiOnlineState when building packet
            LOGICDEBUG CLOUDINFO ON|OFF            (     OFF) - Info going to the Cloud
            LOGICDEBUG MEMTRACK ON|OFF             (     OFF) - Memory Size Tracking
            LOGICDEBUG SIGMEMTRK ON|OFF            (     OFF) - Memory Size Tracking
            LOGICDEBUG SYMBOLQUEADDTIMEOUT {time}  (   32000) - Timeout for adding to a Symbol's Queue from TLDM Rx (also single/multi queue timeout).
            LOGICDEBUG SENDTOTLDMTIMEOUT {time}    (   10000) - Timeout for SendMessageToTLDMEx() in ms
            LOGICDEBUG APPTOTLDMTIMEOUT {time}     (   32000) - App To TLDM Timeout in App registration message in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG TLDMTOAPPTIMEOUT {time}     (   32000) - TLDM To App Timeout in App registration message in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG APPTOCLOUDTIMEOUT {time}    (   10000) - App To Cloud Timeout in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG CLOUDTOAPPTIMEOUT {time}    (   10000) - Cloud To App Timeout in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG MAXWAVESINSOLUTION {size}   (    1500) - Number of Waves per Logic Solution
            LOGICDEBUG MAXTRANSPERWAVE {size}      (   20000) - Number of Signal transitions per wave
            LOGICDEBUG SYMQUEUEDEPTH {size}        (     250) - Depth of the Symbol Input Queue
            LOGICDEBUG SPLUSQUEUEDEPTH {size}      (     250) - Depth of SIMPL+ Symbol Input Queue
            LOGICDEBUG SPLUSTOLOGICQDEPTH {size}   (     100) - Depth of SIMPL+ to Logic Queue
            LOGICDEBUG LOGICTOSPLUSQDEPTH {size}   (      50) - Depth of Logic to SIMPL+ Queue
            LOGICDEBUG TRANSIENTHEAP {size}        (  102400) - Transient Heap Size in bytes
            LOGICDEBUG REGTIMEOUT {time}           (   20000) - Timeout for Registration Event in ms
            LOGICDEBUG ACTLOGEVENTCOUNT {number}   (       5) - Number of events to pay attention to in the Logic Activity Logger
            LOGICDEBUG ACTLOGSIZE {number}         (       0) - Size of the Logic Activity Logger
            LOGICDEBUG ACTLOGPRIORITY {priority}   (      50) - Priority of the Logic Activity Logger
            LOGICDEBUG ACTLOGSCREEN ON|OFF         (     OFF) - Dump Logic Activity Logger to Screen on fault
            LOGICDEBUG ACTLOGNOFILE ON|OFF         (     OFF) - Avoid dumping Logic Activity Logger to file on fault
            LOGICDEBUG SCHEDNODES {size}           (     200) - Number of Loopnodes in the Scheduler
            LOGICDEBUG REPORTNODES {size}          (      10) - Report if more than this number loopnodes exceeded
                                                                before servicing scheduler
            LOGICDEBUG RCBCHECK {size}             (       4) - Set the number of passes before servicing analogs in the scheduler
            LOGICDEBUG TIMEREPORT {size}           (      10) - Set the number of ms required to pass before posting the time
                                                                to execute RunLoopNodeCheck()
            LOGICDEBUG SHOWRMLTIME ON|OFF          (     OFF) - Show time between Run Main Loop
            LOGICDEBUG RMLTIME {size}              (      10) - Min Time needed to print the Run Main Loop time
            LOGICDEBUG SHOWSSQTIME ON|OFF          (     OFF) - Show time for Single Step Queue Solution
            LOGICDEBUG SSQTIME {size}              (      10) - Min Time needed to print the Single Step Queue Solution time
            LOGICDEBUG SHOWMSQTIME ON|OFF          (     OFF) - Show time for Multi Step Queue Solution
            LOGICDEBUG MSQTIME {size}              (      10) - Min Time needed to print the Multi Step Queue Solution time
            LOGICDEBUG SHOWSIQTIME ON|OFF          (     OFF) - Show time for Symbol Input Queue Solution
            LOGICDEBUG SIQTIME {size}              (      10) - Min Time needed to print the Symbol Input Queue Solution time
            LOGICDEBUG CONTIMEOUT {time}           (    2000) - General console write timeout for logic in ms (not for DBGSIGNAL/MDBGSIGNAL).
            LOGICDEBUG BACNETSTOPPINGHBEAT {time}  (    4500) - Dot print timeout while waiting for Bacnet to complete stop, in ms.
                                                                (Keep to 5000 or under to keep toolbox happy)
            LOGICDEBUG BACNETSTOPPEDTIMEOUT {time} (      15) - Overall timeout for Bacnet to complete stop, in min.
            LOGICDEBUG ALL ON|OFF                             - Turn on/off all of the above.
            LOGICDEBUG LGC ON|OFF                             - Turn on/off LOGIC, SYMPROC, SYMSIGPROC.
    
      
  
LOGMESSage |  (*) Write a message to the log from the console  
      
    
    LOGMESSAGE[:program#] {DEBUGLEVEL} {MESSAGE}
            Write a message to the log from the console
            program#: number of program to execute. (default=1)
            DEBUGLEVEL (expected range 1-10).
            MESSAGE - String to write to log.
    
      
  
LOGOFF |  Logs the currently authenticated user out of the system  
      
    
    Logs the currently authenticated user out of the system  
  
MAKEDIR |  Creates a directory  
      
    
    Creates a directory  
  
MDBGSIGnal |  Sets or clears Debug flag for signal processing  
      
    
    Sets or clears Debug flag for signal processing  
  
MDGBSIGnal |  (*) Set/view Debug flags and signal values  
      
    
    MDBGSIGNAL[:program#] {Parameters}
            program#: number of program to execute. (default=1)
            MDBGSIGNAL -R                   - Turn off all debug flags (Global, Signal specific, and Ignore)
            MDBGSIGNAL -A:ON                - Turn on Global debug flag
            MDBGSIGNAL -A:OFF               - Turn off Global debug flag
            MDBGSIGNAL -A:SHOW              - Show global & signal debug status
            MDBGSIGNAL -A:SYNC              - Write values of non-zero digital & analog signals, non-transient serial strings
            MDBGSIGNAL -S:ON {signum(s)}    - Turn on signal-specific debug flag for signal {signum}
            MDBGSIGNAL -S:OFF {signum(s)}   - Turn off signal-specific debug flag for signal {signum}
            MDBGSIGNAL -S:SHOW {signum(s)}  - Show status of signal-specific debug flag & ignore flag for signal {signum}
            MDBGSIGNAL -S:SYNC {signum(s)}  - Show value of signal {signum}
            MDBGSIGNAL -I:ON {signum(s)}    - Turn on ignore-global debug flag for signal {signum}
            MDBGSIGNAL -I:OFF {signum(s)}   - Turn off ignore-global debug flag for signal {signum}
              {signum(s)} is a single Hex number (i.e. 0x0014) or a decimal number (i.e. 20) or
              a list of space separated numbers.  To specify a range, put two signum(s) separated by a colon
              i.e. 0x14:0x20 would perform the operation for signals 0x14 through 0x20 inclusive.
              Multiple single numbers and multiple ranges are allowed.
    
      
  
MESSage |  Display a message on the screen.  
      
    
    MESSAGE [string]
    Display a message on the screen.
            MESSAGE [string]
            string - ASCII string to display on screen. Maximum length is 240 characters.
            No parameters - restore previous display
    
      
  
MIPTable |  Display Master IP Table  
      
    
    MIPTABLE [-T]
            -T Display data in a tabular format
            No Arguments. Shows IP Table for Master Entry
    
      
  
MOVEfile |  Move a file to a different directory  
      
    
    MOVEFILE sourcespec destspec
            sourcespec - source file name specification (could be relative to current dir)
            destspec - destination file name specification (could be relative to current dir)
            filenames with embedded spaces must be enclosed in double quotes("The File")
    
      
  
MYCRESTRON |  Setup MyCrestron Domain & Password, and attempt to register system  
      
    
    Format: MyCrestron DOMAIN PASSWORD
            DOMAIN - sets MyCrestron domain
            PASSWORD - sets MyCrestron password
            No parameter - displays current setting
    
      
  
NATENAble |  Enable/disable Network Address Translator (NAT)  
      
    
    NATENABLE [ON | OFF]
            No parameter - displays current setting
    
      
  
NETSTAT |  Displays protocol statistics and current TCP/IP network connections  
      
    
    usage : netstat
        ?    Display this help message.
     The default is to displays all connections and listening ports.
    
      
  
NUMNOHBRESPonsecnt |  Set maximum number of no response allowed for CIP Heartbeat Messaging  
      
    
    NUMNOHBRESPONSECNT [count]
            count - Number of times we do not receive a response to the CIP heartbeat before we close the socket. Default value is 3.
            No parameter - displays current setting
    
      
  
NVRAMCLEAR |  Clear NVRAM with zeros  
      
    
    NVRAMCLEAR [-P:ALL | -P:Specific Program Identifier] [-D]
            -P: Clear NVRAM for a specific program or ALL programs. If not present, ALL assumed.
            -D: Deallocate NVRAM memory.
    
      
  
NVRAMGET |  Retrieve contents of NVRAM from the system  
      
    
    NVRAMGET [-P:ALL | -P:Specific Program Identifier]
            -P: Get NVRAM for a specific program or ALL programs. If not present, ALL assumed.
    
      
  
NVRAMPUT |  Send contents of NVRAM to the system  
      
    
    NVRAMPUT [-P:ALL | -P:Specific Program Identifier]
            -P: Put NVRAM for a specific program or ALL programs. If not present, ALL assumed.
    
      
  
NVRAMREBOOT |  Print reboot information  
      
    
    NVRAMREBOOT [SHOW]
            SHOW - display the last reboot message in NVRAM
    
      
  
OCSP |  Display/Set OCSP configuration for SSL communication.  
      
    
    OCSP -L:OFF|STAPLEONLY|ONLINE {-N:NumOfNonces} {-T:TimeoutInSeconds}
            where 'OFF' is no OCSP verification,
            where 'STAPLEONLY' check certificate staple (no staple is a failure),
            where 'ONLINE' checks staple, if no staple then check validity with responder,
            where '-N:#' sets the number of nonces (currently 0 is none, any non-zero means use a nonce.)
            where '-T:#' sets the timeout in seconds to connect to responder (for ONLINE only)
            No parameter - displays current settings
    
      
  
OOTBF |  Console command to enable OOTBF debug data  
      
    
     debug
     grid
     ver
     errtest
    OOTBF Debug is off
    
      
  
OSD |  start On Screen Display when boot  
      
    
    OSD [ON, OFF]
            ON - start on screen display when system boots
            OFF - do not start on screen display when system boots
            no arguments shows current state
    
      
  
PACKET |  (*) Generates packets  
      
    
    PACKET - Creates/Sends packets
            Syntax:  PACKET [-N] [-S:E | -S:C] [-F:form] [-P] [-I:{ID}] -[T:{Type}] {Packet Specific Data}
            Options:
            -N:  Do not clear character buffer before building
            -B:  Build a packet using {packet options}
            -S:{Network to send to}
                    E:  Send completed packet via main Ethernet
                    C:  Send completed packet via main cresnet
            -R:"...": Build a raw packet from the contents of the string "..."
                      "\x" style sequences are legal.  COUNT byte is auto-computed (NTX style)
            -F:form:  Use Form "form" to build the packet.
            -P:  Print current buffer
            -I:  Device ID (or list for wrapping)
                 ex:  -I:0xAA, -I:15, -I:0xAA.0xBB.0xCC (AA, BB are wrapped, CC is the inner packet)
            -T:  Packet Type
                 0x00 ("DIGITAL")    - Digital
                 0x01 ("ANALOG")     - Analog
                 0x14 ("SYMANALOG")  - Symmetric Analog
                 0x1C ("GENCFG")     - Generic Device Config
                 0x1D ("CLXRCB")     - CLX RCB
                 ex:  -T:0x01 or -T:"ANALOG" to specify Analog type.
            To get {Packet Specific Data}, do "PACKET -T:{Type} ?"
    
      
  
PASSTHRU |  Enter passthru mode console<->device  
      
    
    Valid options are:
       any number allowed as argument
     CRESnet - cresnet device
     ETHERnet - CIP or Client/Serv
     SLOT - any sys slot
     COM - build-in com
     IR - one-way IR
     H/W - hardware handshake
     S/W - software handshake
     232 - RS232 mode
    
      
  
PASSTO |  Enter passto mode console<->device  
      
    
    Valid options are:
     CRESnet -  Passto Over Cresnet
     IPID -  Passto Over IP
     SLOT - plug-in card
     CONSole - console mode
        hex number allowed as argument
       Status if no arguments
    
    
      
  
PAUSEPROGram |  Pauses Specified Program  
      
    
     PAUSEPROGRAM {-P:ALL | -P:Specific Program Identifier}
             -P:  Pause a specific program or ALL.  If not present, ALL assumed.
    
    
      
  
PERSISTENTLOG |  Start PersistentLog on system boot  
      
    
    PersistentLog [ON, OFF]
            ON - Start PersistentLog on system bootup
            OFF - Do not start PersistentLog on system bootup
            No arguments - Shows current state
    
      
  
PING |  Ping Remote Node  
      
    
    Usage: ping [-n count] [-i TTL] [-v TOS] [-w timeout] address
    Options:
        -n count      Send count.
        -i TTL        Time to live.
        -v TOS        Type of service
        -w timeout    Timeout (in milliseconds)
        -r count      Record route for count hops.
        -s count      Timestamp route for count hops.
        -S address    Source address to use (IPv6-only).
        -4            Force using IPv4.
        -6            Force using IPv6.
    
    
      
  
PPNDISCOVEr |  Show all PPN devices on cresnet  
      
    
     PPNDISCOVER
    
      
  
PRINTAUDITLOG |  Print the audit log.  
      
    
    No help available for this command.  
  
PROGCOMments |  (*) Shows program "Comment" symbols  
      
    
    PROGCOMMENTS[:program#]
            program#: number of program to execute. (default=1)
            No arguments necessary.
    
      
  
PROGINFO |  (*) Shows Program Statistics  
      
    
    PROGINFO[:program#] {No arguments}
            program#: number of program to execute. (default=1)
            Shows program information.
    
      
  
PROGLOAD |  Loads the specified program  
      
    
    PROGLOAD {-P:ALL | -P:Specific Program Identifier} {-N} {-D} {-X}
             -P:  Load a specific program or ALL.  Must be specified.
             -N   If present, will not update the IP Table
             -D   If present, will not start the program - just register it.
             -X   If present, will not fail for tools/firmware compatability issues.
    
    
      
  
PROGREAdy |  Sends the program ready status  
      
    
     PROGREADY
             No parameter needed - displays current program ready status
    
    
      
  
PROGREGister |  Registers/Unregisters the specified program  
      
    
     PROGREGISTER {-P:ALL | -P:Specific Program Identifier} [-U] [-C:SSPDllName]
             -P:  (Un)Register the specified program or ALL
             -U:  if present, will unregister the program
             -C:  if present, indicates the entry point for a Simpl Sharp PRO program - (This is the name of the Simpl Sharp PRO DLL)
             no arguments lists which programs are registered
    
    
      
  
PROGRESet |  Restarts the specified program  
      
    
     PROGRESET {-P:ALL | -P:Specific Program Identifier} {-V} {-D}
             -P:  Reset a specific program or ALL.  If not present, ALL assumed.
             -V:  Verbose reset.
             -D:  Don't keep DBGSIGNAL information (PROGRESET normally preserves DBGSIGNAL flags).
    
    
      
  
PROGSTATs |  (*) Shows statistics on the current program  
      
    
    PROGSTATS[:program#]
            program#: number of program to execute. (default=1)
            No arguments necessary.
    
      
  
PROGUPTIME |  (*) Display the time the program is running  
      
    
    PROGUPTIME[:program#]
            program#: number of program to execute. (default=1)
            No arguments necessary.
    
      
  
RAMFree |  Show available RAM file space  
      
    
    RAMFREE
            no parameters needed
    
      
  
RCONsole |  Send Command to Remote console  
      
    
    rcon [cresnet] [hexID][.subslot hexSlot..]|[slot decSlot] [command string]
    
      
  
READI2C |  Read i2c data  
      
    
            READI2C [device] [subaddr] [number of bytes in dec] - Read I2C device
              device - device index, range <0..7>
              subaddr - sub-address in hex, e.g. register addr
              device | name
              =========================
              00     | SYSTEM ID
              01     | FPGA-RF PCA9538
              02     | RESETs PCA9539
              03     | BOARD ID
              04     | FAN_LM63
              05     | RTC DS3231
              06     | PMIC
              07     | SMARTREFLEX
    
      
  
REBOOT |  Perform system reboot  
      
    
    REBOOT - reboot system
    
      
  
REMBLOCKEDip |  Remove an IP Address from the blocked list  
      
    
    No help available for this command.  
  
REMDns |  Remove an entry to DNS server List  
      
    
    REMDNS ip_address
            ip_address - IP address in dot decimal notation
    
      
  
REMMaster |  Remove a master entry to IP table  
      
    
    Format: REMMaster cip_id ip_address/name
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
    
      
  
REMOTESYSlog |  Enable/disable remote system logging of errors.  
      
    
    REMOTESYSLOG [-S:] {-E:} {-A} [-I:address] [-P:port]
            -S:ON|OFF       Enable or disable Remote System Error Logging
            -E:OK|INFO|NOTICE|WARNING|ERROR|FATAL
            OK - log to Syslog all OKs and above
            INFO - log to Syslog all info and above
            NOTICE - log to Syslog all notices and above  (default)
            WARNING  - log to Syslog warnings and above
            ERROR - log to Syslog errors and above
            FATAL - log to Syslog fatal errors and above
            -A  Log to Syslog contents of the Audit log provided that Audit Logging is enabled.
            -I:address  Remote Syslog server IP address in dot decimal notation or
                             ASCII string containing the server host name (max 255 chars)
            -P:port  Remote Syslog server port number in decimal
            No parameter - displays current setting
    
      
  
REMOVEDIR |  Remove a Directory  
      
    
    REMOVEDIR directory
            directory - string containing directory specification
    
      
  
REMOVETBCLIENT |  Removes Console Client Configuration  
      
    
    REMOVETBCLIENT
            Removes console client configuration
    
      
  
REMOVEUserfromgroup |  Remove an existing local or domain user from an existing local group  
      
    
    No help available for this command.  
  
REMPOrtmap |  Remove a port map from the port forwarding table.  
      
    
    REMPOrtmap {-d} ext_port int_port ip_address/hostname protocol
            -d   - Option for port forwarding from the LAN side to the CS side or from the CS side to the DMNET side of Router
            ext_port   - port number on the LAN side of Router when {-d} is not selected. Otherwise it is a port number on the CS side of Router
            int_port   - port number on the CS side of Router when {-d} is not selected.  Otherwise it is a port number on the DMNET side of Router
            ip_address - IP address (in dot decimal notation) of the device on the CS side of Router when {-d} is not selected. Otherwise the device is on
    the DMNET side of Router
            hostname   - Hostname of the device on the CS side of Router when {-d} is not selected. Otherwise the device is on the DMNET side of Router
            protocol   - IP protocol for the portmap service (TCP | UDP | Both)
    
      
  
REMPeer |  Remove a peer(slave) entry to IP table  
      
    
    Format: REMPeer cip_id ip_address/name [-D:device_id] [-C:cipport] [-P:program]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            device_id       - ID in device redirection table (in hex) (must be < 256)
            port number     - port number for the connection (in dec) (must be > 256)
            program         - program number which uses device (in dec) (default 1)
    
      
  
REPORTCRESNET |  Show all devices on the main cresnet leg  
      
    
     REPORTCRESNET  [] | [ALL]
     Display all cresnet devices / Single cresnet device
    
      
  
REPORTPPNTABLe |  Displays Cresnet PPN table if available  
      
    
    Displays Cresnet PPN table if available  
  
RESERVEDLeases |  Display/Update Control Subnet's Reserved DHCP Leases.  
      
    
    RESERVEDLeases [ADD | REM | CLEAR_ALL]
             ADD -  MAC_Address IP_Address Description
             REM -  MAC_Address
             CLEAR_ALL - Clears all reserved leases
             No parameter - Displays Current reserved DHCP leases in tabular format
    
      
  
RESETPassword |  Reset an existing local user's password  
      
    
    No help available for this command.  
  
RESTORe |  Restore factory defaults  
      
    
    RESTORE
            No parameter
    
      
  
RESUMEPROGram |  Resumes Specified Program  
      
    
     RESUMEPROGRAM {-P:ALL | -P:Specific Program Identifier}
             -P:  Resume a specific program or ALL.  If not present, ALL assumed.
    
    
      
  
RI2CGen |  Read i2c data  
      
    
     RI2CGEN [bus] [adr] [sub] [sublen] [dec num_bytes_to_read] - show I2C data
            bus - i2c bus, in decimal, range <1..3>.
            adr - i2c address, hex bytes.
            sub - i2c sub address hex bytes, e.g. register addr
            sublen - sub address len 0..4 bytes.
            num_bytes_to_read - number of bytes to read in decimal.
    
      
  
RJSTATUS |  Retrieve RJ requested status  
      
    
    Retrieve RJ requested status
    RJSTATUS type,join number
    
      
  
ROUTERREboot |  Reboot the router  
      
    
     ROUTERREBOOT
             Reboot the router (Caution will lose ethernet connectivity) .
    
    
      
  
ROUTERUPLOAD |  Upload firmware to the router  
      
    
     ROUTERUPLOAD [PATCH PatchFileName] [BOOTLOADER] [COMBINED]
             No parameters - Upload the firmware on the router (Caution will lose ethernet connectivity) .
             PATCH - Upload the specified patch firmware to the router (Caution will lose ethernet connectivity) .
             PatchFileName - Upload the specified patch file to the router .
             BOOTLOADER - Upload the bootloader to the router (Caution will lose ethernet connectivity) .
             COMBINED - Upload the combined bootloader+firmware to the router (Caution will lose ethernet connectivity) .
    
    
      
  
ROUTERUPTIME |  Indicates router uptime  
      
    
     ROUTERUPTIME
             Indicates router uptime.
    
    
      
  
ROUTESYMSTAT |  (*) Check Connection status of route symbols  
      
    
    ROUTESYMSTAT displays crosspoint connections
            syntax: ROUTESYMSTAT [-C:ControlId] [-E:EquipId]
            Options:
            -C:  Control Id number 0-65535, displays all crosspoints for the specified Control Id
            -E:  Equipment Id number 0-65535, displays all crosspoints for the specified Equipment Id
            No Options: display all crosspoints
    
      
  
RPRTCRESNETIDBYPPn |  Report cresnet ID by PPN  
      
    
     RPRTCRESNETIDBYPPN [4 Byte Hex PPN Number]
    
      
  
RPRTPPNBYCRESNETId |  Report PPN by cresnet ID  
      
    
     RPRTPPNBYCRESNETID [Cresnet Id in Hex]
    
      
  
SCREENSHOT |  Take a screen shot.  
      
    
    SCREENSHOT [filename]
    filename - Name of the file to save the screen shot to.
    The overlay parameter will save a screenshot of video if it's playing.
    Note: All files will be saved to the \ROMDISK\user\system\ folder.
    
      
  
SDEBUG |  (*) Check connection status of route symbols  
      
    
    SDEBUG[:program#] arguments
            program#: number of program to execute. (default=1)
            -D[ON|OFF]:  Set device to have it's debug info printed (ON) or not (OFF).  Followed by a space and:
              R  :  Turn on/off debug flag for all registered devices.
              A  :  Turn on/off debug flag for all devices.
              C  :  Turn on/off debug flag for all top-level Cresnet devices.
              C##:  Turn on/off debug flag for Cresnet ID ##.
              E  :  Turn on/off debug flag for all top-level Ethernet devices.
              E##:  Turn on/off debug flag for Ethernet ID ##.
              S  :  Turn on/off debug flag for all top-level Slots.
              S##:  Turn on/off debug flag for Slot ##.
              D##:  Turn on/off debug flag for Device ##.
                Note:  ISTAT DEV or ISTAT REGDEV can be used to list device numbers.
              ex:  SDEBUG -DON C0x25 turns on debug flag for Cresnet ID 25
              Dotted notation is valid for C, E, S commands above, i.e.:
                SDEBUG -DON C0x25.A turns on debug flag for Cresnet ID 25, Port A
                SDEBUG -DON S9.0x25.A turns on debug flag for Slot 9, ID 0x25, Port A
            -TXR[ON|OFF]:  Show transmitted packets in raw form.
            -TXI[ON|OFF]:  Show transmitted packets in interpreted form.
            -TXF[0|1]   :  Transmit Interpreted form: 0=Machine Parseable, 1=Human Readable.
            -RXR[ON|OFF]:  Show received packets in raw form.
            -RXI[ON|OFF]:  Show received packets in interpreted form.
            -RXF[0|1]   :  Receive Interpreted form: 0=Machine Parseable, 1=Human Readable.
            -PR[ON|OFF] :  Show ASCII characters in Raw Packets.
            -PI[ON|OFF] :  Show ASCII characters in Interpreted packets.
            -SB[ON|OFF] :  Suppress printing of broadcast packets.
            -SU[ON|OFF] :  Suppress printing of unresolvable packets (direct-to-wire packets going to an ID
                           not in the program).
            -O[ON|OFF]  :  Show Online/Offline Interpeted Messages.  Note that Online/Offline messages
                           will show regardless if interpretation is on.
            -S[0|1]     :  Show current settings, 0:Machine Parseable, 1:Human Readable.
            -QP[#]      :  Set quick-profile #; if #=?, show QP formats.
            -CON[ON|OFF]:  Write debug output to console
            -RM[ON|OFF|] :  Write debug output to Removable Media
            -SZ{size}   :  Set RM Log File Size maximum
            -ST[ON|OFF] :  Show Time before packet
            -SD[ON|OFF] :  Show Date when Time is printed
            NOTE:  A device *MUST* be in the currently running program in order to be debugged!
    
      
  
SECURECIPport |  Set Secure(SSL) port number for CIP  
      
    
    SECURECIPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current value
    
      
  
SECURECTPport |  Set/Get Secure CTPPort  
      
    
    SECURECTPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current value
    
      
  
SECUREGatewaymode |  Set/Display secure gateway operation mode.  
      
    
    SECUREGATEWAYMODE [DEFAULT | SECUREONLY | SECURENONCS | SECUREEXT]
            DEFAULT     - Accept both secure and unsecure Gateway CIP connections on all network interfaces.
            SECUREONLY  - Accept only secure Gateway CIP connections on all network interfaces.
            SECURENONCS - Accept only secure Gateway CIP connections from non control subnet.
                          Accept both secure and unsecure Gateway CIP connections on the control subnet ( Router Only Control Systems).
            SECUREEXT   - Accept only secure Gateway CIP connections from external IP addresses (from different subnets than any of the connected
    networks)
            No parameter - displays current Secure gateway mode settings.
    
      
  
SECUREWebport |  Set Secure(SSL) port number for Web.  
      
    
    SECUREWEBPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays current value
    
      
  
SENDCNETPKT |  Send a Cresnet Packet  
      
    
     SENDCNETPKT {Parameters}
            SENDCNETPKT {data (w/o count)}   - Send a Cresnet packet.
            data is a string of 2-digit hex bytes.
            For example: "SENDCNETPKT 03000000\r" sends a digital high to join 1 on ID 3.
     SendCresnetPacket: Packet sent successfully
    
      
  
SENDIPTABLE |  Transfer the IP table to Internal flash  
      
    
    SENDIPTABLE [program]
            program - which program the table is for (default = 1)
    
      
  
SETANALOGJOIN |  Set a analog join value  
      
    
    Process a serial join.
    SETANALOGJOIN [join#] [join value]
            [join#] - positive integer
            [join value]
    
      
  
SETCRESNETIDBYPPn |  Set cresnet ID by PPN  
      
    
    Valid options are:
       Status if no arguments
    Syntax: SETCRESNETIDBYPPN [HEX cnet ID] [HEX 4-byte Address | ALL ]
    
      
  
SETCSAUTHENTICATION |  Set Control System Authentication credentials.  
      
    
    SetCSAuthentication -N:Username -P:Password
    Sets Control System Authentication parameters for CIP connect message.
             -N: specifies name of a local or domain (domain\user) user
             -P: specifies password.
    
      
  
SETDIGITALJOIN |  Process a digital join  
      
    
    Process a digital join.
    SETDIGITALJOIN [join#] [join value]
            [join#] - positive integer
            [join value]  - (0=FALSE, 1=TRUE)
    
      
  
SETLOCKOUTTIME |  Set time that an IP is blocked from login  
      
    
    No help available for this command.  
  
SETLOGINAttempts |  Set the maximum number of login attempts before a user is blocked  
      
    
    No help available for this command.  
  
SETLogoffidletime |  Set idle time allowed before current user is automatically logged off  
      
    
    No help available for this command.  
  
SETPAsswordrule |  Set password rules for local users  
      
    
    SETPASSWORDRULE {-ALL | -NONE} | {-LENGTH:minPasswordLength} {-MIXED} {-DIGIT} {-SPECIAL}
            -ALL: all rules will be applied.
            -NONE: no rule will be applied.
            -LENGTH: specifies minimum password length. By default, the minimum length is 6. This parameter can't be combined with NONE.
            -MIXED: password must contain a lower and upper case character. This parameter can't be combined with NONE.
            -DIGIT: password must contain a number. This parameter can't be combined with NONE.
            -SPECIAL: password must contain a special character. This parameter can't be combined with NONE.
    
      
  
SETPPNBYCRESNETId |  Set PPN by cresnet ID  
      
    
    Valid options are:
       Status if no arguments
    Syntax: SETPPNBYCRESNETID [HEX cnet ID] [4 byte Hex Adr]
    
      
  
SETPPNBYPPn |  Change old PPN to new PPN  
      
    
    Valid options are:
       Status if no arguments
    Syntax: SETPPNBYPPN [Hex OldAdr]|ALL [HEX NewAdr]
    
      
  
SETSERIALJOIN |  Process a serial join  
      
    
    Process a serial join.
    SETSERIALJOIN [join#] [join value]
            [join#] - positive integer
            [join value]
    
      
  
SETSIGnal |  (*) Set the state of a signal in the program  
      
    
    SETSIGNAL[:program#] signal_number value {-U}
            program#: number of program to execute. (default=1)
            signal number - Hex Number (i.e. 0x0000000B) or Decimal number (i.e. 11)
            value         - 0 or 1 for Digital
                          - pXX : Pulse XX ms long for Digital
                          - iXX : Inverse pulse XX ms long for Digital
                          - 0 to 65535 for Analog
                          - Quoted string for Strings
            -U            - Assumes UTF-16 encoding of the string (default ASCII).
    
      
  
SETTBCLIENTCONNFRVR |  Set Console Client to try and reconnect after a disconnect  
      
    
    SETTBCLIENTCONNFRVR [ON|OFF]
            Sets Console Client to reconnect after a disconnect
    
      
  
SETTBCLIENTIPA |  Set Console Client Server IP Address  
      
    
    SETTBCLIENTIPA [ip_address | HostName]
            ip_address - IP address in dot decimal notation
            HostName - TBClient server hostName
    
      
  
SETTBCLIENTNUMRETRY |  Set Console Client number of retries  
      
    
    SETTBCLIENTNUMRETRY [numberofretries]
            numberofretries - Max number of retries
            0 indicates that the console client connection will keep on trying to connect to the server
    
      
  
SETTBCLIENTPORTNUM |  Set Console Client Server Port Number  
      
    
    SETTBCLIENTPORTNUM [portnumber]
            portNumber - Port Number in decimal notation
    
      
  
SHOWARPtable |  Display interface ARP table  
      
    
    SHOWARPTABLE
            No parameters
    
      
  
SHOWEXTRAerrors |  Enables extended errors  
      
    
    SHOWEXTRAERRORS [{option}] [OFF | ON]
            {option}  [OFF | ON] turns on or off specified option
                    Px - extra for Program x on (x = program number)
                    CON - extra for console
                    SYS - extra for general system information
                    ENET - extra for ethernet communications
                    OSD - extra for On Screen Display
                    BAC - extra for BACnet communications
                    CRESTIMERENG - extra for Crestron Timer Engine
                    AUTOUPDATE - extra for Crestron Auto Updater
                    WEB - extra for Crestron Web Scripting (IIS/ISAPI)
            OFF - turns all off
            ON - turns all on
            No parameter - displays current setting
    
      
  
SHOWHW |  Display hardware configuration  
      
    
     SHOWHW
     No parameters
    
      
  
SHOWLICENSE |  Display list of licensed application(s).  
      
    
    SHOWLICENSE - display list of licensed application(s).
    
      
  
SHOWPORTMAP |  Display the current portmaps for the router.  
      
    
    SHOWPORTMAP [-ALL]
            -ALL shows both user and system level ports.
            No arguments shows only user level ports.
    
      
  
SIGDEBUG |  (*) List Sig information for the specified device.  
      
    
    SIGDEBUG[:program#] -T:[Transport] -I:[DeviceID].{[Subslot(s)]}
            -T:E|C|S     Device is apart of Ethernet, Cresnet, or an internal Slots.
            -I:ID        ID of the device with optional subslots. Ex: 3.1.1.
    
      
  
SIGNALTIMESTAMP |  (*) Show signal timestamps  
      
    
    SIGNALTIMESTAMP not supported in this build.
    
      
  
SNTP |  Configure network time synchronization  
      
    
    SNTP [START |STOP| SYNC] [SERVER:address] [PERIOD:time}
            START  - starts periodic synchronization
            STOP   - stop periodic synchronization
            SYNC   - force synchronization
            SERVER - address of server to synchronize with
            PERIOD - how often synchronization is done (in minutes min=10)
            No parameter - displays current setting
    
      
  
SOCKETSendtimeout |  Set TCP Socket Send Timeout value in Milliseconds  
      
    
    SOCKETSENDTIMEOUT [value]
            value - desired timeout in milliseconds
            No parameter - displays current value
    
      
  
SPDISDBGTHREAD |  (*) S+ Disable Debug Thread command.  
      
    
    SPDISDBGTHREAD[:program#]
             Disable Debug Threads.
    
      
  
SPENADBGTHREAD |  (*) S+ Enable Debug Thread command.  
      
    
    SPENADBGTHREAD[:program#]
            Enable Debug Threads.
    
      
  
SPLUSDBGRX |  (*) S+ Rx Debug.  
      
    
    SPLUSDBGRX[:program#] ON|OFF
            View signals received by SIMPL+.
            ON  - Enable Debugs
            OFF - Disable Debugs
    
      
  
SPLUSDBGTX |  (*) S+ Tx Debug.  
      
    
    SPLUSDBGTX[:program#] ON|OFF
            View signals transmitted by SIMPL+.
            ON  - Enable Debugs
            OFF - Disable Debugs
    
      
  
SPLUSLOAD |  (*) Test loading a SIMPL+ module  
  

SPLUSTEST |  (*) Print receive signal times (min,max, ave.) for each module  
      
    
    SPLUSDBGRX[:program#]
            Print receive signal times (min,max, ave.) for each module.
            No arguments necessary.
    
      
  
SPLUSTasks |  (*) Get a list of running S+ Tasks.  
      
    
    SPLUSTasks[:program#]
            View running S+ Tasks.
            No arguments necessary.
    
      
  
SPSHOWPOOLERR |  (*) S+ Show Smart Thread Pool Error.  
      
    
    SPSHOWPOOLERR[:program#]
            Show Thread Pool Errors
    
      
  
SSHARPDebug |  (*) Set SimplSharpPro Debugs  
      
    
    SSHARPDebug[:program#] {Parameters}
            APPTOTLDMSENDMESSAGETIMEOUT time          10000    Timeout for sending messages to the TLDM in ms
            TLDMTOAPPSENDMESSAGETIMEOUT time          20000    Timeout for receiving messages from the TLDM in ms
            SENDTOTLDMTIMEOUT time                    10000    Timeout for SendToTldmEx() calls in ms
            HEARTBEAT number                             20    Number of Heartbeats before app manager forces a restart.
            UPREQTIMEOUT number                       30000    Timeout for obtaning Join collection mutexes for normal access/update req.
            BUILDIFOFFLINE ON|OFF                       OFF    Build/Send packet even if device is offline.
            SENDPARAMETERS ON|OFF                       OFF    Always obey SendParameters() call.
            PJG ON|OFF                                  OFF    Page Join Gating debugs.
            UPREQ ON|OFF                                OFF    Update Request debug.
            PJGTIMEOUT time                           10200    Timeout for to wait for Page Join Gating Sync event
            DMPS3 ON|OFF                                OFF    Show some DMPS3 debug info.
            ERSLEEPY                                           Show ErSleepy device information.
            DTADELAY                                    OFF    TLDM Data to App Delay debugs.
            BACNETSTOPPEDTIMEOUT                         15    Overall timeout for Bacnet to complete stop, in min.
    
      
  
SSHPORT |  Set/Get the SSH Port  
      
    
    SSHPORT [OFF | ON | portnumber]
            [OFF | ON] - Disables/Enables SSH. Default is ON
            portnumber - desired port number (in decimal).
            No parameter - displays current value
    
      
  
SSL |  Display/Set SSL type.  
      
    
    SSL [OFF | SELF | CA] [-P:password] {TLSSSL | TLSONLY | TLS1.2ONLY}
            where 'OFF' turns off SSL,
            where 'SELF' sets SSL to use 'self-signed' certificates,
            where 'CA' sets SSL to use 'CA' issued certificates,
            where '-P:' supplies password for opening the private key file when SSL is set to CA,
            where 'TLSSSL' implies that we support SSL fallback (default) for client/server connections.
            where 'TLSONLY' implies that we do not support SSL fallback for client/server connections.
            where 'TLS1.2ONLY' implies that we ONLY support TLS1.2 for client/server connections.
            No parameter - displays current setting
    
      
  
SSLVERIFY |  Display/Set SSL certificate verification.  
      
    
    SSLVERIFY [OFF |  CA]
            where 'OFF' disables checking certificates (allow both SELF and CA certificates),
            where 'CA' ensures that the certificate is issued by a CA,
            No parameter - displays current setting
    
      
  
SSPTASKs |  (*) Show currently executing user threads in SIMPL# Pro.  
      
    
    SSPTASKs[:program#]
            View a list of the executing user threads in a SIMPL# Pro program.
            No arguments necessary.
    
      
  
STARTTBCLIENT |  Enables Console Client Connection  
      
    
    STARTTBCLIENT
            Enables Console Client connection
    
      
  
STOPLIGHTBYPPn |  Stop Light And Poll mode  
      
    
    Valid options are:
       Status if no arguments
    Syntax: STOPLIGHTBYPPN [4 byte Hex Adr]|ALL [SHOW]
    
      
  
STOPPROGram |  Stops the specified program  
      
    
     STOPPROGRAM {-P:ALL | -P:Specific Program Identifier} {-V} {-K}
             -P:  Stop a specific program or ALL.  If not present, ALL assumed.
             -V:  Verbose shutdown.
             -K:  Keep DBGSIGNAL information (STOPRPG normally clears DBGSIGNAL flags)
    
    
      
  
STOPTBCLIENT |  Disable Console Client Connection  
      
    
    STOPTBCLIENT
            Disables Console Client connection - will break connection
    
      
  
SUDO |  Sudo Command  
      
    
    SUDO cmd [param1 param2 ...]
            cmd: command to execute.
            param1,param2,...: parameters for the command.
    
      
  
SUSERPROGCMD |  (*) Send a command from the console to the user program(Suppress prompt)  
      
    
    SUSERPROGCMD[:program#] {quoted string}
            program#: number of program to execute. (default=1)
            Escape sequences will be translated, quotes will not be sent to user program.
            The program needs a "User Program Commands" symbol to receive the data
    
      
  
SYMDEBUG |  (*) Symbol debug operations  
      
    
    SYMBOLDEBUG {Parameters}
              -ON:#### : Turn on Debug for Symbol ####.
              -OFF:#### : Turn off Debug for Symbol ####.
              -L : List symbols being debugged.
              -C : Clear debugging bits for all symbols.
              -S : Save debug symbol list to registry.
    
      
  
SYMSETSIG |  (*) Set the state of a signal in the program  
      
    
    SYMSETSIG[:program#] symbol_number index value [A | D | S]
            program#: number of program to execute. (default=1)
            symbol number - Hex Number (i.e. 0x0000000B) or Decimal number (i.e. 11)
                            Can be gotten from ISTAT PROG | DEV | REGDEV
            index         - Hex Number (i.e. 0x0000000B) or Decimal number (i.e. 11)
                            0 based index into existing signals on symbol.
            value         - 0 or 1 for Digital
                          - pXX : Pulse XX ms long for Digital
                          - iXX : Inverse pulse XX ms long for Digital
                          - 0 to 65535 for Analog
                          - Quoted string for Strings
            [A|D|S]       - Optional List specifier for Trilisted symbols
                            (Analog, Digital, Serial).  index is then 0 based
                            into the respective list.
    
      
  
SYSLOG |  Enable/disable system UI log.  
      
    
    SYSLOG [ON|OFF|CLEAR|PRINT|LOGNOTICEON|LOGNOTICEOFF|LOGEXTRAON|LOGEXTRAOFF]
             Enable/disable UI system logging.
             No Parameters - Displays current setting
    
      
  
SYSMON |  System Monitor Control  
      
    
    Local commands affecting individual monitors
            xx [c|d|e|f|r|s|?] - show/flags/help specific monitors
            ? - show this monitor help
            Calibrate - reset idle system load factor
            Disable|OFF - stop monitoring this option
            Enable|ON  - start monitoring this option
            Flags [#dec value] - set specific flags to value
            Reset - reset min/max stats for this monitor
            Show run-time - toggle run-time display for this monitor
    Example:
     3 show on - will set run-time display option to ON
    Global commands affecting all
      Disable|OFF - disable globally
      Enable|ON - enable globally
      Id stats - show cresnet stats by ID
      Minmax - show minimum/maximum stats for all
      Reset  - reset min/max stats
      Save  - save settings
      Timing xx - update loop in seconds
    
      
  
SYSMSG |  Enable/disable system message display.  
      
    
    SYSMSG [ON|OFF]
             Enable/disable system message display.
             No Parameters - Displays current setting
    
      
  
SYSTEMKEY |  Display system key.  
      
    
    SYSTEMKEY - display system key.
    
      
  
SYSTHREADPOOL |  (*) Set or show the size of the system thread pool  
      
    
    SYSTHREADPOOL[:program#] [threadpoolsize]
            Sets the system thread pool size. Used for Async socket opeations/Timers/Invoke operations.
            hreadpoolsize  - Thread Pool Size
            No Parameters - Returns the current thread pool size.
    
      
  
TCPKEEPALIVE |  Enable/disable TCP Keep Alive  
      
    
    TCPKeepAlive [ON | OFF]
            Enables/Disables TCP Keep Alive
            TCP Keep Alive is supported for Client-Servers / Direct Socket  Client-Servers / Console connections
            No parameter - displays current setting
    
      
  
TELNETport |  Enable/disable the Telnet port  
      
    
    TELNETPORT [OFF | ON ]
            No parameter - displays current setting
    
      
  
TESTDNS |  Test DNS Server  
      
    
    TESTDNS string
            string - ASCII string containing host name
    
      
  
TESTWATCH |  Test watchdog timer  
      
    
    TESTWATCH [HW | SW]
            HW - test the hardware watchdog timer
            SW - test the software watchdog timer
    
      
  
THREADPOOLINFO |  (*) Information about the S+ Thread pool.  
      
    
    THREADPOOLINFO[:program#]
            View S+ Thread Pool Information.
            No arguments necessary.
    
      
  
THREADPOOLSIZE |  (*) Get or Set the S+ ThreadPoolSize.  
      
    
    THREADPOOLSIZE[:program#] [INITPOOLSIZE]
            INITPOOLSIZE - Set the initial number of threads in the pool.
            No Parameter - Display the size of the thread pool.
    
      
  
TIMEZone |  Set the timezone  
      
    
    TIMEZONE [LIST | zone]
            LIST - print timezones
            zone - number of the timezone to set
            No parameter - displays current setting
    
      
  
TIMEdate |  Set the time and date  
      
    
    TIMEDATE [hh:mm:ss mm-dd-yyyy]
            hh:mm:ss - time in hours (use 24hr), mins and secs
            mm/dd/yyyy or mm-dd-yyyy - date in months(1-12), day(1-31) and year
            No parameter - displays current setting
    
      
  
TRANSFERLICense |  Transfer application license.  
      
    
    TRANSERLICENSE [VENDORID] [MODULEID] [SYSTEMKEY] [HOSTNAME] - transfer license to other controller
            VENDORID - vendor id, valid range (1...65535)
            MODULEID - module id, valid range (0...65535)
            SYSTEMKEY - system key for other controller
            HOSTNAME - hostname for other controller
    
      
  
TRIGGEREVents |  Trigger timer events for application id.  
      
    
    Trigger timer event for specified event group within program id.
    TRIGGEREVENTS -I:ProgramTag -G:GroupEventName -E:EventName
             -I: ProgramTag/UserDefinedTag
             -G: Group Event Name
             -E: Event Name
    
      
  
TYPE |  Display file contents  
      
    
    TYPE filename
            filename - the name of the file to display
    
      
  
UCMD |  (*) Send a command from the console to the user program  
      
    
    USERPROGCMD[:program#] {quoted string}
            program#: number of program to execute. (default=1)
            Escape sequences will be translated, quotes will not be sent to user program.
            The program needs a "User Program Commands" symbol to receive the data
    
      
  
UPDATEPassword |  Update current local user's password  
      
    
    No help available for this command.  
  
UPLOAD |  Load file into cresnet device  
      
    
    Valid options are:
     CRESnet -  UPLOAD Over Cresnet
     SLOT - plug-in card
     UPLOad - device upgrade
     CODE - device upgrade
     FIrmware - device upgrade
     DATA - xmodem xfer mode
     SCreen - xmodem xfer mode
        hex number allowed as argument
     UPLOAD [SLOT|CNET(default)] ID_OR_SLOT_NUM [FIRMWARE |CODE | SCREEN |DATA(default)]
    
      
  
UPTIME |  Display the time the system is running  
      
    
    UPTIME
            no parameters needed
    
      
  
USERINFOrmation |  Show access information for a specific user.  
      
    
    No help available for this command.  
  
USERPROGCMD |  (*) Send a command from the console to the user program  
      
    
    USERPROGCMD[:program#] {quoted string}
            program#: number of program to execute. (default=1)
            Escape sequences will be translated, quotes will not be sent to user program.
            The program needs a "User Program Commands" symbol to receive the data
    
      
  
VERsion |  Version Command  
      
    
    VERSION [-v]
            -v : show extended version info.
    
      
  
WAVEDUMP |  (*) Dump Logic Wave Information  
      
    
    WAVEDUMP[:program#] arguments
            program#: number of program to execute. (default=1)
            Set parameters/display the Logic Wave history.
            -C:ON|OFF  Dump list of last 0 symbols executed after a
                       "Could not solve logic within 1500 waves." error to Console.  Currently OFF.
            -F:ON|OFF  Dump list of last 0 symbols executed after a
                       "Could not solve logic within 1500 waves." error to File.  Currently OFF.
            -S:#       Store information for up to this number of symbols (Currently 0)
            -L         Dump the wavelist.
            Note:  Wave Dumps may not show a full history for a solution depending on the size of the wave history.
                   When using this command it is highly recommended to use the -C:ON and/or -F:ON form to dump the list immediately, not -L.
    
      
  
WEBINIT |  Initialize Webserver default file.  
      
    
    WEBINIT
            no parameters needed
    
      
  
WEBPORT |  Set port number for Webserver.  
      
    
    WEBPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays current value
    
      
  
WEBSERVer |  Enable/disable Webserver.  
      
    
    WEBSERVER [ON | OFF]
            No parameter - displays current setting
    
      
  
WHO |  Generate a report of the Ethernet consoles  
      
    
    WHO
             No Parameter neccessary
    
      
  
WHOAmi |  Display current user's identity  
      
    
    WHOAMI
            No parameters needed.
    
      
  
WI2CGen |  Write i2c data  
      
    
     WI2CGEN [bus] [adr] [sub] [sublen] [data0]...[data n] - set I2C data
            bus - i2c bus, in decimal, range <1..3>.
            adr - i2c address, hex bytes.
            sub - i2c sub address, hex bytes, e.g. register addr
            sublen - sub address len 0..4 bytes.
            [data0]...[data n]: data in hex.
    
      
  
WRITEI2C |  Write i2c data  
      
    
            WRITEI2C [device] [subaddr] [byte0] ... [byteN] - write I2C device
              device  - device index, range <0..7>
              subaddr - sub-address in hex, e.g. register addr
              [byte0..byteN] - data in hex
              device | name
              =========================
              00     | SYSTEM ID
              01     | FPGA-RF PCA9538
              02     | RESETs PCA9539
              03     | BOARD ID
              04     | FAN_LM63
              05     | RTC DS3231
              06     | PMIC
              07     | SMARTREFLEX
    
      
  
XGETfile |  Use XMODEM to transfer file from ROM  
      
    
    XGET filename
            filename - name of the file
    
      
  
XLOADCERtfile |  Use XMODEM to transfer certificate file to ROM  
      
    
    XLOADCERTFILE size date time name
            size - size of the file in bytes
            date - date of the file (MM-DD-YY)
            time - UTC time of the file (HH:MM:SS)
            name - name of the file
    
      
  
XPUTfile |  Use XMODEM to transfer file to ROM  
      
    
    XPUT size date time name
            size - size of the file in bytes
            date - date of the file (MM-DD-YY)
            time - UTC time of the file (HH:MM:SS)
            name - name of the file
    
    

