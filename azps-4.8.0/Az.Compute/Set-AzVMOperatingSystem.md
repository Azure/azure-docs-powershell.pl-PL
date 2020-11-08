---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 39AADD19-2EDD-4C1F-BC9E-22186DD9A085
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmoperatingsystem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMOperatingSystem.md
ms.openlocfilehash: c22e1a09f20eca32cb21056ae45334f0d55ce14b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062863"
---
# Set-AzVMOperatingSystem

## STRESZCZENIe
Ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.

## POLECENIA

### Windows (domyślnie)
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-ProvisionVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDisableVMAgent
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-PatchMode <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### WindowsDisableVMAgentWinRmHttps
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Windows] [-ComputerName] <String>
 [-Credential] <PSCredential> [[-CustomData] <String>] [-DisableVMAgent] [-EnableAutoUpdate]
 [[-TimeZone] <String>] [-WinRMHttp] [-WinRMHttps] [-WinRMCertificateUrl] <Uri> [-PatchMode <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Linux
```
Set-AzVMOperatingSystem [-VM] <PSVirtualMachine> [-Linux] [-ComputerName] <String> [-Credential] <PSCredential>
 [[-CustomData] <String>] [-DisablePasswordAuthentication] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzVMOperatingSystem** ustawia właściwości systemu operacyjnego dla maszyny wirtualnej.
Możesz określić poświadczenia logowania, nazwę komputera i typ systemu operacyjnego.

## Przykłady

### Przykład 1: Ustawianie właściwości systemu operacyjnego dla nowych maszyn wirtualnych
```
$SecurePassword = ConvertTo-SecureString "Password" -AsPlainText -Force
$Credential = New-Object System.Management.Automation.PSCredential ("FullerP", $SecurePassword); 
$AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" 
$VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
$ComputerName = "ContosoVM122"
$WinRMCertUrl = "http://keyVaultName.vault.azure.net/secrets/secretName/secretVersion"
$TimeZone = "Pacific Standard Time"
$CustomData = "echo 'Hello World'"
$VirtualMachine = Set-AzVMOperatingSystem -VM $$VirtualMachine -Windows -ComputerName $ComputerName -Credential $Credential -CustomData $CustomData -WinRMHttp -WinRMHttps -WinRMCertificateUrl $WinRMCertUrl -ProvisionVMAgent -EnableAutoUpdate -TimeZone $TimeZone -PatchMode "AutomaticByPlatform"
```

Pierwsze polecenie konwertuje hasło na bezpieczny ciąg, a następnie zapisuje je w zmiennej $SecurePassword.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help ConvertTo-SecureString` .
Drugie polecenie tworzy poświadczenie dla użytkownika FullerP i hasło przechowywane w $SecurePassword, a następnie zapisuje poświadczenia w zmiennej $Credential.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help New-Object` .
Trzecia komenda Pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.
Czwarte polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.
Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.
Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Następne cztery polecenia przypisują wartości do zmiennych, które mają być używane w poniższym poleceniu.
Ponieważ można określić te ciągi bezpośrednio w poleceniu **Set-AzVMOperatingSystem** , ta metoda jest używana tylko do czytelności.
Możesz jednak skorzystać z takiej metody jak w przypadku skryptów.
Ostatnie polecenie ustawia właściwości systemu operacyjnego dla maszyny wirtualnej przechowywanej w $VirtualMachine.
Polecenie korzysta z poświadczeń przechowywanych w $Credential.
W poleceniu użyto zmiennych przypisanych we wcześniejszych poleceniach dla określonych parametrów.

## PARAMETRÓW

### -ComputerName
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

### — Poświadczenie
Określa nazwę użytkownika i hasło maszyny wirtualnej jako obiekt **PSCredential** .
Aby uzyskać poświadczenia, użyj polecenia cmdlet Get-Credential.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .

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

### -CustomData
Określa zakodowany ciąg Base-64 z danymi niestandardowymi.
Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.
Maksymalna długość tablicy binarnej to 65535 bajtów.<br>
**Uwaga: nie przekazuj żadnych kluczy tajnych ani haseł we właściwości customData**<br>
Tej właściwości nie można zaktualizować po utworzeniu maszyny wirtualnej. <br>
customData jest przekazywana do maszyny wirtualnej, która ma zostać zapisana jako plik, aby uzyskać więcej informacji, zobacz [dane niestandardowe na platformie Azure](https://azure.microsoft.com/en-us/blog/custom-data-and-cloud-init-on-windows-azure/) VM <br>
Aby uzyskać informacje na temat używania chmury-init dla maszyny wirtualnej Linux, zobacz [Używanie chmury-init w celu dostosowania maszyny wirtualnej Linux podczas jej tworzenia](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init) .

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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
Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.

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
Wyłącz agenta obsługi maszyny wirtualnej.

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
Wskazuje, że to polecenie cmdlet umożliwia automatyczne aktualizowanie.

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

### -Linux
Wskazuje, że typ systemu operacyjnego to Linux.

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

### -Patchmode
Określa tryb IaaS maszyny wirtualnej w trybie gościnnym.<br><br>
Możliwe wartości:<br>
**Ręczna** — możesz sterować stosowaniem poprawek na maszynie wirtualnej. W tym celu należy ręcznie zastosować poprawki w maszynie wirtualnej. W tym trybie aktualizacje automatyczne są wyłączone. Właściwość WindowsConfiguration. enableAutomaticUpdates musi mieć wartość FAŁSZ<br>
**AutomaticByOS** — maszyna wirtualna zostanie automatycznie zaktualizowana przez system operacyjny. Właściwość WindowsConfiguration. enableAutomaticUpdates musi mieć wartość true. <br >
**AutomaticByPlatform** — maszyna wirtualna zostanie automatycznie zaktualizowana przez system operacyjny. Właściwości provisionVMAgent i WindowsConfiguration. enableAutomaticUpdates muszą być prawdziwe

```yaml
Type: System.String
Parameter Sets: Windows, WindowsWinRmHttps, WindowsDisableVMAgent, WindowsDisableVMAgentWinRmHttps
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionVMAgent
Wskazuje, że ustawienia wymagają zainstalowania agenta maszyny wirtualnej na maszynie wirtualnej.

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

### -TimeZone
Określa strefę czasową maszyny wirtualnej. na przykład \" Pacyfik (czas standardowy) \" . <br>
Możliwe wartości mogą być [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) wartością ze stref czasowych zwróconych przez [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).

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

### -VM
Określa lokalny obiekt maszyny wirtualnej, na którym należy ustawić właściwości systemu operacyjnego.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzVM.
Utwórz obiekt maszyny wirtualnej przy użyciu New-AzVMConfig polecenia cmdlet.

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

### -Windows
Wskazuje, że typ systemu operacyjnego to Windows.

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
Określa identyfikator URI certyfikatu usługi WinRM.
Należy je zapisać w magazynie kluczy.

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

### -WinRMHttp
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
Wskazuje, że w tym systemie operacyjnym jest używany protokół HTTPS.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

### System. Management. Automation. SwitchParameter

### System. String

### System. Management. Automation. PSCredential

### System. URI

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSVirtualMachine

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[Nowe — AzVMConfig](./New-AzVMConfig.md)


