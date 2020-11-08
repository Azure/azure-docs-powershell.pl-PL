---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222556"
---
# <span data-ttu-id="2d2bb-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="2d2bb-101">Get-AzEventHub</span></span>

## <span data-ttu-id="2d2bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2bb-103">Pobiera szczegóły pojedynczego centrum zdarzeń lub pobiera listę koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="2d2bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d2bb-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d2bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d2bb-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2bb-106">Polecenie cmdlet Get-AzEventHub zwraca informacje o centrum zdarzeń lub listę wszystkich koncentratorów zdarzeń w bieżącym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="2d2bb-107">W przypadku podanej nazwy centrum zdarzeń zostaną zwrócone szczegółowe dane dotyczące pojedynczego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="2d2bb-108">Jeśli nie podano nazwy centrum zdarzeń, zostanie zwrócona lista wszystkich koncentratorów zdarzeń w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="2d2bb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d2bb-109">EXAMPLES</span></span>

### <span data-ttu-id="2d2bb-110">Przykład 1: określony EventHub</span><span class="sxs-lookup"><span data-stu-id="2d2bb-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="2d2bb-111">Zwraca szczegóły MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="2d2bb-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="2d2bb-112">Przykład 2: Lista EventHub w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="2d2bb-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="2d2bb-113">Zwraca listę koncentratorów zdarzeń w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="2d2bb-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="2d2bb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d2bb-114">PARAMETERS</span></span>

### <span data-ttu-id="2d2bb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2bb-115">-DefaultProfile</span></span>
<span data-ttu-id="2d2bb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d2bb-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2d2bb-117">-MaxCount</span></span>
<span data-ttu-id="2d2bb-118">Określ maksymalną liczbę zwracanych EventHubs.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="2d2bb-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d2bb-119">-Name</span></span>
<span data-ttu-id="2d2bb-120">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="2d2bb-120">EventHub Name</span></span>

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

### <span data-ttu-id="2d2bb-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2d2bb-121">-Namespace</span></span>
<span data-ttu-id="2d2bb-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2d2bb-122">Namespace Name</span></span>

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

### <span data-ttu-id="2d2bb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2bb-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d2bb-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2d2bb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2d2bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2bb-125">CommonParameters</span></span>
<span data-ttu-id="2d2bb-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2bb-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d2bb-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2bb-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d2bb-128">INPUTS</span></span>

### <span data-ttu-id="2d2bb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2d2bb-129">System.String</span></span>

## <span data-ttu-id="2d2bb-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d2bb-130">OUTPUTS</span></span>

### <span data-ttu-id="2d2bb-131">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2d2bb-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="2d2bb-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d2bb-132">NOTES</span></span>

## <span data-ttu-id="2d2bb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d2bb-133">RELATED LINKS</span></span>
