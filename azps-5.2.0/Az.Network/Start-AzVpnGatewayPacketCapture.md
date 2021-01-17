---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365038"
---
# <span data-ttu-id="aa0db-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aa0db-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="aa0db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aa0db-102">SYNOPSIS</span></span>
<span data-ttu-id="aa0db-103">Rozpoczyna operację przechwytywania pakietów na bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="aa0db-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="aa0db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aa0db-104">SYNTAX</span></span>

### <span data-ttu-id="aa0db-105">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="aa0db-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0db-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="aa0db-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa0db-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0db-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa0db-108">Opis</span><span class="sxs-lookup"><span data-stu-id="aa0db-108">DESCRIPTION</span></span>
<span data-ttu-id="aa0db-109">Rozpoczyna operację przechwytywania pakietów na bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="aa0db-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="aa0db-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aa0db-110">EXAMPLES</span></span>

### <span data-ttu-id="aa0db-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa0db-111">Example 1</span></span>
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

### <span data-ttu-id="aa0db-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="aa0db-112">Example 2</span></span>
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

## <span data-ttu-id="aa0db-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aa0db-113">PARAMETERS</span></span>

### <span data-ttu-id="aa0db-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa0db-114">-AsJob</span></span>
<span data-ttu-id="aa0db-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="aa0db-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa0db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa0db-116">-DefaultProfile</span></span>
<span data-ttu-id="aa0db-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa0db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa0db-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="aa0db-118">-FilterData</span></span>
<span data-ttu-id="aa0db-119">Opcje filtrowania dotyczące uruchamiania funkcji przechwytywania pakietów w bramie VPN.</span><span class="sxs-lookup"><span data-stu-id="aa0db-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="aa0db-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa0db-120">-InputObject</span></span>
<span data-ttu-id="aa0db-121">Obiekt bramy sieci VPN, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="aa0db-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="aa0db-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aa0db-122">-Name</span></span>
<span data-ttu-id="aa0db-123">Nazwa bramy sieci VPN, w której ma zostać rozpoczęte przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="aa0db-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="aa0db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa0db-124">-ResourceGroupName</span></span>
<span data-ttu-id="aa0db-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="aa0db-125">The resource group name.</span></span>

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

### <span data-ttu-id="aa0db-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa0db-126">-ResourceId</span></span>
<span data-ttu-id="aa0db-127">Identyfikator zasobu platformy Azure VpnGateway, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="aa0db-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="aa0db-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa0db-128">-Confirm</span></span>
<span data-ttu-id="aa0db-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0db-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa0db-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa0db-130">-WhatIf</span></span>
<span data-ttu-id="aa0db-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa0db-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa0db-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="aa0db-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa0db-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa0db-133">CommonParameters</span></span>
<span data-ttu-id="aa0db-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa0db-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa0db-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa0db-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa0db-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa0db-136">INPUTS</span></span>

### <span data-ttu-id="aa0db-137">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="aa0db-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="aa0db-138">System. String</span><span class="sxs-lookup"><span data-stu-id="aa0db-138">System.String</span></span>

## <span data-ttu-id="aa0db-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aa0db-139">OUTPUTS</span></span>

### <span data-ttu-id="aa0db-140">Microsoft. Azure. Commands. Network. models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="aa0db-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="aa0db-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aa0db-141">NOTES</span></span>

## <span data-ttu-id="aa0db-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa0db-142">RELATED LINKS</span></span>

[<span data-ttu-id="aa0db-143">Zatrzymaj — AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="aa0db-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)