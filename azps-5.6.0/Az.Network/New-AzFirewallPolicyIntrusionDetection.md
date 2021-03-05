---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetection.md
ms.openlocfilehash: 3587917e1a4216445e59b182ce6307c7a94684bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996493"
---
# <span data-ttu-id="445bb-101">New-AzFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="445bb-101">New-AzFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="445bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="445bb-102">SYNOPSIS</span></span>
<span data-ttu-id="445bb-103">Tworzy nowe wykrywanie intruzów zasad zapory platformy Azure w celu skojarzenia z zasadami zapory</span><span class="sxs-lookup"><span data-stu-id="445bb-103">Creates a new Azure Firewall Policy Intrusion Detection to associate with Firewall Policy</span></span>

## <span data-ttu-id="445bb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="445bb-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetection -Mode <String>
 [-SignatureOverride <PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]>]
 [-BypassTraffic <PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="445bb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="445bb-105">DESCRIPTION</span></span>
<span data-ttu-id="445bb-106">Polecenie **cmdlet New-AzFirewallPolicyIntrusionDetection** tworzy obiekt wykrywania intruzów zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="445bb-106">The **New-AzFirewallPolicyIntrusionDetection** cmdlet creates an Azure Firewall Policy Intrusion Detection Object.</span></span>

## <span data-ttu-id="445bb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="445bb-107">EXAMPLES</span></span>

### <span data-ttu-id="445bb-108">Przykład 1: 1.</span><span class="sxs-lookup"><span data-stu-id="445bb-108">Example 1: 1.</span></span> <span data-ttu-id="445bb-109">Tworzenie wykrywania intruzów w trybie</span><span class="sxs-lookup"><span data-stu-id="445bb-109">Create intrusion detection with mode</span></span>
```powershell
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert"
```

<span data-ttu-id="445bb-110">W tym przykładzie jest wykrywane intruzowanie przy użyciu trybu alertu (wykrywania).</span><span class="sxs-lookup"><span data-stu-id="445bb-110">This example creates intrusion detection with Alert (detection) mode</span></span>

### <span data-ttu-id="445bb-111">Przykład 2: 2.</span><span class="sxs-lookup"><span data-stu-id="445bb-111">Example 2: 2.</span></span> <span data-ttu-id="445bb-112">Tworzenie wykrywania włamań za pomocą zastępować podpisu</span><span class="sxs-lookup"><span data-stu-id="445bb-112">Create intrusion detection with signature overrides</span></span>
```powershell
PS C:\> $signatureOverride = New-AzFirewallPolicyIntrusionDetectionSignatureOverride -Id "123456798" -Mode "Deny"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Alert" -SignatureOverride $signatureOverride
```

<span data-ttu-id="445bb-113">W tym przykładzie jest konstruowanie wykrywania intruzów z określonym zastępowaniem podpisu</span><span class="sxs-lookup"><span data-stu-id="445bb-113">This example creates intrusion detection with specific signature override</span></span>

### <span data-ttu-id="445bb-114">Przykład 3: 3.</span><span class="sxs-lookup"><span data-stu-id="445bb-114">Example 3: 3.</span></span> <span data-ttu-id="445bb-115">Tworzenie zasad zapory z wykrywaniem intruzów skonfigurowanym z ustawieniem ruchu obejścia</span><span class="sxs-lookup"><span data-stu-id="445bb-115">Create firewall policy with intrusion detection configured with bypass traffic setting</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "10.0.0.0"
PS C:\> $intrusionDetection = New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
PS C:\> New-AzFirewallPolicy -Name fp1 -Location "westus2" -ResourceGroup TestRg -SkuTier "Premium" -IntrusionDetection $intrusionDetection
```

<span data-ttu-id="445bb-116">W tym przykładzie jest wykrywane wykrycie łamania z ustawieniem ruchu obejścia</span><span class="sxs-lookup"><span data-stu-id="445bb-116">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="445bb-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="445bb-117">PARAMETERS</span></span>

### <span data-ttu-id="445bb-118">-BypassTraffic</span><span class="sxs-lookup"><span data-stu-id="445bb-118">-BypassTraffic</span></span>
<span data-ttu-id="445bb-119">Lista reguł, które ruch ma pomijać.</span><span class="sxs-lookup"><span data-stu-id="445bb-119">List of rules for traffic to bypass.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445bb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="445bb-120">-DefaultProfile</span></span>
<span data-ttu-id="445bb-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="445bb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445bb-122">— tryb</span><span class="sxs-lookup"><span data-stu-id="445bb-122">-Mode</span></span>
<span data-ttu-id="445bb-123">Ogólny stan wykrywania włamań.</span><span class="sxs-lookup"><span data-stu-id="445bb-123">Intrusion Detection general state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Off, Alert, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445bb-124">-SignatureOverride</span><span class="sxs-lookup"><span data-stu-id="445bb-124">-SignatureOverride</span></span>
<span data-ttu-id="445bb-125">Lista określonych stanów podpisów.</span><span class="sxs-lookup"><span data-stu-id="445bb-125">List of specific signatures states.</span></span>

```yaml
Type: PSAzureFirewallPolicyIntrusionDetectionSignatureOverride[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445bb-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="445bb-126">-Confirm</span></span>
<span data-ttu-id="445bb-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="445bb-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445bb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="445bb-128">-WhatIf</span></span>
<span data-ttu-id="445bb-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="445bb-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="445bb-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="445bb-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="445bb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="445bb-131">CommonParameters</span></span>
<span data-ttu-id="445bb-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="445bb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="445bb-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="445bb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="445bb-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="445bb-134">INPUTS</span></span>

### <span data-ttu-id="445bb-135">Brak</span><span class="sxs-lookup"><span data-stu-id="445bb-135">None</span></span>

## <span data-ttu-id="445bb-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="445bb-136">OUTPUTS</span></span>

### <span data-ttu-id="445bb-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span><span class="sxs-lookup"><span data-stu-id="445bb-137">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetection</span></span>

## <span data-ttu-id="445bb-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="445bb-138">NOTES</span></span>

## <span data-ttu-id="445bb-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="445bb-139">RELATED LINKS</span></span>
