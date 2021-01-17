---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376700"
---
# <span data-ttu-id="830d3-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="830d3-101">Get-AzEventHub</span></span>

## <span data-ttu-id="830d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="830d3-102">SYNOPSIS</span></span>
<span data-ttu-id="830d3-103">Pobiera szczegóły pojedynczego centrum zdarzeń lub pobiera listę koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="830d3-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="830d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="830d3-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="830d3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="830d3-105">DESCRIPTION</span></span>
<span data-ttu-id="830d3-106">Polecenie cmdlet Get-AzEventHub zwraca informacje o centrum zdarzeń lub listę wszystkich koncentratorów zdarzeń w bieżącym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="830d3-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="830d3-107">W przypadku podanej nazwy centrum zdarzeń zostaną zwrócone szczegółowe dane dotyczące pojedynczego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="830d3-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="830d3-108">Jeśli nie podano nazwy centrum zdarzeń, zostanie zwrócona lista wszystkich koncentratorów zdarzeń w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="830d3-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="830d3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="830d3-109">EXAMPLES</span></span>

### <span data-ttu-id="830d3-110">Przykład 1: określony EventHub</span><span class="sxs-lookup"><span data-stu-id="830d3-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="830d3-111">Zwraca szczegóły MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="830d3-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="830d3-112">Przykład 2: Lista EventHub w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="830d3-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="830d3-113">Zwraca listę koncentratorów zdarzeń w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="830d3-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="830d3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="830d3-114">PARAMETERS</span></span>

### <span data-ttu-id="830d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="830d3-115">-DefaultProfile</span></span>
<span data-ttu-id="830d3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="830d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="830d3-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="830d3-117">-MaxCount</span></span>
<span data-ttu-id="830d3-118">Określ maksymalną liczbę zwracanych EventHubs.</span><span class="sxs-lookup"><span data-stu-id="830d3-118">Determine the maximum number of EventHubs to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="830d3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="830d3-119">-Name</span></span>
<span data-ttu-id="830d3-120">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="830d3-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830d3-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="830d3-121">-Namespace</span></span>
<span data-ttu-id="830d3-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="830d3-122">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830d3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="830d3-123">-ResourceGroupName</span></span>
<span data-ttu-id="830d3-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="830d3-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="830d3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="830d3-125">CommonParameters</span></span>
<span data-ttu-id="830d3-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="830d3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="830d3-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="830d3-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="830d3-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="830d3-128">INPUTS</span></span>

### <span data-ttu-id="830d3-129">System. String</span><span class="sxs-lookup"><span data-stu-id="830d3-129">System.String</span></span>

## <span data-ttu-id="830d3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="830d3-130">OUTPUTS</span></span>

### <span data-ttu-id="830d3-131">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="830d3-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="830d3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="830d3-132">NOTES</span></span>

## <span data-ttu-id="830d3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="830d3-133">RELATED LINKS</span></span>
