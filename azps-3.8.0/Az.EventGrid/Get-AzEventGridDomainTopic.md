---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainTopic.md
ms.openlocfilehash: 10ea1dca3ef550bcbd38082a8b27a19dd2ffb46a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894774"
---
# Get-AzEventGridDomainTopic

## STRESZCZENIe
Umożliwia wyświetlenie szczegółów dotyczących domeny siatki zdarzeń lub wyświetlenie listy wszystkich tematów dotyczących domeny siatki zdarzeń w obszarze określona domena siatki zdarzeń w bieżącej subskrypcji platformy Azure.

## POLECENIA

### DomainTopicNameParameterSet (domyślny)
```
Get-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name <String>]
 [-ODataQuery <String>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceIdDomainTopicParameterSet
```
Get-AzEventGridDomainTopic [-ResourceId] <String> [-ODataQuery <String>] [-Top <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### NextLinkParameterSet
```
Get-AzEventGridDomainTopic [-NextLink <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet Get-AzEventGridDomainTopic powoduje wyświetlenie szczegółów określonego tematu domeny siatki zdarzeń lub listy wszystkich tematów dotyczących domeny w siatce zdarzeń w określonej domenie w bieżącej subskrypcji platformy Azure.
Jeśli jest podana nazwa tematu domeny, zostaną zwrócone szczegóły dotyczące jednej z nich.
Jeśli nie podano nazwy tematu domeny, zostanie zwrócona Lista tematów dotyczących domeny pod określoną nazwą domeny. Liczba elementów zwróconych na tej liście jest kontrolowana przez parametr najwyższy. Jeśli najszukana wartość nie jest określona lub $null, lista będzie zawierać wszystkie elementy tematów domeny. W przeciwnym razie na początku będzie wskazywana Maksymalna liczba elementów, które mają zostać zwrócone na liście.
Jeśli więcej tematów dotyczących domeny jest wciąż dostępnych, w następnej rozmowie należy użyć wartości z NextLink, aby uzyskać następną stronę tematów domeny.
Na koniec parametr ODataQuery jest wykorzystywany do filtrowania wyników wyszukiwania. Kwerenda filtrująca podąża za składnią funkcji OData tylko przy użyciu właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

## Przykłady

### Przykład 1

Pobiera Szczegóły tematu domeny w siatce zdarzeń \` DomainTopic1 w \` obszarze Domena zdarzeń \` Domain1 \` w grupie zasób \` MyResourceGroupName \` .

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -DomainTopicName DomainTopic1

ResourceGroupName : MyResourceGroupName
DomainName        : DomainTopic1
DomainTopicName   : Topic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Przykład 2

Umożliwia wyświetlenie szczegółów tematu domeny w siatce zdarzeń \` DomainTopic1 w \` obszarze domeny \` Domain1 \` w grupie zasobów \` MyResourceGroupName \` przy użyciu opcji ResourceID.

```powershell
PS C:\> Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1"

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Przykład 3

Lista wszystkich tematów dotyczących domeny siatki zdarzeń w obszarze Domena zdarzeń \` Domain1 \` w grupie zasób \` MyResourceGroupName \` bez stronicowania (wszystkie wyniki są zwracane w jednym zasobie).

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Przykład 4

Lista wszystkich tematów dotyczących domeny w siatce zdarzeń \` w obszarze Domain1 domeny \` w grupie zasób \` MyResourceGroupName \` bez stronicowania (wszystkie wyniki są zwracane w jednym zasobie) przy użyciu opcji ResourceID

```powershell
PS C:\> $result=Get-AzEventGridDomainTopic -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1"
PS C:\> echo $result.PsDomainTopicsList


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic1
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic1
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic2
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic2
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded


ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
DomainTopicName   : DomainTopic3
Id                : /subscriptions/20902276-e53b-4421-8565-f57bcad74f6e/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/DomainTopic3
Type              : Microsoft.EventGrid/domains/topics
ProvisioningState : Succeeded
```

### Przykład 5

Wyświetlanie tematów dotyczących domeny w siatce zdarzeń (jeśli istnieją) w obszarze Domain Domain1 (jeśli istnieje) \` \` w grupie zasoby \` MyResourceGroupName \` , która spełnia tematy $odataFilter 10 tematów dotyczących domeny w danym momencie. Jeśli jest dostępnych więcej wyników, $result. NextLink nie będzie $null. Aby uzyskać dostęp do kolejnych stron tematów domeny, użytkownik powinien ponownie zadzwonić Get-AzEventGridDomainTopic i używa wyników. NextLink uzyskana z poprzedniej rozmowy. Osoba dzwoniąca powinna zatrzymać się w wyniku. NextLink się $null.

```powershell
PS C:\> $total = 0
PS C:\> $odataFilter = "Name ne 'ABCD'"
PS C:\> $result = Get-AzEventGridDomainTopic -ResourceGroup MyResourceGroupName -DomainName Domain1 -Top 10 -ODataQuery $odataFilter
PS C:\> $total += $result.Count
PS C:\> while ($result.NextLink -ne $Null)
    {
        $result = Get-AzEventGridDomainTopic -NextLink $result.NextLink
        $total += $result.Count
    }

PS C:\> echo "Total number of domain topics is $Total"
```

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -NazwaDomeny
EventGrid nazwa domeny.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: Domain

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Nazwa tematu domeny EventGrid.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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
Accept pipeline input: False
Accept wildcard characters: False
```

### -ODataQuery
Kwerenda OData używana do filtrowania wyników listy. Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Nazwa grupy zasobów.

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
Identyfikator zasobu reprezentujący temat domeny lub domeny siatki zdarzeń.

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Początek
Kwerenda OData używana do filtrowania wyników listy. Filtrowanie jest obecnie dozwolone tylko w przypadku właściwości Name. Obsługiwane operacje obejmują: zawiera, EQ (za równe), ne (nierówne), oraz lub nie.

```yaml
Type: System.Int32
Parameter Sets: DomainTopicNameParameterSet, ResourceIdDomainTopicParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. Int32

## WYSYŁA

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic

### Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopicListInstance

## INFORMACYJN

## LINKI POKREWNE
