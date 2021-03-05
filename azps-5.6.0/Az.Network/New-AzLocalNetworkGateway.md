---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 2a5b3260aff2167de9d46ad276d7ced1f0373b95
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992559"
---
# <span data-ttu-id="91adb-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91adb-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="91adb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91adb-102">SYNOPSIS</span></span>
<span data-ttu-id="91adb-103">Tworzy lokalną bramę sieciową</span><span class="sxs-lookup"><span data-stu-id="91adb-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="91adb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91adb-104">SYNTAX</span></span>

### <span data-ttu-id="91adb-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="91adb-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91adb-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="91adb-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91adb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="91adb-107">DESCRIPTION</span></span>
<span data-ttu-id="91adb-108">Lokalna brama sieciowa to obiekt reprezentujący lokalne urządzenie sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="91adb-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="91adb-109">Polecenie cmdlet **New-AzLocalNetworkGateway** tworzy obiekt reprezentujący lokalną bramę na podstawie nazwy, nazwy grupy zasobów, lokalizacji i adresu IP bramy, a także prefiksu adresu sieci lokalnej, która będzie nawiązywać połączenie z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91adb-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="91adb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91adb-110">EXAMPLES</span></span>

### <span data-ttu-id="91adb-111">Przykład 1. Tworzenie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="91adb-111">Example 1: Create a Local Network Gateway</span></span>
```powershell
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="91adb-112">Tworzy obiekt lokalnej bramy sieciowej o nazwie "myLocalGW" w grupie zasobów "myRG" w lokalizacji "Zachód US" z adresem IP "23.99.221.164" i prefiksem adresu "10.5.51.0/24" w zamowie.</span><span class="sxs-lookup"><span data-stu-id="91adb-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="91adb-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91adb-113">PARAMETERS</span></span>

### <span data-ttu-id="91adb-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="91adb-114">-AddressPrefix</span></span>
```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="91adb-115">-AsJob</span></span>
<span data-ttu-id="91adb-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="91adb-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91adb-117">— Asn</span><span class="sxs-lookup"><span data-stu-id="91adb-117">-Asn</span></span>
```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="91adb-118">-BgpPeeringAddress</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91adb-119">-DefaultProfile</span></span>
<span data-ttu-id="91adb-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91adb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91adb-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="91adb-121">-Force</span></span>
<span data-ttu-id="91adb-122">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="91adb-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="91adb-123">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="91adb-123">-Fqdn</span></span>
<span data-ttu-id="91adb-124">FQDN bramy sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="91adb-124">FQDN of local network gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayFqdn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="91adb-125">-GatewayIpAddress</span></span>
```yaml
Type: System.String
Parameter Sets: ByLocalNetworkGatewayIpAddress
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="91adb-126">-Location</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91adb-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-128">- PeerWeight</span><span class="sxs-lookup"><span data-stu-id="91adb-128">-PeerWeight</span></span>
```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91adb-129">-ResourceGroupName</span></span>
<span data-ttu-id="91adb-130">Określa grupę zasobów, do której należy brama sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="91adb-130">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="91adb-131">-Tag</span></span>
<span data-ttu-id="91adb-132">Pary klucz-wartość w postaci tabeli skrótu.</span><span class="sxs-lookup"><span data-stu-id="91adb-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="91adb-133">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="91adb-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91adb-134">-Confirm</span></span>
<span data-ttu-id="91adb-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91adb-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91adb-136">-WhatIf</span></span>
<span data-ttu-id="91adb-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91adb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91adb-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="91adb-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91adb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91adb-139">CommonParameters</span></span>
<span data-ttu-id="91adb-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91adb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91adb-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91adb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91adb-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91adb-142">INPUTS</span></span>

### <span data-ttu-id="91adb-143">System.String</span><span class="sxs-lookup"><span data-stu-id="91adb-143">System.String</span></span>

### <span data-ttu-id="91adb-144">System.String[]</span><span class="sxs-lookup"><span data-stu-id="91adb-144">System.String[]</span></span>

### <span data-ttu-id="91adb-145">System.UInt32</span><span class="sxs-lookup"><span data-stu-id="91adb-145">System.UInt32</span></span>

### <span data-ttu-id="91adb-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="91adb-146">System.Int32</span></span>

### <span data-ttu-id="91adb-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="91adb-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="91adb-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91adb-148">OUTPUTS</span></span>

### <span data-ttu-id="91adb-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91adb-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="91adb-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91adb-150">NOTES</span></span>

## <span data-ttu-id="91adb-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91adb-151">RELATED LINKS</span></span>

[<span data-ttu-id="91adb-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91adb-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="91adb-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91adb-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="91adb-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="91adb-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
