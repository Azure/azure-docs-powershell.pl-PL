---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: ec7307b6bd6d01b7b3f6e2656026eea78e0d3704
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951873"
---
# <span data-ttu-id="50c48-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50c48-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="50c48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50c48-102">SYNOPSIS</span></span>
<span data-ttu-id="50c48-103">Rozpoczyna operację przechwytywania pakietów w bramie vpn.</span><span class="sxs-lookup"><span data-stu-id="50c48-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="50c48-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50c48-104">SYNTAX</span></span>

### <span data-ttu-id="50c48-105">ByVpnGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="50c48-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c48-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="50c48-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50c48-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="50c48-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50c48-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="50c48-108">DESCRIPTION</span></span>
<span data-ttu-id="50c48-109">Rozpoczyna operację przechwytywania pakietów w bramie vpn.</span><span class="sxs-lookup"><span data-stu-id="50c48-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="50c48-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50c48-110">EXAMPLES</span></span>

### <span data-ttu-id="50c48-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50c48-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="50c48-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="50c48-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="50c48-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50c48-113">PARAMETERS</span></span>

### <span data-ttu-id="50c48-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="50c48-114">-AsJob</span></span>
<span data-ttu-id="50c48-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="50c48-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50c48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50c48-116">-DefaultProfile</span></span>
<span data-ttu-id="50c48-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50c48-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50c48-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="50c48-118">-FilterData</span></span>
<span data-ttu-id="50c48-119">Opcje filtrowania służące do uruchamiania przechwytywania pakietów w bramie vpn.</span><span class="sxs-lookup"><span data-stu-id="50c48-119">Filter options for start packet capture on Vpn Gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c48-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50c48-120">-InputObject</span></span>
<span data-ttu-id="50c48-121">Obiekt Vpn Gateway, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="50c48-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50c48-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50c48-122">-Name</span></span>
<span data-ttu-id="50c48-123">Nazwa bramy vpn, na której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="50c48-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50c48-124">-ResourceGroupName</span></span>
<span data-ttu-id="50c48-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50c48-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50c48-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50c48-126">-ResourceId</span></span>
<span data-ttu-id="50c48-127">Identyfikator zasobu Azure w usłudze VpnGateway, w którym ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="50c48-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50c48-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="50c48-128">-Confirm</span></span>
<span data-ttu-id="50c48-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="50c48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50c48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50c48-130">-WhatIf</span></span>
<span data-ttu-id="50c48-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50c48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50c48-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="50c48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50c48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50c48-133">CommonParameters</span></span>
<span data-ttu-id="50c48-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50c48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50c48-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50c48-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50c48-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50c48-136">INPUTS</span></span>

### <span data-ttu-id="50c48-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="50c48-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="50c48-138">System.String</span><span class="sxs-lookup"><span data-stu-id="50c48-138">System.String</span></span>

## <span data-ttu-id="50c48-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50c48-139">OUTPUTS</span></span>

### <span data-ttu-id="50c48-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="50c48-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="50c48-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50c48-141">NOTES</span></span>

## <span data-ttu-id="50c48-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50c48-142">RELATED LINKS</span></span>

[<span data-ttu-id="50c48-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="50c48-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)