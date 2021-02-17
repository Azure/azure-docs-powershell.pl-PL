---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198675"
---
# <span data-ttu-id="5ddab-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ddab-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="5ddab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ddab-102">SYNOPSIS</span></span>
<span data-ttu-id="5ddab-103">Usuwa regułę autoryzacji przestrzeni nazw, kolejki lub tematu autobusu usług z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ddab-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="5ddab-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ddab-104">SYNTAX</span></span>

### <span data-ttu-id="5ddab-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5ddab-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ddab-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ddab-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ddab-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="5ddab-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ddab-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ddab-108">DESCRIPTION</span></span>
<span data-ttu-id="5ddab-109">Polecenie **cmdlet Remove-AzServiceBusAuthorizationRule** usuwa regułę autoryzacji przestrzeni nazw, kolejki lub tematu autobusu usług dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ddab-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="5ddab-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ddab-110">EXAMPLES</span></span>

### <span data-ttu-id="5ddab-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ddab-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="5ddab-112">Usuwa regułę autoryzacji `SBAuthoRule1` przestrzeni nazw `SB-Example1` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ddab-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="5ddab-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5ddab-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="5ddab-114">Usuwa regułę autoryzacji `SBAuthoRule1` kolejki `SBQueue` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ddab-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="5ddab-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5ddab-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="5ddab-116">Usuwa regułę autoryzacji `SBAuthoRule1` tematu `SBTopic` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ddab-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="5ddab-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ddab-117">PARAMETERS</span></span>

### <span data-ttu-id="5ddab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ddab-118">-DefaultProfile</span></span>
<span data-ttu-id="5ddab-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ddab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ddab-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5ddab-120">-Force</span></span>
<span data-ttu-id="5ddab-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ddab-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ddab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ddab-122">-InputObject</span></span>
<span data-ttu-id="5ddab-123">Obiekt ServiceBus AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="5ddab-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="5ddab-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5ddab-124">-Name</span></span>
<span data-ttu-id="5ddab-125">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="5ddab-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="5ddab-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="5ddab-126">-Namespace</span></span>
<span data-ttu-id="5ddab-127">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="5ddab-127">Namespace Name</span></span>

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

### <span data-ttu-id="5ddab-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ddab-128">-PassThru</span></span>
<span data-ttu-id="5ddab-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="5ddab-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5ddab-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5ddab-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5ddab-131">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="5ddab-131">-Queue</span></span>
<span data-ttu-id="5ddab-132">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="5ddab-132">Queue Name</span></span>

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

### <span data-ttu-id="5ddab-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ddab-133">-ResourceGroupName</span></span>
<span data-ttu-id="5ddab-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="5ddab-134">Resource Group Name</span></span>

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

### <span data-ttu-id="5ddab-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="5ddab-135">-Topic</span></span>
<span data-ttu-id="5ddab-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="5ddab-136">Topic Name</span></span>

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

### <span data-ttu-id="5ddab-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ddab-137">-Confirm</span></span>
<span data-ttu-id="5ddab-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ddab-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ddab-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ddab-139">-WhatIf</span></span>
<span data-ttu-id="5ddab-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ddab-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ddab-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ddab-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ddab-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ddab-142">CommonParameters</span></span>
<span data-ttu-id="5ddab-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ddab-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ddab-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ddab-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ddab-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ddab-145">INPUTS</span></span>

### <span data-ttu-id="5ddab-146">System.String</span><span class="sxs-lookup"><span data-stu-id="5ddab-146">System.String</span></span>

### <span data-ttu-id="5ddab-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="5ddab-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="5ddab-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ddab-148">OUTPUTS</span></span>

### <span data-ttu-id="5ddab-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ddab-149">System.Boolean</span></span>

## <span data-ttu-id="5ddab-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ddab-150">NOTES</span></span>

## <span data-ttu-id="5ddab-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ddab-151">RELATED LINKS</span></span>
