---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bbe600feb7618bef94a0d1799e1d2709ce7f0157
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553914"
---
# <span data-ttu-id="ec4b4-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="ec4b4-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="ec4b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec4b4-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4b4-103">Pobiera szczegóły pojedynczego centrum zdarzeń lub pobiera listę koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec4b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec4b4-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

## <span data-ttu-id="ec4b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec4b4-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4b4-106">Polecenie cmdlet Get-AzureRmEventHub zwraca informacje o centrum zdarzeń lub listę wszystkich koncentratorów zdarzeń w bieżącym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="ec4b4-107">W przypadku podanej nazwy centrum zdarzeń zostaną zwrócone szczegółowe dane dotyczące pojedynczego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="ec4b4-108">Jeśli nie podano nazwy centrum zdarzeń, zostanie zwrócona lista wszystkich koncentratorów zdarzeń w określonym obszarze nazw.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="ec4b4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec4b4-109">EXAMPLES</span></span>

### <span data-ttu-id="ec4b4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec4b4-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="ec4b4-111">Zwraca szczegóły MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec4b4-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="ec4b4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ec4b4-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="ec4b4-113">Zwraca listę koncentratorów zdarzeń w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="ec4b4-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="ec4b4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec4b4-114">PARAMETERS</span></span>

### <span data-ttu-id="ec4b4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4b4-115">-ResourceGroupName</span></span>
<span data-ttu-id="ec4b4-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-116">Resource group name.</span></span>

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

### <span data-ttu-id="ec4b4-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec4b4-117">-Name</span></span>
<span data-ttu-id="ec4b4-118">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-118">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4b4-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec4b4-119">-Namespace</span></span>
<span data-ttu-id="ec4b4-120">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="ec4b4-120">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="ec4b4-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec4b4-121">INPUTS</span></span>

### <span data-ttu-id="ec4b4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ec4b4-122">System.String</span></span>

## <span data-ttu-id="ec4b4-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec4b4-123">OUTPUTS</span></span>

### <span data-ttu-id="ec4b4-124">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. EventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ec4b4-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ec4b4-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec4b4-125">NOTES</span></span>

## <span data-ttu-id="ec4b4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec4b4-126">RELATED LINKS</span></span>

