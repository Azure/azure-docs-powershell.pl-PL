---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/update-azcognitiveservicesaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Update-AzCognitiveServicesAccountNetworkRuleSet.md
ms.openlocfilehash: 0f094ba8bdfa8dbf40f2af8495ee2f8cfa6fca16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326816"
---
# <span data-ttu-id="ce088-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce088-101">Update-AzCognitiveServicesAccountNetworkRuleSet</span></span>

## <span data-ttu-id="ce088-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce088-102">SYNOPSIS</span></span>
<span data-ttu-id="ce088-103">Aktualizowanie właściwości NetworkRule konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="ce088-103">Update the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ce088-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce088-104">SYNTAX</span></span>

```
Update-AzCognitiveServicesAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IpRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce088-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ce088-105">DESCRIPTION</span></span>
<span data-ttu-id="ce088-106">Polecenie cmdlet **Update-AzCognitiveServicesAccountNetworkRuleSet** aktualizuje właściwość NetworkRule konta usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="ce088-106">The **Update-AzCognitiveServicesAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Cognitive Services account</span></span>

## <span data-ttu-id="ce088-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce088-107">EXAMPLES</span></span>

### <span data-ttu-id="ce088-108">Przykład 1: aktualizowanie wszystkich właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON</span><span class="sxs-lookup"><span data-stu-id="ce088-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -DefaultAction Allow -IpRule (@{IpAddressOrRange="200.0.0.0/24"},@{IpAddressOrRange="28.2.0.0/16"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2"})
```

<span data-ttu-id="ce088-109">To polecenie aktualizuje wszystkie właściwości NetworkRule, reguły wprowadzania za pomocą notacji JSON.</span><span class="sxs-lookup"><span data-stu-id="ce088-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="ce088-110">Przykład 2: aktualizowanie właściwości Bypass dla NetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce088-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount"
```

<span data-ttu-id="ce088-111">To polecenie umożliwia zaktualizowanie właściwości Bypass NetworkRule (inne właściwości nie zostaną zmienione).</span><span class="sxs-lookup"><span data-stu-id="ce088-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="ce088-112">Przykład 3: porządkowanie reguł NetworkRule z usług poznawczych</span><span class="sxs-lookup"><span data-stu-id="ce088-112">Example 3: Clean up rules of NetworkRule of a Cognitive Services account</span></span>
```
PS C:\> Update-AzCognitiveServicesAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "myaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="ce088-113">To polecenie czyści reguły NetworkRuleego konta usług poznawczych (inne właściwości nie zmieniają się).</span><span class="sxs-lookup"><span data-stu-id="ce088-113">This command clean up rules of NetworkRule of a Cognitive Services account (other properties not change).</span></span>

## <span data-ttu-id="ce088-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce088-114">PARAMETERS</span></span>

### <span data-ttu-id="ce088-115">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="ce088-115">-DefaultAction</span></span>
<span data-ttu-id="ce088-116">Konto usług poznawczych NetworkRule DefaultAction.</span><span class="sxs-lookup"><span data-stu-id="ce088-116">Cognitive Services Account NetworkRule DefaultAction.</span></span> <span data-ttu-id="ce088-117">Wartość domyślna `Deny` .</span><span class="sxs-lookup"><span data-stu-id="ce088-117">Default value `Deny`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce088-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce088-118">-DefaultProfile</span></span>
<span data-ttu-id="ce088-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ce088-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce088-120">-IpRule</span><span class="sxs-lookup"><span data-stu-id="ce088-120">-IpRule</span></span>
<span data-ttu-id="ce088-121">Konto usług poznawczych NetworkRule IpRules.</span><span class="sxs-lookup"><span data-stu-id="ce088-121">Cognitive Services Account NetworkRule IpRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce088-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce088-122">-Name</span></span>
<span data-ttu-id="ce088-123">Nazwa konta usług poznawczych.</span><span class="sxs-lookup"><span data-stu-id="ce088-123">Cognitive Services Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce088-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce088-124">-ResourceGroupName</span></span>
<span data-ttu-id="ce088-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ce088-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="ce088-126">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="ce088-126">-VirtualNetworkRule</span></span>
<span data-ttu-id="ce088-127">Konto usług poznawczych NetworkRule VirtualNetworkRules.</span><span class="sxs-lookup"><span data-stu-id="ce088-127">Cognitive Services Account NetworkRule VirtualNetworkRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce088-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce088-128">-Confirm</span></span>
<span data-ttu-id="ce088-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce088-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce088-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce088-130">-WhatIf</span></span>
<span data-ttu-id="ce088-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce088-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce088-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce088-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce088-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce088-133">CommonParameters</span></span>
<span data-ttu-id="ce088-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce088-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce088-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce088-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce088-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce088-136">INPUTS</span></span>

### <span data-ttu-id="ce088-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ce088-137">System.String</span></span>

### <span data-ttu-id="ce088-138">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="ce088-138">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSIpRule[]</span></span>

### <span data-ttu-id="ce088-139">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="ce088-139">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="ce088-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce088-140">OUTPUTS</span></span>

### <span data-ttu-id="ce088-141">Microsoft. Azure. Commands. Management. CognitiveServices. models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ce088-141">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="ce088-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce088-142">NOTES</span></span>

## <span data-ttu-id="ce088-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce088-143">RELATED LINKS</span></span>
