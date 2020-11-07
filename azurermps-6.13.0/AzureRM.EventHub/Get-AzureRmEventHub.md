---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: 6ae26d1d5061989ac93756812cf48494e9101978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717412"
---
# <span data-ttu-id="3b306-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="3b306-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="3b306-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3b306-102">SYNOPSIS</span></span>
<span data-ttu-id="3b306-103">Pobiera szczegóły pojedynczego centrum zdarzeń lub pobiera listę koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3b306-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b306-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3b306-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b306-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3b306-105">DESCRIPTION</span></span>
<span data-ttu-id="3b306-106">Polecenie cmdlet Get-AzureRmEventHub zwraca informacje o centrum zdarzeń lub listę wszystkich koncentratorów zdarzeń w bieżącym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="3b306-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="3b306-107">W przypadku podanej nazwy centrum zdarzeń zostaną zwrócone szczegółowe dane dotyczące pojedynczego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="3b306-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="3b306-108">Jeśli nie podano nazwy centrum zdarzeń, zostanie zwrócona lista wszystkich koncentratorów zdarzeń w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="3b306-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="3b306-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3b306-109">EXAMPLES</span></span>

### <span data-ttu-id="3b306-110">Przykład 1-określony EventHub</span><span class="sxs-lookup"><span data-stu-id="3b306-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="3b306-111">Zwraca szczegóły MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="3b306-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="3b306-112">Przykład 2-Lista EventHub w określonym obszarze nazw</span><span class="sxs-lookup"><span data-stu-id="3b306-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="3b306-113">Zwraca listę koncentratorów zdarzeń w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="3b306-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="3b306-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3b306-114">PARAMETERS</span></span>

### <span data-ttu-id="3b306-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b306-115">-DefaultProfile</span></span>
<span data-ttu-id="3b306-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3b306-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b306-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3b306-117">-MaxCount</span></span>
<span data-ttu-id="3b306-118">Określ maksymalną liczbę zwracanych EventHubs.</span><span class="sxs-lookup"><span data-stu-id="3b306-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="3b306-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3b306-119">-Name</span></span>
<span data-ttu-id="3b306-120">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="3b306-120">EventHub Name</span></span>

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

### <span data-ttu-id="3b306-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3b306-121">-Namespace</span></span>
<span data-ttu-id="3b306-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="3b306-122">Namespace Name</span></span>

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

### <span data-ttu-id="3b306-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b306-123">-ResourceGroupName</span></span>
<span data-ttu-id="3b306-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="3b306-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3b306-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b306-125">CommonParameters</span></span>
<span data-ttu-id="3b306-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b306-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b306-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b306-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b306-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3b306-128">INPUTS</span></span>

### <span data-ttu-id="3b306-129">System. String</span><span class="sxs-lookup"><span data-stu-id="3b306-129">System.String</span></span>

## <span data-ttu-id="3b306-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3b306-130">OUTPUTS</span></span>

### <span data-ttu-id="3b306-131">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="3b306-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="3b306-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3b306-132">NOTES</span></span>

## <span data-ttu-id="3b306-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3b306-133">RELATED LINKS</span></span>
