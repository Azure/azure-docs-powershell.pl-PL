---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMUsage.md
ms.openlocfilehash: 5d4f114ef93e0febf7c113f73b8007a9322be752
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718945"
---
# Get-AzureRmVMUsage

## STRESZCZENIe
Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVMUsage [-Location] <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVMUsage** Pobiera liczbę rdzeni maszyny wirtualnej użytkowania dla lokalizacji.

## Przykłady

### Przykład 1: pobieranie użycia licznika podstawowego dla lokalizacji
```
PS C:\> Get-AzureRmVMUsage -Location "Central US"
```

To polecenie uzyskuje użycie licznika rdzenia maszyny wirtualnej dla pozycji Centrala amerykańska.

## PARAMETRÓW

### — Lokalizacja
Określa lokalizację, w której to polecenie cmdlet pobiera użycie licznika rdzenia maszyny wirtualnej.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVM](./Get-AzureRmVM.md)


