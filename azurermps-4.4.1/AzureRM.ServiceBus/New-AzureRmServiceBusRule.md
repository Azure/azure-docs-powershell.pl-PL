---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 39cd0759f18c84f78a2e6a75f8e1c9b257fb9da9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719241"
---
# <span data-ttu-id="370ab-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="370ab-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="370ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="370ab-102">SYNOPSIS</span></span>
<span data-ttu-id="370ab-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="370ab-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="370ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="370ab-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="370ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="370ab-105">DESCRIPTION</span></span>
<span data-ttu-id="370ab-106">Polecenie cmdlet **New-AzureRmServiceBusRule** tworzy nową regułę dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="370ab-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="370ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="370ab-107">EXAMPLES</span></span>

### <span data-ttu-id="370ab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="370ab-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="370ab-109">Polecenie cmdlet **New-AzureRmServiceBusRule** tworzy nową regułę dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="370ab-109">The **New-AzureRmServiceBusRule** cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="370ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="370ab-110">PARAMETERS</span></span>

### <span data-ttu-id="370ab-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="370ab-111">-Confirm</span></span>
<span data-ttu-id="370ab-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="370ab-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="370ab-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="370ab-113">-Name</span></span>
<span data-ttu-id="370ab-114">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="370ab-114">Rule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ab-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="370ab-115">-Namespace</span></span>
<span data-ttu-id="370ab-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="370ab-116">Namespace Name.</span></span>

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

### <span data-ttu-id="370ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="370ab-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="370ab-118">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ab-119">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="370ab-119">-SqlExpression</span></span>
<span data-ttu-id="370ab-120">Wyrażenie SQL Fillter</span><span class="sxs-lookup"><span data-stu-id="370ab-120">Sql Fillter Expression</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ab-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="370ab-121">-Subscription</span></span>
<span data-ttu-id="370ab-122">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="370ab-122">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ab-123">— Temat</span><span class="sxs-lookup"><span data-stu-id="370ab-123">-Topic</span></span>
<span data-ttu-id="370ab-124">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="370ab-124">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="370ab-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="370ab-125">-WhatIf</span></span>
<span data-ttu-id="370ab-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="370ab-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="370ab-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="370ab-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="370ab-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="370ab-128">INPUTS</span></span>

### <span data-ttu-id="370ab-129">System. String</span><span class="sxs-lookup"><span data-stu-id="370ab-129">System.String</span></span>


## <span data-ttu-id="370ab-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="370ab-130">OUTPUTS</span></span>

### <span data-ttu-id="370ab-131">Microsoft. Azure. Commands. ServiceBus. models. RulesAttributes</span><span class="sxs-lookup"><span data-stu-id="370ab-131">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>


## <span data-ttu-id="370ab-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="370ab-132">NOTES</span></span>

## <span data-ttu-id="370ab-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="370ab-133">RELATED LINKS</span></span>

