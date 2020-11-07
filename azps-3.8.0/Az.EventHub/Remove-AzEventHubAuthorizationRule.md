---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 91c38686d8621f3bba521d738cc125e4b8473188
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894769"
---
# <span data-ttu-id="20cb3-101">Remove-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="20cb3-101">Remove-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="20cb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="20cb3-103">Usuwa określoną regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="20cb3-103">Removes the specified Event Hub authorization rule.</span></span>

## <span data-ttu-id="20cb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20cb3-104">SYNTAX</span></span>

### <span data-ttu-id="20cb3-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20cb3-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20cb3-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="20cb3-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20cb3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20cb3-107">DESCRIPTION</span></span>
<span data-ttu-id="20cb3-108">Polecenie cmdlet Remove-AzEventHubAuthorizationRule powoduje usunięcie i usunięcie określonej reguły autoryzacji z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="20cb3-108">The Remove-AzEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="20cb3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20cb3-109">EXAMPLES</span></span>

### <span data-ttu-id="20cb3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20cb3-110">Example 1</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="20cb3-111">Usuwa regułę autoryzacji \` MyAuthRuleName \` z obszaru nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="20cb3-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="20cb3-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="20cb3-112">Example 2</span></span>
```
PS C:\> Remove-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="20cb3-113">Usuwa regułę autoryzacji \` MyAuthRuleName \` z MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="20cb3-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="20cb3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20cb3-114">PARAMETERS</span></span>

### <span data-ttu-id="20cb3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20cb3-115">-DefaultProfile</span></span>
<span data-ttu-id="20cb3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20cb3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20cb3-117">— EventHub</span><span class="sxs-lookup"><span data-stu-id="20cb3-117">-EventHub</span></span>
<span data-ttu-id="20cb3-118">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="20cb3-118">EventHub Name</span></span>

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

### <span data-ttu-id="20cb3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="20cb3-119">-Force</span></span>
<span data-ttu-id="20cb3-120">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="20cb3-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="20cb3-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20cb3-121">-Name</span></span>
<span data-ttu-id="20cb3-122">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="20cb3-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="20cb3-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="20cb3-123">-Namespace</span></span>
<span data-ttu-id="20cb3-124">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="20cb3-124">Namespace Name</span></span>

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

### <span data-ttu-id="20cb3-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20cb3-125">-PassThru</span></span>
<span data-ttu-id="20cb3-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="20cb3-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="20cb3-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="20cb3-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="20cb3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20cb3-128">-ResourceGroupName</span></span>
<span data-ttu-id="20cb3-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="20cb3-129">Resource Group Name</span></span>

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

### <span data-ttu-id="20cb3-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20cb3-130">-Confirm</span></span>
<span data-ttu-id="20cb3-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20cb3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20cb3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20cb3-132">-WhatIf</span></span>
<span data-ttu-id="20cb3-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20cb3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20cb3-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20cb3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20cb3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20cb3-135">CommonParameters</span></span>
<span data-ttu-id="20cb3-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20cb3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20cb3-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20cb3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20cb3-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20cb3-138">INPUTS</span></span>

### <span data-ttu-id="20cb3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="20cb3-139">System.String</span></span>

## <span data-ttu-id="20cb3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20cb3-140">OUTPUTS</span></span>

### <span data-ttu-id="20cb3-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20cb3-141">System.Boolean</span></span>

## <span data-ttu-id="20cb3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20cb3-142">NOTES</span></span>

## <span data-ttu-id="20cb3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20cb3-143">RELATED LINKS</span></span>
