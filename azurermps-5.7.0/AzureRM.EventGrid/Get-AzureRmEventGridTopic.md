---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopic.md
ms.openlocfilehash: e71c479624cd77e25adbd4fbfdc609cfa89918b3
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/21/2020
ms.locfileid: "93719685"
---
# Get-AzureRmEventGridTopic

## STRESZCZENIe
Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### ResourceGroupNameParameterSet (domyślny)
```
Get-AzureRmEventGridTopic [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzureRmEventGridTopic [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzureRmEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.
W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.
Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów.

## Przykłady

### Przykład 1
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .

### Przykład 2
```
PS C:\> Get-AzureRmEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .

### Przykład 3
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName
```

Lista wszystkich tematów dotyczących siatki zdarzeń w MyResourceGroupName grupy \` zasobów \` .

### Przykład 4
```
PS C:\> Get-AzureRmEventGridTopic
```

Lista wszystkich tematów siatki zdarzeń w ramach subskrypcji.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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
Nazwa tematu EventGrid.

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu reprezentujący temat siatki zdarzeń.

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
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

### System. String
Microsoft. Azure. Commands. EventGrid. models. PSTopic

## WYSYŁA

### Microsoft. Azure. Commands. EventGrid. models. PSTopic
System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventGrid. MODELES. PSTopicListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]

## INFORMACYJN

## LINKI POKREWNE

