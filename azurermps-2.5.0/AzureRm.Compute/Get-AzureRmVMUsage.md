---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmusage
schema: 2.0.0
ms.openlocfilehash: 210c66f91836b40c719d91907fc78bd907d0fe86
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899382"
---
# Get-AzureRmVMUsage

## STRESZCZENIe
Pobiera użycie licznika rdzenia maszyny wirtualnej dla lokalizacji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
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

### Microsoft. Azure. Commands. COMPUTE. models. PSUsage

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVM](./Get-AzureRmVM.md)


