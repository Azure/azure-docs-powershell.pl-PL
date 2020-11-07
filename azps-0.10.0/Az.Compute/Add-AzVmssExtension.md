---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssExtension.md
ms.openlocfilehash: 97c8824bca395ddd8fb23ebb4750ab35931c5d51
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893865"
---
# Add-AzVmssExtension

## STRESZCZENIe
Dodaje rozszerzenie do VMSS.

## POLECENIA

```
Add-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>]
 [-ForceUpdateTag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Add-AzVmssExtension** dodaje rozszerzenie do zestawu skali maszyny wirtualnej (VMSS).

## Przykłady

### Przykład 1: Dodawanie rozszerzenia do VMSS
```
PS C:\> Add-AzVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

To polecenie powoduje dodanie rozszerzenia do usługi zarządzania maszyną.

## PARAMETRÓW

### -AutoUpgradeMinorVersion
Wskazuje, czy wersja rozszerzenia ma być automatycznie aktualizowana do nowszej wersji pomocniczej.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceUpdateTag
Jeśli wartość jest podana i jest różna od poprzedniej wartości, program obsługi rozszerzeń zostanie zmuszony do zaktualizowania, nawet jeśli konfiguracja rozszerzenia nie została zmieniona.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę rozszerzenia, które zostało dodane przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProtectedSetting
Określa prywatną konfigurację rozszerzenia w postaci ciągu.
To polecenie cmdlet szyfruje konfigurację prywatną.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wydawca
Określa nazwę wydawcy rozszerzenia.
Gdy program Publisher zarejestruje rozszerzenie, program Publisher podaje nazwę.
Może to zrobić za pomocą polecenia cmdlet [Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md) w celu uzyskania wydawcy.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Setting
Określa konfigurację publiczną w postaci ciągu dla rozszerzenia.
To polecenie cmdlet nie szyfruje konfiguracji publicznej.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
Określa typ rozszerzenia.
Aby uzyskać typ rozszerzenia, można użyć polecenia cmdlet [Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Określa wersję rozszerzenia, która ma być używana dla tej maszyny wirtualnej.
Aby uzyskać wersję rozszerzenia, możesz użyć polecenia cmdlet [Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
Określ obiekt VMSS.
Aby utworzyć obiekt, możesz użyć [nowego-AzVmssConfig](./New-AzVmssConfig.md) .

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### VirtualMachineScaleSet
Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu

## WYSYŁA

###  
To polecenie cmdlet nie generuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzVmssExtension](./Remove-AzVmssExtension.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMExtensionImageType](./Get-AzVMExtensionImageType.md)

[Get-AzVMExtensionImage](./Get-AzVMExtensionImage.md)

[Nowe — AzVmssConfig](./New-AzVmssConfig.md)
