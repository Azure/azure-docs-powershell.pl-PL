---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 166b47a231b2ca6fc2cf74137212e60123f25445
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553095"
---
# <span data-ttu-id="0427c-101">Set-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0427c-101">Set-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="0427c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0427c-102">SYNOPSIS</span></span>
<span data-ttu-id="0427c-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji danej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0427c-103">Updates the specified authorization rule description for the given Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0427c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0427c-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> [-NamespaceName] <String>
 [-QueueName] <String> [-AuthRuleObj] <SharedAccessAuthorizationRuleAttributes>
 [[-AuthorizationRuleName] <String>] [[-Rights] <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0427c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0427c-105">DESCRIPTION</span></span>
<span data-ttu-id="0427c-106">Polecenie cmdlet **Set-AzureRmServiceBusQueueAuthorizationRule** umożliwia zaktualizowanie opisu określonej reguły autoryzacji danej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0427c-106">The **Set-AzureRmServiceBusQueueAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus queue.</span></span>

## <span data-ttu-id="0427c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0427c-107">EXAMPLES</span></span>

### <span data-ttu-id="0427c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0427c-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="0427c-109">Dodaje do **zarządzania** prawa dostępu do reguły autoryzacji `SBAuthoRule1` kolejki `SB-Queue_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="0427c-109">Adds **Manage** to the access rights of the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1`.</span></span>

## <span data-ttu-id="0427c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0427c-110">PARAMETERS</span></span>

### <span data-ttu-id="0427c-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="0427c-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="0427c-112">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="0427c-112">The authorization rule name.</span></span> <span data-ttu-id="0427c-113">Wymagane, jeśli nie podano parametru **-AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="0427c-113">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="0427c-114">-AuthRuleObj</span></span>
<span data-ttu-id="0427c-115">Obiekt reguły autoryzacji kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0427c-115">The Service Bus queue authorization rule object.</span></span>

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0427c-116">-NamespaceName</span></span>
<span data-ttu-id="0427c-117">Nazwa obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0427c-117">The Service Bus namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-118">-QueueName</span><span class="sxs-lookup"><span data-stu-id="0427c-118">-QueueName</span></span>
<span data-ttu-id="0427c-119">Nazwa kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0427c-119">The Service Bus queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-120">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0427c-120">-ResourceGroup</span></span>
<span data-ttu-id="0427c-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0427c-121">The name of the resource group.</span></span>

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

### <span data-ttu-id="0427c-122">-Prawa</span><span class="sxs-lookup"><span data-stu-id="0427c-122">-Rights</span></span>
<span data-ttu-id="0427c-123">Prawa; na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj").</span><span class="sxs-lookup"><span data-stu-id="0427c-123">The rights; for example @("Listen","Send","Manage").</span></span> <span data-ttu-id="0427c-124">Wymagany, jeśli nie podano parametru "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="0427c-124">Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0427c-125">-Confirm</span></span>
<span data-ttu-id="0427c-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0427c-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0427c-127">-WhatIf</span></span>
<span data-ttu-id="0427c-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0427c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0427c-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0427c-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0427c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0427c-130">CommonParameters</span></span>
<span data-ttu-id="0427c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0427c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0427c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0427c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0427c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0427c-133">INPUTS</span></span>

### <span data-ttu-id="0427c-134">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0427c-134">-ResourceGroup</span></span>
 <span data-ttu-id="0427c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="0427c-135">System.String</span></span>

### <span data-ttu-id="0427c-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="0427c-136">-NamespaceName</span></span>
 <span data-ttu-id="0427c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="0427c-137">System.String</span></span>

### <span data-ttu-id="0427c-138">-QueueName</span><span class="sxs-lookup"><span data-stu-id="0427c-138">-QueueName</span></span>
 <span data-ttu-id="0427c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0427c-139">System.String</span></span>

### <span data-ttu-id="0427c-140">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="0427c-140">-AuthRuleObj</span></span>
 <span data-ttu-id="0427c-141">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0427c-141">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0427c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0427c-142">OUTPUTS</span></span>

### <span data-ttu-id="0427c-143">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0427c-143">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0427c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0427c-144">NOTES</span></span>

## <span data-ttu-id="0427c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0427c-145">RELATED LINKS</span></span>

