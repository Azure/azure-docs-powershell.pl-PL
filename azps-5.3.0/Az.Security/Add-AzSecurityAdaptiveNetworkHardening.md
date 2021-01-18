---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98503093"
---
# <span data-ttu-id="575c4-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="575c4-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="575c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="575c4-102">SYNOPSIS</span></span>
<span data-ttu-id="575c4-103">Wymusza udzielanie określonych reguł na NSG (s) wymienionych w żądaniu</span><span class="sxs-lookup"><span data-stu-id="575c4-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="575c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="575c4-104">SYNTAX</span></span>

### <span data-ttu-id="575c4-105">ResourceGroupLevelResource (domyślny)</span><span class="sxs-lookup"><span data-stu-id="575c4-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="575c4-106">Opis</span><span class="sxs-lookup"><span data-stu-id="575c4-106">DESCRIPTION</span></span>
<span data-ttu-id="575c4-107">Przydziały w sieci adaptacyjnej są automatycznie obliczane przez usługę Azure Security Center, za pomocą tego polecenia cmdlet można wymuszać podane reguły na NSG (s) wymienionym w żądaniu.</span><span class="sxs-lookup"><span data-stu-id="575c4-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="575c4-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="575c4-108">EXAMPLES</span></span>

### <span data-ttu-id="575c4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="575c4-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="575c4-110">Wymusza udzielanie określonych reguł na NSG (s) wymienionych w żądaniu</span><span class="sxs-lookup"><span data-stu-id="575c4-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="575c4-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="575c4-111">PARAMETERS</span></span>

### <span data-ttu-id="575c4-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="575c4-112">-DefaultProfile</span></span>
<span data-ttu-id="575c4-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="575c4-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="575c4-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="575c4-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="575c4-115">Nazwa zasobu adaptacyjnego dotyczącego zabezpieczania sieci.</span><span class="sxs-lookup"><span data-stu-id="575c4-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="575c4-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="575c4-116">-ResourceGroupName</span></span>
<span data-ttu-id="575c4-117">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="575c4-117">Resource group name.</span></span>

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

### <span data-ttu-id="575c4-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="575c4-118">-ResourceName</span></span>
<span data-ttu-id="575c4-119">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="575c4-119">Resource name.</span></span>

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

### <span data-ttu-id="575c4-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="575c4-120">-ResourceNamespace</span></span>
<span data-ttu-id="575c4-121">Obszar nazw zasobu.</span><span class="sxs-lookup"><span data-stu-id="575c4-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="575c4-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="575c4-122">-ResourceType</span></span>
<span data-ttu-id="575c4-123">Typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="575c4-123">The type of the resource.</span></span>

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

### <span data-ttu-id="575c4-124">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="575c4-124">-SubscriptionId</span></span>
<span data-ttu-id="575c4-125">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="575c4-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="575c4-126">— Reguły</span><span class="sxs-lookup"><span data-stu-id="575c4-126">-Rules</span></span>
<span data-ttu-id="575c4-127">Reguły, które należy wymusić.</span><span class="sxs-lookup"><span data-stu-id="575c4-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="575c4-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="575c4-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="575c4-129">Identyfikatory zasobów platformy Azure dla aktywnych grup zabezpieczeń sieci, które zostaną zaktualizowane przy użyciu utworzonych reguł zabezpieczeń na podstawie reguł zabezpieczania sieci adaptacyjnej.</span><span class="sxs-lookup"><span data-stu-id="575c4-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="575c4-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="575c4-130">-PassThru</span></span>
<span data-ttu-id="575c4-131">Zwracanie wartości oznaczającej sukces lub niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="575c4-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="575c4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="575c4-132">CommonParameters</span></span>
<span data-ttu-id="575c4-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="575c4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="575c4-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="575c4-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="575c4-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="575c4-135">INPUTS</span></span>

### <span data-ttu-id="575c4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="575c4-136">System.String</span></span>

### <span data-ttu-id="575c4-137">Microsoft. Azure. Commands. SecurityCenter. modele. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="575c4-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="575c4-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="575c4-138">OUTPUTS</span></span>

### <span data-ttu-id="575c4-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="575c4-139">System.Boolean</span></span>

## <span data-ttu-id="575c4-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="575c4-140">NOTES</span></span>

## <span data-ttu-id="575c4-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="575c4-141">RELATED LINKS</span></span>