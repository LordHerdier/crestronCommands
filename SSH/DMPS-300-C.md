# Commandset for the DMPS-300-C

> DMPS-300-C Cntrl Eng [v4.007.0032 (Oct 16 2013), #008D7598]
>
> 114 normal commands found. 103 hidden commands available.

ADDDns |  Add an entry to DNS server List  
---|---  
      
    
    ADDDNS ip_address
            ip_address - IP address in dot decimal notation
    
      
  
ADDSlave |  Add a slave/peer entry to IP table  
      
    
    Format: ADDSlave cip_id ip_address/name [device_id] [port number]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            device_id       - ID in device redirection table (in hex) (must be < 256)
            port number     - port number for the connection (in dec) (must be > 256)
    
      
  
AUTODIScovery |  Commands for Ethernet auto discovery  
      
    
    AUTODISCOVERY [ON | OFF | QUERY | LIST | HOSTS | LIGHTBYIP ipaddress | LIGHTBYTYPE type | STOPLIGHT | SETNEXTID id | SQUAWK | SETHOSTNAME ipaddress
    hostname | CLEARBYIP ipaddress | CLEARBYTYPE type | FORCEBYTYPE type]
            on : enables autodiscovery functions
            off : disables autodiscovery functions
            query : runs the discovery query
            list : displays the list of nodes discovered
            hosts : displays the list of hostnames
            lightbyip : puts in the device at the specified IP address into light-n-poll mode.
            lightbytype : puts in the devices of the specified type into light-n-poll mode.
            stoplight : removes all devices from light-n-poll mode.
            setnextid : indicates that the next ID to set is id.  Entered in hex.
            squawk : simulates pressing the SW-R button in light and poll mode.
            sethostname: assigned the given hostname to the device at specified ip address.
            clearbyip : clears the IP table in the device at the specified IP address.
            clearbytype : clears the IP table in the devices of the specified type.
            forcebytype : force the device of the specified type to the previous chosen ID.
    
      
  
AUTONEGot |  Set auto negotiation for Ethernet Device  
      
    
    AUTONEGOT [device_num (ON | 10HALF | 10FULL | 100HALF | 100FULL)]
            device_num - number of device to set (0 or 1)
            ON - autonegotiation is ON
            10HALF - autonegotiation is OFF, use 10mps, half duplex.
            10FULL - autonegotiation is OFF, use 10mps, full duplex.
            100HALF - autonegotiation is OFF, use 100mps, half duplex.
            100FULL - autonegotiation is OFF, use 100mps, full duplex.
            No parameter - displays current setting
    
      
  
BROADcast |  Enable/disable broadcasting of errors  
      
    
    BROADCAST [ON | OFF]
            No parameter - displays current setting
    
      
  
BYE |  Close user session.  
      
    
    BYE
            No parameter
    
      
  
CARDS |  Display Cards Detected in System  
      
    
    CARDS
            -FORCE - rescan internal plug-in cards
    
      
  
CD |  Change current file directory.  
      
    
    CD [directory]
            directory - string containing directory specification
            No parameter - display current setting
    
      
  
CHKENTRY |  Print the instances of a Simpl+ module.  
      
    
    CHKENTRY modulename
            module - name of the Simpl+ module of interest.
    
      
  
CIPPORT |  Set port number for CIP.  
      
    
    CIPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current setting
    
      
  
CLEARerr |  Clears the current error log  
      
    
    CLEARERR -L
            -L:  Clear Error LED only.  If not specified, clears the error log.
    
      
  
COMPACT |  Remove invalid files from system  
      
    
    COMPACT
            No parameters
    
      
  
CONFIGTag |  [tag# 1-9] [value 0-65535]  
      
    
    1 0
    2 0
    3 0
    4 0
    5 0
    6 0
    7 0
    8 0
    9 0
    
      
  
COPYfile |  Copy a file to a different directory  
      
    
    COPYFILE sourcespec destspec
            sourcespec - source file name specification (could be relative to current dir)
            destspec - destination file name specification (could be relative to current dir)
            filenames with embedded spaces must be enclosed in double quotes("The File")
      
  
CREATECsr |  Generate a CSR  
      
    
    CREATECSR       CN:SN:LN:ON:OUN:SN:EA:
            where CN = 2 letter country code
            where SN = Full state or province name
            where LN = Locality or city name
            where ON = Organization or company name
            where OUN= Organizational Unit name or division
            where SN = site name or domain name
            where EA = Email address
    
      
  
CRESNETSTAtictis |  Report Cresnet Stats  
      
    
    Valid options are:
     SHOW - Show Stats Once
     RESet - Reset Stats
     STARt - Start Stats
     STOP - Stop Stats
     INCrement - Incremental diff
     ACCumulate - Accumulate
     LEG - Stats by Leg
     ID - Stats by Cnet ID
     PERiod - Update period in sec
       Status if no arguments
    
      
  
CTPPORT |  Set port number for CTP (console).  
      
    
    CTPPORT [portnumber]
            portnumber - desired port number > 4095 (in decimal).
            No parameter - displays current setting
    
      
  
CYCLEPOWER |  Cycle power to backplane  
      
    
    CYCLEPOWER
            No parameter needed - cycles 24V to the backplane.
    
      
  
DBGDEVice |  Simulate incoming packets for the selected device  
      
    
    DBGDEVICE {Parameters}
            DBGDEVICE {devnum} {packet}   - Simulate an incoming packet {packet} for device {devnum}
              {devnum} is a Hex number (i.e. 0x0014) or a decimal number (i.e. 20)
              {packet} is a Quoted string representation of a packet without an ID or count
                    (i.e. "\x00\x01\x80" represents a digital low for join 1)
    
      
  
DBGPKTRX |  Show/hide all packets received by the device symbol layer.  
      
    
    DBGPKTRX {Parameters}
            DBGPKTTX ON|OFF [C|S|E|All [ID]] - Show/Hide packets received by the device symbol layer.
            C|S|E|All:  From Cresnet, Slot, Ethernet, All
            ID:         ID, All if none specified.  May be entered as 0x## or ##
    
            Current Status:  OFF
    
      
  
DBGPKTTX |  Show/hide all packets sent by the device symbol layer.  
      
    
    DBGPKTTX {Parameters}
            DBGPKTTX ON|OFF [C|S|E|All [ID]] - Show/Hide packets sent by the device symbol layer.
            C|S|E|All:  To Cresnet, Slot, Ethernet, All
            ID:         ID, All if none specified.  May be entered as 0x## or ##
    
            Current Status:  OFF
    
      
  
DBGSIGnal |  Sets or clears Debug flag for signal processing  
      
    
    Sets or clears Debug flag for signal processing  
  
DBGTRANSMITTER |  (*) Sets or clears Debug flag for IR/RF Transmitter  
      
    
    Sets or clears Debug flag for IR/RF TransmitterCustomizable help. See the text file donotexec.upc  
  
DEBug |  Set/View run-time debug options  
      
    
    Valid options are:
     CHOST - Cnet Host Wait time
     AUDIO - set MP2 equalizer/codec
     CONsole - via current console
     COMport - via built-in serial
            syntax: com A-F [<baud>]
     MAIn - via main serial
     TCP - via tcp <port>
     DISable - all debugs OFF
     ASCII -  ASCII only
     MIXED -  ASCII and hex
     HEX_ONLy -  hex, no ACSII
     HEX -  hex with space
     NO_ZERoes -  skip zeroes
     ALL_HEX -  all hexadecimal
     SER_DATa -  serial data only
     SINGLe_id - single cresnet ID
     POLL - poll one ID # of times
            syntax: poll [ID [#times]|[ON|OFF]
     POWERUP - powerup ON|OFF
     ON - all or powerup
     OFF - all or powerup
     SAVE - save in EEPROM
     Gtest - gtest calls->
     LEVel - set debug level(0-3)
            syntax: debug # ON|OFF [lev #]
     DIRECT - direct printing
     INPut - debug port console
            syntax: debug input ON|OFF
     USB - via usb console
     HELP - show levels bitmap
       Status if no arguments
    
     #0 bitmap:
    
    To use debug:
       - enable debug output: DEBUG [CONSOLE|COMPORT|MAIN|USB]
          if using comport specify port and baud: DEBUG COM C 115200
       - specify what to debug(run DEBUG with no parameters for opt#): DEBUG opt# [ON|OFF]
       - to kill all debugs: DEBUG OFF
       - to restore or clear settings after powerup(does autosave): DEBUG POWERUP [ON|OFF]
       - to save manually debug conf(DEBUG OFF does not autosave): DEBUG SAVE
    
      
  
DEFRouter |  Set default router.  
      
    
    DEFROUTER [device_num ip_address]
            device_num - specified Ethernet device [0,1]
            ip_address - IP address in dot decimal notation
            No parameter - displays current value
    
      
  
DELete |  Delete file(s)  
      
    
    DELETE filesearchstring
            filesearchstring - search string which may contain wildcards
    
      
  
DHCP |  Enable/disable dynamic IP addressing  
      
    
    DHCP [ON | OFF | REL_RENEW]
            ON - enables DHCP for LAN A
            OFF - disables DHCP for LAN A
            REL_RENEW - performs a DHCP release and renew
            No parameter - displays current setting
    
      
  
DHCPOPT |  Sets DHCP Server Options  
      
    
    DHCPOPT [HOSTNAME | FQDN]
            HOSTNAME - Send LocalHostName in DHCP Discover Request - Default Option.
            FQDN - Send the Fully Qualified Domain Name in DHCP Discover Request.
            No parameter - displays current setting
    
      
  
DIR |  File(s) directory  
      
    
    DIR filesearchstring
            filesearchstring - search string which may contain wildcards
    
      
  
DOMAinname |  Set the domain name for DNS environment  
      
    
    DOMAINNAME [string | /CLEAR ]
            string - ASCII string containing domain name
            /CLEAR - clears the value
            No parameter - current value
    
      
  
DSTSTATus |  Current EEPROM DST Setting  
      
    
    EEPROM DST Status: 1
    
      
  
ECHo |  Enable/disable character echoing  
      
    
    ECHO [ON | OFF]
            No parameter - displays current setting
    
      
  
EEprom |  Displays the parameters stored in EEPROM  
      
    
    EEPROM
            No parameter needed
    
      
  
ENTRYpts |  Print Simpl+ Modules in program.  
      
    
    ENTRYPTS {-I}
            -I:  Show associated instances.
    
      
  
EPTEST |  Destructive EEPROM Test  
      
    
    EPTEST
            No parameter needed
    
      
  
ERRlog |  Prints the current error log  
      
    
    ERRLOG [NOTICE | WARNING | ERROR | FATAL]
            NOTICE - print all notices and above (default)
            WARNING - print all warnings and above
            ERROR - print all errors and above
            FATAL - print all fatal errors and above
    
      
  
ESTatus |  Display the status of the Ethernet  
      
    
    ESTATUS
            No parameter needed
    
      
  
ETHERNET |  Enable/disable Ethernet  
      
    
    ETHERNET [ON | OFF]
            No parameter - displays current setting
    
      
  
ETHERTEST |  Start Ethernet test  
      
    
    Command Blocked from this console type.
      
  
ETHWdog |  Enable/disable Ethernet Watchdog  
      
    
    ETHWDOG [ON/OFF]
    
      
  
ETYpefilt |  Filter packets based on ethernet type field  
      
    
    
    
      
  
FANcontrol |  Set/Show Fan Controls  
      
    
     Syntax: Fan [command] [value] [noSave]
      available commands:
     Set           [degrees C]
     Time          [sec]
     Proportional  [float]
     Integral      [float]
     Derivative    [float]
     ? - this help
    
      
  
FILECHECK |  Perform an integrity test on the file system  
      
    
    FILECHECK [/NVRAM]
            No parameter - performs a flash file system check
            /NVRAM - performs a NVRAM file system check
    
      
  
FILEUPLOAd |  Load from file system into internal device  
      
    
    Syntax: [CODE|DATA(default)] [SLOT|CNET(default)] ID_OR_SLOT_NUM FILE_NAME_STR
    
      
  
FLASHTEST |  Show available file space  
      
    
    FLASHTEST [loops]
            loops - numbers of times through the chip
            No parameter needed - performs one loop of the check on second flash chip
    
      
  
FORCEDREBOOT |  Forces system reboot  
      
    
    FORCEDREBOOT [-c] - reboot system
            No parameters
      
  
FPPASSWORD |  Set front panel password.  
      
    
    FPPASSWORD [password]
            password - numerical string using digits (1-6)
            No parameter - current setting
    
      
  
FREE |  Show available file space  
      
    
    FREE
            No parameter needed
    
      
  
GETCODE |  Retrieve code needed for eControl2 activation  
      
    
    GETCODE
    
    
      
  
GETIPTABLE |  Transfer the IP table from Internal flash  
      
    
    GETIPTABLE
            no parameters.
    
      
  
GMToffset |  Set/View the system GMT Offset  
      
    
    GMTOFFSET {value}
            {value} is the GMT Offset in Minutes, from -720 to 780
            Current GMT Offset is 0
    
      
  
GTEst |  Run various driver tests  
      
    
    This command runs Gennady's routines test
    
      
  
HEAPfree |  Show available heap space  
      
    
    HEAPFREE [Max|#num]
            Max - find Maximum contiguous free block
            #num - allocate block of this size
    
      
  
HELP |  Display help screens  
      
    
    HELP - Detailed help available.  Type a command followed by
           a space and '?' to see options for that command
           (i.e. HELP ?)
    HELP ALL will display a list of all commands.
    HELP DEVice will display a list of cmds specific to this device.
    HELP ETHERnet will display a list of Ethernet commands.
    HELP FILE will display a list of commands for file operations.
    HELP SYStem will display a list of general system commands.
    HELP xxx* will display a list of commands starting with xxx.
    
      
  
HOSTname |  Set the host name for DNS environment  
      
    
    HOSTNAME [string | /CLEAR ]
            string - ASCII string containing host name
            /CLEAR - clears the value
            No parameter - current value
    
      
  
I2CERRor |  Enable I2C error reporting  
      
    
    I2CERROR [OFF | ON ]
            No parameter - displays current setting
    
      
  
I2CTEST |  Run a test of the I2C bus  
      
    
    I2CTEST count
            count - number of times to run the test
    
      
  
ICMP |  Enable/disable ICMP ping  
      
    
    ICMP [ON | OFF]
            No parameter - displays current setting
    
      
  
IDNUMber |    
      
    
            No parameter - displays current setting
    
      
  
INFO |  Print Software Capabilities  
      
    
    INFO
            No parameters
    
      
  
INITIALIZE |  Clear file system  
      
    
    INITIALIZE
            No parameters
    
      
  
INTSENDCNETPKT |  Send a Cresnet Packet to Internal Cresnet  
      
    
    INTSENDCNETPKT {Parameters}
    INTSENDCNETPKT {data (w/o count)}   - Send a Cresnet packet to the internal Cresnet.
            data is a string of 2-digit hex bytes.
            For example: "INTSENDCNETPKT 03000000\r" sends a digital high to join 1 on ID 3.
      
  
IPAddress |  Set IP address.  
      
    
    IPADDRESS [device_num ip_address]
            device_num - specified Ethernet device [0,1]
            ip_address - IP address in dot decimal notation
            No parameter - displays current value
    
      
  
IPMask |  Set IP subnet mask.  
      
    
    IPMASK [device_num ip_address]
            device_num - specified Ethernet device [0,1]
            ip_address - IP address in dot decimal notation
            No parameter - displays current value
    
      
  
IPTable |  Display IP table.  
      
    
    IPTABLE [-I:ID]
            -I:ID:  ID to display entry for
            No Arguments shows entire IP Table
    
      
  
ISDIR |  Check to see if path is a directory.  
      
    
    ISDIR directory
            directory - string containing directory specification
    
      
  
ISTAT |  Check Internal Status of Program  
      
    
    ISTAT {Parameters}
            ISTAT SIG                   - Show internal status on signals.
            ISTAT PROG [-Q]             - Show internal status on program, /Q=Do Not List Symbols
            ISTAT SYM {number}          - Show internal status of specified symbol
            ISTAT DEV                   - Show devices in system only.
            ISTAT REGDEV                - Show successfully registered devices in system only.
            ISTAT LIST {number}         - List all occurances of compiler code {number} in the program.
            ISTAT SHOWDEBUG {number}    - Show Debug Info for symbol {number} in the program.
            ISTAT SYMQUE                - Show number of entries in symbol input queue for devices that have them.
            ISTAT PSTRINGS              - Show size of each perm. string & total space for all fixed strings.
            ISTAT SPLUS {TASKSTAT name} - Show SIMPL Windows S# for the given SIMPL+ TASKSTAT taskname
            ISTAT WAVELIST                   - Show last 0 symbols processed
                    (Use LOGICDEBUG WAVESTORE command to change size)
    
      
  
JOINGETINANalog |  Read Analog Input Joins to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETINDIgital |  Read Digital Input Joins to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETINSErial |  Read Serial Input Joins to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#
    
      
  
JOINGETINTparam |  Read Integer Params to Console  
      
    
    Direct signal read
        syntax:   [type] Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETOUTANalog |  Read Analog Output Joins to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETOUTDIgital |  Read Digital Output Joins to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINGETOUTSErial |  Read Serial Output Joins to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#
    
      
  
JOINGETSERparam |  Read Serial Params to Console  
      
    
    Direct signal read
        syntax:   Xact# slot#[.subslot#...] join#1...[join#N]
    
      
  
JOINMONITORSlot |  Start/Stop TJI monitor  
      
    
    Total devices 0 (Max 32)
    # :   Idx   xAction  state  Slot
    -----------------------------------
    
      
  
JOINSETANalog |  Set Analog Joins from Console  
      
    
    Direct signal write
       syntax: [type] slot#[.subslot#...] join#1=val#1 ...[join#N=val#N]
    
      
  
JOINSETDIgital |  Set Digital Joins from Console  
      
    
    Direct signal write
       syntax: slot#[.subslot#...] join#1=val#1 ...[join#N=val#N]
    
      
  
JOINSETINTparam |  Send Integer Parameter from Console  
      
    
    Direct signal write
       syntax:  [type] slot#[.subslot#...] param#1=val#1 ...[param#N=val#N]
    
      
  
JOINSETPAcket |  Send Any Packet from Console  
      
    
    Direct signal write
       syntax: slot#[.subslot#...] ["[ASCII_string]] | [hex_byte_1...hex_byte_N]
    
      
  
JOINSETSERParam |  Send Serial Parameter from Console  
      
    
    Direct signal write
       syntax: slot#[.subslot#...] param# ["[ASCII_string]]  | [hex_byte_1...hex_byte_N]
    
      
  
JOINSETSErial |  Send Any Packet from Console  
      
    
    Direct signal write
       syntax: [type] slot#[.subslot#...] ["[ASCII_string]] | [hex_byte_1...hex_byte_N]
    
      
  
KILLPROGram |  Remove the current program from the system and restart the control system  
      
    
    KILLPROGRAM [CURRENT | INTERNAL | CF | BOTH]
            CURRENT - kill program currently running
            INTERNAL - kill program stored in internal flash memory
            CF - kill program stored in compact flash memory
            BOTH - kill program stored in both internal and compact flash memory
            No arguments - default to current
    
      
  
KILLSOCKET |  Cancel an active TCP console socket  
      
    
    KILLSOCKET [CTP1 | CTP2 | TELNET1 | TELNET2 | SCTP1 | SCTP2]
            CTP1 - kill the first CTP console
            CTP2 - kill the second CTP console
            TELNET1 - kill the first Telnet console
            TELNET2 - kill the second Telnet console
            SCTP1 - kill the first secure CTP console
            SCTP2 - kill the second secure CTP console
    
      
  
LIGHTBYPPN |  start squack mode  
      
    
    Valid options are:
       Status if no arguments
    
    Syntax: LIGHTBYPPN [4 byte Hex Adr]|ALL
    
      
  
LISTDNS |  Display the list of DNS servers  
      
    
    LISTDNS
            no parameters needed
    
      
  
LISTENSTAT |  Generate a report of the Ethernet listen sockets  
      
    
    LISTENSTAT
            No parameter necessary
    
      
  
LOGICDebug |  Set Logic Debug Options  
      
    
    LOGICDEBUG {Parameters}
                                        Current State
            LOGICDEBUG LOGIC ON|OFF         ( OFF)        - Logic info
            LOGICDEBUG SKEDDER ON|OFF       ( OFF)        - Event Scheduler info
            LOGICDEBUG SYMPROC ON|OFF       ( OFF)        - Show Symbols as Processed
            LOGICDEBUG CLDL ON|OFF          ( OFF)        - CLDL info
            LOGICDEBUG MBUFFER ON|OFF       ( OFF)        - MBUFFER info
            LOGICDEBUG RAMP ON|OFF          ( OFF)        - RAMP info
            LOGICDEBUG TXTIME ON|OFF        ( OFF)        - Show time before/after packet transmission to driver
            LOGICDEBUG ABUFFER ON|OFF       ( OFF)        - ABUFFER info
            LOGICDEBUG SMEM ON|OFF          ( OFF)        - SMEM info
            LOGICDEBUG PRESETV ON|OFF       ( OFF)        - PRESETV info
            LOGICDEBUG MMCLAMP ON|OFF       ( OFF)        - MMCLAMP info
            LOGICDEBUG MMSCALER ON|OFF      ( OFF)        - MMSCALER info
            LOGICDEBUG MSLAVE ON|OFF        ( OFF)        - MasterSlave symbol info
            LOGICDEBUG SYMSIGPROC ON|OFF    ( OFF)        - Show signals changed for symbols being processed
    
            LOGICDEBUG CLOCKDRIVER ON|OFF   ( OFF)        - Clock Driver Debug
            LOGICDEBUG UPREQ ON|OFF         ( OFF)        - Debug update request
            LOGICDEBUG WAVEDUMP ON|OFF      ( OFF)        - Dump WaveData after Wave Error
    
            LOGICDEBUG MEMTRACK ON|OFF      ( OFF)        - Memory Size Tracking
            LOGICDEBUG SIGMEMTRK ON|OFF     ( OFF)        - Memory Size Tracking
                    (System is NOT compiled with memory tracking - MEMTRACK, SIGMEMTRK are useless)
            LOGICDEBUG WAVESTORE {size}    (    0)        - Size of Logic Wave History
            LOGICDEBUG TRANPERWAVE {size}  (    0)        - Max Number of Transitions Per Wave
                    (Using Default of 9000 Transitions per wave)
    
            LOGICDEBUG ALL ON|OFF                         - Turn on/off all of the above.
            LOGICDEBUG LGC ON|OFF                         - Turn on/off LOGIC, SYMPROC, SYMSIGPROC.
    
      
  
MDBGSIGnal |  Sets or clears Debug flag for signal processing  
      
    
    Sets or clears Debug flag for signal processing  
  
MEMCheck |  Run memory check on heap.  
      
    
    MEMCHECK
            no parameters needed
    
      
  
MEMFrag |  Show Holes in memory heap.  
      
    
    MEMFRAG {arguments}
            -l:  Show list format
            -g{:clustersize}:  Graphical format.  Default clustersize of 10240 bytes.
            No Arguments is equivalent to -g:10240.
    
      
  
MEMREAD |  Read physical memory.  
      
    
    MEMREAD [BYTE | WORD | LONG] address [length]
            [BYTE | WORD | LONG] - memory access type (default to LONG)
            address    - the address for the memory access
            [length]   - number of elements to show
    
      
  
MEMREport |  Report Memory Statistics.  
      
    
    MEMREPORT Command not implemented in this version.
    
      
  
MEMWRITE |  Write physical memory.  
      
    
    MEMWRITE [BYTE | WORD | LONG] address data
            [BYTE | WORD | LONG] - memory access type (default to LONG)
            address    - the address for the memory access
            data       - hex numbers representing the data separated by spaces
    
      
  
MESSage |  Display a message on the screen.  
      
    
    MESSAGE [string]
            string - ASCII string to display on screen
            No parameters - restore previous display
    
      
  
MODEMINITstring |  Change the default Modem initialization string.  
      
    
    MODEMINITSTRING "{init string}"
            {init string}:  String to send to modem.  64 characters Max.
            No Arguments:   Shows current init string
    
      
  
MOVEfile |  Move a file to a different directory  
      
    
    MOVEFILE sourcespec destspec
            sourcespec - source file name specification (could be relative to current dir)
            destspec - destination file name specification (could be relative to current dir)
            filenames with embedded spaces must be enclosed in double quotes("The File")
      
  
Main |  Help screen  
  

NVMEMSLOTANADump |  Dump NV Mem slot Analog Join Information  
  

NVMEMSLOTDIGDump |  Dump NV Mem slot Digital Join Information  
  

NVMEMSLOTINFO |  Dump NV Mem slot Information  
      
    
     NVMEMSLOTINFO
             Dumps out NVMem Slot Information
    
      
  
NVMEMSLOTINIT |  Initialize NVMem Slot  
      
    
     NVMEMSLOTNITialize
             Initializes the contents of the NVMemSlot. All data will be lost and Reboot will be required
    
      
  
NVMEMSLOTSERDump |  Dump NV Mem slot Serial Join Information  
  

NVRAMCLEAR |  Clear NVRAM with zeros  
      
    
    NVRAMCLEAR
            No parameter needed
    
      
  
NVRAMDISK |  Format NV RAM file system  
      
    
    NVRAMDISK [ parameter]
    where parameter is "OFF", "64K" or "128K"
            No parameter - displays current setting
    
      
  
NVRAMFILL |  Fill NVRAM with a known pattern  
      
    
    NVRAMFILL
            No parameter needed
    
      
  
NVRAMGET |  Retrieve the contents of NVRAM  
      
    
    NVRAMGET [parameter]
            where the optional "parameter" is either PROGRAM or DISK.
            NVRAMGET retrieves NVRAM program or disk area which is used.
    
      
  
NVRAMPUT |  Send the contents of NVRAM to the system  
      
    
    NVRAMPUT [parameter]
            where the optional "parameter" is either PROGRAM or DISK.
            NVRAMPUT retrieves NVRAM program or disk area which is used.
    
      
  
NVRAMREBOOT |  Use NVRAM to store the reboot message  
      
    
    NVRAMREBOOT [OFF | ON | SHOW]
            OFF - disable writing reboot messages to NVRAM
            ON - enable writing reboot messages to NVRAM
            SHOW - display the last reboot message in NVRAM
    
      
  
NVRAMTEST |  Destructive NVRAM Test  
      
    
    NVRAMTEST
            No parameter needed
    
      
  
OLDUSDST |  Reverts back to the old DST schedule for US  
      
    
    OLDUSDST [ON | OFF]
            No parameter - displays current setting
    
      
  
OPTION |  Set and display system options  
      
    
    Valid options are:
       Status if no arguments
     ADANTO - set name to ADANTO
            syntax: ADANTO [ON|OFF]
     MAX_CNEt_packet - set maximum Cnet length
            syntax: Max_Cnet 188
     BCAST_LIGHtnpoll - Bcast LnP Clr ON|OFF
     COM ERROR - Comports Err Reporting
            syntax: com [cons|logic ON|OFF]
     CONsole - Com Err to Console
            syntax: com console ON|OFF
     LOGic - Com Err to Logic
            syntax: com logic ON|OFF
     MSX uploads - MSX-like cresnet uploads
            syntax: MSX ON|OFF
     WAIT_After - Slow PRO2 cresnet
            syntax: Wait_after ON|OFF
     WAIT_Before - Slow PRO2 cresnet tx
            syntax: Wait_before ON|OFF
     SWAP_cnet - swap int and ext Cnets
            syntax: Swap ON|OFF
    
      
  
PACKET |  Create and send Cresnet packets  
      
    
    PACKET - Creates/Sends packets
            Syntax:  PACKET [-NC] [-SE | -SC | -SS] [-Fform] [-P] [-I{ID}] -[T{Type}] {Packet Specific Data}
    
            Options:
            -NC:  Do not clear character buffer before building
            -SE:  Send completed packet via main ethernet
            -SC:  Send completed packet via main cresnet
            -SS:  Send completed packet to slot
            -SLE: Simulate logic receiving a packet from an Ethernet Device
            -SLC: Simulate logic receiving a packet from a Cresnet Device
            -SLS: Simulate logic receiving a packet from a Slot
            -R"...": Build a raw packet from the contents of the string "..."
                       "\x" style sequences are legal.  COUNT byte is auto-computed (NTX style)
            -Fform:  Use Form "form" to build the packet.
            -P:  Print current buffer
            -I:  Device ID (or list for wrapping)
                 ex:  -I0xAA, -I15, -I0xAA.0xBB.0xCC (AA, BB are wrapped, CC is the inner packet)
            -T:  Packet Type
                 0x00 ("DIGITAL")    - Digital
                 0x01 ("ANALOG")     - Analog
                 0x02 ("PORTFORCE")  - Port Force
                 0x12 ("SERIAL")     - Serial
                 0x14 ("SYMANALOG")  - Symmetric Analog
                 0x1C ("GENCFG")     - Generic Device Config
                 0x1D ("CLXRCB")     - CLX RCB
                 0x1A ("ENGSLAVE")   - Engage Slave Mode
                 0x27 ("RPTDIGITAL") - Repeat Style Digital
                 ex:  -T0x01 or -T"ANALOG" to specify Analogtype.
            To get {Packet Specific Data}, do "PACKET -T{Type} ?"
    
      
  
PASSTHRU |  Enter passthru mode console<->device  
      
    
    Valid options are:
       any number allowed as argument
     CRESnet - cresnet device
     NPA - poll accelerator
     ETHERnet - CIP or Client/Serv
     SLOT - any sys slot
     COM - build-in com
     IR - one-way IR
     H/W - hardware handshake
     S/W - software handshake
     232 - RS232 mode
     422 - RS422 mode
     485 - RS485 mode
    
      
  
PASSTO |  Enter passto mode console<->device  
      
    
    Valid options are:
     CRESnet -  Passto Over Cresnet
     IPID -  Passto Over IP
     SLOT - plug-in card
     CONSole - console mode
     XPUT - xmodem xfer mode
     DATA - xmodem xfer mode
     UPLOad - device upgrade
     CODE - device upgrade
     SCreen - xmodem xfer mode
     FIrmware - device upgrade
        hex number allowed as argument
    
      
  
PASSWORD |  Set console password.  
      
    
    PASSWORD
            No parameters.  Respond to prompts
    
      
  
PAUSEPROGram |  Pauses the current program  
      
    
    PAUSEPROGRAM
            No arguments necessary.
    
      
  
PHYR |  Read PHY register  
      
    
    PHYR addr reg
            addr - address of the PHY chip (0 - 31)
            reg - selects which register to read
    
      
  
PHYSTATus |  Display PHY status  
      
    
    PHYSTATUS addr
            addr - address of the PHY chip (0 - 31)
    
      
  
PHYW |  Write PHY register  
      
    
    PHYW addr reg data
            addr - address of the PHY chip (0 - 31)
            reg - selects which register to read
            data - value (in hex) to write to register
    
      
  
PING |  Ping remote node.  
      
    
    PING ip_address
            ip_address - IP address in dot decimal notation
    
      
  
PPNDISCOVEr |  Show all PPN devices on cresnet  
      
    
    93.1 100.0 0 entries found
    
      
  
PROGCOMments |  Shows program "Comment" symbols  
      
    
    PROGCOMMENTS
            No arguments necessary.
    
      
  
PROGINFO |  Shows Program Statistics  
      
    
    PROGINFO {No arguments}
            Shows program information.
    
      
  
PROGREAdy |  Sends the program ready status  
      
    
    PROGREADY
            No parameter needed - displays current program ready status
    
      
  
PROGRESet |  Reloads and restarts the program  
      
    
    PROGRESET
            No arguments necessary.
    
      
  
PROGSTATs |  Show statistics on the current program  
      
    
    PROGSTATS
            No arguments necessary.
    
      
  
PROGUPTIME |  Display the time the program is running  
      
    
    PROGUPTIME
            no parameters needed
    
      
  
PROTINITIAlize |  Clear file system  
      
    
    PROTINITIALIZE
            No parameters
    
      
  
PROTSIZE |  Sets the size of the Protected Area in Flash  
      
    
    PROTSIZE size
            No parameter - displays current setting
    
      
  
RAMFree |  Show available RAM file space  
      
    
    RAMFREE
            No parameters
    
      
  
RANDOMIZEPPn |  randomize PPN slave devices  
      
    
    Valid options are:
       Status if no arguments
    
    Syntax: RANDOMIZEPPN [4 byte Hex Adr]|ALL [HEX cnet ID]
    
      
  
RCONsole |  Send Command to Remote console  
      
    
    rcon [cresnet hexID][.subslot hexID..]|[slot decSlot][.subslot hexID..] [command string]
    
      
  
REBOOT |  Perform system reboot  
      
    
    REBOOT [-c] - reboot system
            No parameters
      
  
REMDns |  Remove an entry to DNS server List  
      
    
    REMDNS ip_address
            ip_address - IP address in dot decimal notation
    
      
  
REMOVETBCLIENT |  Removes Console Client Configuration  
      
    
    REMOVETBCLIENT
            Removes console client configuration
    
      
  
REMSlave |  Remove a slave/peer entry from IP table  
      
    
    Format: REMSlave cip_id ip_address/name [device_id] [port number]
            cip_id - ID of the CIP node (in hex)
            ip_address/name - IP address in dot decimal notation
                            - or name of the site for DNS lookup
            device_id       - ID in device redirection table (in hex) (must be < 256)
            port number     - port number for the connection (in dec) (must be > 256)
    
      
  
REPORTCRESNET |  Show all devices on the main cresnet leg  
      
    
    Valid options are:
    
    Syntax: REPORTCRESNET [<HEX ID>]
    
      
  
REPORTPPNTABLe |  Displays Cresnet PPN table if available  
      
    
    Displays Cresnet PPN table if available  
  
RESTORe |  Restore factory defaults  
      
    
    RESTORE
            No parameter
    
      
  
RESUMEPROGram |  Resumes the current program  
      
    
    RESUMEPROGRAM
            No arguments necessary.
    
      
  
RI2C |  Read I2C strings  
      
    
    Usage: ri2c [adr] [sub] [dec num_bytes_to_read]
    
      
  
ROUTESYMSTAT |  Check Connection status of route symbols  
      
    
    ROUTESYMBOLSTATUS
            No Parameters Required.
            Shows connection status of route symbols in program.
    
      
  
RPRTCRESNETIDBYPPn |  Report cresnet ID by PPN  
      
    
    
    
      
  
RPRTPPNBYCRESNETId |  Report PPN by cresnet ID  
      
    
    
    
      
  
RTScts |  Set/clear HW handshaking  
      
    
    RTSCTS [ON | OFF]
            No parameter - displays current setting
    
      
  
SAVEPAram |  Save system paramters.  
      
    
    SAVE
            No parameter
    
      
  
SAVEPPNTABLe |  Save discovered devices  
      
    
    
    
      
  
SCHEDQOverflow |  Set/Clear Event Scheduler Queue Overflow Dump  
      
    
    SCHEDQOVERFLOW {-E:ON|OFF}
            No argument:  Show current setting
            ON:   Dump symbols enqueued if "Error: Que is Full: CEventSchedulerHelper::m_pSchedulerUpdateQue (0014:001F:0014)" happens
            OFF:  Turn off symbol dump on above error
    
      
  
SDEBUG |  Monitor packets to/from logic with options  
      
    
    SDEBUG arguments
    
            -D[ON|OFF]:  Set device to have it's debug info printed (ON) or not (OFF).  Followed by a space and:
              A  :  Turn on/off debug flag for all devices.
              C  :  Turn on/off debug flag for all top-level Cresnet devices.
              C##:  Turn on/off debug flag for Cresnet ID ##.
              E  :  Turn on/off debug flag for all top-level Ethernet devices.
              E##:  Turn on/off debug flag for Ethernet ID ##.
              S  :  Turn on/off debug flag for all top-level Slots.
              S##:  Turn on/off debug flag for Slot ##.
    
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
    
            -ST[ON|OFF] :  Show Time before packet
            -SD[ON|OFF] :  Show Date when Time is printed
    
            NOTE:  A device *MUST* be in the currently running program in order to be debugged!
    
      
  
SECURECIPport |  Set Secure(SSL) port number for CIP.  
      
    
    SECURECIPPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays current setting
    
      
  
SECURECTPport |  Set Secure(SSL) port number for CTP.  
      
    
    SECURECTPPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays current setting
    
      
  
SECUREWEBport |  Set Secure(SSL) port number for Web.  
      
    
    SECUREWEBPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays current setting
    
      
  
SELFTEST |  Initiate the self test procedure  
      
    
    Valid options are:
     SIlent - no screen output
     VERBose - show more info
     DEbug - show low-level info
     LOops - 0-nonstop,XXX-times
     SKIP - no button test
     COM6x - built-in COM
     CRESnet - built-in cresnet
     VERSiport - built-in IO
     FP - front panel
     SLOT - Plug-in Ybus slot
    
      
  
SENDCNETPKT |  Send a Cresnet Packet  
      
    
    SENDCNETPKT {Parameters}
            SENDCNETPKT {data (w/o count)}   - Send a Cresnet packet.
            data is a string of 2-digit hex bytes.
            For example: "SENDCNETPKT 03000000\r" sends a digital high to join 1 on ID 3.
      
  
SENDIPTABLE |  Transfer the IP table to Internal flash  
      
    
    SENDIPTABLE
            no parameters.
    
      
  
SENDKEY |  Add eControl2 Activation Key  
      
    
    SENDKEY [key]
    
      
  
SENDMAIL |  Send an e-mail  
      
    
    SENDMAIL from;to;[subject];[message]
    
      
  
SENDMODEMINITstring |  Turn on/off sending of Modem Init string at program startup.  
      
    
    SENDMODEMINITSTRING {ON|OFF}
            ON:   Sends the modem init string at startup.
            OFF:  Does not send the modem init string at startup.
            No Arguments:  Show current setting.
    
      
  
SERial |  Set serial comm parameters  
      
    
    SERIAL [baud,parity,databits,stopbits]
            baud - baud rate (300 - 460800) (in dec.)
            parity - single character representing parity (N,O,E)
            databits - number of data bits (5-8)
            stopbits - number of stop bits (1,2)
            No parameter - displays current setting
    
      
  
SETCRESNETIDBYPPn |  Set cresnet ID by PPN  
      
    
    Valid options are:
       Status if no arguments
    
    Syntax: SETCRESNETIDBYPPN [HEX cnet ID HEX 4-byte Address]|ALL
    
      
  
SETERRLOG |  Set ErrorLog to display/Ignore errors  
      
    
    SETERRLOG [LM63] [ON | OFF]
    ON: Report to Errlog
    OFF: Don't report to Errlog
    No parameter - displays current setting
    
      
  
SETPPNBYCRESNETId |  Set PPN by cresnet ID  
      
    
    Valid options are:
       Status if no arguments
    
    Syntax: SETPPNBYCRESNETID [HEX cnet ID] [4 byte Hex Adr]
    
      
  
SETPPNBYPPn |  Change old PPN to new PPN  
      
    
    Valid options are:
       Status if no arguments
    
    Syntax: SETPPNBYPPN [Hex OldAdr]|ALL [HEX NewAdr]
    
      
  
SETSIGnal |  Set the state of a signal in the program  
      
    
    SETSIGNAL signal_number value
            signal number - Hex Number (i.e. 0x0000000B) or Decimal number (i.e. 11)
            value         - 0 or 1 for Digital
                          - pXX : Pulse XX ms long for Digital
                          - iXX : Inverse pulse XX ms long for Digital
                          - 0 to 65535 for Analog
                          - Quoted string for Strings
    
      
  
SETTBCLIENTCONNFRVR |  Set Console Client to try and reconnect after a disconnect  
      
    
    SETTBCLIENTCONNFRVR [ON|OFF]
            Sets Console Client to reconnect after a disconnect
    
      
  
SETTBCLIENTIPA |  Set Console Client Server IP Address  
      
    
    SETTBCLIENTIPA [ip_address | HostName]
            ip_address - IP address in dot decimal notation
            HostName - Hostname
    
      
  
SETTBCLIENTNUMRETRY |  Set Console Client number of retries  
      
    
    SETTBCLIENTNUMRETRY [numberofretries]
            numberofretries - Max number of retries
            0 indicates that the console client connection will keep on trying to connect to the server
    
      
  
SETTBCLIENTPORTNUM |  Set Console Client Server Port Number  
      
    
    SETTBCLIENTPORTNUM [portnumber]
            portNumber - Port Number in decimal notation
    
      
  
SETTBCLIENTTIMEOUT |  Set Console Client Idle Timeout  
      
    
    SETTBCLIENTTIMEOUT [timeOutinSeconds]
            timeOutinSeconds - Idle Timeout in seconds after which connection is closed
            0 indicates that the console client connection will never closed because of a timeout
    
      
  
SHORTMESSage |  Display a message on the screen with a 2second timeout.  
      
    
    SHORTMESSAGE [string]
            string - ASCII string to display on screen for 2 seconds
    
      
  
SHOWEXTRAerrors |  Enables extended errors  
      
    
    SHOWEXTRAERRORS [OFF | ON ]
            No parameter - displays current setting
    
      
  
SHOWHW |  Display hardware configuration  
      
    
    SHOWHW
            No parameters
    
      
  
SNMP |  Enable/disable Simple Network Management Protocol  
      
    
    SNMP [ON | OFF | WIPE]
            No parameter - displays current setting
    
      
  
SNMPIOAdd |  Add an entry to the SNMP IO tables  
      
    
    SNMPIOADD <DIGITAL/ANALOG/SERIAL> <SNMPGET/SNMPSET> <NUM> <STRING>
    
      
  
SNMPIORemove |  Remove an entry from the SNMP IO tables  
      
    
    SNMPIOREMOVE [ALL] <DIGITAL/ANALOG/SERIAL> <SNMPGET/SNMPSET>  <NUM>
    
      
  
SNMPIOSInk |  Retrieve a value SET by the SNMP manager  
      
    
    SNMPIOSINK <DIGITAL/ANALOG/SERIAL> <NUM>
    
      
  
SNMPIOSOurce |  Provide a value for the SNMP manager to GET  
      
    
    SNMPIOSOURCE <DIGITAL/ANALOG/SERIAL> <ID> <VALUE>
    
      
  
SNMPMANager |  Configure an SNMP manager  
      
    
    SNMPMANAGER <ADD/REMOVE> <NAME> <ADDRESS> <PARAMS>
    Where PARAMS = one of:
    NoAuthNoPriv-v1, NoAuthNoPriv-v2, NoAuthNoPriv-v3, AuthNoPriv-v3, AuthPriv-v3
    Auth = authentication, Priv = privacy
    
      
  
SNMPMonitor |  Configure SNMP monitoring and trap generation  
      
    
    SNMPMONITOR <ADD/REMOVE> <OID> <COMP> <VALUE> <DESC>
            OID: Object Identifier to monitor
            COMP: Comparator EQUALS, LESSTHAN or GREATERTHAN
            VALUE: Value to compare against
            DESC: Simple text description of this probe (no spaces, 200 chars max.)
    
      
  
SNMPPass |  Configure SNMP usernames and passwords  
      
    
    SNMPPASS v1v2 <PASSWORD>
            PASSWORD: aka the community for SNMPv1/v2
    or
    SNMPPASS v3 <USERNAME> <PASSWORD> [<PRIVPASSWORD>]
            USERNAME: security name for SNMPv3
            PASSWORD: authentication password for SNMPv3
            PRIVPASSWORD: privacy password for SNMPv3
    
      
  
SNMPTRap |  Send an SNMP trap  
      
    
    SNMPTRAP <NUM> <STRING>
    
      
  
SOCKETTO |  SetSocketTimeout  
      
    
    SOCKETTO timeout
            timeout      - timeout value in seconds
            No parameter - displays current setting
    
      
  
SPLUSMEMSIZe |  Sets the size of the Area for Compiled SIMPL+ code  
      
    
    SPLUSMEMSIZE [1M | 1_25M | 1_5M | 1_75M | 2M]
            No parameter - displays current setting
    
      
  
SPLUSTASKS |  Show SIMPL+ Task Information  
      
    
    SPLUSTASKS {{-E}|{-W}} | {-N:TaskName}}
            Shows information about created SIMPL+ tasks.
            -E:  Show Event Dispatcher information
            -W:  Supress display of Wait() information
            -N:  Display information for SIMPL+ task with the name "TaskName"
    
      
  
SSL |  Display/Set SSL type  
      
    
    Command Blocked from this console type.
      
  
STARTTBCLIENT |  Enables Console Client Connection  
      
    
    STARTTBCLIENT
            Enables Console Client connection
    
      
  
STOPLIGHTBYPPn |  stop squack mode  
      
    
    Valid options are:
       Status if no arguments
    
    Syntax: STOPLIGHTBYPPN [4 byte Hex Adr]|ALL [SHOW]
    
      
  
STOPPROGram |  Stop the current program  
      
    
    STOPPROGRAM
            No arguments necessary.
    
      
  
STOPTBCLIENT |  Disable Console Client Connection  
      
    
    STOPTBCLIENT
            Disables Console Client connection - will break connection
    
      
  
SUSERPROGCMD |  Send a command from the console to the user program(surpress prompt)  
      
    
    SUSERPROGCMD {quoted string}
            Escape sequences will be translated, quotes will not be sent to user program.
            The program needs a "User Program Commands" symbol to receive the data
    
      
  
SYMSETSIG |  Set the state of a signal in the program  
      
    
    SYMSETSIG symbol_number index value [A | D | S]
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
    
      
  
SYSTEM |  Xmodem download new firmware  
      
    
    SYSTEM
            no parameters.
    
      
  
TELNETport |  Enable/disable the Telnet port  
      
    
    TELNETPORT [OFF | ON ]
            No parameter - displays current setting
    
      
  
TESTDNS |  Test DNS server  
      
    
    TESTDNS string
            string - ASCII string containing host name
    
      
  
TESTWATCH |  Test watchdog timer  
      
    
    TESTWATCH [HW | SW | NULL]
            HW - test the hardware watchdog timer
            SW - test the software watchdog timer
            NULL - test the NULL pointer access
    
      
  
TIMEdate |  Set the time and date  
      
    
    TIMEDATE [hh:mm:ss mm/dd/yyyy]
            hh:mm:ss - time in hours (use 24hr), mins and secs
            mm/dd/yyyy - date in months(1-12), day(1-31) and year
            No parameter - displays current setting
    
      
  
TYPE |  Display file contents  
      
    
    TYPE filename
            filename - the name of the file to display
    
      
  
UPLOAD |  Load file into cresnet device  
      
    
    Valid options are:
        hex number allowed as argument
     SLOT -
     SCreen -
     FIrmware -
    
      
  
UPTIME |  Display the time the system is running  
      
    
    UPTIME
            no parameters needed
    
      
  
USERPASSword |  Set user password.  
      
    
    USERPASSWORD
            No parameters.  Respond to prompts
    
      
  
USERPROGCMD |  Send a command from the console to the user program  
      
    
    USERPROGCMD {quoted string}
            Escape sequences will be translated, quotes will not be sent to user program.
            The program needs a "User Program Commands" symbol to receive the data
    
      
  
VERsion |  Print version to console  
      
    
    VERSION [-v]
            -v : show extended version info.
    
      
  
VNVRAMCLEAR |  Clear NVRAM with zeros without confirmation  
      
    
    VNVRAMCLEAR
            No parameter needed
    
      
  
WATCHDOG |  Enable the hardware watchdog timer  
      
    
    WATCHDOG [ON | OFF]
            No parameter - displays current setting
    
      
  
WAVEDUMP |  Dump Logic Wave Information  
      
    
    WAVEDUMP
            Set parameters/display the Logic Wave history.
            -W:ON|OFF  Dump list of last 0 symbols executed after a
                       "Could not solve logic within 1000 waves." error.  Currently OFF.
            -S:#       Store information for up to this number of symbols (Currently 0)
            -L         Dump the wavelist.
    
            Note:  Wave Dumps may not show a full history for a solution depending on the size of the wave history.
    
      
  
WEBINIT |  Initialize Webserver default file  
      
    
    WEBINIT
            No parameter needed
    
      
  
WEBPORT |  Set port number for Webserver.  
      
    
    WEBPORT [portnumber]
            portnumber - desired port number (in decimal).
            No parameter - displays current setting
    
      
  
WEBSERVer |  Enable/disable Webserver  
      
    
    WEBSERVER [ON | OFF]
            No parameter - displays current setting
    
      
  
WHO |  Generate a report of the Ethernet consoles  
      
    
    WHO
            No parameter necessary
    
      
  
WI2C |  Write I2C strings  
      
    
    Usage: wi2c [adr] [sub] [data0] ... [data n]
      Length is calculated automatically by counting number of data bytes
    
      
  
WINS |  Enable/disable WINS client  
      
    
    WINS [ON | OFF]
            No parameter - displays current setting
    
      
  
XGETfile |  Use XMODEM to retrieve file from system  
      
    
    XGET filesearchstring
            filesearchstring - search string which may contain wildcards
    
      
  
XLOADCERtfile |  Use XMODEM to transfer certificate file to ROM  
      
    
    XLOADCERTFILE
            no parameters.
    
      
  
XONxoff |  Set/clear SW handshaking  
      
    
    XONXOFF [ON | OFF]
            No parameter - displays current setting
    
      
  
XPUTfile |  Use XMODEM to transfer file to ROM  
      
    
    For files w/ headers: XPUT
            no parameters.
    For files w/out headers: XPUT size date time name
            size - size of the file in bytes
            date - date of the file (MM-DD-YY)
            time - time of the file (HH:MM:SS)
            name - name of the file
    
    

