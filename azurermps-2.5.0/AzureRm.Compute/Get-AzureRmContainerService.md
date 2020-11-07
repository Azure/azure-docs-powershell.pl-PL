---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: AFF75E0B-CB88-45ED-9067-7F43E2BA485C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcontainerservice
schema: 2.0.0
ms.openlocfilehash: 5db21871b84801d57deebf98e27bbe153285631a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899387"
---
# Get-AzureRmContainerService

## STRESZCZENIe
Pobiera usługę kontenera.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmContainerService [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmContainerService** pobiera usługę kontenera.
Możesz wyświetlić właściwości usługi kontenera zawierającej stan, liczbę wzorców i agentów oraz w pełni kwalifikowaną nazwę domeny dla wzorców i agentów.

## Przykłady

### Przykład 1: Uzyskiwanie usługi kontenera
```
PS C:\> Get-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

To polecenie uzyskuje usługę kontenera o nazwie CSResourceGroup17.

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

### -Name (nazwa)
Określa nazwę usługi kontenera, która jest pobierana przez to polecenie cmdlet.

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

### -ResourceGroupName
Określa grupę zasobów usługi kontenera, która jest pobierana przez to polecenie cmdlet.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSContainerService

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzureRmContainerService](./New-AzureRmContainerService.md)

[Remove-AzureRmContainerService](./Remove-AzureRmContainerService.md)

[Update-AzureRmContainerService](./Update-AzureRmContainerService.md)


