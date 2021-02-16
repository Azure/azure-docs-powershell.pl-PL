---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: 667a8214fc7df27ce46dc28ddbdeabd1b00dce5b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194987"
---
# Set-AzVMAccessExtension

## SYNOPSIS
Dodaje rozszerzenie MACHINEAccess do maszyny wirtualnej.

## SKŁADNIA

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVMAccessExtension** dodaje do maszyny wirtualnej rozszerzenie MACHINE MACHINEACCESSAccess (Virtual Machine Access). Rozszerzenie PROGRAMU VMAccess może być używane do ustawienia hasła tymczasowego i należy je zmienić natychmiast po zalogowaniu się na komputerze. Nie jest to obsługiwane w kontrolerach domen systemu Windows.

## PRZYKŁADY

### Przykład 1. Dodawanie rozszerzenia PROGRAMU VMAccess
```powershell
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.4" -UserName "PFuller" -Password "Password"
```

To polecenie powoduje dodanie rozszerzenia MACHINEAccess dla maszyny wirtualnej o nazwie VirtualMachine07 w grupie ResourceGroup11.
To polecenie określa wersję obsługi typu i nazwy programu obsługi dla programu VMAccess.

### Przykład 2

Dodaje rozszerzenie MACHINEAccess do maszyny wirtualnej. (wygenerowane automatycznie)

```powershell <!-- Aladdin Generated Example --> 
Set-AzVMAccessExtension -Credential <PSCredential> -Location 'Central US' -Name 'ContosoTest' -ResourceGroupName 'ResourceGroup11' -TypeHandlerVersion '2.4' -VMName 'VirtualMachine07'
```

## PARAMETERS

### - Credential
Określa nazwę użytkownika i hasło dla maszyny wirtualnej jako **obiekt PSCredential.**
Jeśli wpiszesz nazwę inną niż bieżące konto administratora lokalnego w maszyny wirtualnej, rozszerzenie PROGRAMU VMAccess doda lokalne konto administratora o tej nazwie i przypisze do tego konta określone hasło. Jeśli lokalne konto administratora na maszyny wirtualnej już istnieje, zresetuje hasło, a jeśli konto jest wyłączone, zostanie w nim własne rozszerzenie PROGRAMU VMAccess.
Aby uzyskać poświadczenia, użyj Get-Credential cmdlet.
Aby uzyskać więcej informacji, wpisz `Get-Help Get-Credential` .

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -DisableAutoUpgradeMinorVersion
```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
Wskazuje, że to polecenie cmdlet wymusza ponowne uruchomić tę samą konfigurację rozszerzenia na komputerze wirtualnym bez odinstalowywania i ponownego instalowania rozszerzenia.
Wartość może być dowolnym ciągiem innym niż bieżąca wartość.
Jeśli forceUpdateTag nie zostanie zmieniony, program obsługi nadal stosuje aktualizacje ustawień publicznych lub chronionych.

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

### — Lokalizacja
Określa lokalizację maszyny wirtualnej.

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

### — Nazwa
Określa nazwę rozszerzenia, które dodaje to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NoWait
Rozpoczyna operację i zwraca bezpośrednio przed jej ukończeniem. Aby ustalić, czy operacja została pomyślnie ukończona, użyj innego mechanizmu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.
Aby uzyskać wersję, uruchom Get-AzVMExtensionImage cmdlet z wartością Microsoft.Compute dla parametru *PublisherName* i VMAccessAgent dla *parametru Type.* TypeHandlerVersion musi mieć wartość 2.0 lub większą, ponieważ wersja 1 jest przestarzała.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Określa nazwę maszyny wirtualnej.
To polecenie cmdlet dodaje program MACHINEAccess dla maszyny wirtualnej, która określa ten parametr.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.Management.Automation.PSCredential

### System.String

### System.Management.Automation.SwitchParameters

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTATKI

## LINKI POKREWNE

[Get-AzVMAccessExtension](./Get-AzVMAccessExtension.md)

[Remove-AzVMAccessExtension](./Remove-AzVMAccessExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)


