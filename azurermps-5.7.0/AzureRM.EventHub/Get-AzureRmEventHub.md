---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544340"
---
# <span data-ttu-id="6e922-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="6e922-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="6e922-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e922-102">SYNOPSIS</span></span>
<span data-ttu-id="6e922-103">Pobiera szczegóły pojedynczego centrum zdarzeń lub pobiera listę koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6e922-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e922-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e922-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e922-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6e922-105">DESCRIPTION</span></span>
<span data-ttu-id="6e922-106">Polecenie cmdlet Get-AzureRmEventHub zwraca informacje o centrum zdarzeń lub listę wszystkich koncentratorów zdarzeń w bieżącym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="6e922-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="6e922-107">W przypadku podanej nazwy centrum zdarzeń zostaną zwrócone szczegółowe dane dotyczące pojedynczego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="6e922-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="6e922-108">Jeśli nie podano nazwy centrum zdarzeń, zostanie zwrócona lista wszystkich koncentratorów zdarzeń w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="6e922-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="6e922-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e922-109">EXAMPLES</span></span>

### <span data-ttu-id="6e922-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6e922-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="6e922-111">Zwraca szczegóły MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="6e922-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="6e922-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6e922-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="6e922-113">Zwraca listę koncentratorów zdarzeń w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="6e922-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="6e922-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e922-114">PARAMETERS</span></span>

### <span data-ttu-id="6e922-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e922-115">-DefaultProfile</span></span>
<span data-ttu-id="6e922-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e922-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e922-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e922-117">-Name</span></span>
<span data-ttu-id="6e922-118">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="6e922-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e922-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6e922-119">-Namespace</span></span>
<span data-ttu-id="6e922-120">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="6e922-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e922-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e922-121">-ResourceGroupName</span></span>
<span data-ttu-id="6e922-122">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="6e922-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e922-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e922-123">CommonParameters</span></span>
<span data-ttu-id="6e922-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e922-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6e922-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e922-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e922-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e922-126">INPUTS</span></span>

### <span data-ttu-id="6e922-127">System. String</span><span class="sxs-lookup"><span data-stu-id="6e922-127">System.String</span></span>


## <span data-ttu-id="6e922-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e922-128">OUTPUTS</span></span>

### <span data-ttu-id="6e922-129">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="6e922-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="6e922-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e922-130">NOTES</span></span>

## <span data-ttu-id="6e922-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e922-131">RELATED LINKS</span></span>
