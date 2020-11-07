---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 3a1d9c2f415d56263529fcd66aa1ee9535823bbf
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872092"
---
# <span data-ttu-id="e2808-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2808-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="e2808-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2808-102">SYNOPSIS</span></span>
<span data-ttu-id="e2808-103">Rozpoczyna operację przechwytywania pakietów w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2808-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="e2808-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2808-104">SYNTAX</span></span>

### <span data-ttu-id="e2808-105">ByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e2808-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2808-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e2808-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2808-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e2808-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2808-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e2808-108">DESCRIPTION</span></span>
<span data-ttu-id="e2808-109">Rozpoczyna operację przechwytywania pakietów w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2808-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="e2808-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2808-110">EXAMPLES</span></span>

### <span data-ttu-id="e2808-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e2808-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="e2808-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e2808-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="e2808-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2808-113">PARAMETERS</span></span>

### <span data-ttu-id="e2808-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e2808-114">-AsJob</span></span>
<span data-ttu-id="e2808-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e2808-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e2808-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2808-116">-Confirm</span></span>
<span data-ttu-id="e2808-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2808-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2808-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2808-118">-DefaultProfile</span></span>
<span data-ttu-id="e2808-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2808-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2808-120">-FilterData</span><span class="sxs-lookup"><span data-stu-id="e2808-120">-FilterData</span></span>
<span data-ttu-id="e2808-121">Opcje filtrowania dotyczące rozpoczynania przechwytywania pakietów w połączeniu bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2808-121">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="e2808-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e2808-122">-InputObject</span></span>
<span data-ttu-id="e2808-123">Obiekt połączenie bramy sieci wirtualnej, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="e2808-123">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2808-124">-Name</span></span>
<span data-ttu-id="e2808-125">Nazwa połączenia bramy sieci wirtualnej, w którym można uruchomić przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="e2808-125">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2808-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2808-126">-ResourceGroupName</span></span>
<span data-ttu-id="e2808-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e2808-127">The resource group name.</span></span>

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

### <span data-ttu-id="e2808-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2808-128">-ResourceId</span></span>
<span data-ttu-id="e2808-129">Identyfikator zasobu platformy Azure VirtualNetworkGatewayConnection, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="e2808-129">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="e2808-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2808-130">-WhatIf</span></span>
<span data-ttu-id="e2808-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2808-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2808-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e2808-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2808-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2808-133">CommonParameters</span></span>
<span data-ttu-id="e2808-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2808-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2808-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2808-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2808-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2808-136">INPUTS</span></span>

### <span data-ttu-id="e2808-137">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="e2808-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="e2808-138">System. String</span><span class="sxs-lookup"><span data-stu-id="e2808-138">System.String</span></span>

## <span data-ttu-id="e2808-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2808-139">OUTPUTS</span></span>

### <span data-ttu-id="e2808-140">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="e2808-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="e2808-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2808-141">NOTES</span></span>

## <span data-ttu-id="e2808-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2808-142">RELATED LINKS</span></span>
[<span data-ttu-id="e2808-143">Zatrzymaj — AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="e2808-143">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)