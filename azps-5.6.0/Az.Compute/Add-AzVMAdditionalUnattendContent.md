---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMAdditionalUnattendContent.md
ms.openlocfilehash: 2ec50d8e0c11143f72e327a7b73784c1a49e926c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991565"
---
# Add-AzVMAdditionalUnattendContent

## SYNOPSIS
Umożliwia dodanie informacji do nienadzorowanych plików odpowiedzi Instalatora systemu Windows.

## SKŁADNIA

```
Add-AzVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Add-AzVMAdditionalUnattendContent** umożliwia dodanie informacji do nienadzorowanych plików odpowiedzi Instalatora systemu Windows.
Określ dodatkowe informacje w formacie xml z kodem base 64, które to polecenie cmdlet dodaje do unattend.xml pliku.

## PRZYKŁADY

### Przykład 1. Dodawanie zawartości do unattend.xml
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie Grupa Zasobów11, a następnie przechowuje ten obiekt w zmiennej $AvailabilitySet zasobów.
Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie przechowuje go w $VirtualMachine zmienną.
To polecenie przypisuje nazwę i rozmiar do maszyny wirtualnej.
Maszynę wirtualną należy do zestawu dostępności przechowywanego w $AvailabilitySet.
Trzecie polecenie tworzy obiekt poświadczeń przy użyciu Get-Credential cmdlet, a następnie zapisuje wynik w $Credential danych.
Polecenie monituje o nazwę użytkownika i hasło.
Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .
Czwarte polecenie używa polecenia **cmdlet Set-AzVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.
Piąte polecenie przypisuje zawartość do zmiennej $AucContent danych.
Zawartość zawiera hasło.
Ostatnie polecenie dodaje zawartość przechowywaną w pliku $AucContent do unattend.xml pliku.

## PARAMETERS

### — Zawartość
Określa zawartość zakodowaną w formacie XML o podstawie 64.
To polecenie cmdlet dodaje zawartość do unattend.xml pliku.
Zawartość XML musi mieć mniej niż 4 KB i musi zawierać element główny ustawienia lub funkcji wstawianych przez to polecenie cmdlet.

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

### -SettingName
Określa nazwę ustawienia, którego dotyczy zawartość.
Dopuszczalne wartości dla tego parametru to:
- FirstLogonCommands
- AutoLogon

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — MASZYNY WIRTUALNEJ
Określa obiekt maszyny wirtualnej, który zostanie zmodyfikowany przez to polecenie cmdlet.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzVM.](./Get-AzVM.md)
Utwórz obiekt maszyny wirtualnej za pomocą polecenia cmdlet [New-AzVMConfig.](./New-AzVMConfig.md)

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.SettingNames, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## NOTATKI

## LINKI POKREWNE

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

[New-AzVMConfig](./New-AzVMConfig.md)
