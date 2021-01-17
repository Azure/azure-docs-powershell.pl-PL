---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365043"
---
# <span data-ttu-id="bdfad-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdfad-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="bdfad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdfad-102">SYNOPSIS</span></span>
<span data-ttu-id="bdfad-103">Rozpoczyna operację przechwytywania pakietów w połączeniu VPN.</span><span class="sxs-lookup"><span data-stu-id="bdfad-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="bdfad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdfad-104">SYNTAX</span></span>

### <span data-ttu-id="bdfad-105">ByVpnConnectionName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdfad-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdfad-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="bdfad-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdfad-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="bdfad-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdfad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="bdfad-108">DESCRIPTION</span></span>
<span data-ttu-id="bdfad-109">Rozpoczyna operację przechwytywania pakietów w połączeniu VPN.</span><span class="sxs-lookup"><span data-stu-id="bdfad-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="bdfad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdfad-110">EXAMPLES</span></span>

### <span data-ttu-id="bdfad-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdfad-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="bdfad-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bdfad-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="bdfad-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdfad-113">PARAMETERS</span></span>

### <span data-ttu-id="bdfad-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdfad-114">-AsJob</span></span>
<span data-ttu-id="bdfad-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bdfad-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdfad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdfad-116">-DefaultProfile</span></span>
<span data-ttu-id="bdfad-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdfad-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdfad-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="bdfad-118">-FilterData</span></span>
<span data-ttu-id="bdfad-119">Opcje filtrowania dotyczące uruchamiania funkcji przechwytywania pakietów w połączeniu VPN.</span><span class="sxs-lookup"><span data-stu-id="bdfad-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="bdfad-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bdfad-120">-InputObject</span></span>
<span data-ttu-id="bdfad-121">Obiekt połączenia VPN, w którym jest uruchamiany przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="bdfad-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfad-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="bdfad-122">-LinkConnectionName</span></span>
<span data-ttu-id="bdfad-123">Nazwy SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="bdfad-123">The names of the SiteLinkConnection.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfad-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdfad-124">-Name</span></span>
<span data-ttu-id="bdfad-125">Nazwa połączenia z siecią VPN, w którym przechwytywanie pakietów jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdfad-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfad-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="bdfad-126">-ParentResourceName</span></span>
<span data-ttu-id="bdfad-127">Nazwa Vpngateway nadrzędnego.</span><span class="sxs-lookup"><span data-stu-id="bdfad-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdfad-128">-ResourceGroupName</span></span>
<span data-ttu-id="bdfad-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bdfad-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdfad-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bdfad-130">-ResourceId</span></span>
<span data-ttu-id="bdfad-131">Identyfikator zasobu platformy Azure VpnConnection, w którym jest uruchamiane przechwytywanie pakietów.</span><span class="sxs-lookup"><span data-stu-id="bdfad-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdfad-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdfad-132">-Confirm</span></span>
<span data-ttu-id="bdfad-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdfad-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdfad-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdfad-134">-WhatIf</span></span>
<span data-ttu-id="bdfad-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdfad-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdfad-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdfad-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdfad-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdfad-137">CommonParameters</span></span>
<span data-ttu-id="bdfad-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdfad-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdfad-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="bdfad-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdfad-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdfad-140">INPUTS</span></span>

### <span data-ttu-id="bdfad-141">Microsoft. Azure. Commands. Network. models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="bdfad-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="bdfad-142">System. String</span><span class="sxs-lookup"><span data-stu-id="bdfad-142">System.String</span></span>

## <span data-ttu-id="bdfad-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdfad-143">OUTPUTS</span></span>

### <span data-ttu-id="bdfad-144">Microsoft. Azure. Commands. Network. models. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="bdfad-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="bdfad-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdfad-145">NOTES</span></span>

## <span data-ttu-id="bdfad-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdfad-146">RELATED LINKS</span></span>

[<span data-ttu-id="bdfad-147">Zatrzymaj — AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bdfad-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)