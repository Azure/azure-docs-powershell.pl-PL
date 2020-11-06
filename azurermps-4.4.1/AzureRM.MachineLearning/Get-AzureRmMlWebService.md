---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlWebService.md
ms.openlocfilehash: 14fbb8631a15321df9ae6834456649d00caae897
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553849"
---
# Get-AzureRmMlWebService

## STRESZCZENIe
Pobiera informacje podsumowujące dotyczące jednej lub wielu usług sieci Web.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmMlWebService [-ResourceGroupName <String>] [-Name <String>] [-Region <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Pobiera informacje o defintion usługi sieci Web.
W zależności od przekazanego paramenters polecenie cmdlet zwraca defintion dla konkretnej usługi sieci Web, kolekcję defintions dla usług sieci Web dla określonej grupy zasobów w ramach bieżącego abonamentu lub kolekcję defintions dla usług sieci Web w ramach bieżącej subskrypcji.

## Przykłady

### --------------------------Przykład 1: uzyskiwanie szczegółowych informacji o konkretnej usłudze sieci Web--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup" -Name "mywebservicename"
```

### --------------------------Przykład 2: pobieranie wszystkich zasobów usług sieci Web w bieżącej subskrypcji--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlWebService
```

### --------------------------Przykład 3: pobieranie wszystkich usług sieci Web w bieżącej subskrypcji i danej grupie zasobów--------------------------
@ {Paragraph = PS C: \\ \> }





```
Get-AzureRmMlWebService -ResourceGroupName "myresourcegroup"
```

## PARAMETRÓW

### -Name (nazwa)
Nazwa usługi sieci Web, do której są pobierane dane szczegółowe.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Grupa zasobów, z której są pobierane szczegóły dotyczące usługi sieci Web.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Nazwa regionu

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### Znaleziono

## INFORMACYJN
Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, maszyna, nauka maszynowa, Azure

## LINKI POKREWNE

