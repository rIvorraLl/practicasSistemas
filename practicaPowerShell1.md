## 1.-

```powershell

 Get-Help Get-Help

NAME
    Get-Help
    
SYNTAX
    Get-Help [[-Name] <string>] [-Path <string>] [-Category {Alias | Cmdlet | Provider | General | FAQ 
    | Glossary | HelpFile | ScriptCommand | Function | Filter | ExternalScript | All | DefaultHelp | 
    DscResource | Class | Configuration}] [-Full] [-Component <string[]>] [-Functionality <string[]>] 
    [-Role <string[]>] [<CommonParameters>]
    
    Get-Help [[-Name] <string>] -Detailed [-Path <string>] [-Category {Alias | Cmdlet | Provider | 
    General | FAQ | Glossary | HelpFile | ScriptCommand | Function | Filter | ExternalScript | All | 
    DefaultHelp | DscResource | Class | Configuration}] [-Component <string[]>] [-Functionality 
    <string[]>] [-Role <string[]>] [<CommonParameters>]
    
    Get-Help [[-Name] <string>] -Examples [-Path <string>] [-Category {Alias | Cmdlet | Provider | 
    General | FAQ | Glossary | HelpFile | ScriptCommand | Function | Filter | ExternalScript | All | 
    DefaultHelp | DscResource | Class | Configuration}] [-Component <string[]>] [-Functionality 
    <string[]>] [-Role <string[]>] [<CommonParameters>]
    
    Get-Help [[-Name] <string>] -Parameter <string[]> [-Path <string>] [-Category {Alias | Cmdlet | 
    Provider | General | FAQ | Glossary | HelpFile | ScriptCommand | Function | Filter | ExternalScript 
    | All | DefaultHelp | DscResource | Class | Configuration}] [-Component <string[]>] [-Functionality 
    <string[]>] [-Role <string[]>] [<CommonParameters>]
    
    Get-Help [[-Name] <string>] -Online [-Path <string>] [-Category {Alias | Cmdlet | Provider | 
    General | FAQ | Glossary | HelpFile | ScriptCommand | Function | Filter | ExternalScript | All | 
    DefaultHelp | DscResource | Class | Configuration}] [-Component <string[]>] [-Functionality 
    <string[]>] [-Role <string[]>] [<CommonParameters>]
    

ALIASES
    None
    

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial 
    help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Get-Help -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2096483.
 ```
 
 ```powershell
 Get-Help New-TimeSpan

NAME
    New-TimeSpan
    
SYNTAX
    New-TimeSpan [[-Start] <datetime>] [[-End] <datetime>] [<CommonParameters>]
    
    New-TimeSpan [-Days <int>] [-Hours <int>] [-Minutes <int>] [-Seconds <int>] [<CommonParameters>]
    

ALIASES
    None
    

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial 
    help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help New-TimeSpan -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2096709.
```
 
 ```powershell
 Get-Help pwd

NAME
    Get-Location
    
SYNTAX
    Get-Location [-PSProvider <string[]>] [-PSDrive <string[]>] [<CommonParameters>]
    
    Get-Location [-Stack] [-StackName <string[]>] [<CommonParameters>]
    

ALIASES
    gl
    pwd
    

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial 
    help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Get-Location -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2096495.
 ```
 
 ```powershell
 Get-Help Read-Host

NAME
    Read-Host
    
SYNTAX
    Read-Host [[-Prompt] <Object>] [-MaskInput] [<CommonParameters>]
    
    Read-Host [[-Prompt] <Object>] [-AsSecureString] [<CommonParameters>]
    

ALIASES
    None
    

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial 
    help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Read-Host -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2096610.
 ```
 
 ```powershell
 Get-Help Rename-Item

NAME
    Rename-Item
    
SYNTAX
    Rename-Item [-Path] <string> [-NewName] <string> [-Force] [-PassThru] [-Credential <pscredential>] 
    [-WhatIf] [-Confirm] [<CommonParameters>]
    
    Rename-Item [-NewName] <string> -LiteralPath <string> [-Force] [-PassThru] [-Credential 
    <pscredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
    

ALIASES
    rni
    ren
    

REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial 
    help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Rename-Item -Online" or
           go to https://go.microsoft.com/fwlink/?LinkID=2097153.
 ```
 
 ## 2.-
 ```powershell
 > Get-Help Get-Help -examples
 
 --- Example 1: Display basic help information about a cmdlet ---
    
    Get-Help Format-Table
    Get-Help -Name Format-Table
    Format-Table -?
    
    `Get-Help <cmdlet-name>` is the simplest and default syntax of `Get-Help` cmdlet. You can omit the 
    Name parameter.
    
    The syntax `<cmdlet-name> -?` works only for cmdlets.
    --- Example 2: Display basic information one page at a time ---
    
    help Format-Table
    man Format-Table
    Get-Help Format-Table | Out-Host -Paging
    
    `help` is a function that runs `Get-Help` cmdlet internally and displays the result one page at a 
    time.
    
    `man` is an alias for the `help` function.
    
    `Get-Help Format-Table` sends the object down the pipeline. `Out-Host -Paging` receives the output 
    from the pipeline and displays it one page at a time. For more information, see Out-Host 
    (Out-Host.md).
    ------- Example 3: Display more information for a cmdlet -------
    
    Get-Help Format-Table -Detailed
    Get-Help Format-Table -Full
    
    The Detailed parameter displays the help article's detailed view that includes parameter 
    descriptions and examples.
    
    The Full parameter displays the help article's full view that includes parameter descriptions, 
    examples, input and output object types, and additional notes.
    
    The Detailed and Full parameters are effective only for the commands that have help files installed 
    on the computer. The parameters aren't effective for the conceptual ( about_ ) help articles.
    Example 4: Display selected parts of a cmdlet by using parameters
    
    Get-Help Format-Table -Examples
    Get-Help Format-Table -Parameter *
    Get-Help Format-Table -Parameter GroupBy
    
    The Examples parameter displays the help file's NAME and SYNOPSIS sections, and all the Examples. 
    You can't specify an Example number because the Examples parameter is a switch parameter.
    
    The Parameter parameter displays only the descriptions of the specified parameters. If you specify 
    only the asterisk (`*`) wildcard character, it displays the descriptions of all parameters. When 
    Parameter specifies a parameter name such as GroupBy , information about that parameter is shown.
    
    These parameters aren't effective for the conceptual ( about_ ) help articles.
    ---------- Example 5: Display online version of help ----------
    
    Get-Help Format-Table -Online
    
    
    -------- Example 6: Display help about the help system --------
    
    Get-Help
    
    
    ---------- Example 7: Display available help articles ----------
    
    Get-Help *
    
    
    ------- Example 8: Display a list of conceptual articles -------
    
    Get-Help about_*
    
    
    --------- Example 9: Search for a word in cmdlet help ---------
    
    Get-Help Add-Member -Full | Out-String -Stream | Select-String -Pattern Clixml
    
    the Export-Clixml cmdlet to save the instance of the object, including the additional members...
    can use the Import-Clixml cmdlet to re-create the instance of the object from the information...
    Export-Clixml
    Import-Clixml
    
    `Get-Help` uses the Full parameter to get help information for `Add-Member`. The 
    MamlCommandHelpInfo object is sent down the pipeline. `Out-String` uses the Stream parameter to 
    convert the object into a string. `Select-String` uses the Pattern parameter to search the string 
    for Clixml .
    -- Example 10: Display a list of articles that include a word --
    
    Get-Help -Name remoting
    
    Name                              Category  Module                    Synopsis
    ----                              --------  ------                    --------
    Install-PowerShellRemoting.ps1    External                            Install-PowerShellRemoting.ps1
    Disable-PSRemoting                Cmdlet    Microsoft.PowerShell.Core Prevents remote users...
    Enable-PSRemoting                 Cmdlet    Microsoft.PowerShell.Core Configures the computer...
    
    
    ---------- Example 11: Display provider-specific help ----------
    
    Get-Help Get-Item -Path SQLSERVER:\DataCollection
    
    NAME
    
        Get-Item
    
    SYNOPSIS
    
        Gets a collection of Server objects for the local computer and any computers
    
        to which you have made a SQL Server PowerShell connection.
        ...
    
    Set-Location SQLSERVER:\DataCollection
    SQLSERVER:\DataCollection> Get-Help Get-Item
    
    NAME
    
        Get-Item
    
    SYNOPSIS
    
        Gets a collection of Server objects for the local computer and any computers
    
        to which you have made a SQL Server PowerShell connection.
        ...
    
    
    ------------ Example 12: Display help for a script ------------
    
    Get-Help -Name C:\PS-Test\MyScript.ps1
    ```
    
    ```
    >  Get-Help New-TimeSpan -examples
    
    - Example 1: Create a TimeSpan object for a specified duration -
    
    $TimeSpan = New-TimeSpan -Hours 1 -Minutes 25
    $TimeSpan
    
    Days              : 0
    Hours             : 1
    Minutes           : 25
    Seconds           : 0
    Milliseconds      : 0
    Ticks             : 51000000000
    TotalDays         : 0.0590277777777778
    TotalHours        : 1.41666666666667
    TotalMinutes      : 85
    TotalSeconds      : 5100
    TotalMilliseconds : 5100000
    
    
    --- Example 2: Create a TimeSpan object for a time interval ---
    
    New-TimeSpan -End (Get-Date -Year 2010 -Month 1 -Day 1)
    
    
    ---- Example 3: Get the date 90 days from the current date ----
    
    $90days = New-TimeSpan -Days 90
    (Get-Date) + $90days
    
    These commands return the date that is 90 days after the current date.
    -- Example 4: Discover the TimeSpan since a file was updated --
    
    Get-ChildItem $PSHOME\en-us\about_remote.help.txt | New-TimeSpan
    
    Days              : 321
    Hours             : 21
    Minutes           : 59
    Seconds           : 22
    Milliseconds      : 312
    Ticks             : 278135623127728
    TotalDays         : 321.916230471907
    TotalHours        : 7725.98953132578
    TotalMinutes      : 463559.371879547
    TotalSeconds      : 27813562.3127728
    TotalMilliseconds : 27813562312.7728
    ```
    

```powershell
>  Get-Help pwd -examples
 -------- Example 1: Display your current drive location --------
    
    PS C:\Windows> Get-Location
    
    Path
    ----
    C:\Windows
    
    For instance, if you are in the `Windows` directory of the `C:` drive, it displays the path to that 
    directory.
    Example 2: Display your current location for different drives
    
    PS C:\> Set-Location C:\Windows
    PS C:\Windows> Set-Location HKLM:\Software\Microsoft
    PS HKLM:\Software\Microsoft> Set-Location "HKCU:\Control Panel\Input Method"
    PS HKCU:\Control Panel\Input Method> Get-Location -PSDrive C
    
    Path
    ----
    C:\Windows
    
    PS HKCU:\Control Panel\Input Method> Get-Location -PSDrive HKLM
    
    Path
    ----
    HKLM:\Software\Microsoft
    
    PS HKCU:\Control Panel\Input Method> Set-Location C:
    PS C:\Windows> Get-Location -PSProvider Registry
    
    Path
    ----
    HKCU:\Control Panel\Input Method
    
    
    ------------ Example 3: Get locations using stacks ------------
    
    PS C:\> Push-Location C:\Windows
    PS C:\Windows>Push-Location System32
    PS C:\Windows\System32>Push-Location WindowsPowerShell -StackName Stack2
    C:\Windows\System32\WindowsPowerShell>Get-Location -Stack
    
    Path
    ----
    C:\Windows
    C:\
    
    C:\Windows\System32\WindowsPowerShell>Get-Location -StackName Stack2
    
    Path
    ----
    C:\Windows\System32
    
    
    ---------- Example 4: Customize the PowerShell prompt ----------
    
    PS C:\>
    function prompt { 'PowerShell: ' + (Get-Location) + '> '}
    PowerShell: C:\>
    
    The function that defines the prompt includes a `Get-Location` command, which is run whenever the 
    prompt appears in the console.
    
    The format of the default PowerShell prompt is defined by a special function named `prompt`. You 
    can change the prompt in your console by creating a new function named `prompt`.
    
    To see the current prompt function, type the following command: `Get-Content Function:\prompt`
```


```powershell
--------- Example 1: Save console input to a variable ---------
    
    $Age = Read-Host "Please enter your age"
    
    
    ------- Example 2: Save console input as a secure string -------
    
    $pwd_secure_string = Read-Host "Enter a Password" -AsSecureString
    
    
    ------- Example 3: Mask input and as a plaintext string -------
    
    $pwd_string = Read-Host "Enter a Password" -MaskInput
```


```powershell
------------------- Example 1: Rename a file -------------------
    
    Rename-Item -Path "c:\logfiles\daily_file.txt" -NewName "monday_file.txt"
    
    
    -------------- Example 2: Rename and move an item --------------
    
    Rename-Item -Path "project.txt" -NewName "d:\archive\old-project.txt"
    
    Rename-Item : can't rename because the target specified represents a path or device name.
    At line:1 char:12
    + Rename-Item <<<<  -path project.txt -NewName d:\archive\old-project.txt
    + CategoryInfo          : InvalidArgument: (:) [Rename-Item], PS>  Move-Item -Path "project.txt" -De
    stination "d:\archive\old-project.txt"
    
    This example attempts to rename the `project.txt` file in the current directory to 
    `old-project.txt` in the `D:\Archive` directory. The result is the error shown in the output.
    
    Use the `Move-Item` cmdlet, instead.
    --------------- Example 3: Rename a registry key ---------------
    
    Rename-Item -Path "HKLM:\Software\MyCompany\Advertising" -NewName "Marketing"
    
    
    --------------- Example 4: Rename multiple files ---------------
    
    Get-ChildItem *.txt
    
    Directory: C:\temp\files
    
    Mode                LastWriteTime         Length Name
    ----                -------------         ------ ----
    -a----        10/3/2019   7:47 AM           2918 Friday.TXT
    -a----        10/3/2019   7:46 AM           2918 Monday.Txt
    -a----        10/3/2019   7:47 AM           2918 Wednesday.txt
    
    Get-ChildItem *.txt | Rename-Item -NewName { $_.Name -replace '.txt','.log' }
    Get-ChildItem *.log
```

