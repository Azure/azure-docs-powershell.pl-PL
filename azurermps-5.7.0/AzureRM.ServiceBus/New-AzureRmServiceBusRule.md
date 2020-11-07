---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusRule.md
ms.openlocfilehash: 22e54316bd38907c1ab22e3b2c35e1b6949b0034
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717689"
---
# <span data-ttu-id="077ca-101">New-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="077ca-101">New-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="077ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="077ca-102">SYNOPSIS</span></span>
<span data-ttu-id="077ca-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="077ca-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="077ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="077ca-104">SYNTAX</span></span>

```
New-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="077ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="077ca-105">DESCRIPTION</span></span>
<span data-ttu-id="077ca-106">Polecenie cmdlet **New-AzureRmServiceBusRule** tworzy nową regułę dla danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="077ca-106">The **New-AzureRmServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="077ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="077ca-107">EXAMPLES</span></span>

### <span data-ttu-id="077ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="077ca-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="077ca-109">Polecenie cmdlet New-AzureRmServiceBusRule tworzy nową regułę dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="077ca-109">The New-AzureRmServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

## <span data-ttu-id="077ca-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="077ca-110">PARAMETERS</span></span>

### <span data-ttu-id="077ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="077ca-111">-DefaultProfile</span></span>
<span data-ttu-id="077ca-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="077ca-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="077ca-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="077ca-113">-Name</span></span>
<span data-ttu-id="077ca-114">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="077ca-114">Rule Name</span></span>

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

### <span data-ttu-id="077ca-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="077ca-115">-Namespace</span></span>
<span data-ttu-id="077ca-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="077ca-116">Namespace Name.</span></span>

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

### <span data-ttu-id="077ca-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="077ca-117">-ResourceGroupName</span></span>
<span data-ttu-id="077ca-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="077ca-118">The name of the resource group</span></span>

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

### <span data-ttu-id="077ca-119">-Sqlexpression</span><span class="sxs-lookup"><span data-stu-id="077ca-119">-SqlExpression</span></span>
<span data-ttu-id="077ca-120">Wyrażenie SQL Fillter</span><span class="sxs-lookup"><span data-stu-id="077ca-120">Sql Fillter Expression</span></span>

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

### <span data-ttu-id="077ca-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="077ca-121">-Subscription</span></span>
<span data-ttu-id="077ca-122">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="077ca-122">Subscription Name</span></span>

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

### <span data-ttu-id="077ca-123">— Temat</span><span class="sxs-lookup"><span data-stu-id="077ca-123">-Topic</span></span>
<span data-ttu-id="077ca-124">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="077ca-124">Topic Name.</span></span>

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

### <span data-ttu-id="077ca-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="077ca-125">-Confirm</span></span>
<span data-ttu-id="077ca-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="077ca-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="077ca-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="077ca-127">-WhatIf</span></span>
<span data-ttu-id="077ca-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="077ca-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="077ca-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="077ca-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="077ca-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="077ca-130">CommonParameters</span></span>
<span data-ttu-id="077ca-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="077ca-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="077ca-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="077ca-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="077ca-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="077ca-133">INPUTS</span></span>

### <span data-ttu-id="077ca-134">System. String</span><span class="sxs-lookup"><span data-stu-id="077ca-134">System.String</span></span>

## <span data-ttu-id="077ca-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="077ca-135">OUTPUTS</span></span>

### <span data-ttu-id="077ca-136">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="077ca-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="077ca-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="077ca-137">NOTES</span></span>

## <span data-ttu-id="077ca-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="077ca-138">RELATED LINKS</span></span>

