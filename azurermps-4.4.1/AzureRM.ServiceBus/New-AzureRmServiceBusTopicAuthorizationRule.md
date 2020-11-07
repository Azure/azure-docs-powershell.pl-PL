---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: 603eb1363e15b58a324f7131dd986a7c84371a89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716879"
---
# <span data-ttu-id="f6506-101">New-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f6506-101">New-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="f6506-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6506-102">SYNOPSIS</span></span>
<span data-ttu-id="f6506-103">Tworzy nową regułę autoryzacji dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="f6506-103">Creates a new authorization rule for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6506-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6506-104">SYNTAX</span></span>

```
New-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -Name <String> [-Rights] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6506-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6506-105">DESCRIPTION</span></span>
<span data-ttu-id="f6506-106">Polecenie cmdlet **New-AzureRmServiceBusTopicAuthorizationRule** tworzy nową regułę autoryzacji dla określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="f6506-106">The **New-AzureRmServiceBusTopicAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus topic.</span></span>

## <span data-ttu-id="f6506-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6506-107">EXAMPLES</span></span>

### <span data-ttu-id="f6506-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f6506-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="f6506-109">Tworzy regułę autoryzacji `SBTopicAuthoRule1` z uprawnieniami **odsłuchiwania** i **wysyłania** dla tematu `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="f6506-109">Creates authorization rule `SBTopicAuthoRule1` with **Listen** and **Send** rights for the topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="f6506-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6506-110">PARAMETERS</span></span>

### <span data-ttu-id="f6506-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f6506-111">-ResourceGroup</span></span>
<span data-ttu-id="f6506-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f6506-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f6506-113">-Prawa</span><span class="sxs-lookup"><span data-stu-id="f6506-113">-Rights</span></span>
<span data-ttu-id="f6506-114">Prawa; na przykład @ ("nasłuchuj"; "Wyślij"; "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="f6506-114">The rights; for example, @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="f6506-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f6506-115">-Confirm</span></span>
<span data-ttu-id="f6506-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6506-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6506-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6506-117">-WhatIf</span></span>
<span data-ttu-id="f6506-118">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6506-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6506-119">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f6506-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6506-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6506-120">-DefaultProfile</span></span>
<span data-ttu-id="f6506-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f6506-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6506-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f6506-122">-Name</span></span>
<span data-ttu-id="f6506-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="f6506-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f6506-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f6506-124">-Namespace</span></span>
<span data-ttu-id="f6506-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f6506-125">Namespace Name.</span></span>

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

### <span data-ttu-id="f6506-126">— Temat</span><span class="sxs-lookup"><span data-stu-id="f6506-126">-Topic</span></span>
<span data-ttu-id="f6506-127">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="f6506-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6506-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6506-128">CommonParameters</span></span>
<span data-ttu-id="f6506-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6506-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6506-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6506-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6506-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6506-131">INPUTS</span></span>

### <span data-ttu-id="f6506-132">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f6506-132">-ResourceGroup</span></span>
 <span data-ttu-id="f6506-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f6506-133">System.String</span></span>
 

### <span data-ttu-id="f6506-134">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f6506-134">-NamespaceName</span></span>
 <span data-ttu-id="f6506-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f6506-135">System.String</span></span>
 

### <span data-ttu-id="f6506-136">-Tematname</span><span class="sxs-lookup"><span data-stu-id="f6506-136">-TopicName</span></span>
 <span data-ttu-id="f6506-137">System. String</span><span class="sxs-lookup"><span data-stu-id="f6506-137">System.String</span></span>
 

### <span data-ttu-id="f6506-138">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f6506-138">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f6506-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f6506-139">System.String</span></span>

## <span data-ttu-id="f6506-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6506-140">OUTPUTS</span></span>

### <span data-ttu-id="f6506-141">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f6506-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="f6506-142">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onrules/SBTopicAuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 Location: zachód AMERYKAŃSKIe znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="f6506-142">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f6506-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6506-143">NOTES</span></span>

## <span data-ttu-id="f6506-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6506-144">RELATED LINKS</span></span>

