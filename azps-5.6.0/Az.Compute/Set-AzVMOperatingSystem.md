---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: 75eb0ef60443cdbf2dfe3fa53202d3c8141d4888
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990445"
---
# Set-AzVMOperatingSystem

## SYNOPSIS
Ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.

## SKŁADNIA

### Windows (domyślne)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-EnableHotpatching]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-EnableHotpatching] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-PatchMode <String>] [-DisablePasswordAuthentication]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVMOperatingSystem** ustawia właściwości systemu operacyjnego maszyny wirtualnej.
Możesz określić poświadczenia logowania, nazwę komputera i typ systemu operacyjnego.

## PRZYKŁADY

### Przykład 1. Ustawianie właściwości systemu operacyjnego dla nowej maszyny wirtualnej
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w $SecurePassword danych.
Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .
Drugie polecenie tworzy poświadczenia dla użytkownika FullerP i hasło przechowywane w programie $SecurePassword, a następnie przechowuje poświadczenia w $Credential danych.
Aby uzyskać więcej informacji, wpisz `Get-Help New-Object` .
Trzecie polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $AvailabilitySet zasobów.
Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Następne cztery polecenia przypiszą wartości do zmiennych, których można użyć w następującym poleceniu.
Ponieważ można określić te ciągi bezpośrednio w **poleceniu Set-AzVMOperatingSystem,** ta metoda jest używana tylko w celu czytelności.
Można jednak użyć takiego podejścia, jak to w skryptach.
Końcowe polecenie określa właściwości systemu operacyjnego maszyny wirtualnej przechowywanej w $VirtualMachine.
To polecenie używa poświadczeń przechowywanych w $Credential.
W przypadku niektórych parametrów polecenie używa zmiennych przypisanych w poprzednich poleceniach.

### Przykład 2. Ustawianie właściwości systemu operacyjnego dla nowej maszyny wirtualnej z włączonym poprawianie poprawek
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform" -EnableHotPatching
```

Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w $SecurePassword danych.
Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .
Drugie polecenie tworzy poświadczenia dla użytkownika FullerP i hasło przechowywane w programie $SecurePassword, a następnie przechowuje poświadczenia w $Credential danych.
Aby uzyskać więcej informacji, wpisz `Get-Help New-Object` .
Trzecie polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $AvailabilitySet zasobów.
Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Następne cztery polecenia przypiszą wartości do zmiennych, których można użyć w następującym poleceniu.
Ponieważ można określić te ciągi bezpośrednio w **poleceniu Set-AzVMOperatingSystem,** ta metoda jest używana tylko w celu czytelności.
Można jednak użyć takiego podejścia, jak to w skryptach.
Końcowe polecenie określa właściwości systemu operacyjnego maszyny wirtualnej przechowywanej w $VirtualMachine.
To polecenie używa poświadczeń przechowywanych w $Credential.
W przypadku niektórych parametrów polecenie używa zmiennych przypisanych w poprzednich poleceniach.
To polecenie włącza hotpatching na komputerze wirtualnym.

### Przykład 3. Ustawianie właściwości systemu operacyjnego dla nowej maszyny wirtualnej systemu Linux
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -PatchMode "AutomaticByPlatform"
```

Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w $SecurePassword danych.
Aby uzyskać więcej informacji, wpisz `Get-Help ConvertTo-SecureString` .
Drugie polecenie tworzy poświadczenia dla użytkownika FullerP i hasło przechowywane w programie $SecurePassword, a następnie przechowuje poświadczenia w $Credential danych.
Aby uzyskać więcej informacji, wpisz `Get-Help New-Object` .
Trzecie polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie przechowuje ten obiekt w $AvailabilitySet zasobów.
Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Kolejne dwa polecenia przypiszą wartości do zmiennych, których można użyć w następującym poleceniu.
Końcowe polecenie określa właściwości systemu operacyjnego maszyny wirtualnej przechowywanej w $VirtualMachine.
To polecenie używa poświadczeń przechowywanych w $Credential.
W przypadku niektórych parametrów polecenie używa zmiennych przypisanych w poprzednich poleceniach.
Polecenie ustawia wartość trybu poprawki na komputerze wirtualnym na wartość "AutomaticByPlatform".

## PARAMETERS

### — Nazwa_komputera
Określa nazwę komputera.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - Credential
Określa nazwę użytkownika i hasło dla maszyny wirtualnej jako **obiekt PSCredential.**
Aby uzyskać poświadczenia, użyj Get-Credential cmdlet.
Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - CustomData
Określa ciąg, który ma być przekazywany do maszyny wirtualnej. Aby uzyskać więcej informacji, [zobacz Dane niestandardowe w maszyny wirtualne platformy Azure.](https://docs.microsoft.com/en-us/azure/virtual-machines/custom-data)
**Uwaga: przechowywanie poufnych informacji w danych niestandardowych nie jest zalecane.**


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisablePasswordAuthentication
Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasłem.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableVMAgent
Wyłącz agenta maszyny wirtualnej inicjowania obsługi administracyjnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableAutoUpdate
Wskazuje, że to polecenie cmdlet umożliwia automatyczną aktualizację.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableHotpatching
Umożliwia klientom poprawianie maszyn wirtualnych platformy Azure bez konieczności ponownego rozruchu. Aby włączyćHotpatching, dla "provisionVMAgent" należy ustawić wartość true, a wartość "patchMode" musi być ustawiona na wartość "AutomaticByPlatform".

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Linux
Wskazuje, że typem systemu operacyjnego jest Linux.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PatchMode
Określa tryb łatania poprawek przez gościa do maszyny wirtualnej IaaS.<br><br>
Możliwe wartości:<br>
**Ręcznie** — kontrolujesz aplikację poprawek na maszynę wirtualną. W tym celu należy ręcznie zastosować poprawki wewnątrz maszyny wirtualnej. W tym trybie aktualizacje automatyczne są wyłączone. właściwość WindowsConfiguration.enableAutomaticUpdates musi mieć wartość false<br>
**AutomaticByOS** — maszynę wirtualną zostanie automatycznie zaktualizowana przez system operacyjny. Właściwość WindowsConfiguration.enableAutomaticUpdates musi być prawdziwa. <br >
**AutomaticByPlatform** — maszynę wirtualną będzie automatycznie aktualizowana przez system operacyjny. Właściwości provisionVMAgent i WindowsConfiguration.enableAutomaticUpdates muszą być prawdziwe

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Oznacza, że ustawienia wymagają, aby agent maszyny wirtualnej był zainstalowany na maszyny wirtualnej.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - Strefa czasowa
Określa strefę czasową maszyny wirtualnej. np. \" Pacyfik (czas \" standardowy). <br>
Możliwe wartości mogą [być](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id z stref czasowych zwracanych przez [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — MASZYNY WIRTUALNEJ
Określa lokalny obiekt maszyny wirtualnej, na którym mają być ustawiane właściwości systemu operacyjnego.
Aby uzyskać obiekt maszyny wirtualnej, użyj Get-AzVM cmdlet.
Utwórz obiekt maszyny wirtualnej za pomocą New-AzVMConfig cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### — Windows
Wskazuje, że typem systemu operacyjnego jest system Windows.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMCertificateUrl
Określa URI certyfikatu usługi WinRM.
Musi to być przechowywane w magazynie kluczy.

```yaml
Type: System.Uri
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### —WinRMHttp
Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTP WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WinRMHttps
Oznacza, że w tym systemie operacyjnym jest używany protokół HTTPS WinRM.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WindowsWinRmHttps, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: True
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.Management.Automation.SwitchParameters

### System.String

### System.Management.Automation.PSCredential

### System.Uri

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)


