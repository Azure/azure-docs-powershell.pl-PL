---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridSubscription.md
ms.openlocfilehash: 987882928ee215ed2da842e924386f5dec8b862f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705502"
---
# Get-AzEventGridSubscription

## STRESZCZENIe
Pobiera szczegóły abonamentu wydarzenia lub pobiera listę wszystkich subskrypcji zdarzeń w bieżącej subskrypcji platformy Azure.

## POLECENIA

### EventSubscriptionTopicNameParameterSet (domyślny)
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdEventSubscriptionParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### EventSubscriptionDomainNameParameterSet
```
Get-AzEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [-DomainName <String>] [-DomainTopicName <String>] [-IncludeFullEndpointUrl] [-ODataQuery <String>]
 [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### EventSubscriptionTopicTypeNameParameterSet
```
Get-AzEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>] [[-Location] <String>]
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

## Opis
Polecenie cmdlet Get-AzEventGridSubscription pobiera szczegóły określonego abonamentu w siatce zdarzeń lub listę wszystkich subskrypcji siatki zdarzeń w bieżącej subskrypcji platformy Azure lub grupie zasobów.
Jeśli jest podana nazwa subskrypcji zdarzenia, zostanie zwrócona wartość szczegółów pojedynczego abonamentu siatki zdarzeń.
Jeśli nie podano nazwy subskrypcji zdarzeń, zostanie zwrócona lista wszystkich subskrypcji zdarzeń. Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy. Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy subskrypcji zdarzeń. W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.
Jeśli dalsze subskrypcje zdarzeń są nadal dostępne, w następnej rozmowie należy użyć wartości z NextLink, aby uzyskać następną stronę abonamentów zdarzeń.
Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania. Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla tematu \` Temat1 \` w MyResourceGroupNameach grupy zasobów \` \` .

### Przykład 2
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla tematu \` Temat1 \` w grupie zasobów \` MyResourceGroupName \` , w tym pełny adres URL punktu końcowego, jeśli jest to subskrypcja zdarzeń oparta na składniku webhook.

### Przykład 3
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

Zapoznaj się z listą wszystkich subskrypcji zdarzeń utworzonych dla tematu \` Temat1 \` w grupie zasób \` MyResourceGroupName \` bez stronicowania.

### Przykład 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 10 abonamentów zdarzeń utworzonych dla tematu \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` , które spełniają zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 5
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla MyResourceGroupName grupy zasobów \` \` .

### Przykład 6
```powershell
PS C:\> Get-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

Pobiera szczegóły subskrypcji zdarzeń \` EventSubscription1 \` utworzonych dla obecnie wybranej subskrypcji platformy Azure.

### Przykład 7
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName
```

Pobiera listę wszystkich globalnych subskrypcji zdarzeń utworzonych w ramach grupy zasobów \` MyResourceGroupName \` bez stronicowania.

### Przykład 8
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Top 5 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 5 abonamentów zdarzeń utworzonych w ramach grupy zasobów \` MyResourceGroupName \` , które spełniają zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 9
```powershell
PS C:\> Get-AzEventGridSubscription
```

Pobiera listę wszystkich globalnych subskrypcji zdarzeń utworzonych w ramach obecnie wybranej subskrypcji platformy Azure bez stronicowania.

### Przykład 10
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 15 abonamentów zdarzeń globalnych (jeśli istnieją) utworzonych w ramach obecnie wybranej subskrypcji platformy Azure spełniającej zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 11
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

Pobiera listę wszystkich regionalnych subskrypcji zdarzeń utworzonych w obszarze grupy zasobów \` MyResourceGroupName \` w określonej lokalizacji \` westus2 \` bez stronicowania.

### Przykład 12
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2 -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 15 abonamentów zdarzeń regionalnych (jeśli istnieją) utworzonych w obszarze grup zasobów \` MyResourceGroupName \` w określonej lokalizacji \` westus2 \` , która spełnia zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 13
```powershell
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego obszaru nazw EventHub bez stronicowania.

### Przykład 14
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" -Top 25 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 25 abonamentów zdarzeń utworzonych dla określonego obszaru nazw EventHub, który spełnia warunki kwerendy $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 15
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla określonego typu tematu (obszary nazw EventHub) w określonej lokalizacji bez podziału na strony.

### Przykład 16
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location -Top 15 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 15 abonamentów zdarzeń utworzonych dla określonego typu tematu (obszary nazw EventHub) w określonej lokalizacji spełniającej zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 17
```powershell
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

Pobiera listę wszystkich subskrypcji zdarzeń utworzonych dla konkretnej grupy zasobów bez podziału na strony.

### Przykład 18
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> Get-AzEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName -Top 100 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridSubscription $result.NextLink
```

Lista pierwszych 100ych subskrypcji zdarzeń (jeśli istnieją) utworzonych dla konkretnej grupy zasobów, które spełniają zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony subskrypcji zdarzeń, użytkownik powinien ponownie zadzwonić Get-AzEventGridSubscription i używa wyniku. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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
Obiekt domeny EventGrid.

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

### -NazwaDomeny
EventGrid nazwa domeny.

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
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeFullEndpointUrl
Dołącz pełny adres URL punktu końcowego do miejsca docelowego subskrypcji zdarzenia.

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

### -Inputobject
Obiekt tematu EventGrid.

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
Pozycję

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
Łącze do następnej strony, które mają zostać uzyskane. Ta wartość jest uzyskiwana za pomocą pierwszego Get-AzEventGrid polecenia cmdlet, gdy więcej zasobów jest wciąż dostępnych do zbadania.

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
Kwerenda OData używana do filtrowania wyników listy. Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

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
Position: 0
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

### -Początek
Kwerenda OData używana do filtrowania wyników listy. Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

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

### -Tematname
Nazwa tematu EventGrid.

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TopicTypeName
Nazwa tematu

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
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

### System. String

### Microsoft. Azure. Commands. EventGrid. models. PSTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomain

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## WYSYŁA

### Microsoft. Azure. Commands. EventGrid. models. PSEventSubscription

## INFORMACYJN

## LINKI POKREWNE
