---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: 00213d4829d4b389f19a01ad9748517608657136
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233138"
---
# <span data-ttu-id="19de1-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="19de1-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="19de1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19de1-102">SYNOPSIS</span></span>
<span data-ttu-id="19de1-103">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="19de1-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="19de1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19de1-104">SYNTAX</span></span>

### <span data-ttu-id="19de1-105">IPRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19de1-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19de1-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19de1-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19de1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="19de1-107">DESCRIPTION</span></span>
<span data-ttu-id="19de1-108">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="19de1-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="19de1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19de1-109">EXAMPLES</span></span>

### <span data-ttu-id="19de1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="19de1-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="19de1-111">Usuwa IpMask NetworkRuleSet z danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="19de1-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="19de1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19de1-112">PARAMETERS</span></span>

### <span data-ttu-id="19de1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="19de1-113">-AsJob</span></span>
<span data-ttu-id="19de1-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="19de1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="19de1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19de1-115">-DefaultProfile</span></span>
<span data-ttu-id="19de1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19de1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19de1-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="19de1-117">-IpMask</span></span>
<span data-ttu-id="19de1-118">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="19de1-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="19de1-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="19de1-119">-IpRuleObject</span></span>
<span data-ttu-id="19de1-120">Obiekt konfiguracji IPRule</span><span class="sxs-lookup"><span data-stu-id="19de1-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="19de1-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19de1-121">-Name</span></span>
<span data-ttu-id="19de1-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="19de1-122">Namespace Name</span></span>

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

### <span data-ttu-id="19de1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19de1-123">-PassThru</span></span>
<span data-ttu-id="19de1-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="19de1-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="19de1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19de1-125">-ResourceGroupName</span></span>
<span data-ttu-id="19de1-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="19de1-126">Resource Group Name</span></span>

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

### <span data-ttu-id="19de1-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19de1-127">-Confirm</span></span>
<span data-ttu-id="19de1-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19de1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19de1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19de1-129">-WhatIf</span></span>
<span data-ttu-id="19de1-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19de1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19de1-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19de1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19de1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19de1-132">CommonParameters</span></span>
<span data-ttu-id="19de1-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19de1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="19de1-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19de1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19de1-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19de1-135">INPUTS</span></span>

### <span data-ttu-id="19de1-136">System. String</span><span class="sxs-lookup"><span data-stu-id="19de1-136">System.String</span></span>

### <span data-ttu-id="19de1-137">Microsoft. Azure. Commands. EventHub. modele. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="19de1-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="19de1-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19de1-138">OUTPUTS</span></span>

### <span data-ttu-id="19de1-139">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="19de1-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="19de1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19de1-140">NOTES</span></span>

## <span data-ttu-id="19de1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19de1-141">RELATED LINKS</span></span>