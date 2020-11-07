---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 53358ef1afc53eed779000c7bb8912b312980784
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705430"
---
# <span data-ttu-id="7a0a2-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="7a0a2-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="7a0a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a0a2-102">SYNOPSIS</span></span>
<span data-ttu-id="7a0a2-103">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7a0a2-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="7a0a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a0a2-104">SYNTAX</span></span>

### <span data-ttu-id="7a0a2-105">IPRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a0a2-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a0a2-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a0a2-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a0a2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7a0a2-107">DESCRIPTION</span></span>
<span data-ttu-id="7a0a2-108">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7a0a2-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="7a0a2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a0a2-109">EXAMPLES</span></span>

### <span data-ttu-id="7a0a2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a0a2-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="7a0a2-111">Usuwa IpMask NetworkRuleSet z danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="7a0a2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a0a2-112">PARAMETERS</span></span>

### <span data-ttu-id="7a0a2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7a0a2-113">-AsJob</span></span>
<span data-ttu-id="7a0a2-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7a0a2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7a0a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a0a2-115">-DefaultProfile</span></span>
<span data-ttu-id="7a0a2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a0a2-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="7a0a2-117">-IpMask</span></span>
<span data-ttu-id="7a0a2-118">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="7a0a2-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="7a0a2-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="7a0a2-119">-IpRuleObject</span></span>
<span data-ttu-id="7a0a2-120">Obiekt konfiguracji IPRule</span><span class="sxs-lookup"><span data-stu-id="7a0a2-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="7a0a2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a0a2-121">-Name</span></span>
<span data-ttu-id="7a0a2-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7a0a2-122">Namespace Name</span></span>

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

### <span data-ttu-id="7a0a2-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a0a2-123">-PassThru</span></span>
<span data-ttu-id="7a0a2-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7a0a2-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7a0a2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a0a2-125">-ResourceGroupName</span></span>
<span data-ttu-id="7a0a2-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7a0a2-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7a0a2-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a0a2-127">-Confirm</span></span>
<span data-ttu-id="7a0a2-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a0a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a0a2-129">-WhatIf</span></span>
<span data-ttu-id="7a0a2-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a0a2-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a0a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a0a2-132">CommonParameters</span></span>
<span data-ttu-id="7a0a2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a0a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7a0a2-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a0a2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a0a2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a0a2-135">INPUTS</span></span>

### <span data-ttu-id="7a0a2-136">System. String</span><span class="sxs-lookup"><span data-stu-id="7a0a2-136">System.String</span></span>

### <span data-ttu-id="7a0a2-137">Microsoft. Azure. Commands. EventHub. modele. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7a0a2-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="7a0a2-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a0a2-138">OUTPUTS</span></span>

### <span data-ttu-id="7a0a2-139">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="7a0a2-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="7a0a2-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a0a2-140">NOTES</span></span>

## <span data-ttu-id="7a0a2-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a0a2-141">RELATED LINKS</span></span>