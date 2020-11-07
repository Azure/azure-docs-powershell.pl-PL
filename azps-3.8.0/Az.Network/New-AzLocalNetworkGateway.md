---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: f355d011bbd810fa309cd8b7d64ed95090a00ea6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894385"
---
# <span data-ttu-id="195c1-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195c1-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="195c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="195c1-102">SYNOPSIS</span></span>
<span data-ttu-id="195c1-103">Tworzy bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="195c1-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="195c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="195c1-104">SYNTAX</span></span>

### <span data-ttu-id="195c1-105">ByLocalNetworkGatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="195c1-105">ByLocalNetworkGatewayIpAddress</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>]
 [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="195c1-106">ByLocalNetworkGatewayFqdn</span><span class="sxs-lookup"><span data-stu-id="195c1-106">ByLocalNetworkGatewayFqdn</span></span>
```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String> [-Fqdn <String>]
 [-AddressPrefix <String[]>] [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="195c1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="195c1-107">DESCRIPTION</span></span>
<span data-ttu-id="195c1-108">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="195c1-108">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>
<span data-ttu-id="195c1-109">Polecenie cmdlet **New-AzLocalNetworkGateway** tworzy obiekt reprezentujący bramę on-środowisku na podstawie nazwy, nazwy, lokalizacji i adresu IP bramy oraz prefiksu adresu sieci lokalnej, który będzie łączyć się z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="195c1-109">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="195c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="195c1-110">EXAMPLES</span></span>

### <span data-ttu-id="195c1-111">1: Tworzenie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="195c1-111">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="195c1-112">Tworzy obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG" w lokalizacji "Zachodnia USA" z adresem IP "23.99.221.164" oraz prefiksem adresu "10.5.51.0/24" on-środowisku.</span><span class="sxs-lookup"><span data-stu-id="195c1-112">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="195c1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="195c1-113">PARAMETERS</span></span>

### <span data-ttu-id="195c1-114">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="195c1-114">-AddressPrefix</span></span>
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

### <span data-ttu-id="195c1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="195c1-115">-AsJob</span></span>
<span data-ttu-id="195c1-116">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="195c1-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="195c1-117">-ASN</span><span class="sxs-lookup"><span data-stu-id="195c1-117">-Asn</span></span>
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

### <span data-ttu-id="195c1-118">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="195c1-118">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="195c1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="195c1-119">-DefaultProfile</span></span>
<span data-ttu-id="195c1-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="195c1-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="195c1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="195c1-121">-Force</span></span>
<span data-ttu-id="195c1-122">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="195c1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="195c1-123">-FQDN</span><span class="sxs-lookup"><span data-stu-id="195c1-123">-Fqdn</span></span>
<span data-ttu-id="195c1-124">FQDN bramy sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="195c1-124">FQDN of local network gateway.</span></span>

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

### <span data-ttu-id="195c1-125">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="195c1-125">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="195c1-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="195c1-126">-Location</span></span>
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

### <span data-ttu-id="195c1-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="195c1-127">-Name</span></span>
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

### <span data-ttu-id="195c1-128">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="195c1-128">-PeerWeight</span></span>
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

### <span data-ttu-id="195c1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="195c1-129">-ResourceGroupName</span></span>
<span data-ttu-id="195c1-130">Określa grupę zasobów, do której należy lokalna Brama sieci.</span><span class="sxs-lookup"><span data-stu-id="195c1-130">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="195c1-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="195c1-131">-Tag</span></span>
<span data-ttu-id="195c1-132">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="195c1-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="195c1-133">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="195c1-133">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="195c1-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="195c1-134">-Confirm</span></span>
<span data-ttu-id="195c1-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195c1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="195c1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="195c1-136">-WhatIf</span></span>
<span data-ttu-id="195c1-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="195c1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="195c1-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="195c1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="195c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="195c1-139">CommonParameters</span></span>
<span data-ttu-id="195c1-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="195c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="195c1-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="195c1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="195c1-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="195c1-142">INPUTS</span></span>

### <span data-ttu-id="195c1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="195c1-143">System.String</span></span>

### <span data-ttu-id="195c1-144">System. String []</span><span class="sxs-lookup"><span data-stu-id="195c1-144">System.String[]</span></span>

### <span data-ttu-id="195c1-145">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="195c1-145">System.UInt32</span></span>

### <span data-ttu-id="195c1-146">System. Int32</span><span class="sxs-lookup"><span data-stu-id="195c1-146">System.Int32</span></span>

### <span data-ttu-id="195c1-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="195c1-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="195c1-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="195c1-148">OUTPUTS</span></span>

### <span data-ttu-id="195c1-149">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195c1-149">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="195c1-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="195c1-150">NOTES</span></span>

## <span data-ttu-id="195c1-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="195c1-151">RELATED LINKS</span></span>

[<span data-ttu-id="195c1-152">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195c1-152">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="195c1-153">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195c1-153">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="195c1-154">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="195c1-154">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
