---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 2b4ddf625e5565de0d345a5477d3ba368dcb186b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718271"
---
# <span data-ttu-id="12b58-101">Set-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12b58-101">Set-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="12b58-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12b58-102">SYNOPSIS</span></span>
<span data-ttu-id="12b58-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji dla danej przestrzeni nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="12b58-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12b58-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12b58-104">SYNTAX</span></span>

### <span data-ttu-id="12b58-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12b58-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b58-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12b58-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b58-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="12b58-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12b58-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12b58-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12b58-109">Opis</span><span class="sxs-lookup"><span data-stu-id="12b58-109">DESCRIPTION</span></span>
<span data-ttu-id="12b58-110">Polecenie cmdlet **Set-AzureRmServiceBusAuthorizationRule** aktualizuje opis określonej reguły autoryzacji w danym obszarze nazw lub kolejce lub sekcji magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="12b58-110">The **Set-AzureRmServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="12b58-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12b58-111">EXAMPLES</span></span>

### <span data-ttu-id="12b58-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="12b58-112">Example 1</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="12b58-113">Usuwa **Zarządzanie** z poziomu praw dostępu reguły autoryzacji `AuthoRule1` w obszarze nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="12b58-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="12b58-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="12b58-114">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="12b58-115">Usuwa **Zarządzanie** z praw dostępu do reguły autoryzacji `AuthoRule1` w kolejce `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="12b58-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="12b58-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="12b58-116">Example 2</span></span>
```
PS C:\> $authRuleObj = Get-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="12b58-117">Usuwa **Zarządzanie** z poziomu praw dostępu do reguły autoryzacji `AuthoRule1` w temacie `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="12b58-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="12b58-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12b58-118">PARAMETERS</span></span>

### <span data-ttu-id="12b58-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12b58-119">-DefaultProfile</span></span>
<span data-ttu-id="12b58-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12b58-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12b58-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12b58-121">-InputObject</span></span>
<span data-ttu-id="12b58-122">Obiekt AuthorizationRule ServiceBus</span><span class="sxs-lookup"><span data-stu-id="12b58-122">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12b58-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12b58-123">-Name</span></span>
<span data-ttu-id="12b58-124">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12b58-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="12b58-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12b58-125">-Namespace</span></span>
<span data-ttu-id="12b58-126">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="12b58-126">Namespace Name</span></span>

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

### <span data-ttu-id="12b58-127">-Queue</span><span class="sxs-lookup"><span data-stu-id="12b58-127">-Queue</span></span>
<span data-ttu-id="12b58-128">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="12b58-128">Queue Name</span></span>

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

### <span data-ttu-id="12b58-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12b58-129">-ResourceGroupName</span></span>
<span data-ttu-id="12b58-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="12b58-130">Resource Group Name</span></span>

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

### <span data-ttu-id="12b58-131">-Prawa</span><span class="sxs-lookup"><span data-stu-id="12b58-131">-Rights</span></span>
<span data-ttu-id="12b58-132">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="12b58-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12b58-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="12b58-133">-Topic</span></span>
<span data-ttu-id="12b58-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="12b58-134">Topic Name</span></span>

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

### <span data-ttu-id="12b58-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12b58-135">-Confirm</span></span>
<span data-ttu-id="12b58-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b58-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12b58-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12b58-137">-WhatIf</span></span>
<span data-ttu-id="12b58-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12b58-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12b58-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="12b58-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12b58-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12b58-140">CommonParameters</span></span>
<span data-ttu-id="12b58-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12b58-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12b58-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12b58-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12b58-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12b58-143">INPUTS</span></span>

### <span data-ttu-id="12b58-144">System. String</span><span class="sxs-lookup"><span data-stu-id="12b58-144">System.String</span></span>

### <span data-ttu-id="12b58-145">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="12b58-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="12b58-146">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="12b58-146">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="12b58-147">System. String []</span><span class="sxs-lookup"><span data-stu-id="12b58-147">System.String[]</span></span>

## <span data-ttu-id="12b58-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12b58-148">OUTPUTS</span></span>

### <span data-ttu-id="12b58-149">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="12b58-149">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="12b58-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12b58-150">NOTES</span></span>

## <span data-ttu-id="12b58-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12b58-151">RELATED LINKS</span></span>
