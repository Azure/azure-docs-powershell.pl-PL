---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLocalNetworkGateway.md
ms.openlocfilehash: 37255dfda50d7c055aad6941bbf417d1aa852d35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890477"
---
# <span data-ttu-id="c79cd-101">New-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c79cd-101">New-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="c79cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c79cd-102">SYNOPSIS</span></span>
<span data-ttu-id="c79cd-103">Tworzy bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="c79cd-103">Creates a Local Network Gateway</span></span>

## <span data-ttu-id="c79cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c79cd-104">SYNTAX</span></span>

```
New-AzLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c79cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c79cd-105">DESCRIPTION</span></span>
<span data-ttu-id="c79cd-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="c79cd-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="c79cd-107">Polecenie cmdlet **New-AzLocalNetworkGateway** tworzy obiekt reprezentujący bramę on-środowisku na podstawie nazwy, nazwy, lokalizacji i adresu IP bramy oraz prefiksu adresu sieci lokalnej, który będzie łączyć się z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c79cd-107">The **New-AzLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="c79cd-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c79cd-108">EXAMPLES</span></span>

### <span data-ttu-id="c79cd-109">1: Tworzenie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="c79cd-109">1: Create a Local Network Gateway</span></span>
```
New-AzLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="c79cd-110">Tworzy obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG" w lokalizacji "Zachodnia USA" z adresem IP "23.99.221.164" oraz prefiksem adresu "10.5.51.0/24" on-środowisku.</span><span class="sxs-lookup"><span data-stu-id="c79cd-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="c79cd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c79cd-111">PARAMETERS</span></span>

### <span data-ttu-id="c79cd-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="c79cd-112">-AddressPrefix</span></span>
```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c79cd-113">-AsJob</span></span>
<span data-ttu-id="c79cd-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c79cd-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c79cd-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="c79cd-115">-Asn</span></span>
```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="c79cd-116">-BgpPeeringAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c79cd-117">-DefaultProfile</span></span>
<span data-ttu-id="c79cd-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c79cd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="c79cd-119">-Force</span></span>
<span data-ttu-id="c79cd-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c79cd-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c79cd-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="c79cd-121">-GatewayIpAddress</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c79cd-122">-Location</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c79cd-123">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="c79cd-124">-PeerWeight</span></span>
```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c79cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="c79cd-126">Określa grupę zasobów, do której należy lokalna Brama sieci.</span><span class="sxs-lookup"><span data-stu-id="c79cd-126">Specifies the resource group that the local network gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="c79cd-127">-Tag</span></span>
<span data-ttu-id="c79cd-128">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c79cd-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="c79cd-129">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="c79cd-129">For example:</span></span>

<span data-ttu-id="c79cd-130">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="c79cd-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c79cd-131">-Confirm</span></span>
<span data-ttu-id="c79cd-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c79cd-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c79cd-133">-WhatIf</span></span>
<span data-ttu-id="c79cd-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c79cd-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c79cd-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c79cd-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c79cd-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c79cd-136">CommonParameters</span></span>
<span data-ttu-id="c79cd-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c79cd-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c79cd-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c79cd-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c79cd-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c79cd-139">INPUTS</span></span>

## <span data-ttu-id="c79cd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c79cd-140">OUTPUTS</span></span>

### <span data-ttu-id="c79cd-141">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c79cd-141">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="c79cd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c79cd-142">NOTES</span></span>

## <span data-ttu-id="c79cd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c79cd-143">RELATED LINKS</span></span>

[<span data-ttu-id="c79cd-144">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c79cd-144">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="c79cd-145">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c79cd-145">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)

[<span data-ttu-id="c79cd-146">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="c79cd-146">Set-AzLocalNetworkGateway</span></span>](./Set-AzLocalNetworkGateway.md)
