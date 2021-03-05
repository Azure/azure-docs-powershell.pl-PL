---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 665f090f8de059afa4a7f1bd95685e3364a21611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991362"
---
# Get-AzEventGridSubscription

## SYNOPSIS
Pobiera szczegóły subskrypcji zdarzeń lub pobiera listę wszystkich subskrypcji zdarzeń w bieżącej subskrypcji platformy Azure.

## SKŁADNIA

### EventSubscriptionTopicNameParameterSet (Domyślne)
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-TopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceId] <String> [-IncludeFullEndpointUrl]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [-EventSubscriptionName <String>] [-ResourceGroupName <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [-ResourceGroupName <String>] [-TopicTypeName <String>] [-Location <String>]
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionCustomTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-InputObject] <PSTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionDomainTopicInputObjectParameterSet
```
Get-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridSubscription [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie cmdlet Get-AzEventGridSubscription pobiera szczegóły określonej subskrypcji siatki zdarzeń lub listę wszystkich subskrypcji siatki zdarzeń w bieżącej subskrypcji platformy Azure lub grupie zasobów.
Jeśli podano nazwę subskrypcji zdarzenia, zwracane są szczegóły pojedynczej subskrypcji siatki zdarzeń.
Jeśli nazwa subskrypcji wydarzenia nie jest podano, zostanie zwrócona lista wszystkich subskrypcji zdarzeń. Liczba elementów zwracanych na tej liście jest kontrolowana przez parametr Top. Jeśli wartość Top nie zostanie określona lub $null, lista będzie zawierać wszystkie elementy subskrypcji zdarzeń. W przeciwnym razie top wskaże maksymalną liczbę elementów, które mają zostać zwrócone na liście.
Jeśli nadal dostępnych jest więcej subskrypcji zdarzeń, wartość w programie NextLink powinna być używana podczas następnego połączenia w celu uzyskania następnej strony subskrypcji zdarzeń.
Na koniec parametr ODataQuery służy do filtrowania wyników wyszukiwania. Zapytanie filtrujące korzysta ze składni OData tylko przy użyciu właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.

## PRZYKŁADY

### Przykład 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Pobiera szczegóły subskrypcji zdarzenia EventSubscription1 utworzonej dla tematu Topic1 w grupie zasobów \` \` \` \` \` MyResourceGroupName. \`

### Przykład 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Pobiera szczegółowe informacje dotyczące subskrypcji zdarzeń EventSubscription1 utworzonej dla tematu Topic1 w grupie zasobów \` \` Nazwa_grupy Zasobów \` \` \` MyResourceGroupName, \` w tym pełny adres URL punktu końcowego, jeśli jest to subskrypcja zdarzeń oparta na sieci Web.

### Przykład 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Uzyskaj listę wszystkich subskrypcji zdarzeń utworzonych dla tematu Temat1 w grupie zasobów \` \` \` Nazwa_grupy_zasobów Bez \` podziałów na strony.

### Przykład 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 10 subskrypcji zdarzeń (jeśli są) utworzonych dla tematu Temat1 w grupie zasobów Nazwa_grupy zasobów, która spełnia $odataFilter \` \` \` \` zapytania. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Pobiera szczegółowe informacje dotyczące subskrypcji zdarzeń \` EventSubscription1 utworzonej dla \` grupy zasobów \` Nazwa_grupy_zasobów. \`

### Przykład 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonej dla obecnie wybranej subskrypcji platformy Azure.

### Przykład 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Pobiera listę wszystkich subskrypcji zdarzeń globalnych utworzonych w ramach grupy zasobów \` MyResourceGroupName \` bez podziałów na strony.

### Przykład 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 5 subskrypcji zdarzeń (jeśli są tworzone) utworzonych w ramach grupy zasobów Nazwa_grupy zasobów, spełniających $odataFilter \` \` grupy zasobów. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Pobiera listę wszystkich subskrypcji wydarzenia globalnego utworzonych w ramach obecnie wybranej subskrypcji platformy Azure bez podziałów na strony.

### Przykład 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 15 subskrypcji zdarzeń globalnych (jeśli są dostępne) utworzonych w ramach obecnie wybranej subskrypcji platformy Azure, które zaspokajają $odataFilter usługi. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Pobiera listę wszystkich subskrypcji zdarzeń regionalnych utworzonych w grupie zasobów MyResourceGroupName w określonej lokalizacji \` \` na \` zachódus2 \` bez podziałów na strony.

### Przykład 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 15 subskrypcji zdarzeń regionalnych (jeśli są tworzone) utworzonych w ramach grupy zasobów Nazwa_grupy zasobów MyResourceGroupName w określonej lokalizacji \` \` \` westus2, która spełnia $odataFilter \` grupy zasobów. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonej przestrzeni nazw aplikacji EventHub bez podziałów na strony.

### Przykład 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 25 subskrypcji zdarzeń (jeśli są one utworzone) dla określonej przestrzeni nazw aplikacji EventHub, która spełnia $odataFilter zapytania. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego typu tematu (przestrzenie nazw aplikacji EventHub) w określonej lokalizacji bez podziałów na strony.

### Przykład 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 15 subskrypcji zdarzeń (jeśli są one utworzone) dla określonego typu tematu (przestrzenie nazw aplikacji EventHub) w określonej lokalizacji, która spełnia $odataFilter zapytania. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

### Przykład 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonej grupy zasobów bez podziałów na strony.

### Przykład 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 100 subskrypcji zdarzeń (jeśli są) utworzonych dla określonej grupy zasobów, która spełnia $odataFilter zapytania. Jeśli dostępnych jest więcej wyników, $result. Nie można $null NextLink. W celu uzyskania kolejnych stron subskrypcji zdarzeń użytkownik powinien ponownie na Get-AzEventGridSubscription korzysta z wyników. Przycisk NextLink uzyskany z poprzedniej rozmowy. Po wyniku powinna zostać zatrzymana dzwoniąca. NextLink staje się $null.

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

### -DomainInputObject
Obiekt Domeny EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainName
Nazwa domeny EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DomainTopicInputObject
Obiekt tematu domeny EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DomainTopicName
Nazwa tematu domeny EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventSubscriptionName
Nazwa subskrypcji wydarzenia

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Uwzględnij pełny adres URL punktu końcowego miejsca docelowego subskrypcji zdarzenia.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Obiekt tematu w aplikacji EventGrid.

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### — Lokalizacja
Lokalizacja

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
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
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu, do którego utworzono subskrypcje zdarzeń.

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Na górze
Zapytanie OData używane do filtrowania wyników listy. Filtrowanie jest obecnie dozwolone tylko we właściwości Name. Obsługiwane operacje to: CONTAINS, eq (dla równości), ne (dla nie równa się), ORAZ, LUB i NIE.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionDomainNameParameterSet, EventSubscriptionTopicTypeNameParameterSet, EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicName
Nazwa tematu w aplikacji EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
Nazwa topicType

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
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

### Microsoft.Azure.Commands.EventGrid.Models.PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription

## NOTATKI

## LINKI POKREWNE
