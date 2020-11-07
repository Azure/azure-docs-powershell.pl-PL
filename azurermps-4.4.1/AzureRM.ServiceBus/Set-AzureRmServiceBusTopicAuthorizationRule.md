---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: bbc6c0119f0f8f424b508adc38b5de80cd097734
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718696"
---
# <span data-ttu-id="8e5b4-101">Set-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8e5b4-101">Set-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="8e5b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e5b4-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji dla danego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-103">Updates the specified authorization rule description for the given Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e5b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e5b4-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 -InputObj <SharedAccessAuthorizationRuleAttributes> [-Name <String>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e5b4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8e5b4-105">DESCRIPTION</span></span>
<span data-ttu-id="8e5b4-106">Polecenie cmdlet **Set-AzureRmServiceBusTopicAuthorizationRule** umożliwia zaktualizowanie opisu określonej reguły autoryzacji określonego tematu magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-106">The **Set-AzureRmServiceBusTopicAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Service Bus topic.</span></span>

## <span data-ttu-id="8e5b4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e5b4-107">EXAMPLES</span></span>

### <span data-ttu-id="8e5b4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e5b4-108">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthorizationRuleName SBTopicAuthoRule1

PS C:\> $authRuleObj.Rights.Add("Manage")

PS C:\> Set-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -AuthRuleObj $authRuleObj
```

<span data-ttu-id="8e5b4-109">Dodaje do sekcji **Zarządzanie** prawami dostępu w ramach reguły autoryzacji `SBTopicAuthoRule1` `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="8e5b4-109">Adds **Manage** to the access rights of the authorization rule `SBTopicAuthoRule1` on topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="8e5b4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e5b4-110">PARAMETERS</span></span>

### <span data-ttu-id="8e5b4-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8e5b4-111">-ResourceGroup</span></span>
<span data-ttu-id="8e5b4-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="8e5b4-113">-Prawa</span><span class="sxs-lookup"><span data-stu-id="8e5b4-113">-Rights</span></span>
<span data-ttu-id="8e5b4-114">Intelektualn na przykład @ ("nasłuchuj"; "Wyślij"; "Zarządzaj").</span><span class="sxs-lookup"><span data-stu-id="8e5b4-114">Rights; for example, @("Listen","Send","Manage").</span></span> <span data-ttu-id="8e5b4-115">Wymagane, jeśli nie podano parametru **-AuthruleObj** .</span><span class="sxs-lookup"><span data-stu-id="8e5b4-115">Required if **-AuthruleObj** is not specified.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5b4-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e5b4-116">-Confirm</span></span>
<span data-ttu-id="8e5b4-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e5b4-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e5b4-118">-WhatIf</span></span>
<span data-ttu-id="8e5b4-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e5b4-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e5b4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e5b4-121">-DefaultProfile</span></span>
<span data-ttu-id="8e5b4-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e5b4-123">-InputObj</span><span class="sxs-lookup"><span data-stu-id="8e5b4-123">-InputObj</span></span>
<span data-ttu-id="8e5b4-124">ServiceBus temat AuthorizationRule obiekt.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-124">ServiceBus Topic AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5b4-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e5b4-125">-Name</span></span>
<span data-ttu-id="8e5b4-126">AuthorizationRule nazwa — wymagane, jeśli nie podano parametru "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="8e5b4-126">AuthorizationRule Name - Required if 'AuthruleObj' not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e5b4-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8e5b4-127">-Namespace</span></span>
<span data-ttu-id="8e5b4-128">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-128">Namespace Name.</span></span>

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

### <span data-ttu-id="8e5b4-129">— Temat</span><span class="sxs-lookup"><span data-stu-id="8e5b4-129">-Topic</span></span>
<span data-ttu-id="8e5b4-130">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-130">Topic Name.</span></span>

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

### <span data-ttu-id="8e5b4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e5b4-131">CommonParameters</span></span>
<span data-ttu-id="8e5b4-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e5b4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e5b4-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e5b4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e5b4-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e5b4-134">INPUTS</span></span>

### <span data-ttu-id="8e5b4-135">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="8e5b4-135">-ResourceGroup</span></span>
 <span data-ttu-id="8e5b4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8e5b4-136">System.String</span></span>

### <span data-ttu-id="8e5b4-137">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8e5b4-137">-NamespaceName</span></span>
 <span data-ttu-id="8e5b4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8e5b4-138">System.String</span></span>

### <span data-ttu-id="8e5b4-139">-Tematname</span><span class="sxs-lookup"><span data-stu-id="8e5b4-139">-TopicName</span></span>
 <span data-ttu-id="8e5b4-140">System. String</span><span class="sxs-lookup"><span data-stu-id="8e5b4-140">System.String</span></span>

### <span data-ttu-id="8e5b4-141">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="8e5b4-141">-AuthRuleObj</span></span>
 <span data-ttu-id="8e5b4-142">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8e5b4-142">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="8e5b4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e5b4-143">OUTPUTS</span></span>

### <span data-ttu-id="8e5b4-144">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="8e5b4-144">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="8e5b4-145">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/Authorization reguły/SBTopicAuthoRule1: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 Location: zachodnie znaczniki USA: prawa: {Listen, Send, Manage}</span><span class="sxs-lookup"><span data-stu-id="8e5b4-145">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_exampl1/authorization Rules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send, Manage}</span></span>

## <span data-ttu-id="8e5b4-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e5b4-146">NOTES</span></span>

## <span data-ttu-id="8e5b4-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e5b4-147">RELATED LINKS</span></span>

