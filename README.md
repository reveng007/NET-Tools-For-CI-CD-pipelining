# NET Tools for CI CD pipelining:

NET Tools for CI CD pipelining usecase!

1. SharpSCCM: https://github.com/Mayyhem/SharpSCCM/ (URL of modified: .zip)

> => This solution has 2 projects. CodeCepticon only supports single-project solution file. \
> => Can build: x64 as well as AnyCPU binaries in 4.8 and 4.7.2 NET Version.
> => Have to check for x86!

2. Certify: https://github.com/GhostPack/Certify/ (URL of modified: .zip)

> => Can build: x64 as well as AnyCPU binaries in 4.8 and 4.7.2 NET Version.
> => Have to check for x86!

3. CertifyKit: https://github.com/Hagrid29/CertifyKit (URL of modified: .zip)

> => Can build: x64 as well as AnyCPU binaries in 4.8 and 4.7.2 NET Version.
> => Have to check for x86!

4. CertStealer: https://github.com/TheWover/CertStealer (URL of modified: .zip)

> => Can build: x64 as well as AnyCPU binaries in 4.8, 4.7.2 and 3.5 NET Version.
> => Have to check for x86!

5. SharpSystemTriggers: https://github.com/cube0x0/SharpSystemTriggers
   - SharpSpoolTrigger: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.
   - SharpEfsTrigger: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.
   - SharpDcomTrigger: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.
   - Midl2Bytes: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.

6. Rubeus: https://github.com/GhostPack/Rubeus (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.

7. Seatbelt: https://github.com/GhostPack/Seatbelt (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.

8. SharpView: https://github.com/tevora-threat/SharpView (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version.

9. SharpHound: https://github.com/SpecterOps/SharpHound (URL of modified: .zip)
> => Can build: x64, AnyCPU and x86 binaries in 4.8 NET Version.
> => Build via MSBuild Binary was causing error, So Compiled binaries via Visual Studio in this case, and kept those binaries here as it is.

10. SharpDPAPI: https://github.com/GhostPack/SharpDPAPI
   - SharpChrome: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => Can build: x64, AnyCPU and x86 binaries in 4.8 and 4.7.2 NET Version. \
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
    </Compile>]
...
...
...
```
> From: `..\SharpDPAPI\Domain\Version.cs` to `..\..\SharpDPAPI-all\SharpDPAPI\Domain\Version.cs`, cause I have created 2 seperate folders solely for Codecepticon compilation of SharpChrome and SharpDPAPI independently and both SharpDPAPI and SharpChrome folder are made independent of one another.
   - SharpDPAPI: Created different folder as well as different .sln file. (URL of modified: .zip)
   > => 


