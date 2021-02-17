---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 862b6f295a997b2027520a3f9c6a9f4f9cfb5ae9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200362"
---
# <span data-ttu-id="c0e4f-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0e4f-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c0e4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e4f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e4f-103">Aktualizuje określoną regułę autoryzacji w Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="c0e4f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c0e4f-104">SYNTAX</span></span>

### <span data-ttu-id="c0e4f-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="c0e4f-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e4f-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c0e4f-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e4f-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c0e4f-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e4f-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c0e4f-108">DESCRIPTION</span></span>
<span data-ttu-id="c0e4f-109">Polecenie Set-AzEventHubAuthorizationRule aktualizuje określoną regułę autoryzacji w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="c0e4f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c0e4f-110">EXAMPLES</span></span>

### <span data-ttu-id="c0e4f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0e4f-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="c0e4f-112">Aktualizuje regułę autoryzacji MyAuthRuleName, aby udzielić uprawnień zarządzania do centrum zdarzeń MyEventHubName o zakresie przestrzeni nazw \` \` \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="c0e4f-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c0e4f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0e4f-113">PARAMETERS</span></span>

### <span data-ttu-id="c0e4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e4f-114">-DefaultProfile</span></span>
<span data-ttu-id="c0e4f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0e4f-116">-EventHub</span><span class="sxs-lookup"><span data-stu-id="c0e4f-116">-EventHub</span></span>
<span data-ttu-id="c0e4f-117">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="c0e4f-117">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e4f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e4f-118">-InputObject</span></span>
<span data-ttu-id="c0e4f-119">Obiekt AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c0e4f-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e4f-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c0e4f-120">-Name</span></span>
<span data-ttu-id="c0e4f-121">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="c0e4f-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="c0e4f-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="c0e4f-122">-Namespace</span></span>
<span data-ttu-id="c0e4f-123">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="c0e4f-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e4f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e4f-124">-ResourceGroupName</span></span>
<span data-ttu-id="c0e4f-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c0e4f-125">Resource Group Name</span></span>

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

### <span data-ttu-id="c0e4f-126">— Prawa</span><span class="sxs-lookup"><span data-stu-id="c0e4f-126">-Rights</span></span>
<span data-ttu-id="c0e4f-127">Prawa, np. @("Posłuchaj","Wyślij","Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="c0e4f-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e4f-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0e4f-128">-Confirm</span></span>
<span data-ttu-id="c0e4f-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0e4f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e4f-130">-WhatIf</span></span>
<span data-ttu-id="c0e4f-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e4f-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0e4f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e4f-133">CommonParameters</span></span>
<span data-ttu-id="c0e4f-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0e4f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e4f-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0e4f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e4f-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0e4f-136">INPUTS</span></span>

### <span data-ttu-id="c0e4f-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c0e4f-137">System.String</span></span>

### <span data-ttu-id="c0e4f-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c0e4f-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="c0e4f-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="c0e4f-139">System.String[]</span></span>

## <span data-ttu-id="c0e4f-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0e4f-140">OUTPUTS</span></span>

### <span data-ttu-id="c0e4f-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="c0e4f-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="c0e4f-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c0e4f-142">NOTES</span></span>

## <span data-ttu-id="c0e4f-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0e4f-143">RELATED LINKS</span></span>
