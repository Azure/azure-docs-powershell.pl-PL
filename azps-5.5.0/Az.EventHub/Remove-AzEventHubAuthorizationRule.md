---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237869"
---
# <span data-ttu-id="aa1b8-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="aa1b8-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="aa1b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="aa1b8-103">Usuwa określoną regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="aa1b8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa1b8-104">SYNTAX</span></span>

### <span data-ttu-id="aa1b8-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="aa1b8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa1b8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="aa1b8-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa1b8-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa1b8-107">DESCRIPTION</span></span>
<span data-ttu-id="aa1b8-108">Polecenie Remove-AzEventHubAuthorizationRule cmdlet usuwa określoną regułę autoryzacji z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="aa1b8-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa1b8-109">EXAMPLES</span></span>

### <span data-ttu-id="aa1b8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa1b8-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="aa1b8-111">Usuwa regułę autoryzacji \` MyAuthRuleName \` z przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="aa1b8-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="aa1b8-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="aa1b8-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="aa1b8-113">Usuwa regułę autoryzacji \` MyAuthRuleName z centrum zdarzeń \` \` MyEventHubName. \`</span><span class="sxs-lookup"><span data-stu-id="aa1b8-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="aa1b8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa1b8-114">PARAMETERS</span></span>

### <span data-ttu-id="aa1b8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa1b8-115">-DefaultProfile</span></span>
<span data-ttu-id="aa1b8-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa1b8-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="aa1b8-117">-EventHub</span></span>
<span data-ttu-id="aa1b8-118">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="aa1b8-118">EventHub Name</span></span>

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

### <span data-ttu-id="aa1b8-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="aa1b8-119">-Force</span></span>
<span data-ttu-id="aa1b8-120">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="aa1b8-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="aa1b8-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aa1b8-121">-Name</span></span>
<span data-ttu-id="aa1b8-122">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="aa1b8-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="aa1b8-123">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="aa1b8-123">-Namespace</span></span>
<span data-ttu-id="aa1b8-124">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="aa1b8-124">Namespace Name</span></span>

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

### <span data-ttu-id="aa1b8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa1b8-125">-PassThru</span></span>
<span data-ttu-id="aa1b8-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="aa1b8-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa1b8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa1b8-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa1b8-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="aa1b8-129">Resource Group Name</span></span>

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

### <span data-ttu-id="aa1b8-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa1b8-130">-Confirm</span></span>
<span data-ttu-id="aa1b8-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa1b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa1b8-132">-WhatIf</span></span>
<span data-ttu-id="aa1b8-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa1b8-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa1b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa1b8-135">CommonParameters</span></span>
<span data-ttu-id="aa1b8-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa1b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa1b8-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa1b8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa1b8-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa1b8-138">INPUTS</span></span>

### <span data-ttu-id="aa1b8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="aa1b8-139">System.String</span></span>

## <span data-ttu-id="aa1b8-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa1b8-140">OUTPUTS</span></span>

### <span data-ttu-id="aa1b8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="aa1b8-141">System.Boolean</span></span>

## <span data-ttu-id="aa1b8-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa1b8-142">NOTES</span></span>

## <span data-ttu-id="aa1b8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa1b8-143">RELATED LINKS</span></span>
