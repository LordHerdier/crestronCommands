# Commandset for the DMPS3-4K-150-C

> DMPS3-4K-150-C Cntrl Eng [v1.7001.4523.04604 (May 21 2021), #8B02431A]
> @E-00107fc92ed0
>
> 207 normal commands found. 150 hidden commands available.

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
    
      
  
ADDLOCKEDUser |  Add a user account to the locked list  
      
    
    No help available for this command.  
  
ADDMASTER |  Console command to enter the Peer System IP Address and IPID  
      
    
    [IPID] [IP Address]
    Current Settings: IPID = 0  IP Address =
    
      
  
ADDPORTMAP |  Add a port map to the NAT table  
      
    
            ADDPORTMAP ext_port int_port ip_address protocol
            ext_port   - port number on the WAN side of NAT
            int_port   - port number on the LAN side of NAT
            ip_address - IP address (in dot decimal notation)
                         of the device on the LAN side of NAT
            protocol   - IP protocol for the portmap service (TCP | UDP | Both)
    
      
  
ADDPeer |  Add a peer(slave) entry to IP table  
      
    
    Format: ADDPeer cip_id ip_address/name [-D:device_id] [-C:cipport] [-P:program] [-U:RoomId]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            RoomId  - Upto 32 characters. Valid characters are A-Z and 0-9.
                           -        This is used for communication with a Virtual Control server
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
             -P:  Dump app info for a specific program.   If not present, ALL assumed.
    
    
      
  
ARMBITset |  AV manager Debug  
      
    
             Set ARM Upgrade Bit Map
             ARMBITSET [value] ( Each bit indicate one ARM [1-2])
             [value]: 0: no ARM need upgrade; 7: 2 ARMs and FPGA need upgrade
    
      
  
ARMBLBITSET |  AV manager Debug  
      
    
             Set ARM Boot Loader Upgrade Bit Map
             ARMBLBITSET [value] ( Each bit indicate one ARM [1-3])
             [value]: 0: no ARM  Boot Loader need upgrade; 3: 2 ARMs Boot Loader need upgrade
    
      
  
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
            NONE- To go back to the Default Plugin Catalog URL which is https://www.crestron.com/autofwupdates/AU-Plugin-Catalog.txt.
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
      
    
    AUTODISCOVERY [ON | OFF | QUERY | LIST | HOSTS | SETNUMTIMESQUERYMSGSENT times | SETDELAYBETWEENQUERYMSGINMS delayInMs | OPTION
    autodiscoveryqueryoption | ADAPTER autodiscoveryadapteroption]
            on : enables autodiscovery functions
            off : disables autodiscovery functions
            query : runs the discovery query
            list : displays the list of nodes discovered
            hosts : displays the list of hostnames
                    NoForceAll : Will not force all the devices into light-n-poll mode if the specified device type is not found.
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
    
      
  
AVMANAGERSTAT |  AV manager status.  
      
    
    ** dm_hd_mfs_avmanager status **
    Default priority:251
    Video priority:251
    HW version:0
    Task info
    TaskList[6]: Name (ID, Running, Created, Current)
    Task[0]: CMRx_0 (0x060e0102, 1, 1, 0)
    Task[1]: CMTx_0 (0x07ee00fe, 1, 1, 0)
    Task[2]: CMRx_1 (0x06390102, 1, 1, 0)
    Task[3]: CMTx_1 (0x069a0102, 1, 1, 0)
    Task[4]: CnAvQ (0x06d9010e, 1, 1, 0)
    Task[5]: Proc67D00AE_Task5 (0x06420186, 0, 1, 0)
    Timer info:
    TimerList[1]: Name (ID, Running, Created, Current)
    Timer[0]: Proc67D00AE_Timer6 (0x075e0182, 1, 1, 0)
    Queue info:
    QueueList[0]: Name (CurrQ, MaxQ, HighQ, MaxSize, NumRead, NumWrite, Flags)
    Lock info:
    Count: 10
    MemoryManager:
     MemMgr buffers: small 160/1/0, medium 80/1/0, large 40/1/0, exlarge 24/0/0
    TLDM:
    Slot: 251
    Stream1 - Digital usage (125 of 800) Stream1 - Analog usage (170 of 800) Stream1 - Serial usage (40 of 400)
    EnableJoinFeedback:1
    EnableThrottle:0
    FeedbackTimer:100
    ThrottleTimeout:108000
    
      
  
AVMDEBug |  CMDEBUG command.  
      
    
    To use debug Table: DEBUG [INDEX] [ON|OFF]
    
      
  
BENCHMARKS |  Run Platform benchmarks  
      
    
    BENCHMARKS {Test Number}
    1 - Run All Benchmarks
    2 - Platform Time Reference
    3 - Benckmark Threads
    4 - Benchmark Mutex
    5 - Benchmark CriticalSection
    6 - Benchmark Crestron Queue
    
      
  
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
             Where Certificate_Store = [ROOT|MACHINE|USER|INTERMEDIATE|WEBSOCKET]
             ADD  Certificate_Store -                  Add Certificate(from known location) To Specified Certificate Store (MACHINE store requires
    password)
             REM  Certificate_Store Certificate_Name Certificate_UID -  Remove Specified Certificate From Specified Certificate Store
             LIST Certificate_Store -                  List All Certificates In Specified Certificate Store
             VIEW Certificate_Store Certificate_Name Certificate_UID -  View Details Of Specified Certificate In Specified Certificate Store
             No parameter -                            Lists Usage
    
      
  
CGIO |  Clear GIO pin on the MFMSys Blade  
      
    
            CGIO [pin_index]
    Pin Name                        Pin    Name
    00: TP37                        01: FAN_POWER_EN                02: FAULT_LED (RED)
    03: PGOOD_LED (GREEN)           04: CRESNET_RXEN_TXEN_N         05: EXT_ETH_PHY_RST_N
    06: MEZZ_LAN_ETH_PHY_RST_N      07: MEZZ_RST_OUT                08: PROC_INIT_DONE
    09: BASE_ID0                    0A: BASE_ID1                    0B: BASE_ID2
    0C: LVDS_PARA_VIDEO_PWDN_N      0D: FP_SETUP_BUTTON             0E: UNUSED_02
    0F: UNUSED_03                   10: UNUSED_04                   11: BOARD_ID0
    12: BOARD_ID1                   13: BOARD_ID2                   14: BOARD_ID3
    15: BOARD_ID4                   16: BOARD_ID5                   17: BOARD_ID6
    18: BOARD_ID7                   19: BOARD_REV0                  1A: BOARD_REV1
    1B: SYSID_REV0                  1C: SYSID_REV1                  1D: SYSID_REV2
    1E: RSVD_FP_ID0                 1F: RSVD_FP_ID1                 20: TP10
    21: MEZZ_USB_ETH_CONT_RST_N     22: MEZZ_FRONT_PANEL_RST_N      23: USB_PORT3_ENABLE_N
    24: USB_PORT4_ENABLE_N          25: MEZZ_ETH_SWITCH_RST_N       26: USB_PORT1_ENABLE_N
    27: USB_PORT2_ENABLE_N          28: USB_ETH_PHY_RST_N           29: TP70
    2A: RSVD_FP_SPARE0              2B: RSVD_FP_SPARE1              2C: CPU1_MEZZ_GPIO_1
    2D: CPU1_MEZZ_GPIO_2            2E: CPU2_MEZZ_GPIO_1            2F: CPU2_MEZZ_GPIO_2
    30: TP34                        31: MEZZ_CPU1_GPIO_1            32: MEZZ_CPU1_GPIO_2
    33: MEZZ_CPU1_GPIO_3            34: MEZZ_CPU2_GPIO_1            35: MEZZ_CPU2_GPIO_2
    36: MEZZ_CPU2_GPIO_3            37: MEZZ_CPU1_RESET_N           38: MEZZ_CPU2_RESET_N
    
      
  
CIPHER |  Set/Get the class of ciphers/algorithms used for the encryption  
      
    
    CIPHER [STRONG/ALL]
            parameter - desired set of ciphers/algorithms SSH server will use for encryption
            No parameter - displays current value
            NOTE: This command has been deprecated and no longer has any effect
    
      
  
CIPPORT |  Set port number for CIP  
      
    
    CIPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current value
    
      
  
CLEARAUDITLOG |  Clear the audit log.  
      
    
    No help available for this command.  
  
CLEARCSAUTHENTICATION |  Clear Control System Authentication credentials.  
      
    
    ClearCSAuthentication
    Clear Control System Authentication parameters for CIP connect message.
    
      
  
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
    
      
  
COURTESYPORT |  Add/Remove Courtesy port for service  
      
    
            COURTESYPORT [port number/ALL] [on/off]
            COURTESYPORT Add/Remove Courtesy port
    
      
  
CREATECsr |  Generate a CSR.  
      
    
    CREATECSR C:ST:L:O:OU:CN:E [-I:option] [-S:DNS:domain1[,DNS:domain2][,DNS:domain3],...]
            where C = 2 letter country code (leave blank if not needed)
            where ST = state or province name (leave blank if not needed)
            where L = locality or city name (leave blank if not needed)
            where O = organization name (required)
            where OU= organizational or unit name (leave blank if not needed)
            where CN = Common name (required)
            where E = email address (leave blank if not needed)
            where -I: Ignore blank parameters. Options are True or False.
            where -S: Subject alternative name parameter(s).
                    May specify multiple items separated by commas.
    
      
  
CSPROJECTRemove |  Remove the project from Control System  
      
    
    CSPROJECTREMOVE  {-P:ALL | -P:Specific Project name  -T: WebXPanel | -T:MobileApp  -U:TB | -U:AU }
             -P:  Remove a specific project or ALL.  Must be specified.
              -T:  Project type 'WebXPanel' or 'MobileAp'
             -U: the console command requestor ID, 'TB' - toolbox or 'AU' - Autoupdate
    
      
  
CSPROJECTload |  Load the project in Control System  
      
    
    CSPROJECTLOAD { -P:Specific Project name  -T: WebXPanel | -T:MobileApp  -U:TB | -U:AU   }
                      -P:  Load a specific project or  no parameter Show current installed projects
                      -T:  Project type 'WebXPanel' or 'MobileApp' Optional for CH5 MobileApp and WebxPanel projects
                      -U: the console command requestor ID, 'TB' - toolbox or 'AU' - Autoupdate
    
      
  
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
    
    
      
  
DEFAULTPORTMAP |  Setup default port mappings  
      
    
            DEFAULTPORTMAP
            Adds all default port mappings.
    
      
  
DEFGWUPD |  Update Default Gateway Address and update permission  
      
    
            DEFGWUPD [on / off] -- Update Default Gw Address on service port and disable/enable default Gw address update.
    
      
  
DEFRouter |  Set default router.  
      
    
    DEFROUTER [device_num ip_address]
            device_num - specified Ethernet device  [0 - 1]
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
    
      
  
DEVice |  Device command.  
      
    
    DEVICE LIST
            lists all devices in the system
    DEVICE  [INST]     ...
    DEVICE  [INST] USER     ...
            lists all devices in the system
            Values are in hexadecimal
    Device Commands:
            INIT
            PRINT
            HALT
            TX
            RX
            DBGSET
            DBGGET
            LOAD
            SET
            GET
            DETECT
            TEST
            ERASE
            ENABLE
            DISABLE
            DUMP
            ?
    
      
  
DHCP |  Enable/disable dynamic IP addressing.  
      
    
    DHCP [device_num [ON | OFF | REL_RENEW]]
            ON - enables DHCP for device_num
            OFF - disables DHCP for device_num
            REL_RENEW - performs a DHCP release and renew for device_num
            No parameter - displays current setting for all devices
    
      
  
DHCPOPT |  Sets DHCP Server Options  
      
    
    DHCPOPT [HOSTNAME | FQDN]
            HOSTNAME - Send Local HostName in DHCP Discover Request - Default Option
            FQDN - Send the Fully Qualified Domain Name in DHCP Discover Request
            No parameter - displays current setting
    
      
  
DIR |  List files and directories in current directory  
      
    
    DIR filesearchstring
        filesearchstring - search string which may contain wildcards
    
      
  
DMANALYZE |  Set mirroring to backplane port  
      
    
            DMANALYZE [on/off]          -- for all ports
            DMANALYZE [on/off] -P[port] -- for one port
            Set ethernet switch in DM_ANALYZE: analyzeport 9, port0-7 mirror to analyze
    
      
  
DMPING |  DMPING command  
      
    
    Pinging all devices. Please wait....... (Could take up to 4 seconds)
    DMPING
            Display all DM connected Endpoints that have ethernet connection with this box.
            No parameters
    
    
      
  
DMRCon |  DMRCON command  
      
    
             DMRCON all [slot decSlot][.subslot hexSlot..] [command string]
    
    
      
  
DMSAFECASCADE |  DM SafeCascade command  
      
    
    Safe Cascading is OFF
    . Reboot to take effect
    
      
  
DMUPLOAD |  Upload endpoint via DMnet  
      
    
             Upload Endpoint Firmware syntax:
             DMUPLOAD [A|B] [Slot].1 [file name]
             [A|B|C|D] : A - for firmware, B - for bootloader
             Security  : C - for firmware, D - for bootloader
             valid slots: 9, 10, 11
    Done with DMUPLOAD command!
    
      
  
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
    
      
  
DUMPDMIPCONFIG |  Reports DM IP Config  
      
    
    DUMPDMIPCONFIG:
    Reports DM IP Config:
    
      
  
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
    
      
  
ENABLEFDEBUG |  Enable fdebug  
      
    
    To use field debug: FDEBUG [INDEX] [ON|OFF]
    01 HDMI RX
    02 HDMI TX
    03 ANALOG RX
    04 HDCP MAX DEVICE TEST
    05 CP VERIFICATION
    06 EDID
    07 CRESNET RX
    08 CRESNET TX
    09 HDMI RX AUDIO
    10 DSP
    11 HDMI FIBER
    12 USB
    13 HDCP RX
    14 HDCP TX
    15 HDMI TX AUDIO
    16 STREAM
    17 DM RX
    18 DM TX
    19 SERIAL PORT
    20 DM MASTER
    21 DM SLAVE
    22 ETHERNET
    23 DMNET CEC
    24 SDI RX
    25 SCALER
    26 ANALOG TX
    27 OW RX
    28 OW TX
    29 VS RX
    30 VS TX
    31 OW POLL
    32 OW EDID
    33 OW HDCP
    34 OVERLAY HANDLER
    35 LVDS RX
    36 HDMI CEC
    37 AUDIO DAC
    38 FPGA
    39 ENCAPSULATION
    40 SWITCHER
    41 DP RX
    42 TOUCH
    43 CALTOUCH
    44 IR TX
    45 DM CONTROLLER
    46 SYSTEM STATS
    47 EXT TOOL EDID
    48 USB I
    49 VIDEO MSG HANDLER
    50 FRONT PANEL
    51 CNET MASTER
    52 LCD MANAGER
    53 INTERAPP
    54 TEST GEN
    55 TEST AMP
    56 CHANNEL MGR
    57 AVM MGR
    58 AVM CNET MGR
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    To disable all field debugs: FDEBUG OFF
    To enable all field debugs: FDEBUG ON
    To use field debug: FDEBUG [INDEX] [ON|OFF]
    01 HDMI RX
    02 HDMI TX
    03 ANALOG RX
    04 HDCP MAX DEVICE TEST
    05 CP VERIFICATION
    06 EDID
    07 CRESNET RX
    08 CRESNET TX
    09 HDMI RX AUDIO
    10 DSP
    11 HDMI FIBER
    12 USB
    13 HDCP RX
    14 HDCP TX
    15 HDMI TX AUDIO
    16 STREAM
    17 DM RX
    18 DM TX
    19 SERIAL PORT
    20 DM MASTER
    21 DM SLAVE
    22 ETHERNET
    23 DMNET CEC
    24 SDI RX
    25 SCALER
    26 ANALOG TX
    27 OW RX
    28 OW TX
    29 VS RX
    30 VS TX
    31 OW POLL
    32 OW EDID
    33 OW HDCP
    34 OVERLAY HANDLER
    35 LVDS RX
    36 HDMI CEC
    37 AUDIO DAC
    38 FPGA
    39 ENCAPSULATION
    40 SWITCHER
    41 DP RX
    42 TOUCH
    43 CALTOUCH
    44 IR TX
    45 DM CONTROLLER
    46 SYSTEM STATS
    47 EXT TOOL EDID
    48 USB I
    49 VIDEO MSG HANDLER
    50 FRONT PANEL
    51 CNET MASTER
    52 LCD MANAGER
    53 INTERAPP
    54 TEST GEN
    55 TEST AMP
    56 CHANNEL MGR
    57 AVM MGR
    58 AVM CNET MGR
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    To disable all field debugs: FDEBUG OFF
    To enable all field debugs: FDEBUG ON
    
      
  
ENABLEFEature |  Enable/disable optional features  
      
    
    ENABLEFEATURE  [ON, OFF]
            FEATURE - Feature to be enabled/disabled or ALL
            ON - start feature when system boots
            OFF - do not start feature when system boots
            feature by itself shows current state for next boot
    
      
  
EPDEBUg |  EPDEBUG command.  
      
    
    DmEpDebugCmd fails read EPDEBUG, disable all
    To use debug Table: DEBUG [INDEX] [ON|OFF]
    
      
  
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
    
      
  
ESWDEBUG |  Ethernet switch debug commands  
      
    
            ESWDEBUG -R -- set rate limits on all ports
            ESWDEBUG -F[all] -- read FDB entry
            ESWDEBUG -F[n]   -- erase FDB per port
            ESWDEBUG -S[port/all] -W[state] -- read/write STP state
            ESWDEBUG -E               -- read all FEC registers
            ESWDEBUG -E[reg_name] -W[data] -- write one FEC register
            ESWDEBUG -X[port] -- read all registers from phy 8710
            ESWDEBUG -Y[port] -- read all registers from phy 88E1114
            ESWDEBUG -O[on/off/ ] -- enable/disable polling on FEC. no param for read
            ESWDEBUG -L[port] -- prints all PIRL registers per port
            ESWDEBUG -L[port] [engine] [reg] -W[data]-- writes one PIRL register
            ESWDEBUG -A[num]
            ESWDEBUG -D[num] - delay for PHY init
            ESWDEBUG -V[num] - value for PHY init
            ESWDEBUG -C      - read phy counter, number of attempts before link is up
    
      
  
ESWMAINT |  Ethernet switch test  
      
    
            ESWMAINT Command check ESW state
    
      
  
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
    
      
  
FDEBUG |  FDEBUG command.  
      
    
    To use field debug: FDEBUG [INDEX] [ON|OFF]
    01 HDMI RX
    02 HDMI TX
    03 ANALOG RX
    04 HDCP MAX DEVICE TEST
    05 CP VERIFICATION
    06 EDID
    07 CRESNET RX
    08 CRESNET TX
    09 HDMI RX AUDIO
    10 DSP
    11 HDMI FIBER
    12 USB
    13 HDCP RX
    14 HDCP TX
    15 HDMI TX AUDIO
    16 STREAM
    17 DM RX
    18 DM TX
    19 SERIAL PORT
    20 DM MASTER
    21 DM SLAVE
    22 ETHERNET
    23 DMNET CEC
    24 SDI RX
    25 SCALER
    26 ANALOG TX
    27 OW RX
    28 OW TX
    29 VS RX
    30 VS TX
    31 OW POLL
    32 OW EDID
    33 OW HDCP
    34 OVERLAY HANDLER
    35 LVDS RX
    36 HDMI CEC
    37 AUDIO DAC
    38 FPGA
    39 ENCAPSULATION
    40 SWITCHER
    41 DP RX
    42 TOUCH
    43 CALTOUCH
    44 IR TX
    45 DM CONTROLLER
    46 SYSTEM STATS
    47 EXT TOOL EDID
    48 USB I
    49 VIDEO MSG HANDLER
    50 FRONT PANEL
    51 CNET MASTER
    52 LCD MANAGER
    53 INTERAPP
    54 TEST GEN
    55 TEST AMP
    56 CHANNEL MGR
    57 AVM MGR
    58 AVM CNET MGR
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    (null)
    To disable all field debugs: FDEBUG OFF
    To enable all field debugs: FDEBUG ON
    
      
  
FGETfile |  Uses built-in (S)FTP/HTTP(S) client to transfer file from the server to ROM  
      
    
    FGETfile [url] [local_path] {username:password} {proxy}
            url - fully qualified URL to the file being downloaded from the server
            local_path - destination path to the file in the ROM
            username:password - optional access credentials to the server
            proxy - optional proxy in the form of url
    
      
  
FORCEDREBOOT |  Forces system reboot  
      
    
    FORCEDREBOOT - reboot system
    
      
  
FORMAT |  Format external memory card  
      
    
    FORMAT [index]
            index - index of the external removable memory disk to be formatted
                    (e.g. if index = 2, \RM2 will be formatted)
            if index not specified, \RM will be formatted.
    
      
  
FPUTfile |  Uses built-in (S)FTP/HTTP(S) client to transfer file from ROM to the server  
      
    
    FPUTfile [url] [local_path] {username:password} {proxy}
            url - fully qualified URL to the file being uploaded to the server
            local_path - path to the source file in the ROM
            username:password - optional access credentials to the server
            proxy - optional proxy in the form of url
    
      
  
FREE |  Show available file space  
      
    
    FREE - Indicates free disk space
    
      
  
GETAUDITLOG |  Retrieve the audit log.  
      
    
    No help available for this command.  
  
GETCODE |  Retrieve code needed for eControl2 activation  
      
    
    GETCODE
             Retrieves code needed for eControl2 activation.
    
      
  
GETIPTABLE |  Transfer the IP table from Internal flash  
      
    
    GETIPTABLE [program]
            program - which program the table is for (default = 1)
    
      
  
GETPAsswordrule |  Get password rules for local users  
      
    
    GETPASSWORDRULE
            No parameters needed.
    
      
  
HANDLEbadpacket |  AV manager Debug  
      
    
             Set Levels to handle packet contains only 0s
             HANDLEBADPACKET [value]
             value: 0: Do nothing
             value: 1: Log error only
             value: 2: Send Clear All command to ARM
             value: 3: Log error and send Clear All command to ARM
    
      
  
HARDWAREDEBUG |  HW debug command  
      
    
    [STREAM | ALL]
    
      
  
HARDWARETEST |  HW test command  
      
    
    Stream 1 - ChannelMgr: OK Stream 2 - ChannelMgr: OK
    
      
  
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
    
      
  
I2CTEST |  Read I2C device on the MFMSys Blade  
      
    
            I2CTEST No Arguments
            Tests all I2C devices
    
      
  
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
    
      
  
INTDEFROUT |  Set Flag Update/Not Default Gatewayin Internal LAN  
      
    
    
      
  
IPAddress |  Set IP address.  
      
    
    IPADDRESS [device_num ip_address]
            device_num - specified Ethernet device  [0 - 1]
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
    
      
  
IPMask |  Set IP Subnet Mask.  
      
    
    IPMASK [device_num ip_address]
            device_num - specified Ethernet device  [0 - 1]
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
      
    
    LISTDNSEX
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
  
LISTLOCKEDUsers |  List the locked user accounts  
      
    
    No help available for this command.  
  
LISTUSERS |  List of users authenticated on this system  
      
    
    No help available for this command.  
  
LOADIPTABle |  Load New IPTable  
      
    
    LOADIPTABLE -p:[AppId] [path]   Loads program specific DIP file from removable
            media to the internal \sys directory
            -P:Specific Program Identifier
            path - path on removable media including "\",
            e.g \RM\TmpDir or \RM2\dipDir
            Example: LOADIPTABLE -p:1 \RM\dipDir
            Note: program MUST be restarted for new IPTABLE to take effect
    
    
      
  
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
            LOGICDEBUG ACTLOGEVENTCOUNT {number}   (       5) - Number of events to pay attention to in the Logic Activity Logger
            LOGICDEBUG ACTLOGNOFILE ON|OFF         (     OFF) - Avoid dumping Logic Activity Logger to file on fault
            LOGICDEBUG ACTLOGPRIORITY {priority}   (      50) - Priority of the Logic Activity Logger
            LOGICDEBUG ACTLOGSCREEN ON|OFF         (     OFF) - Dump Logic Activity Logger to Screen on fault
            LOGICDEBUG ACTLOGSIZE {number}         (       0) - Size of the Logic Activity Logger
            LOGICDEBUG ALL ON|OFF                             - Turn on/off all of the above.
            LOGICDEBUG ANSKEDDER ON|OFF            (     OFF) - Analog Event Scheduler info
            LOGICDEBUG APPTOCLOUDTIMEOUT {time}    (   10000) - App To Cloud Timeout in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG APPTOTLDMTIMEOUT {time}     (   32000) - App To TLDM Timeout in App registration message in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG BACNETSTOPPEDTIMEOUT {time} (      15) - Overall timeout for Bacnet to complete stop, in min.
            LOGICDEBUG BACNETSTOPPINGHBEAT {time}  (    4500) - Dot print timeout while waiting for Bacnet to complete stop, in ms.
                                                                (Keep to 5000 or under to keep toolbox happy)
            LOGICDEBUG BUILDIFOFFLINE ON|OFF       (     OFF) - Ignore m_uiOnlineState when building packet
            LOGICDEBUG CLOUDINFO ON|OFF            (     OFF) - Info going to the Cloud
            LOGICDEBUG CLOUDTOAPPTIMEOUT {time}    (   10000) - Cloud To App Timeout in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG CONTIMEOUT {time}           (    2000) - General console write timeout for logic in ms (not for DBGSIGNAL/MDBGSIGNAL).
            LOGICDEBUG LGC ON|OFF                             - Turn on/off LOGIC, SYMPROC, SYMSIGPROC.
            LOGICDEBUG LOGIC ON|OFF                (     OFF) - Logic info
            LOGICDEBUG LOGICTOSPLUSQDEPTH {size}   (      50) - Depth of Logic to SIMPL+ Queue
            LOGICDEBUG MAXTRANSPERWAVE {size}      (   20000) - Number of Signal transitions per wave
            LOGICDEBUG MAXWAVESINSOLUTION {size}   (    1500) - Number of Waves per Logic Solution
            LOGICDEBUG MEMTRACK ON|OFF             (     OFF) - Memory Size Tracking
            LOGICDEBUG MSQTIME {size}              (      10) - Min Time needed to print the Multi Step Queue Solution time
            LOGICDEBUG PAGEUPDATE ON|OFF           (     OFF) - Show info about Page update requests
            LOGICDEBUG RCBCHECK {size}             (       4) - Set the number of passes before servicing analogs in the scheduler
            LOGICDEBUG REGTIMEOUT {time}           (  100000) - Timeout for Registration Event in ms
            LOGICDEBUG REPORTNODES {size}          (      10) - Report if more than this number loopnodes exceeded
                                                                before servicing scheduler
            LOGICDEBUG RMLTIME {size}              (      10) - Min Time needed to print the Run Main Loop time
            LOGICDEBUG SCHEDNODES {size}           (     200) - Number of Loopnodes in the Scheduler
            LOGICDEBUG SENDTOTLDMTIMEOUT {time}    (   10000) - Timeout for SendMessageToTLDMEx() in ms
            LOGICDEBUG SHOWBOOT ON|OFF             (     OFF) - Show extended logic startup/shutdown info
            LOGICDEBUG SHOWMSQTIME ON|OFF          (     OFF) - Show time for Multi Step Queue Solution
            LOGICDEBUG SHOWREG ON|OFF              (     OFF) - Show extended registration info
            LOGICDEBUG SHOWRMLTIME ON|OFF          (     OFF) - Show time between Run Main Loop
            LOGICDEBUG SHOWSIQTIME ON|OFF          (     OFF) - Show time for Symbol Input Queue Solution
            LOGICDEBUG SHOWSSQTIME ON|OFF          (     OFF) - Show time for Single Step Queue Solution
            LOGICDEBUG SIGMEMTRK ON|OFF            (     OFF) - Memory Size Tracking
            LOGICDEBUG SIQTIME {size}              (      10) - Min Time needed to print the Symbol Input Queue Solution time
            LOGICDEBUG SKEDDER ON|OFF              (     OFF) - Event Scheduler info
            LOGICDEBUG SPLUSTOLOGICQDEPTH {size}   (     100) - Depth of SIMPL+ to Logic Queue
            LOGICDEBUG SPLUSQUEUEDEPTH {size}      (     250) - Depth of SIMPL+ Symbol Input Queue
            LOGICDEBUG SSQTIME {size}              (      10) - Min Time needed to print the Single Step Queue Solution time
            LOGICDEBUG SYMPROC ON|OFF              (     OFF) - Show Symbols as Processed
            LOGICDEBUG SYMBOLQUEADDTIMEOUT {time}  (   32000) - Timeout for adding to a Symbol's Queue from TLDM Rx (also single/multi queue timeout).
            LOGICDEBUG SYMQUEUEDEPTH {size}        (     250) - Depth of the Symbol Input Queue
            LOGICDEBUG SYMSIGPROC ON|OFF           (     OFF) - Show signals changed for symbols being processed
            LOGICDEBUG TIMEREPORT {size}           (      10) - Set the number of ms required to pass before posting the time
                                                                to execute RunLoopNodeCheck()
            LOGICDEBUG TLDMTOAPPTIMEOUT {time}     (   32000) - TLDM To App Timeout in App registration message in ms.
                                                                Specifying INFINITE for time yields an infinite timeout
            LOGICDEBUG TRANSIENTHEAP {size}        (  102400) - Transient Heap Size in bytes
            LOGICDEBUG TXTIME ON|OFF               (     OFF) - Show time before/after packet transmission to driver
            LOGICDEBUG UPREQ ON|OFF                (     OFF) - Debug update request
            LOGICDEBUG VALIDATESKED ON|OFF         (     N/A) - Validate Scheduler Nodes (Requires Custom Firmware)
            LOGICDEBUG WAVETIMING ON|OFF           (     OFF) - Logic Wave Timing.
    
    
      
  
LOGMESSage |  (*) Write a message to the log from the console  
      
    
    LOGMESSAGE[:program#] {DEBUGLEVEL} {MESSAGE}
            Write a message to the log from the console
            program#: number of program to execute. (default=1)
            DEBUGLEVEL (expected range 1-10).
            MESSAGE - String to write to log.
    
      
  
LOGOFF |  Logs the currently authenticated user out of the system  
      
    
    Logs the currently authenticated user out of the system  
  
MAKEDIR |  Create a Directory  
      
    
    MAKEDIR directory
            directory - string containing directory specification
    
      
  
MDBGSIGnal |  (*) Set/View Debug flags and signal values  
      
    
    MDBGSIGNAL[:program#] {Parameters}
            program#: number of program to execute. (default=1)
            MDBGSIGNAL -R                   - Turn off all debug flags (Global, Signal specific, and Ignore)
            MDBGSIGNAL -A:ON                - Turn on Global debug flag
            MDBGSIGNAL -A:OFF               - Turn off Global debug flag
            MDBGSIGNAL -A:SHOW              - Show global & signal debug status
            MDBGSIGNAL -A:SYNC              - Write values of non-zero digital & analog signals, non-transient serial strings
            MDBGSIGNAL -TO:TimeInMs         - Console write timeout in ms [currently 2000 ms]
            MDBGSIGNAL -S:ON {signum(s)}    - Turn on signal-specific debug flag for signal {signum}
            MDBGSIGNAL -S:OFF {signum(s)}   - Turn off signal-specific debug flag for signal {signum}
            MDBGSIGNAL -S:SHOW {signum(s)}  - Show status of signal-specific debug flag & ignore flag for signal {signum}
            MDBGSIGNAL -S:SYNC {signum(s)}  - Show value of signal {signum}
            MDBGSIGNAL -I:ON {signum(s)}    - Turn on ignore-global debug flag for signal {signum}
            MDBGSIGNAL -I:OFF {signum(s)}   - Turn off ignore-global debug flag for signal {signum}
              {signum(s)} is a single Hex number (i.e. 0x0014) or a decimal number (i.e. 20) or
              a list of space seperated numbers.  To specify a range, put two signum(s) separated by a colon
              i.e. 0x14:0x20 would perform the operation for signals 0x14 through 0x20 inclusive.
              Multiple single numbers and multiple ranges are allowed.
            Current Console Transaction ID: 0x00000000
    
      
  
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
    
      
  
NETSTAT |  Displays protocol statistics and current TCP/IP network connections  
      
    
    usage : netstat
        ?    Display this help message.
     The default is to displays all connections and listening ports.
    
      
  
NETSTAT_DM |  Network Statistic  
      
    
            NETSTAT_DM prints statistic per windowsCE port
            NETSTAT_DM [port-name]
            NETSTAT_DM -P -- prints all ports in the system
    
      
  
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
    
    
      
  
PASSTORCON |  PASSTORCON command  
      
    
             DMRCON all [slot decSlot][.subslot hexSlot..] [command string]
    
      
  
PAUSEPROGram |  Pauses Specified Program  
      
    
     PAUSEPROGRAM {-P:ALL | -P:Specific Program Identifier}
             -P:  Pause a specific program or ALL.  If not present, ALL assumed.
    
    
      
  
PERSISTENTLOG |  Start PersistentLog on system boot  
      
    
    PersistentLog [ON, OFF]
            ON - Start PersistentLog on system bootup
            OFF - Do not start PersistentLog on system bootup
            No arguments - Shows current state
    
      
  
PHYOPER |  Operates on 88E1114 PHY  
      
    
            PHYOPER -Lon/off/read -- set on/off link status polling
    
      
  
PING |  Ping Remote Node  
      
    
    Usage: ping [-ncount] [-iTTL] [-vTOS] [-wtimeout] address
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
    Attention: This command has no space between option and option parameter.
    
    
      
  
PORTDUMP |  Dumps all registers related to the port of switch  
      
    
            PORTDUMP[portNumber]
            Dump all port related registers
    
      
  
PORTMIB |  Print port MIBs  
      
    
            PORTMIB [port]
            Print port MIBs
    
      
  
PORTPHYSET |  Set 88E1114 PHY for 100M/1G link  
      
    
            PORTPHYSET [portNumber] [1G or 100M]
            Set external PHY 88E1114 for 1G or 100M link
    
      
  
PORTSTATE |  Print port state  
      
    
            PORTSTATE [portNumber/all]
            Print port or all ports state
    
      
  
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
             -P:  Reset a specific program or ALL.  If not present, ALL assumed..
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
    
      
  
PUSHUPDATE |  Update Main, Blades, and attached Endpoints  
      
    
    Command:  ? :
    PushUpdate Version 1.3.1.1, Built Thursday, May 20, 2021 at 1:48:45 PM
    SmartUpdatePortable Built Thursday, May 20, 2021 at 1:45:27 PM
    Usage: PushUpdate [UNZIP|TEST|RESUME|FULL|LASTREPORT|PARAMS|CANCEL]
             no options - prints this help
             UNZIP = upzips update files
             TEST = prints updates that will be performed
             RESUME = performs updates previously printed by TEST
             FULL = equivalent to running TEST and RESUME
             LASTREPORT = prints most recent human readable update report
             PARAMS = prints parameter info (such as registry-configurable settings)
             CANCEL = safely cancels an update in progress
    Usage: PushUpdate ATOMIC [method] [filename] [ip]
             Performs atomic update.
             method = Atomic update method, such as EndpointFirmware
             filename = Name of desired file. Must be in extracted path
             ip = IP address of target host
    Usage: PushUpdate REPORTDM [ON|OFF]
             Enables or disables use of REPORTDM to accelerate version recon.
    Usage: PushUpdate VERALL [ON|OFF]
             Enables or disables use of VERALL feature to allow advanced application upgrades (LogosDebug).
    
      
  
RAMFree |  Show available RAM file space  
      
    
    RAMFREE
            no parameters needed
    
    

