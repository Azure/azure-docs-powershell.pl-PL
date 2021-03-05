---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 4e28f829a9daa17d5d6f44af10f21e8dc3b1f929
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015889"
---
# <span data-ttu-id="a9a0e-101">Set-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a9a0e-101">Set-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="a9a0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9a0e-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a0e-103">Aktualizuje opis określonej reguły autoryzacji dla danej przestrzeni nazw, kolejki lub tematu danego autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-103">Updates the specified authorization rule description for the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="a9a0e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a9a0e-104">SYNTAX</span></span>

### <span data-ttu-id="a9a0e-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a9a0e-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a0e-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9a0e-106">QueueAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a0e-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a9a0e-107">TopicAuthorizationRuleSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9a0e-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a9a0e-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9a0e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a9a0e-109">DESCRIPTION</span></span>
<span data-ttu-id="a9a0e-110">Polecenie **cmdlet Set-AzServiceBusAuthorizationRule** aktualizuje opis określonej reguły autoryzacji w danej przestrzeni nazw, kolejce lub temacie autobusu usługi.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-110">The **Set-AzServiceBusAuthorizationRule** cmdlet updates the description for the specified authorization rule in the given Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="a9a0e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a9a0e-111">EXAMPLES</span></span>

### <span data-ttu-id="a9a0e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9a0e-112">Example 1</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="a9a0e-113">Usuwa zarządzanie **z** praw dostępu reguły autoryzacji w `AuthoRule1` przestrzeni `SB-Example1` nazw.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-113">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in namespace `SB-Example1`.</span></span>

### <span data-ttu-id="a9a0e-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a9a0e-114">Example 2</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="a9a0e-115">Usuwa zarządzanie **z** praw dostępu reguły autoryzacji w `AuthoRule1` `SBQueue` kolejce.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-115">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in queue `SBQueue`.</span></span>

### <span data-ttu-id="a9a0e-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a9a0e-116">Example 3</span></span>
```powershell
PS C:\> $authRuleObj = Get-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1

PS C:\> $authRuleObj.Rights.Remove("Manage")

PS C:\> Set-AzServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -InputObj $authRuleObj
```

<span data-ttu-id="a9a0e-117">Usuwa zarządzanie **z** praw dostępu do reguły autoryzacji w `AuthoRule1` tym `SBTopic` temacie.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-117">Removes **Manage** from the access rights of the authorization rule `AuthoRule1` in topic `SBTopic`.</span></span>

## <span data-ttu-id="a9a0e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a9a0e-118">PARAMETERS</span></span>

### <span data-ttu-id="a9a0e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9a0e-119">-DefaultProfile</span></span>
<span data-ttu-id="a9a0e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a0e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9a0e-121">-InputObject</span></span>
<span data-ttu-id="a9a0e-122">Obiekt ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a9a0e-122">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="a9a0e-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a9a0e-123">-Name</span></span>
<span data-ttu-id="a9a0e-124">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="a9a0e-124">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="a9a0e-125">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="a9a0e-125">-Namespace</span></span>
<span data-ttu-id="a9a0e-126">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="a9a0e-126">Namespace Name</span></span>

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

### <span data-ttu-id="a9a0e-127">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="a9a0e-127">-Queue</span></span>
<span data-ttu-id="a9a0e-128">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="a9a0e-128">Queue Name</span></span>

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

### <span data-ttu-id="a9a0e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a0e-129">-ResourceGroupName</span></span>
<span data-ttu-id="a9a0e-130">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a9a0e-130">Resource Group Name</span></span>

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

### <span data-ttu-id="a9a0e-131">— Prawa</span><span class="sxs-lookup"><span data-stu-id="a9a0e-131">-Rights</span></span>
<span data-ttu-id="a9a0e-132">Prawa, np. @("Posłuchaj","Wyślij","Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="a9a0e-132">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="a9a0e-133">— Temat</span><span class="sxs-lookup"><span data-stu-id="a9a0e-133">-Topic</span></span>
<span data-ttu-id="a9a0e-134">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="a9a0e-134">Topic Name</span></span>

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

### <span data-ttu-id="a9a0e-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9a0e-135">-Confirm</span></span>
<span data-ttu-id="a9a0e-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9a0e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a0e-137">-WhatIf</span></span>
<span data-ttu-id="a9a0e-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9a0e-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9a0e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a0e-140">CommonParameters</span></span>
<span data-ttu-id="a9a0e-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a0e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a0e-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a0e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a0e-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9a0e-143">INPUTS</span></span>

### <span data-ttu-id="a9a0e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a9a0e-144">System.String</span></span>

### <span data-ttu-id="a9a0e-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a9a0e-145">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="a9a0e-146">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a9a0e-146">System.String[]</span></span>

## <span data-ttu-id="a9a0e-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9a0e-147">OUTPUTS</span></span>

### <span data-ttu-id="a9a0e-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a9a0e-148">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a9a0e-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a9a0e-149">NOTES</span></span>

## <span data-ttu-id="a9a0e-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9a0e-150">RELATED LINKS</span></span>
