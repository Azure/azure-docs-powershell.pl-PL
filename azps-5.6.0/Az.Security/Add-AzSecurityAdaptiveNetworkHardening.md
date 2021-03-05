---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: e0e634a4947953f65c3fd68c9cc3e40dfca17fd2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972529"
---
# <span data-ttu-id="67ed4-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="67ed4-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="67ed4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ed4-102">SYNOPSIS</span></span>
<span data-ttu-id="67ed4-103">Wymusza podane reguły dla NSG wymienionych w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="67ed4-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="67ed4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="67ed4-104">SYNTAX</span></span>

### <span data-ttu-id="67ed4-105">ResourceGroupLevelResource (Default)</span><span class="sxs-lookup"><span data-stu-id="67ed4-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67ed4-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="67ed4-106">DESCRIPTION</span></span>
<span data-ttu-id="67ed4-107">Adaptacyjne połączenia sieciowe są automatycznie obliczane przez Azure Security Center. Za pomocą tego polecenia cmdlet wymuszane są podane reguły dla NSG wymienionych w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="67ed4-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="67ed4-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="67ed4-108">EXAMPLES</span></span>

### <span data-ttu-id="67ed4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="67ed4-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="67ed4-110">Wymusza podane reguły dla NSG wymienionych w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="67ed4-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="67ed4-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ed4-111">PARAMETERS</span></span>

### <span data-ttu-id="67ed4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ed4-112">-DefaultProfile</span></span>
<span data-ttu-id="67ed4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="67ed4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ed4-114">-AdaptiveNetworkSourceEningResourceName</span><span class="sxs-lookup"><span data-stu-id="67ed4-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="67ed4-115">Nazwa zasobu Adaptacyjne nasyłanie sieci.</span><span class="sxs-lookup"><span data-stu-id="67ed4-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ed4-116">-ResourceGroupName</span></span>
<span data-ttu-id="67ed4-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="67ed4-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="67ed4-118">-ResourceName</span></span>
<span data-ttu-id="67ed4-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="67ed4-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="67ed4-120">-ResourceNamespace</span></span>
<span data-ttu-id="67ed4-121">Przestrzeń nazw zasobu.</span><span class="sxs-lookup"><span data-stu-id="67ed4-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="67ed4-122">-ResourceType</span></span>
<span data-ttu-id="67ed4-123">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="67ed4-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-124">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="67ed4-124">-SubscriptionId</span></span>
<span data-ttu-id="67ed4-125">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="67ed4-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-126">— Reguły</span><span class="sxs-lookup"><span data-stu-id="67ed4-126">-Rules</span></span>
<span data-ttu-id="67ed4-127">Reguły do wymuszenia.</span><span class="sxs-lookup"><span data-stu-id="67ed4-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-128">- NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="67ed4-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="67ed4-129">Identyfikatory zasobów platformy Azure efektywnych grup zabezpieczeń sieci, które zostaną zaktualizowane o utworzone reguły zabezpieczeń z adaptacyjnych reguł tworzenia treści sieci.</span><span class="sxs-lookup"><span data-stu-id="67ed4-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ed4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67ed4-130">-PassThru</span></span>
<span data-ttu-id="67ed4-131">Zwraca wartość wskazującą sukces lub porażkę.</span><span class="sxs-lookup"><span data-stu-id="67ed4-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="67ed4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ed4-132">CommonParameters</span></span>
<span data-ttu-id="67ed4-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67ed4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ed4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ed4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ed4-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67ed4-135">INPUTS</span></span>

### <span data-ttu-id="67ed4-136">System.String</span><span class="sxs-lookup"><span data-stu-id="67ed4-136">System.String</span></span>

### <span data-ttu-id="67ed4-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetwork Jakenings.PSSecurityAdaptiveNetworkDeningsRule</span><span class="sxs-lookup"><span data-stu-id="67ed4-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="67ed4-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67ed4-138">OUTPUTS</span></span>

### <span data-ttu-id="67ed4-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67ed4-139">System.Boolean</span></span>

## <span data-ttu-id="67ed4-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="67ed4-140">NOTES</span></span>

## <span data-ttu-id="67ed4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67ed4-141">RELATED LINKS</span></span>