---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 152d6e861d7622e262279c1f665565347e0ab2cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238960"
---
# Add-AzVmssExtension

## SYNOPSIS
Dodaje rozszerzenie do usługi MASZYNY.WIRTUALNE.

## SKŁADNIA

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-EnableAutomaticUpgrade <Boolean>] [-ForceUpdateTag <String>] [-ProvisionAfterExtension <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet AzVmssExtension dodatku Add-AzVmssExtension** dodaje rozszerzenie do zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set).

## PRZYKŁADY

### Przykład 1. Dodawanie rozszerzenia do maszyn wirtualnych
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

To polecenie powoduje dodanie rozszerzenia do usługi maszyny wirtualnej.

### Przykład 2. Dodawanie rozszerzenia do maszyn wirtualnych z ustawieniami i ustawieniami chronionymi
```
PS C:\> $Settings = @{"fileUris" = "[]"; "commandToExecute" = ""};
PS C:\> $ProtectedSettings = @{"storageAccountName" = $stoname; "storageAccountKey" = $stokey};

PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName -Publisher $vmssPublisher  `
  -Type $vmssExtensionType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True  `
  -Setting $Settings -ProtectedSetting $ProtectedSettings
```

To polecenie powoduje dodanie rozszerzenia do usług VMSS z przykładowym skryptem bash w magazynie obiektów blob, określenie adresu URL magazynu obiektów blob i wykonywalnego polecenia w ustawieniach oraz dostępu zabezpieczeń w ustawieniach chronionych. 

## PARAMETERS

### -AutoUpgradeMinorVersion
Wskazuje, czy wersja rozszerzenia powinna zostać automatycznie zaktualizowana do nowszej wersji pomocniczej.

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

### -EnableAutomaticUpgrade
Wskazuje, czy rozszerzenie powinno zostać automatycznie uaktualnione przez platformę, jeśli jest dostępna nowsza wersja rozszerzenia.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceUpdateTag
Jeśli podano wartość inną niż poprzednia, program obsługi rozszerzenia będzie musiał zaktualizować plik nawet wtedy, gdy konfiguracja rozszerzenia się nie zmieniła.

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
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProtectedSetting
Określa prywatną konfigurację rozszerzenia jako ciąg.
To polecenie cmdlet szyfruje konfigurację prywatną.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProvisionAfterExtension
Zbiór nazw rozszerzeń, po których to rozszerzenie wymaga obsługi administracyjnej.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Publisher
Określa nazwę wydawcy rozszerzenia.
Po zarejestrowaniu rozszerzenia wydawca podaje jego nazwę.
Aby pobrać wydawcę, możesz użyć polecenia cmdlet [Get-AzVMImagePublisher.](./Get-AzVMImagePublisher.md)

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

### — Ustawienie
Określa konfigurację publiczną jako ciąg rozszerzenia.
To polecenie cmdlet nie szyfruje konfiguracji publicznej.

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wpisz
Określa typ rozszerzenia.
Aby pobrać typ rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImageType.](./Get-AzVMExtensionImageType.md)

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

### -TypeHandlerVersion
Określa wersję rozszerzenia do użycia dla tej maszyny wirtualnej.
Aby pobrać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImage.](./Get-AzVMExtensionImage.md)

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

### -VirtualMachineScaleSet
Określanie obiektu MASZYNY.MASZYNY.WIRTUALNE.
Aby utworzyć obiekt, możesz użyć konfiguracji [New-AzVmssConfig.](./New-AzVmssConfig.md)

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

### System.Object

## OUTPUTS

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet

## NOTATKI

## LINKI POKREWNE

[Remove-AzVmssExtension](./Remove-AzVmssExtension.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)

[New-AzVmssConfig](./New-AzVmssConfig.md)
