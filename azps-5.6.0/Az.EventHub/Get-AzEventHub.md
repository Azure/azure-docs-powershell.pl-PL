---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: d69e30ff993d2e07c7711d36d8e5ec889bc0f7c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007905"
---
# <span data-ttu-id="82fea-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="82fea-101">Get-AzEventHub</span></span>

## <span data-ttu-id="82fea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82fea-102">SYNOPSIS</span></span>
<span data-ttu-id="82fea-103">Pobiera szczegółowe informacje dotyczące pojedynczego centrum zdarzeń lub listę Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="82fea-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="82fea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="82fea-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82fea-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="82fea-105">DESCRIPTION</span></span>
<span data-ttu-id="82fea-106">Polecenie Get-AzEventHub zwraca szczegóły centrum zdarzeń lub listę wszystkich centrum zdarzeń w bieżącej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="82fea-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="82fea-107">Jeśli podano nazwę Centrum zdarzeń, zostaną zwrócone szczegóły pojedynczego Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="82fea-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="82fea-108">Jeśli nazwa Centrum zdarzeń nie jest podana, jest zwracana lista wszystkich centrum zdarzeń w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="82fea-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="82fea-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="82fea-109">EXAMPLES</span></span>

### <span data-ttu-id="82fea-110">Przykład 1: określono usługę EventHub</span><span class="sxs-lookup"><span data-stu-id="82fea-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="82fea-111">Zwraca szczegóły nazwy \` MyEventHubName centrum \` zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="82fea-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="82fea-112">Przykład 2. Lista aplikacji EventHub w określonej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="82fea-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="82fea-113">Zwraca listę centrum zdarzeń w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="82fea-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="82fea-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82fea-114">PARAMETERS</span></span>

### <span data-ttu-id="82fea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82fea-115">-DefaultProfile</span></span>
<span data-ttu-id="82fea-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="82fea-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82fea-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="82fea-117">-MaxCount</span></span>
<span data-ttu-id="82fea-118">Określ maksymalną liczbę zwracanych przez usługi EventHub.</span><span class="sxs-lookup"><span data-stu-id="82fea-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="82fea-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="82fea-119">-Name</span></span>
<span data-ttu-id="82fea-120">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="82fea-120">EventHub Name</span></span>

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

### <span data-ttu-id="82fea-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="82fea-121">-Namespace</span></span>
<span data-ttu-id="82fea-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="82fea-122">Namespace Name</span></span>

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

### <span data-ttu-id="82fea-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82fea-123">-ResourceGroupName</span></span>
<span data-ttu-id="82fea-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="82fea-124">Resource Group Name</span></span>

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

### <span data-ttu-id="82fea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82fea-125">CommonParameters</span></span>
<span data-ttu-id="82fea-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82fea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82fea-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82fea-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82fea-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82fea-128">INPUTS</span></span>

### <span data-ttu-id="82fea-129">System.String</span><span class="sxs-lookup"><span data-stu-id="82fea-129">System.String</span></span>

## <span data-ttu-id="82fea-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82fea-130">OUTPUTS</span></span>

### <span data-ttu-id="82fea-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="82fea-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="82fea-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="82fea-132">NOTES</span></span>

## <span data-ttu-id="82fea-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82fea-133">RELATED LINKS</span></span>
