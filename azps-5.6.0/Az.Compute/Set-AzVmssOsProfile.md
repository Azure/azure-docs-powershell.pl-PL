---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3E7B9EFA-8BC2-46EB-9AD7-43EAB7FF3891
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvmssosprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssOsProfile.md
ms.openlocfilehash: 046812a0339a0dd33df140f29e00ec8b882c91cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958890"
---
# Set-AzVmssOsProfile

## SYNOPSIS
Ustawia właściwości profilu systemu operacyjnego MASZYNY WIRTUALNE.

## SKŁADNIA

```
Set-AzVmssOsProfile [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-ComputerNamePrefix] <String>]
 [[-AdminUsername] <String>] [[-AdminPassword] <String>] [[-CustomData] <String>]
 [[-WindowsConfigurationProvisionVMAgent] <Boolean>] [[-WindowsConfigurationEnableAutomaticUpdate] <Boolean>]
 [[-TimeZone] <String>] [[-AdditionalUnattendContent] <AdditionalUnattendContent[]>]
 [[-Listener] <WinRMListener[]>] [[-LinuxConfigurationDisablePasswordAuthentication] <Boolean>]
 [[-PublicKey] <SshPublicKey[]>] [[-Secret] <VaultSecretGroup[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVmssOsProfile** ustawia właściwości profilu systemu operacyjnego skalowania maszyny wirtualnej.

## PRZYKŁADY

### Przykład 1. Ustawianie właściwości profilu systemu operacyjnego dla usługi maszyny wirtualnej
```
PS C:\> Set-AzVmssOSProfile -VirtualMachineScaleSet "ContosoVMSS" -ComputerNamePrefix "Test" -AdminUsername $AdminUsername -AdminPassword $AdminPassword
```

To polecenie ustawia właściwości profilu systemu operacyjnego dla maszyn wirtualnych należących do maszyn wirtualnych o nazwie ContosoVMSS.
Polecenie ustawia prefiks nazwy komputera dla wszystkich wystąpień maszyn wirtualnych w usługach VIRTUALSS w celu przetestowania oraz dostarcza nazwę użytkownika i hasło administratora.

## PARAMETERS

### -AdditionalUnattendContent
Określa nienadzorowany obiekt zawartości.
Za pomocą Add-AzVMAdditionalUnattendContent można utworzyć obiekt.

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
Określa hasło administratora, które ma być dla wszystkich wystąpień maszyn wirtualnych w usługach VIRTUALSS.

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
Określa nazwę konta administratora do użycia dla wszystkich wystąpień maszyn wirtualnych w usługach WIRTUALNEJ maszyny wirtualnej. <br>
**Ograniczenia dostępne tylko w systemie Windows:** Nie może kończyć się \" na.\" <br>
**Niedozwolone wartości:** \" \"administrator, \" \" administrator, \" \" użytkownik, \" \" użytkownik1, \" \" test, \" \" user2, \" \" test1, \" \" user3, \" \" admin1, \" \" 1, \" 123, \" \" \" a, \" \" actuser, \" \" adm, \" \" admin2, \" \" aspnet, \" \" backup, \" \" console, \" \" \" \" david, guest, \" \" \" \" john, owner, \" \" root, \" \" server, \" sql, \" \" \" support, \" \" support_388945a0, \" \" sys, \" \" test2, \" \" test3, \" \" user4, \" \" user5. <br>
**Minimalna długość (Linux):** 1 znak <br>
**Maksymalna długość (Linux):** 64 znaki <br>
**Maksymalna długość (w systemie Windows):** 20 znaków  <br>
<li> Aby uzyskać dostęp główny do maszyny wirtualnej systemu Linux, zobacz Korzystanie z uprawnień głównych na komputerach wirtualnych systemu [Linux na platformie Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-use-root-privileges?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
<li> Aby uzyskać listę wbudowanych użytkowników systemu Linux, których nie należy używać w tym polu, zobacz Wybieranie nazw użytkowników systemu Linux na [platformie Azure.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-usernames?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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
Określa prefiks nazwy komputera dla wszystkich wystąpień maszyn wirtualnych w programie VIRTUALSS.
Nazwy komputerów muszą mieć od 1 do 15 znaków.

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

### - CustomData
Określa zakodowany ciąg danych niestandardowych o podstawie 64.
Jest on dekodowany do tablicy binarnej zapisanej jako plik na komputerze wirtualnym.
Maksymalna długość tablicy binarnej to 65 535 bajtów. <br>
Aby uzyskać informacje na temat korzystania z init w chmurze dla maszyny wirtualnej, zobacz Dostosowywanie maszyny wirtualnej systemu Linux podczas tworzenia za pomocą [init w chmurze.](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-using-cloud-init?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)

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

### -LinuxConfigurationDisablePasswordAuthentication
Wskazuje, że to polecenie cmdlet wyłącza uwierzytelnianie hasłem.

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

### - Słuchacz
Określa słuchaczy usługi Zarządzanie zdalne systemu Windows (WinRM).
Umożliwia to zdalne korzystanie z programu Windows PowerShell.
Aby utworzyć słuchacza, Add-AzVmssWinRMListener użyć polecenia cmdlet.

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
Określa obiekt klucza publicznego bezpiecznej powłoki (SSH).
Obiekt można Add-AzVMSshPublicKey za pomocą polecenia cmdlet.

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

### - Tajna
Określa obiekt tajemnic, który zawiera odwołania do certyfikatów, które mają być umieszczane na maszyny wirtualnej.
Możesz użyć tego Add-AzVmssSecret cmdlet, aby utworzyć tajny obiekt.

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

### - Strefa czasowa
Określa strefę czasową maszyny wirtualnej. np. \" Pacyfik (czas \" standardowy). <br>
Możliwe wartości mogą [być](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.id?#System_TimeZoneInfo_Id) TimeZoneInfo.Id z stref czasowych zwracanych przez [TimeZoneInfo.GetSystemTimeZones.](https://docs.microsoft.com/dotnet/api/system.timezoneinfo.getsystemtimezones)

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
Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.
Obiekt można New-AzVmssConfig za pomocą polecenia cmdlet.

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
Wskazuje, czy dla maszyn wirtualnych w usługach MASZYNY WIRTUALNE są włączone aktualizacje automatyczne.

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
Wskazuje, czy agent maszyny wirtualnej powinien być aprowowany na komputerach wirtualnych w maszyny wirtualnej.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

### System.String

### System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### Microsoft.Azure.Management.Compute.Models.AdditionalUnattendContent[]

### Microsoft.Azure.Management.Compute.Models.WinRMListener[]

### Microsoft.Azure.Management.Compute.Models.SshPublicKey[]

### Microsoft.Azure.Management.Compute.Models.VaultSecretGroup[]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTATKI

## LINKI POKREWNE

[Add-AzVMAdditionalUnattendContent](./Add-AzVMAdditionalUnattendContent.md)

[Add-AzVmssWinRMListener](./Add-AzVmssWinRMListener.md)

[Add-AzVMSshPublicKey](./Add-AzVMSshPublicKey.md)

[Add-AzVmssSecret](./Add-AzVmssSecret.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)


