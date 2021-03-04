---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: c8a42bd69cc253d66fede2339f4080558e2f07cb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986070"
---
# <span data-ttu-id="ce7f0-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="ce7f0-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="ce7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7f0-103">Usuwanie jednej reguły IP do zestawu NetworkRuleSet danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ce7f0-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ce7f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ce7f0-104">SYNTAX</span></span>

### <span data-ttu-id="ce7f0-105">IPRulePropertiesParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ce7f0-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7f0-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce7f0-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce7f0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ce7f0-107">DESCRIPTION</span></span>
<span data-ttu-id="ce7f0-108">Usuwanie jednej reguły IP do zestawu NetworkRuleSet danej przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ce7f0-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="ce7f0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ce7f0-109">EXAMPLES</span></span>

### <span data-ttu-id="ce7f0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce7f0-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="ce7f0-111">Usuwamas ip (IpMask) zestawu NetworkRuleSet danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="ce7f0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce7f0-112">PARAMETERS</span></span>

### <span data-ttu-id="ce7f0-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ce7f0-113">-AsJob</span></span>
<span data-ttu-id="ce7f0-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ce7f0-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce7f0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7f0-115">-DefaultProfile</span></span>
<span data-ttu-id="ce7f0-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7f0-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="ce7f0-117">-IpMask</span></span>
<span data-ttu-id="ce7f0-118">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="ce7f0-118">Subnet Resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: IPRulePropertiesParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7f0-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="ce7f0-119">-IpRuleObject</span></span>
<span data-ttu-id="ce7f0-120">Obiekt konfiguracji protokołu IPRule</span><span class="sxs-lookup"><span data-stu-id="ce7f0-120">IPRule Configuration Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes
Parameter Sets: IPRuleInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce7f0-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ce7f0-121">-Name</span></span>
<span data-ttu-id="ce7f0-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="ce7f0-122">Namespace Name</span></span>

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

### <span data-ttu-id="ce7f0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce7f0-123">-PassThru</span></span>
<span data-ttu-id="ce7f0-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ce7f0-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ce7f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="ce7f0-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ce7f0-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ce7f0-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce7f0-127">-Confirm</span></span>
<span data-ttu-id="ce7f0-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7f0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7f0-129">-WhatIf</span></span>
<span data-ttu-id="ce7f0-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce7f0-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7f0-132">CommonParameters</span></span>
<span data-ttu-id="ce7f0-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ce7f0-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce7f0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7f0-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce7f0-135">INPUTS</span></span>

### <span data-ttu-id="ce7f0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="ce7f0-136">System.String</span></span>

### <span data-ttu-id="ce7f0-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ce7f0-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="ce7f0-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce7f0-138">OUTPUTS</span></span>

### <span data-ttu-id="ce7f0-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ce7f0-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ce7f0-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ce7f0-140">NOTES</span></span>

## <span data-ttu-id="ce7f0-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce7f0-141">RELATED LINKS</span></span>