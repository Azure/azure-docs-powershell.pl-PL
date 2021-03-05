---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: 5a33eae7e31ecdc793411bcddc2855d0dbcce8e9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961642"
---
# <span data-ttu-id="06052-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="06052-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="06052-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06052-102">SYNOPSIS</span></span>
<span data-ttu-id="06052-103">Usuwa regułę autoryzacji przestrzeni nazw, kolejki lub tematu autobusu usług z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06052-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="06052-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06052-104">SYNTAX</span></span>

### <span data-ttu-id="06052-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="06052-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06052-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="06052-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06052-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="06052-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06052-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="06052-108">DESCRIPTION</span></span>
<span data-ttu-id="06052-109">Polecenie **cmdlet Remove-AzServiceBusAuthorizationRule** usuwa regułę autoryzacji przestrzeni nazw, kolejki lub tematu autobusu usług dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06052-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="06052-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06052-110">EXAMPLES</span></span>

### <span data-ttu-id="06052-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06052-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="06052-112">Usuwa regułę autoryzacji `SBAuthoRule1` przestrzeni nazw `SB-Example1` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06052-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="06052-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06052-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="06052-114">Usuwa regułę autoryzacji `SBAuthoRule1` kolejki `SBQueue` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06052-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="06052-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="06052-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="06052-116">Usuwa regułę autoryzacji `SBAuthoRule1` tematu `SBTopic` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06052-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="06052-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06052-117">PARAMETERS</span></span>

### <span data-ttu-id="06052-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06052-118">-DefaultProfile</span></span>
<span data-ttu-id="06052-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06052-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06052-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="06052-120">-Force</span></span>
<span data-ttu-id="06052-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06052-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06052-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="06052-122">-InputObject</span></span>
<span data-ttu-id="06052-123">Obiekt ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="06052-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06052-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06052-124">-Name</span></span>
<span data-ttu-id="06052-125">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="06052-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="06052-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="06052-126">-Namespace</span></span>
<span data-ttu-id="06052-127">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="06052-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06052-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="06052-128">-PassThru</span></span>
<span data-ttu-id="06052-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="06052-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="06052-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="06052-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06052-131">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="06052-131">-Queue</span></span>
<span data-ttu-id="06052-132">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="06052-132">Queue Name</span></span>

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

### <span data-ttu-id="06052-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06052-133">-ResourceGroupName</span></span>
<span data-ttu-id="06052-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="06052-134">Resource Group Name</span></span>

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

### <span data-ttu-id="06052-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="06052-135">-Topic</span></span>
<span data-ttu-id="06052-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="06052-136">Topic Name</span></span>

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

### <span data-ttu-id="06052-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06052-137">-Confirm</span></span>
<span data-ttu-id="06052-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06052-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06052-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06052-139">-WhatIf</span></span>
<span data-ttu-id="06052-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06052-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06052-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06052-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06052-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06052-142">CommonParameters</span></span>
<span data-ttu-id="06052-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06052-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06052-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06052-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06052-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06052-145">INPUTS</span></span>

### <span data-ttu-id="06052-146">System.String</span><span class="sxs-lookup"><span data-stu-id="06052-146">System.String</span></span>

### <span data-ttu-id="06052-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="06052-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="06052-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06052-148">OUTPUTS</span></span>

### <span data-ttu-id="06052-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="06052-149">System.Boolean</span></span>

## <span data-ttu-id="06052-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06052-150">NOTES</span></span>

## <span data-ttu-id="06052-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06052-151">RELATED LINKS</span></span>
