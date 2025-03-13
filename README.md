# NET Tools for CI CD pipelining:

NET Tools for CI CD pipelining usecase!

1. SharpSCCM: https://github.com/Mayyhem/SharpSCCM/ (URL of modified: .zip)

> => This solution has 2 projects. CodeCepticon only supports single-project solution file. \
> => Created different folder as well as different .sln file. (URL of modified: .zip). \
> ### => UnitTests Compilation Causing Errors, I tried to run SharpSCCM Individually, I found it to be working against Defender as well as getting executed (Although more testing needs to be done in SCCM enabled env) 
> 
<details><summary>See Details</summary>

![image](https://github.com/user-attachments/assets/3008a056-7502-4ed4-a632-9d3cb6e65dad)

```powershell
PS C:\Users\soumy\Downloads> .\SharpSCCM.exe  get

  _______ _     _ _______  ______  _____  _______ _______ _______ _______
  |______ |_____| |_____| |_____/ |_____] |______ |       |       |  |  |
  ______| |     | |     | |    \_ |       ______| |______ |______ |  |  |    @_Mayyhem

Required command was not provided.

Description:
  A group of commands that fetch objects from SMS Providers via WMI, management points via HTTP(S), or domain controllers via LDAP

Usage:
  SharpSCCM get [command] [options]

Options:
  -sc, --site-code <site-code>  The three character site code (e.g., PS1) (default: the site code of the client running SharpSCCM)
  --debug                       Print debug messages for troubleshooting
  --no-banner                   Do not display banner in command output
  -?, -h, --help                Show help and usage information

Commands:
  admins                        Get information on SCCM administrators and security roles from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  applications                  Get information on applications from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Full Administrator
                                    - Application Administrator
                                    - Application Author
                                    - Application Deployment Manager
                                    - Operating System Deployment Manager
                                    - Operations Administrator
                                    - Read-only Analyst
  classes                       Get a list of WMI classes from an SMS Provider
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  class-instances <wmi-class>   Get information on WMI class instances from an SMS Provider
                                  Permitted security roles:
                                    - ACLs are applied at the object class and instance level
  class-properties <wmi-class>  Get all properties of a specified WMI class from an SMS Provider
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  collections                   Get information on collections from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  collection-members            Get the members of a specified collection from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  collection-rules              Get the rules that are evaluated to add members to a collection from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  deployments                   Get information on deployments from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Full Administrator
                                    - Application Administrator
                                    - Application Author
                                    - Application Deployment Manager
                                    - Operating System Deployment Manager
                                    - Operations Administrator
                                    - Read-only Analyst
  devices                       Get information on devices from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  primary-users                 Get information on primary users set for devices from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Full Administrator
                                    - Application Administrator
                                    - Application Deployment Manager
                                    - Operations Administrator
                                    - Read-only Analyst
  resource-id                   Get the resourceID for a username or device from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  naa, secrets                  Request the machine policy from a management point via HTTP to obtain credentials for network access accounts, collection variables, and task
                                sequences
                                  Requirements:
                                    - Domain computer account credentials
                                        OR
                                    - Local Administrators group membership on a client
                                        OR
                                    - PXE certificate and media GUID (use -c and -m)
  site-info                     Get information about the site, including the site server name, from a domain controller via LDAP
  site-push-settings            Get automatic client push installation settings from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)
  software                      Query a management point for distribution point content locations
  users                         Get information on users from an SMS Provider via WMI
                                  Permitted security roles:
                                    - Any (SMS Admins local group)

[+] Completed execution in 00:00:00.1620716
PS C:\Users\soumy\Downloads> .\SharpSCCM.exe get collection-rules

  _______ _     _ _______  ______  _____  _______ _______ _______ _______
  |______ |_____| |_____| |_____/ |_____] |______ |       |       |  |  |
  ______| |     | |     | |    \_ |       ______| |______ |______ |  |  |    @_Mayyhem

[!] Please specify a collection Name (-n), CollectionID (-i), device Name (-d), user UniqueUserName (-u), or ResourceID (-r) to get applicable rules for
[+] Completed execution in 00:00:00.0946297
PS C:\Users\soumy\Downloads> .\SharpSCCM.exe local

  _______ _     _ _______  ______  _____  _______ _______ _______ _______
  |______ |_____| |_____| |_____/ |_____] |______ |       |       |  |  |
  ______| |     | |     | |    \_ |       ______| |______ |______ |  |  |    @_Mayyhem

Required command was not provided.

Description:
  A group of commands to interact with the local workstation/server

Usage:
  SharpSCCM local [command] [options]

Options:
  --debug         Print debug messages for troubleshooting
  --no-banner     Do not display banner in command output
  -?, -h, --help  Show help and usage information

Commands:
  classes                       Get a list of local WMI classes
  class-instances <wmi-class>   Get information on local WMI class instances
  class-properties <wmi-class>  Get all properties of a specified local WMI class
  client-info                   Get the client software version for the local host via WMI
  create-ccr <target>           Untested function to create a CCR that initiates client push installation to a specified target
                                  Requirements:
                                     - Local Administrators group membership on a primary site server
                                     - ConfigMgr 2003 or 2007
  grep <string-to-find> <path>  Search a specified file for a specified string
  push-logs                     Search for evidence of client push installation
  query <query>                 Execute a given WQL query on the local system
                                  Permitted security roles:
                                    - ACLs are applied at the object class and instance level
  naa, secrets                  Get policy secrets (e.g., network access accounts, task sequences, and collection variables) stored locally in the WMI repository
                                  Requirements:
                                     - Local Administrators group membership on a client
  site-info                     Get the current management point and site code for the local host via WMI
  triage                        Gather information about the site from local log files
  user-sid                      Get the hex SID for the current user

[+] Completed execution in 00:00:00.1553473
PS C:\Users\soumy\Downloads> .\SharpSCCM.exe local triage

  _______ _     _ _______  ______  _____  _______ _______ _______ _______
  |______ |_____| |_____| |_____/ |_____] |______ |       |       |  |  |
  ______| |     | |     | |    \_ |       ______| |______ |______ |  |  |    @_Mayyhem

[+] Client cache contents and permissions for the current user:
    Perms      Size  Date modified          Name
[!] Could not find file 'C:\Windows\ccmcache'.

[+] Searching logs for possible UNC paths:
[!] An unhandled exception of type System.Reflection.TargetInvocationException occurred: Exception has been thrown by the target of an invocation.
```
</details>

> => CodeCepticon Worked with `SharpSCCM` as well as `` \
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

2. Certify: https://github.com/GhostPack/Certify/ (URL of modified: .zip)

> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

3. CertifyKit: https://github.com/Hagrid29/CertifyKit (URL of modified: .zip)

> => Can build: x64, x86 as well as AnyCPU binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

4. CertStealer: https://github.com/TheWover/CertStealer (URL of modified: .zip)

> => Can build: x64, AnyCPU and x86 binaries in 4.8, 4.7.2 and 3.5 NET Version. \
> => CodeCepticon Works! \
> => Copied dependecy dll, `4.CertStealer_TheWover\CertStealer-main\packages\CommandLineParser.1.9.71\lib\net35\CommandLine.dll` to compiled binary folder: For ConfuSerEx UseCase. \
> => Presence of dependecy dll is present in .csproj file. \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

5. SharpSystemTriggers: https://github.com/cube0x0/SharpSystemTriggers
   - SharpSpoolTrigger: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
   > => CodeCepticon Works! \
   > => ConfuserEx profile also added here (AnyCPU/x86/x64)
   - SharpEfsTrigger: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
   > => CodeCepticon Works! \
   > => ConfuserEx profile also added here (AnyCPU/x86/x64)
   - SharpDcomTrigger: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
   > => CodeCepticon Works! \
   > => ConfuserEx profile also added here (AnyCPU/x86/x64)
   - Midl2Bytes: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
   > => CodeCepticon Works! \
   > => ConfuserEx profile also added here (AnyCPU/x86/x64)

6. Rubeus: https://github.com/GhostPack/Rubeus (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

7. Seatbelt: https://github.com/GhostPack/Seatbelt (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

8. SharpView: https://github.com/tevora-threat/SharpView (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => Copied dependecy dll, `8.SharpView_tevora-threat\SharpView-master\packages\PCRE.NET.0.7.0\lib\net45\PCRE.NET.dll` to compiled binary folder: For ConfuSerEx UseCase. \
> => Presence of dependecy dll is present in .csproj file. \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

9. SharpHound: https://github.com/SpecterOps/SharpHound (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 NET Version. \
> => Build via MSBuild Binary was causing error, So Compiled binaries via Visual Studio in this case, and kept those binaries here as it is. \
> => CodeCepticon Works! \
> => Presence of dependecy dll is present in .csproj file (But in a scattered manner). \
> => ConfuserEx profile also added here (AnyCPU/x86/x64) \
> => Copied dependecy dlls to compiled binary folder: For ConfuSerEx UseCase.:
<details><summary>See Details</summary>

```markdown
=> ~\.nuget\packages\sharphoundcommon\4.2.2\lib\net472\SharpHoundCommonLib.dll


`[ERROR] Failed to resolve dependency of 'SharpHound.exe'.
Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: Microsoft.Extensions.Logging.Abstractions, Version=`
# .\nuget.exe install Microsoft.Extensions.Logging.Abstractions -Version 8.0.0 -OutputDirectory .
=> .\9.SharpHound_SpecterOps\SharpHound-2.X\Microsoft.Extensions.Logging.Abstractions.8.0.0\lib\net462\Microsoft.Extensions.Logging.Abstractions.dll


`Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: Microsoft.Bcl.AsyncInterfaces, Version=8.0.0.0, Culture=neutral, PublicKeyToken=cc7b13ffcd2ddd51`
# .\nuget.exe install Microsoft.Bcl.AsyncInterfaces -Version 8.0.0 -OutputDirectory .
=> .\Microsoft.Bcl.AsyncInterfaces.8.0.0\lib\net462\Microsoft.Bcl.AsyncInterfaces.dll


`[ERROR] Failed to resolve dependency of 'SharpHound.exe'.
Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: System.Threading.Channels, Version=8.0.0.0, Culture=neutral, PublicKeyToken=cc7b13ffcd2ddd51`
# .\nuget.exe install System.Threading.Channels -Version 8.0.0 -OutputDirectory .
=> .\System.Threading.Channels.8.0.0\lib\net462\System.Threading.Channels.dll


`[ERROR] Failed to resolve dependency of 'SharpHound.exe'.
Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: System.Threading.Tasks.Extensions, Version=4.2.0.1, Culture=neutral, PublicKeyToken=cc7b13ffcd2ddd51`
# Already downloaded before via previous installations of nuget
=> .\System.Threading.Tasks.Extensions.4.5.4\lib\net461\System.Threading.Tasks.Extensions.dll


`[ERROR] Failed to resolve dependency of 'SharpHound.exe'.
Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: Newtonsoft.Json, Version=13.0.0.0, Culture=neutral, PublicKeyToken=30ad4fe6b2a6aeed`
# Already downloaded before via previous installations of nuget
=> ~\.nuget\packages\newtonsoft.json\13.0.1\lib\net45\Newtonsoft.Json.dll


`[ERROR] Failed to resolve dependency of 'SharpHound.exe'.
Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: CommandLine, Version=2.8.0.0, Culture=neutral, PublicKeyToken=5a870481e358d379`
# Already downloaded before via previous installations of nuget
=> ~\.nuget\packages\commandlineparser\2.8.0\lib\net45\CommandLine.dll


`[ERROR] Failed to resolve dependency of 'SharpHound.exe'.
Exception: dnlib.DotNet.AssemblyResolveException: Could not resolve assembly: ICSharpCode.SharpZipLib, Version=1.3.3.11, Culture=neutral, PublicKeyToken=1b03e6acf1164f73`
# Already downloaded before via previous installations of nuget
=> ~\.nuget\packages\sharpziplib\1.3.3\lib\net45\ICSharpCode.SharpZipLib.dll
```
</details>

10. SharpDPAPI: https://github.com/GhostPack/SharpDPAPI
   - SharpChrome: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
   > => ConfuserEx profile also added here (AnyCPU/x86/x64) \
   > #### => Didn't WORK with CodeCepticon!
> Updated these lines in Newly created/added SharpChrome.sln file:
```xml
<ItemGroup>
    <Compile Include="..\..\SharpDPAPI-all\SharpDPAPI\Domain\Version.cs">
      <Link>Domain\Version.cs</Link>
    </Compile>
    <Compile Include="..\..\SharpDPAPI-all\SharpDPAPI\lib\Backup.cs">
      <Link>lib\Backup.cs</Link>
    </Compile>
    <Compile Include="..\..\SharpDPAPI-all\SharpDPAPI\lib\BigInteger.cs">
      <Link>lib\BigInteger.cs</Link>
    </Compile>
...
...
...
```
> From: `..\SharpDPAPI\Domain\Version.cs` to `..\..\SharpDPAPI-all\SharpDPAPI\Domain\Version.cs`, cause I have created 2 seperate folders solely for Codecepticon compilation of SharpChrome and SharpDPAPI independently and both SharpDPAPI and SharpChrome folder are made independent of one another.
   - SharpDPAPI: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
   > => ConfuserEx profile also added here (AnyCPU/x86/x64) \
   > => CodeCepticon Works!

