---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 496806b6d5ab6b7d6e1c788b7b42424b7e97a8c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992755"
---
# <span data-ttu-id="524e5-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="524e5-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="524e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="524e5-102">SYNOPSIS</span></span>
<span data-ttu-id="524e5-103">Usuwa określoną regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="524e5-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="524e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="524e5-104">SYNTAX</span></span>

### <span data-ttu-id="524e5-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="524e5-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="524e5-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="524e5-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="524e5-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="524e5-107">DESCRIPTION</span></span>
<span data-ttu-id="524e5-108">Polecenie Remove-AzEventHubAuthorizationRule cmdlet usuwa określoną regułę autoryzacji z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="524e5-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="524e5-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="524e5-109">EXAMPLES</span></span>

### <span data-ttu-id="524e5-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="524e5-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="524e5-111">Usuwa regułę autoryzacji \` MyAuthRuleName \` z przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="524e5-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="524e5-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="524e5-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="524e5-113">Usuwa regułę autoryzacji \` MyAuthRuleName z centrum zdarzeń \` \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="524e5-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="524e5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="524e5-114">PARAMETERS</span></span>

### <span data-ttu-id="524e5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="524e5-115">-DefaultProfile</span></span>
<span data-ttu-id="524e5-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="524e5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="524e5-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="524e5-117">-EventHub</span></span>
<span data-ttu-id="524e5-118">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="524e5-118">EventHub Name</span></span>

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

### <span data-ttu-id="524e5-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="524e5-119">-Force</span></span>
<span data-ttu-id="524e5-120">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="524e5-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="524e5-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="524e5-121">-Name</span></span>
<span data-ttu-id="524e5-122">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="524e5-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="524e5-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="524e5-123">-Namespace</span></span>
<span data-ttu-id="524e5-124">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="524e5-124">Namespace Name</span></span>

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

### <span data-ttu-id="524e5-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="524e5-125">-PassThru</span></span>
<span data-ttu-id="524e5-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="524e5-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="524e5-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="524e5-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="524e5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="524e5-128">-ResourceGroupName</span></span>
<span data-ttu-id="524e5-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="524e5-129">Resource Group Name</span></span>

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

### <span data-ttu-id="524e5-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="524e5-130">-Confirm</span></span>
<span data-ttu-id="524e5-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="524e5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="524e5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="524e5-132">-WhatIf</span></span>
<span data-ttu-id="524e5-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="524e5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="524e5-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="524e5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="524e5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="524e5-135">CommonParameters</span></span>
<span data-ttu-id="524e5-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="524e5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="524e5-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="524e5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="524e5-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="524e5-138">INPUTS</span></span>

### <span data-ttu-id="524e5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="524e5-139">System.String</span></span>

## <span data-ttu-id="524e5-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="524e5-140">OUTPUTS</span></span>

### <span data-ttu-id="524e5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="524e5-141">System.Boolean</span></span>

## <span data-ttu-id="524e5-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="524e5-142">NOTES</span></span>

## <span data-ttu-id="524e5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="524e5-143">RELATED LINKS</span></span>
