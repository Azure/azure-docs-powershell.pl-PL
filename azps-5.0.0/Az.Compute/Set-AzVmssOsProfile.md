---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 71bd8ca26755118a4bb9c075ae89bad765922f3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304224"
---
# Set-AzVmssOsProfile

## STRESZCZENIe
Ustawia właściwości profilu systemu operacyjnego VMSS.

## POLECENIA

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzVmssOsProfile** umożliwia ustawienie skali maszyny wirtualnej z ustawionymi właściwościami profilu systemu operacyjnego.

## Przykłady

### Przykład 1: Ustawianie właściwości profilu systemu operacyjnego dla VMSS
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

To polecenie ustawia właściwości profilu systemu operacyjnego dla maszyn wirtualnych należących do VMSS o nazwie ContosoVMSS.
Polecenie ustawia prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS, aby przetestować i poświadczyć nazwę użytkownika i hasło administratora.

## PARAMETRÓW

### -AdditionalUnattendContent
Określa obiekt zawartości nienadzorowanej.
Aby utworzyć obiekt, możesz użyć Add-AzVMAdditionalUnattendContent.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminPassword
Określa hasło administratora, które ma być używane dla wszystkich wystąpień maszyny wirtualnej w VMSS.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AdminUsername
Określa nazwę konta administratora, która ma być używana dla wszystkich wystąpień maszyny wirtualnej w VMSS. <br>
**Ograniczenie dotyczące systemu Windows:** Nie można zakończyć \" .\" <br>
**Niedozwolone wartości:** \" Administrator \" , \" administrator \" , \" użytkownik \" , \" Użytkownik1 \" , \" test \" , Jan, \" \" \" Test1 \" , \" user3 \" , \" admin1 \" , \" 1 \" , \" 123 \" , \" a \" , \" actuser \" , \" adm \" , \" admin2 \" , \" ASPNET, \" Backup, Console, \" \" \" \" \" David \" , \" gość \" , \" Jan \" , \" właściciel \" , \" katalog_główny \" , \" serwer \" , \" SQL \" , \" Obsługa \" , \" Support_388945a0 \" , \" sys \" , \" Test2 \" , \" test3 \" , \" user4 \" , \" user5 \" . <br>
**Minimalna długość (Linux):** 1 znak <br>
**Max-length (Linux):** 64 znaków <br>
**Maks.-length (Windows):** 20 znaków  <br>
<li> Aby uzyskać dostęp do maszyny wirtualnej Linux, zobacz [Używanie uprawnień głównych na maszynach wirtualnych systemu Linux na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).<br>
<li> Aby uzyskać listę wbudowanych użytkowników systemu Linux, których nie należy stosować w tym polu, zobacz [Wybieranie nazw użytkowników dla systemu Linux na platformie Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ComputerNamePrefix
Określa prefiks nazwy komputera dla wszystkich wystąpień maszyny wirtualnej w VMSS.
Nazwy komputerów muszą zawierać od 1 do 15 znaków.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomData
Określa zakodowany ciąg Base-64 z danymi niestandardowymi.
Ta tablica jest zdekodowana do tablicy binarnej zapisanej jako plik na maszynie wirtualnej.
Maksymalna długość tablicy binarnej to 65535 bajtów. <br>
Aby uzyskać informacje na temat używania chmury-init dla maszyny wirtualnej, zobacz [Używanie chmury-init w celu dostosowania maszyny wirtualnej Linux podczas jej tworzenia](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json).

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

### -LinuxConfigurationDisablePasswordAuthentication
Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasła.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Listener
Określa detektory zdalnego zarządzania systemem Windows (WinRM).
Spowoduje to włączenie zdalnego środowiska Windows PowerShell.
Do utworzenia odbiornika można użyć polecenia cmdlet Add-AzVmssWinRMListener.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.WinRMListener[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PublicKey
Określa obiekt klucza publicznego powłoki Secure Shell (SSH).
Aby utworzyć obiekt, możesz użyć polecenia cmdlet Add-AzVMSshPublicKey.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.SshPublicKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Secret
Określa obiekt tajny, który zawiera odwołania do certyfikatu do umieszczenia na maszynie wirtualnej.
Aby utworzyć obiekt sekretny, możesz użyć polecenia cmdlet Add-AzVmssSecret.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TimeZone
Określa strefę czasową maszyny wirtualnej. na przykład \" Pacyfik (czas standardowy) \" . <br>
Możliwe wartości mogą być [TimeZoneInfo.ID](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) wartością ze stref czasowych zwróconych przez [TimeZoneInfo. GetSystemTimeZones](https://docs.microsoft.com/en-us/dotnet/api/system.timezoneinfo.getsystemtimezones).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określa obiekt VMSS.
Aby utworzyć obiekt, możesz użyć polecenia cmdlet New-AzVmssConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WindowsConfigurationEnableAutomaticUpdate
Wskazuje, czy na komputerach wirtualnych w VMSS są włączone aktualizacje automatyczne.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsConfigurationProvisionVMAgent
Wskazuje, czy należy zainicjować obsługę administracyjną agenta maszyny wirtualnej na maszynach wirtualnych w VMSS.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet

### System. String

### System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]

### Microsoft. Azure. Management. COMPUTE. MODELES. AdditionalUnattendContent []

### Microsoft. Azure. Management. COMPUTE. MODELES. WinRMListener []

### Microsoft. Azure. Management. COMPUTE. MODELES. SshPublicKey []

### Microsoft. Azure. Management. COMPUTE. MODELES. VaultSecretGroup []

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Dodaj-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Dodaj-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Dodaj-AzVmssSecret](./Add-AzVmssSecret.md)

[Nowe — AzVmssConfig](./New-AzVmssConfig.md)


