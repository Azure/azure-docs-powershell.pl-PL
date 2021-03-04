---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azfirewallpolicyintrusiondetectionbypasstraffic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzFirewallPolicyIntrusionDetectionBypassTraffic.md
ms.openlocfilehash: dd15a93fc2df022a0b016f9dae4845da13240534
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981697"
---
# <span data-ttu-id="a66d5-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span><span class="sxs-lookup"><span data-stu-id="a66d5-101">New-AzFirewallPolicyIntrusionDetectionBypassTraffic</span></span>

## <span data-ttu-id="a66d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a66d5-102">SYNOPSIS</span></span>
<span data-ttu-id="a66d5-103">Tworzy nowe ustawienie ruchu obejścia zasad zapory platformy Azure</span><span class="sxs-lookup"><span data-stu-id="a66d5-103">Creates a new Azure Firewall Policy Intrusion Detection Bypass Traffic Setting</span></span>

## <span data-ttu-id="a66d5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a66d5-104">SYNTAX</span></span>

```
New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name <String> [-Description <String>] -Protocol <String>
 [-SourceAddress <String[]>] [-DestinationAddress <String[]>] [-SourceIpGroup <String[]>]
 [-DestinationIpGroup <String[]>] -DestinationPort <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a66d5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a66d5-105">DESCRIPTION</span></span>
<span data-ttu-id="a66d5-106">Polecenie **cmdlet New-AzFirewallPolicyIntrusionDetectionBypassTraffic** tworzy obiekt ruchu obejścia ruchu obejścia zasad zapory platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a66d5-106">The **New-AzFirewallPolicyIntrusionDetectionBypassTraffic** cmdlet creates an Azure Firewall Policy Intrusion Detection Bypass Traffic Object.</span></span>

## <span data-ttu-id="a66d5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a66d5-107">EXAMPLES</span></span>

### <span data-ttu-id="a66d5-108">Przykład 1: 1.</span><span class="sxs-lookup"><span data-stu-id="a66d5-108">Example 1: 1.</span></span> <span data-ttu-id="a66d5-109">Tworzenie ruchu obejścia z określonym adresem portu i źródła</span><span class="sxs-lookup"><span data-stu-id="a66d5-109">Create bypass traffic with specific port and source address</span></span>
```powershell
PS C:\> $bypass = New-AzFirewallPolicyIntrusionDetectionBypassTraffic -Name "bypass-setting" -Protocol "TCP" -DestinationPort "80" -SourceAddress "10.0.0.0" -DestinationAddress "*"
PS C:\> New-AzFirewallPolicyIntrusionDetection -Mode "Deny" -BypassTraffic $bypass
```

<span data-ttu-id="a66d5-110">W tym przykładzie jest wykrywane wykrycie łamania z ustawieniem ruchu obejścia</span><span class="sxs-lookup"><span data-stu-id="a66d5-110">This example creates intrusion detection with bypass traffic setting</span></span>

## <span data-ttu-id="a66d5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a66d5-111">PARAMETERS</span></span>

### <span data-ttu-id="a66d5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66d5-112">-DefaultProfile</span></span>
<span data-ttu-id="a66d5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a66d5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a66d5-114">— Opis</span><span class="sxs-lookup"><span data-stu-id="a66d5-114">-Description</span></span>
<span data-ttu-id="a66d5-115">Pomijanie opisu ustawień.</span><span class="sxs-lookup"><span data-stu-id="a66d5-115">Bypass setting description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-116">-DestinationAddress</span><span class="sxs-lookup"><span data-stu-id="a66d5-116">-DestinationAddress</span></span>
<span data-ttu-id="a66d5-117">Lista docelowych adresów IP lub zakresów.</span><span class="sxs-lookup"><span data-stu-id="a66d5-117">List of destination IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-118">-DestinationIpGroup</span><span class="sxs-lookup"><span data-stu-id="a66d5-118">-DestinationIpGroup</span></span>
<span data-ttu-id="a66d5-119">Lista docelowych grup IpGroup.</span><span class="sxs-lookup"><span data-stu-id="a66d5-119">List of destination IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-120">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="a66d5-120">-DestinationPort</span></span>
<span data-ttu-id="a66d5-121">Lista portów docelowych lub zakresów.</span><span class="sxs-lookup"><span data-stu-id="a66d5-121">List of destination ports or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a66d5-122">-Name</span></span>
<span data-ttu-id="a66d5-123">Pomijanie nazwy ustawienia.</span><span class="sxs-lookup"><span data-stu-id="a66d5-123">Bypass setting name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-124">— Protokół</span><span class="sxs-lookup"><span data-stu-id="a66d5-124">-Protocol</span></span>
<span data-ttu-id="a66d5-125">Pomijanie protokołu ustawiania.</span><span class="sxs-lookup"><span data-stu-id="a66d5-125">Bypass setting protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: TCP, UDP, ICMP, ANY

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-126">-SourceAddress</span><span class="sxs-lookup"><span data-stu-id="a66d5-126">-SourceAddress</span></span>
<span data-ttu-id="a66d5-127">Lista źródłowych adresów IP lub zakresów.</span><span class="sxs-lookup"><span data-stu-id="a66d5-127">List of source IP addresses or ranges.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-128">-SourceIpGroup</span><span class="sxs-lookup"><span data-stu-id="a66d5-128">-SourceIpGroup</span></span>
<span data-ttu-id="a66d5-129">Lista źródłowych grup IpGroup.</span><span class="sxs-lookup"><span data-stu-id="a66d5-129">List of source IpGroups.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66d5-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a66d5-130">-Confirm</span></span>
<span data-ttu-id="a66d5-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a66d5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a66d5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a66d5-132">-WhatIf</span></span>
<span data-ttu-id="a66d5-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a66d5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a66d5-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a66d5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a66d5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66d5-135">CommonParameters</span></span>
<span data-ttu-id="a66d5-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66d5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66d5-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a66d5-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66d5-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a66d5-138">INPUTS</span></span>

### <span data-ttu-id="a66d5-139">Brak</span><span class="sxs-lookup"><span data-stu-id="a66d5-139">None</span></span>

## <span data-ttu-id="a66d5-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a66d5-140">OUTPUTS</span></span>

### <span data-ttu-id="a66d5-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span><span class="sxs-lookup"><span data-stu-id="a66d5-141">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicyIntrusionDetectionBypassTrafficSetting</span></span>

## <span data-ttu-id="a66d5-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a66d5-142">NOTES</span></span>

## <span data-ttu-id="a66d5-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a66d5-143">RELATED LINKS</span></span>
