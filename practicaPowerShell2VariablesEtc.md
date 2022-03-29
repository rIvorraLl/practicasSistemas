## Task 1


```powershell
PS /home/alt> $BooleanVar = $True
PS /home/alt> $StringVar = "This is a string"
PS /home/alt> $intVar = 42
```

## Task 2

```powershell
PS /home/alt> Get-Variable

Name                           Value
----                           -----
?                              True
^                              $intVar
$                              42
args                           {}
BooleanVar                     True
ConfirmPreference              High
DebugPreference                SilentlyContinue
EnabledExperimentalFeatures    {}
Error                          {The term 'Out-GridView' is not recognized as a name of a cmdlet, functi…
ErrorActionPreference          Continue
ErrorView                      ConciseView
ExecutionContext               System.Management.Automation.EngineIntrinsics
false                          False
FormatEnumerationLimit         4
HOME                           /home/alt
Host                           System.Management.Automation.Internal.Host.InternalHost
InformationPreference          SilentlyContinue
input                          System.Collections.ArrayList+ArrayListEnumeratorSimple
intVar                         42
IsCoreCLR                      True
IsLinux                        True
IsMacOS                        False
IsWindows                      False
MaximumHistoryCount            4096
MyInvocation                   System.Management.Automation.InvocationInfo
NestedPromptLevel              0
null                           
OutputEncoding                 System.Text.UTF8Encoding
PID                            3988
PROFILE                        /home/alt/.config/powershell/Microsoft.PowerShell_profile.ps1
ProgressPreference             Continue
PSBoundParameters              {}
PSCommandPath                  
PSCulture                      en-US
PSDefaultParameterValues       {}
PSEdition                      Core
PSEmailServer                  
PSHOME                         /opt/microsoft/powershell/7
PSScriptRoot                   
PSSessionApplicationName       wsman
PSSessionConfigurationName     http://schemas.microsoft.com/powershell/Microsoft.PowerShell
PSSessionOption                System.Management.Automation.Remoting.PSSessionOption
PSStyle                        System.Management.Automation.PSStyle
PSUICulture                    en-US
PSVersionTable                 {PSVersion, PSEdition, GitCommitId, OS…}
PWD                            /home/alt
ShellId                        Microsoft.PowerShell
StackTrace                        at System.Management.Automation.CommandDiscovery.LookupCommandInfo(St…
StringVar                      This is a string
true                           True
VerbosePreference              SilentlyContinue
WarningPreference              Continue
WhatIfPreference               False
```

## Task 3

```powershell
PS /home/alt> $intVar1 = 4       
PS /home/alt> $intVar2 = 10      
PS /home/alt> $intVar1 * $intVar2
40
```

# Task 4
```powershell
PS /home/alt> $intVar3 = 10      
PS /home/alt> $intVar4 = 2 
PS /home/alt> $VariableResult = $intVar3 / $intVar4
```

