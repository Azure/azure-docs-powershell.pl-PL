---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopic.md
ms.openlocfilehash: df3f6673729a868e7aeb349a34fba32b2033862e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489829"
---
# Get-AzEventGridTopic

## STRESZCZENIe
Pobiera szczegóły dotyczące siatki zdarzeń lub zawiera listę wszystkich tematów dotyczących siatki zdarzeń w bieżącej subskrypcji platformy Azure.

## POLECENIA

### ResourceGroupNameParameterSet (domyślny)
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

## Opis
Polecenie cmdlet Get-AzEventGridTopic pobiera szczegóły określonego tematu siatki zdarzeń lub listę wszystkich tematów siatki zdarzeń w bieżącej subskrypcji platformy Azure.
W przypadku podanej nazwy tematu jest zwracana wartość szczegółów pojedynczego tematu siatki zdarzeń.
Jeśli nie podano nazwy tematu, zostanie zwrócona Lista tematów. Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy. Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy tematów. W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.
Jeśli więcej tematów jest wciąż dostępnych, w następnej rozmowie należy użyć wartości z NextLink, aby uzyskać następną stronę tematów.
Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania. Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

## Przykłady

### Przykład 1
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1
```

Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .

### Przykład 2
```powershell
PS C:\> Get-AzEventGridTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1"
```

Pobiera Szczegóły tematu w siatce zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów \` \` .

### Przykład 3
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName
```

Wyświetlanie wszystkich tematów siatki zdarzeń w MyResourceGroupName grupy zasobów \` \` bez stronicowania.

### Przykład 4
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Lista pierwszych 10 tematów dotyczących siatki zdarzeń (jeśli istnieją) w \` MyResourceGroupNameach grupy zasobów \` , które spełniają zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony tematów, użytkownik powinien ponownie zadzwonić Get-AzEventGridTopic i używa wyników. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

### Przykład 5
```powershell
PS C:\> Get-AzEventGridTopic
```

Wyświetlanie listy wszystkich tematów dotyczących siatki zdarzeń w subskrypcji bez dzielenia na strony.

### Przykład 6
```powershell
$odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridTopic -Top 10 -ODataQuery $odataFilter
PS C:\> Get-AzEventGridTopic $result.NextLink
```

Lista pierwszych 10 tematów siatki zdarzeń (jeśli istnieją) w subskrypcji spełniającej zapytanie $odataFilter. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać kolejne strony tematów, użytkownik powinien ponownie zadzwonić Get-AzEventGridTopic i używa wyników. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

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

### -Name (nazwa)
Nazwa tematu EventGrid.

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

### -Początek
Maksymalna liczba zasobów do uzyskania. Prawidłowa wartość należy do zakresu od 1 do 100. Jeśli określona jest największa wartość, a dalsze wyniki są nadal dostępne, wynik będzie zawierał link do następnej strony, do której ma zostać przeszukana w NextLink. Jeśli nie określono najwyższych wartości, pełna lista zasobów zostanie zwrócona jednocześnie.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]

## WYSYŁA

### Microsoft. Azure. Commands. EventGrid. models. PSTopic

### Microsoft. Azure. Commands. EventGrid. models. PSTopicListInstance

## INFORMACYJN

## LINKI POKREWNE
