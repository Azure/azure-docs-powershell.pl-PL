---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 1f0b539e2f5a6e2c387738558fb6db8cbe647457
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872091"
---
# <span data-ttu-id="464a9-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="464a9-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="464a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="464a9-102">SYNOPSIS</span></span>
<span data-ttu-id="464a9-103">Rozpoczyna operację przechwytywania pakietów na bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="464a9-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="464a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="464a9-104">SYNTAX</span></span>

### <span data-ttu-id="464a9-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="464a9-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464a9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="464a9-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="464a9-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="464a9-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464a9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="464a9-108">DESCRIPTION</span></span>
<span data-ttu-id="464a9-109">Rozpoczyna operację przechwytywania pakietów na bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="464a9-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="464a9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="464a9-110">EXAMPLES</span></span>

### <span data-ttu-id="464a9-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="464a9-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="464a9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="464a9-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="464a9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="464a9-113">PARAMETERS</span></span>

### <span data-ttu-id="464a9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="464a9-114">-AsJob</span></span>
<span data-ttu-id="464a9-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="464a9-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464a9-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="464a9-116">-Confirm</span></span>
<span data-ttu-id="464a9-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464a9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464a9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464a9-118">-DefaultProfile</span></span>
<span data-ttu-id="464a9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="464a9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464a9-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="464a9-120">-FilterData</span></span>
<span data-ttu-id="464a9-121">Opcje filtrowania dotyczące uruchamiania funkcji przechwytywania pakietów w bramie sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="464a9-121">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="464a9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="464a9-122">-InputObject</span></span>
<span data-ttu-id="464a9-123">Obiekt bramy sieci wirtualnej, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="464a9-123">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="464a9-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="464a9-124">-Name</span></span>
<span data-ttu-id="464a9-125">Nazwa bramy sieci wirtualnej, w której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="464a9-125">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="464a9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="464a9-127">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="464a9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="464a9-128">-ResourceId</span></span>
<span data-ttu-id="464a9-129">Identyfikator zasobu platformy Azure VirtualNetworkGateway, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="464a9-129">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="464a9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464a9-130">-WhatIf</span></span>
<span data-ttu-id="464a9-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464a9-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464a9-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="464a9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464a9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464a9-133">CommonParameters</span></span>
<span data-ttu-id="464a9-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="464a9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464a9-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="464a9-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464a9-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="464a9-136">INPUTS</span></span>

### <span data-ttu-id="464a9-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="464a9-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="464a9-138">System. String</span><span class="sxs-lookup"><span data-stu-id="464a9-138">System.String</span></span>

## <span data-ttu-id="464a9-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="464a9-139">OUTPUTS</span></span>

### <span data-ttu-id="464a9-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="464a9-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="464a9-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="464a9-141">NOTES</span></span>

## <span data-ttu-id="464a9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="464a9-142">RELATED LINKS</span></span>
[<span data-ttu-id="464a9-143">Zatrzymaj — AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="464a9-143">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)