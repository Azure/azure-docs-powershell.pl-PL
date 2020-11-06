---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 098c61be4eaf405d3c3a031601b48f20de1e234a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527278"
---
# <span data-ttu-id="14237-101">New-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="14237-101">New-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="14237-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14237-102">SYNOPSIS</span></span>
<span data-ttu-id="14237-103">Tworzy nową regułę autoryzacji dla określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="14237-103">Creates a new authorization rule for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14237-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14237-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14237-105">Opis</span><span class="sxs-lookup"><span data-stu-id="14237-105">DESCRIPTION</span></span>
<span data-ttu-id="14237-106">Polecenie cmdlet **New-AzureRmServiceBusQueueAuthorizationRule** tworzy nową regułę autoryzacji dla określonej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="14237-106">The **New-AzureRmServiceBusQueueAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus queue.</span></span>

## <span data-ttu-id="14237-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14237-107">EXAMPLES</span></span>

### <span data-ttu-id="14237-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14237-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="14237-109">Tworzy regułę autoryzacji `SBAuthoRule1` przy użyciu **odsłuchiwania i wysyłania** praw do kolejki `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="14237-109">Creates authorization rule `SBAuthoRule1` with **Listen and Send** rights for the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="14237-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14237-110">PARAMETERS</span></span>

### <span data-ttu-id="14237-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="14237-111">-ResourceGroup</span></span>
<span data-ttu-id="14237-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14237-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="14237-113">-Prawa</span><span class="sxs-lookup"><span data-stu-id="14237-113">-Rights</span></span>
<span data-ttu-id="14237-114">Określa prawa; na przykład</span><span class="sxs-lookup"><span data-stu-id="14237-114">Specifies the rights; for example,</span></span>  
<span data-ttu-id="14237-115">@ ("Nasłuchuj"; "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="14237-115">@("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14237-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14237-116">-Confirm</span></span>
<span data-ttu-id="14237-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14237-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14237-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14237-118">-WhatIf</span></span>
<span data-ttu-id="14237-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14237-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14237-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14237-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14237-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14237-121">-DefaultProfile</span></span>
<span data-ttu-id="14237-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14237-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14237-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14237-123">-Name</span></span>
<span data-ttu-id="14237-124">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="14237-124">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14237-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="14237-125">-Namespace</span></span>
<span data-ttu-id="14237-126">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="14237-126">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14237-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="14237-127">-Queue</span></span>
<span data-ttu-id="14237-128">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="14237-128">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14237-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14237-129">CommonParameters</span></span>
<span data-ttu-id="14237-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14237-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14237-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14237-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14237-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14237-132">INPUTS</span></span>

### <span data-ttu-id="14237-133">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="14237-133">-ResourceGroup</span></span>
 <span data-ttu-id="14237-134">System. String</span><span class="sxs-lookup"><span data-stu-id="14237-134">System.String</span></span>
 

### <span data-ttu-id="14237-135">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="14237-135">-NamespaceName</span></span>
 <span data-ttu-id="14237-136">System. String</span><span class="sxs-lookup"><span data-stu-id="14237-136">System.String</span></span>
 

### <span data-ttu-id="14237-137">-QueueName</span><span class="sxs-lookup"><span data-stu-id="14237-137">-QueueName</span></span>
 <span data-ttu-id="14237-138">System. String</span><span class="sxs-lookup"><span data-stu-id="14237-138">System.String</span></span>
 

### <span data-ttu-id="14237-139">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="14237-139">-AuthorizationRuleName</span></span>
 <span data-ttu-id="14237-140">System. String</span><span class="sxs-lookup"><span data-stu-id="14237-140">System.String</span></span>

## <span data-ttu-id="14237-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14237-141">OUTPUTS</span></span>

### <span data-ttu-id="14237-142">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="14237-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="14237-143">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 Location: zachód AMERYKAŃSKIe znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="14237-143">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="14237-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14237-144">NOTES</span></span>

## <span data-ttu-id="14237-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14237-145">RELATED LINKS</span></span>

