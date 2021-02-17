---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: b0010134ac6b819afc3e8621b11d5530a08008a8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193307"
---
# <span data-ttu-id="b520a-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b520a-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="b520a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b520a-102">SYNOPSIS</span></span>
<span data-ttu-id="b520a-103">Rozpoczyna operację przechwytywania pakietów w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="b520a-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="b520a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b520a-104">SYNTAX</span></span>

### <span data-ttu-id="b520a-105">ByName (Default)</span><span class="sxs-lookup"><span data-stu-id="b520a-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b520a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b520a-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b520a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b520a-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b520a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b520a-108">DESCRIPTION</span></span>
<span data-ttu-id="b520a-109">Rozpoczyna operację przechwytywania pakietów w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="b520a-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="b520a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b520a-110">EXAMPLES</span></span>

### <span data-ttu-id="b520a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b520a-111">Example 1</span></span>
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
### <span data-ttu-id="b520a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b520a-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
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
### <span data-ttu-id="b520a-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b520a-113">Example 3</span></span>
<span data-ttu-id="b520a-114">Przykład przechwytywania pakietów dla wszystkich pakietów wewnętrznych i zewnętrznych</span><span class="sxs-lookup"><span data-stu-id="b520a-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
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

## <span data-ttu-id="b520a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b520a-115">PARAMETERS</span></span>

### <span data-ttu-id="b520a-116">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b520a-116">-AsJob</span></span>
<span data-ttu-id="b520a-117">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b520a-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b520a-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b520a-118">-Confirm</span></span>
<span data-ttu-id="b520a-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b520a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b520a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b520a-120">-DefaultProfile</span></span>
<span data-ttu-id="b520a-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b520a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b520a-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="b520a-122">-FilterData</span></span>
<span data-ttu-id="b520a-123">Opcje filtrowania służące do uruchamiania przechwytywania pakietów w wirtualnej bramie sieciowej.</span><span class="sxs-lookup"><span data-stu-id="b520a-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="b520a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b520a-124">-InputObject</span></span>
<span data-ttu-id="b520a-125">Obiekt bramy sieci wirtualnej, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="b520a-125">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="b520a-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b520a-126">-Name</span></span>
<span data-ttu-id="b520a-127">Nazwa wirtualnej bramy sieciowej, na której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="b520a-127">The virtual network gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="b520a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b520a-128">-ResourceGroupName</span></span>
<span data-ttu-id="b520a-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b520a-129">The resource group name.</span></span>

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

### <span data-ttu-id="b520a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b520a-130">-ResourceId</span></span>
<span data-ttu-id="b520a-131">Identyfikator zasobu Azure w witrynie VirtualNetworkGateway, w której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="b520a-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="b520a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b520a-132">-WhatIf</span></span>
<span data-ttu-id="b520a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b520a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b520a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b520a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b520a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b520a-135">CommonParameters</span></span>
<span data-ttu-id="b520a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b520a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b520a-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b520a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b520a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b520a-138">INPUTS</span></span>

### <span data-ttu-id="b520a-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="b520a-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="b520a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b520a-140">System.String</span></span>

## <span data-ttu-id="b520a-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b520a-141">OUTPUTS</span></span>

### <span data-ttu-id="b520a-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="b520a-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="b520a-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b520a-143">NOTES</span></span>

## <span data-ttu-id="b520a-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b520a-144">RELATED LINKS</span></span>
[<span data-ttu-id="b520a-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b520a-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)