---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 9e4612f8b688181ca54c7fa8414d28e3a444b446
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553107"
---
# <span data-ttu-id="dc30e-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dc30e-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="dc30e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc30e-102">SYNOPSIS</span></span>
<span data-ttu-id="dc30e-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji dla danej przestrzeni nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="dc30e-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc30e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc30e-104">SYNTAX</span></span>

### <span data-ttu-id="dc30e-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dc30e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc30e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc30e-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc30e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dc30e-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <SharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc30e-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dc30e-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc30e-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dc30e-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc30e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="dc30e-110">DESCRIPTION</span></span>
<span data-ttu-id="dc30e-111">Polecenie cmdlet **Set-AzureRmServiceBusAuthorizationRule** aktualizuje opis określonej reguły autoryzacji w danym obszarze nazw lub kolejce lub sekcji magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="dc30e-111">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="dc30e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc30e-112">EXAMPLES</span></span>

### <span data-ttu-id="dc30e-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dc30e-113">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="dc30e-114">Usuwa **Zarządzanie** z poziomu praw dostępu reguły autoryzacji `AuthoRule1` w obszarze nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="dc30e-114">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="dc30e-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dc30e-115">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="dc30e-116">Usuwa **Zarządzanie** z praw dostępu do reguły autoryzacji `AuthoRule1` w kolejce `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="dc30e-116">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="dc30e-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dc30e-117">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="dc30e-118">Usuwa **Zarządzanie** z poziomu praw dostępu do reguły autoryzacji `AuthoRule1` w temacie `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="dc30e-118">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="dc30e-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc30e-119">PARAMETERS</span></span>

### <span data-ttu-id="dc30e-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dc30e-120">-Confirm</span></span>
<span data-ttu-id="dc30e-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc30e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc30e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc30e-122">-InputObject</span></span>
<span data-ttu-id="dc30e-123">Obiekt AuthorizationRule ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="dc30e-123">ServiceBus AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc30e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc30e-124">-Name</span></span>
<span data-ttu-id="dc30e-125">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="dc30e-125">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc30e-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dc30e-126">-Namespace</span></span>
<span data-ttu-id="dc30e-127">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="dc30e-127">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc30e-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="dc30e-128">-Queue</span></span>
<span data-ttu-id="dc30e-129">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="dc30e-129">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc30e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc30e-130">-ResourceGroupName</span></span>
<span data-ttu-id="dc30e-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dc30e-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="dc30e-132">-Prawa</span><span class="sxs-lookup"><span data-stu-id="dc30e-132">-Rights</span></span>
<span data-ttu-id="dc30e-133">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="dc30e-133">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc30e-134">— Temat</span><span class="sxs-lookup"><span data-stu-id="dc30e-134">-Topic</span></span>
<span data-ttu-id="dc30e-135">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="dc30e-135">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc30e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc30e-136">-WhatIf</span></span>
<span data-ttu-id="dc30e-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc30e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc30e-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dc30e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc30e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc30e-139">-DefaultProfile</span></span>
<span data-ttu-id="dc30e-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc30e-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc30e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc30e-141">CommonParameters</span></span>
<span data-ttu-id="dc30e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc30e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc30e-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc30e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc30e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc30e-144">INPUTS</span></span>

### <span data-ttu-id="dc30e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="dc30e-145">System.String</span></span>
<span data-ttu-id="dc30e-146">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes system. String []</span><span class="sxs-lookup"><span data-stu-id="dc30e-146">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes System.String[]</span></span>

## <span data-ttu-id="dc30e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc30e-147">OUTPUTS</span></span>

### <span data-ttu-id="dc30e-148">Microsoft. Azure. Commands. ServiceBus. models. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dc30e-148">Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="dc30e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc30e-149">NOTES</span></span>

## <span data-ttu-id="dc30e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc30e-150">RELATED LINKS</span></span>

