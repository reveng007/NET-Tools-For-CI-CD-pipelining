# NET Tools for CI CD pipelining:

NET Tools for CI CD pipelining usecase!

1. SharpSCCM: https://github.com/Mayyhem/SharpSCCM/ (URL of modified: .zip)

> => This solution has 2 projects. CodeCepticon only supports single-project solution file. \
> => Can build: x64 as well as AnyCPU binaries in 4.8 and 4.7.2 NET Version. \

> => Have to check for x86!

> ### Need Some Changes to be made in file.sln of SharpSCCM   => !!!!!

2. Certify: https://github.com/GhostPack/Certify/ (URL of modified: .zip)

> => Can build: x64, AnyCPU anc x86 binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

3. CertifyKit: https://github.com/Hagrid29/CertifyKit (URL of modified: .zip)

> => Can build: x64 as well as AnyCPU binaries in 4.8 and 4.7.2 NET Version. \
> => CodeCepticon Works! \
> => ConfuserEx profile also added here (AnyCPU/x86/x64)

4. CertStealer: https://github.com/TheWover/CertStealer (URL of modified: .zip)

> => Can build: x64 as well as AnyCPU binaries in 4.8, 4.7.2 and 3.5 NET Version. \
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
   > ### => Didn't WORK with CodeCepticon!
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
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.


