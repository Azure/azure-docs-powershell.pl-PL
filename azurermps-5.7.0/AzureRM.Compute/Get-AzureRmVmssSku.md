---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BB6AFC7D-7E74-4D39-B336-A011B98D0682
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVmssSku.md
ms.openlocfilehash: c86bf549c0de3643aaba67143b7df78f6fce798c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526958"
---
# Get-AzureRmVmssSku

## STRESZCZENIe
Pobiera dostępne jednostki SKU dla VMSS.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVmssSku [-ResourceGroupName] <String> [-VMScaleSetName] <String> [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVmssSku** Pobiera dostępne jednostki SKU zestawu skali maszyny wirtualnej (VMSS).

## Przykłady

### Przykład 1. Pobierz wszystkie dostępne jednostki SKU z VMSS
```
PS C:\> Get-AzureRmVmssSku -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

To polecenie pobiera wszystkie dostępne jednostki SKU z VMSS o nazwie ContosoVMSS należącej do grupy zasobów o nazwie contoso.

## PARAMETRÓW

### -ResourceGroupName
Określa nazwę grupy zasobów VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
Gatunek nazwy VMSS.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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

### To polecenie cmdlet nie produkuje żadnych danych wyjściowych.

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVmss](./Get-AzureRmVmss.md)


