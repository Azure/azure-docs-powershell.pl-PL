---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 35e3889603dc7e86a7d10679864adfd34a880b66
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717085"
---
# <span data-ttu-id="7e01c-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7e01c-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="7e01c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7e01c-102">SYNOPSIS</span></span>
<span data-ttu-id="7e01c-103">Usuwa określoną regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7e01c-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e01c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7e01c-104">SYNTAX</span></span>

### <span data-ttu-id="7e01c-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7e01c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e01c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7e01c-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String>
 [-EventHub] <String> [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e01c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7e01c-107">DESCRIPTION</span></span>
<span data-ttu-id="7e01c-108">Polecenie cmdlet Remove-AzureRmEventHubAuthorizationRule powoduje usunięcie i usunięcie określonej reguły autoryzacji z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7e01c-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="7e01c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7e01c-109">EXAMPLES</span></span>

### <span data-ttu-id="7e01c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7e01c-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="7e01c-111">Usuwa regułę autoryzacji \` MyAuthRuleName \` z obszaru nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="7e01c-111">Removes the authorization rule \`MyAuthRuleName\` from the Namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="7e01c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7e01c-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="7e01c-113">Usuwa regułę autoryzacji \` MyAuthRuleName \` z MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="7e01c-113">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="7e01c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e01c-114">PARAMETERS</span></span>

### <span data-ttu-id="7e01c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e01c-115">-DefaultProfile</span></span>
<span data-ttu-id="7e01c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e01c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e01c-117">— EventHub</span><span class="sxs-lookup"><span data-stu-id="7e01c-117">-EventHub</span></span>
<span data-ttu-id="7e01c-118">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="7e01c-118">EventHub Name</span></span>

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

### <span data-ttu-id="7e01c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="7e01c-119">-Force</span></span>
<span data-ttu-id="7e01c-120">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="7e01c-120">Do not ask for confirmation</span></span>

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

### <span data-ttu-id="7e01c-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7e01c-121">-Name</span></span>
<span data-ttu-id="7e01c-122">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7e01c-122">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="7e01c-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7e01c-123">-Namespace</span></span>
<span data-ttu-id="7e01c-124">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7e01c-124">Namespace Name</span></span>

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

### <span data-ttu-id="7e01c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e01c-125">-PassThru</span></span>
<span data-ttu-id="7e01c-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="7e01c-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7e01c-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7e01c-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7e01c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e01c-128">-ResourceGroupName</span></span>
<span data-ttu-id="7e01c-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7e01c-129">Resource Group Name</span></span>

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

### <span data-ttu-id="7e01c-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e01c-130">-Confirm</span></span>
<span data-ttu-id="7e01c-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e01c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e01c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e01c-132">-WhatIf</span></span>
<span data-ttu-id="7e01c-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e01c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e01c-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7e01c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e01c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e01c-135">CommonParameters</span></span>
<span data-ttu-id="7e01c-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e01c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e01c-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e01c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e01c-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e01c-138">INPUTS</span></span>

### <span data-ttu-id="7e01c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7e01c-139">System.String</span></span>

## <span data-ttu-id="7e01c-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7e01c-140">OUTPUTS</span></span>

### <span data-ttu-id="7e01c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7e01c-141">System.Boolean</span></span>

## <span data-ttu-id="7e01c-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7e01c-142">NOTES</span></span>

## <span data-ttu-id="7e01c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e01c-143">RELATED LINKS</span></span>
