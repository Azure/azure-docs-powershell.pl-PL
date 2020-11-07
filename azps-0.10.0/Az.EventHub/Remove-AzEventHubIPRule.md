---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubiprule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/EventHub/EventHub/help/Remove-AzEventHubIPRule.md
ms.openlocfilehash: ee52da845460def78e241d34f25aa9a997e4b7db
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891441"
---
# <span data-ttu-id="41d97-101">Remove-AzEventHubIPRule</span><span class="sxs-lookup"><span data-stu-id="41d97-101">Remove-AzEventHubIPRule</span></span>

## <span data-ttu-id="41d97-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41d97-102">SYNOPSIS</span></span>
<span data-ttu-id="41d97-103">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="41d97-103">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="41d97-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41d97-104">SYNTAX</span></span>

### <span data-ttu-id="41d97-105">IPRulePropertiesParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="41d97-105">IPRulePropertiesParameterSet (Default)</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String> [-IpMask] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="41d97-106">IPRuleInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="41d97-106">IPRuleInputObjectParameterSet</span></span>
```
Remove-AzEventHubIPRule [-ResourceGroupName] <String> [-Name] <String>
 [-IpRuleObject] <PSNWRuleSetIpRulesAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="41d97-107">Opis</span><span class="sxs-lookup"><span data-stu-id="41d97-107">DESCRIPTION</span></span>
<span data-ttu-id="41d97-108">Usuwanie pojedynczej reguły IP do NetworkRuleSet z określonego obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="41d97-108">Remove a single IP rule to the NetworkRuleSet of the given Namespace</span></span>

## <span data-ttu-id="41d97-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41d97-109">EXAMPLES</span></span>

### <span data-ttu-id="41d97-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="41d97-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubIPRule -ResourceGroupName v-ajnavtest -Namespace Eventhub-Namespace1-2389 -IpMask "11.22.33.44"
```

<span data-ttu-id="41d97-111">Usuwa IpMask NetworkRuleSet z danej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="41d97-111">Removes IpMask of the NetworkRuleSet of the given namespace</span></span>

## <span data-ttu-id="41d97-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41d97-112">PARAMETERS</span></span>

### <span data-ttu-id="41d97-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="41d97-113">-AsJob</span></span>
<span data-ttu-id="41d97-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="41d97-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="41d97-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41d97-115">-DefaultProfile</span></span>
<span data-ttu-id="41d97-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41d97-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41d97-117">-IpMask</span><span class="sxs-lookup"><span data-stu-id="41d97-117">-IpMask</span></span>
<span data-ttu-id="41d97-118">Identyfikator zasobu podsieci</span><span class="sxs-lookup"><span data-stu-id="41d97-118">Subnet Resource ID</span></span>

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

### <span data-ttu-id="41d97-119">-IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="41d97-119">-IpRuleObject</span></span>
<span data-ttu-id="41d97-120">Obiekt konfiguracji IPRule</span><span class="sxs-lookup"><span data-stu-id="41d97-120">IPRule Configuration Object</span></span>

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

### <span data-ttu-id="41d97-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41d97-121">-Name</span></span>
<span data-ttu-id="41d97-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="41d97-122">Namespace Name</span></span>

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

### <span data-ttu-id="41d97-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41d97-123">-PassThru</span></span>
<span data-ttu-id="41d97-124">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="41d97-124">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="41d97-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41d97-125">-ResourceGroupName</span></span>
<span data-ttu-id="41d97-126">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="41d97-126">Resource Group Name</span></span>

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

### <span data-ttu-id="41d97-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="41d97-127">-Confirm</span></span>
<span data-ttu-id="41d97-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d97-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="41d97-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="41d97-129">-WhatIf</span></span>
<span data-ttu-id="41d97-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41d97-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="41d97-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="41d97-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="41d97-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41d97-132">CommonParameters</span></span>
<span data-ttu-id="41d97-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41d97-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="41d97-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41d97-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41d97-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41d97-135">INPUTS</span></span>

### <span data-ttu-id="41d97-136">System. String</span><span class="sxs-lookup"><span data-stu-id="41d97-136">System.String</span></span>

### <span data-ttu-id="41d97-137">Microsoft. Azure. Commands. EventHub. modele. PSNWRuleSetIpRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="41d97-137">Microsoft.Azure.Commands.EventHub.Models.PSNWRuleSetIpRulesAttributes</span></span>

## <span data-ttu-id="41d97-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41d97-138">OUTPUTS</span></span>

### <span data-ttu-id="41d97-139">Microsoft. Azure. Commands. EventHub. modele. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="41d97-139">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="41d97-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41d97-140">NOTES</span></span>

## <span data-ttu-id="41d97-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41d97-141">RELATED LINKS</span></span>