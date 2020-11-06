---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBginfoExtension.md
ms.openlocfilehash: c52be698b216d206fe95ba5ea3aefc810f22fff2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526925"
---
# Set-AzureRmVMBginfoExtension

## STRESZCZENIe
Dodaje rozszerzenie BGInfo do maszyny wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureRmVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmVMBGInfoExtension** dodaje rozszerzenie BgInfo do maszyny wirtualnej.

## Przykłady

### Przykład 1: Dodawanie rozszerzenia BGInfo do maszyny wirtualnej
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM"
```
To polecenie powoduje dodanie rozszerzenia BGInfo do maszyny wirtualnej o nazwie ContosoVM w ContosoRG grup zasobów.

### Przykład 2: dodawanie określonej wersji rozszerzenia BGInfo do maszyny wirtualnej
```
PS C:\> Set-AzureRmVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

To polecenie umożliwia dodanie rozszerzenia BGInfo do maszyny wirtualnej o nazwie ContosoVM.
To polecenie określa grupę zasobów i lokalizację maszyny wirtualnej.
Polecenie określa nazwę i wersję rozszerzenia.

## PARAMETRÓW

### -DisableAutoUpgradeMinorVersion
Wskazuje, że to polecenie cmdlet uniemożliwia agentowi gościa platformy Azure automatyczne aktualizowanie rozszerzenia do nowszej wersji pomocniczej.
Domyślnie to polecenie cmdlet umożliwia agentowi gościa aktualizowanie rozszerzenia.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceRerun
Określa, że rozszerzenie powinno być ponownie uruchomione z tymi samymi ustawieniami publicznymi lub chronionymi.
Wartością może być dowolny ciąg różny od bieżącej wartości.

Jeśli forceUpdateTag nie zostanie zmieniony, aktualizacje do ustawień publicznych lub chronionych są nadal stosowane przez program obsługi.

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

### — Lokalizacja
Określa lokalizację maszyny wirtualnej.

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
Określa nazwę rozszerzenia BGInfo, które to polecenie cmdlet dodaje do maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej, z którą to polecenie cmdlet dodaje rozszerzenie.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Określa wersję rozszerzenia, które to polecenie cmdlet dodaje do maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej, do której to polecenie cmdlet dodaje rozszerzenie BGInfo.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.

Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

