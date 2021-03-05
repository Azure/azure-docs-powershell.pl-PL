---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: 2af8125f91618cd929a9389d9327532376e92af1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991334"
---
# Get-AzEventGridTopic

## SYNOPSIS
Pobiera szczegółowe informacje na temat siatki zdarzeń lub listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.

## SKŁADNIA

### ResourceGroupNameParameterSet (Ustawienie domyślne)
```
Get-AzEventGridTopic [[-ResourceGroupName] <String>] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### TopicNameParameterSet
```
Get-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie Get-AzEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.
Jeśli podano nazwę tematu, są zwracane szczegóły pojedynczego tematu siatki zdarzeń.
Jeśli nazwa tematu nie jest podano, zostanie zwrócona lista tematów. Liczba elementów zwracanych na tej liście jest kontrolowana przez parametr Top. Jeśli wartość najwyższa nie zostanie określona lub $null, lista będzie zawierać wszystkie tematy. W przeciwnym razie top wskaże maksymalną liczbę elementów, które mają zostać zwrócone na liście.
Jeśli nadal dostępnych jest więcej tematów, wartość w programie NextLink powinna być używana podczas następnego połączenia w celu uzyskania następnej strony tematów.
Na koniec parametr ODataQuery służy do filtrowania wyników wyszukiwania. Zapytanie filtrujące korzysta ze składni OData tylko przy użyciu właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Pobiera szczegółowe informacje na temat siatki \` zdarzeń tematu1 \` w grupie zasobów \` MyResourceGroupName. \`

### Przykład 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Pobiera szczegółowe informacje na temat siatki \` zdarzeń tematu1 \` w grupie zasobów \` MyResourceGroupName. \`

### Przykład 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Lista wszystkich tematów dotyczących siatki zdarzeń w grupie zasobów \` MyResourceGroupName \` bez podziałów na strony.

### Przykład 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Lista pierwszych 10 tematów dotyczących siatki zdarzeń (jeśli są takie tematy) w grupie zasobów Nazwa_grupy Zasobów, która spełnia $odataFilter \` \` grupy. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. Aby uzyskać dostęp do kolejnych stron tematów, użytkownik powinien na przykład ponownie na Get-AzEventGridTopic z wynikami. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Wymień wszystkie tematy siatki zdarzeń w subskrypcji bez podziałów na strony.

### Przykład 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

W subskrypcji należy wyświetlić 10 pierwszych tematów dotyczących siatki zdarzeń (jeśli są takie), które spełnią $odataFilter zapytania. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. Aby uzyskać dostęp do kolejnych stron tematów, użytkownik powinien na przykład ponownie na Get-AzEventGridTopic z wynikami. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

## PARAMETERS

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure

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

### — Nazwa
Nazwa tematu w aplikacji EventGrid.

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Link do następnej strony zasobów do pobrania. Ta wartość jest uzyskiwana w przypadku pierwszego Get-AzEventGrid cmdlet, gdy nadal jest dostępnych więcej zasobów do zapytania.

```yaml
Type: System.String
Parameter Sets: NextLinkParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ODataQuery
Zapytanie OData używane do filtrowania wyników listy. Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
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
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Na górze
Maksymalna liczba zasobów, które mają zostać uzyskane. Prawidłowa wartość to między 1 a 100. Jeśli zostanie określona najwyższa wartość i nadal będzie dostępnych więcej wyników, wynik będzie zawierać link do następnej strony, do czego ma zostać zaadysowane zapytanie w programie NextLink. Jeśli nie zostanie określona najwyższa wartość, pełna lista zasobów zostanie zwrócona jednocześnie.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ResourceGroupNameParameterSet, TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicListInstance

## NOTATKI

## LINKI POKREWNE
