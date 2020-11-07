---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 1CA26790-C791-4BFD-B986-70F28E3B095B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 7a881b6479561ac7a616158c8054bff592209289
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899341"
---
# Get-AzureRmActionGroup

## STRESZCZENIe
Pobiera grupy akcji.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### BySubscriptionOrResourceGroup (domyślny)
```
Get-AzureRmActionGroup [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByName
```
Get-AzureRmActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmActionGroup umożliwia pobranie** co najmniej jednej grupy akcji.

## Przykłady

### Przykład 1: Uzyskiwanie grupy akcji według identyfikatora subskrypcji
```
PS C:\>Get-AzureRmActionGroup
```

To polecenie umożliwia wyświetlenie listy wszystkich grup akcji dla bieżącej subskrypcji.

### Przykład 2: pobieranie grup akcji dla danej grupy zasobów
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts"
```

To polecenie wyświetla listę grup akcji dla danej grupy zasobów.

### Przykład 3: Uzyskiwanie grupy akcji.
```
PS C:\>Get-AzureRmActionGroup -ResourceGroup "Default-activityLogAlerts" -Name "actionGroup1"
```

To polecenie wyświetla listę (listę z pojedynczym elementem) grupą akcji.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Name (nazwa)
Nazwa grupy akcji.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów

```yaml
Type: System.String
Parameter Sets: BySubscriptionOrResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRmActionGroup](./Set-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Nowe — AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)
