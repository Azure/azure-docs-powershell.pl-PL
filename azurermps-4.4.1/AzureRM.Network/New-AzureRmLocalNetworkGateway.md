---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 3acfbf1462a1f0ae75d95b9f3976c46fd07676f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550884"
---
# <span data-ttu-id="5ceec-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ceec-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="5ceec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ceec-102">SYNOPSIS</span></span>
<span data-ttu-id="5ceec-103">Tworzy bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="5ceec-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ceec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ceec-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ceec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ceec-105">DESCRIPTION</span></span>
<span data-ttu-id="5ceec-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="5ceec-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="5ceec-107">Polecenie cmdlet **New-AzureRmLocalNetworkGateway** tworzy obiekt reprezentujący bramę on-środowisku na podstawie nazwy, nazwy, lokalizacji i adresu IP bramy oraz prefiksu adresu sieci lokalnej, który będzie łączyć się z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ceec-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="5ceec-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ceec-108">EXAMPLES</span></span>

### <span data-ttu-id="5ceec-109">1: Tworzenie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="5ceec-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="5ceec-110">Tworzy obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG" w lokalizacji "Zachodnia USA" z adresem IP "23.99.221.164" oraz prefiksem adresu "10.5.51.0/24" on-środowisku.</span><span class="sxs-lookup"><span data-stu-id="5ceec-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="5ceec-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ceec-111">PARAMETERS</span></span>

### <span data-ttu-id="5ceec-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="5ceec-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="5ceec-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="5ceec-113">-Asn</span></span>
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

### <span data-ttu-id="5ceec-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="5ceec-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="5ceec-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ceec-115">-Force</span></span>
<span data-ttu-id="5ceec-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="5ceec-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ceec-117">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ceec-117">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="5ceec-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ceec-118">-Location</span></span>
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

### <span data-ttu-id="5ceec-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ceec-119">-Name</span></span>
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

### <span data-ttu-id="5ceec-120">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="5ceec-120">-PeerWeight</span></span>
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

### <span data-ttu-id="5ceec-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ceec-121">-ResourceGroupName</span></span>
<span data-ttu-id="5ceec-122">Określa grupę zasobów, do której należy lokalna Brama sieci.</span><span class="sxs-lookup"><span data-stu-id="5ceec-122">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="5ceec-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="5ceec-123">-Tag</span></span>
<span data-ttu-id="5ceec-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="5ceec-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5ceec-125">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="5ceec-125">For example:</span></span>

<span data-ttu-id="5ceec-126">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="5ceec-126">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5ceec-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ceec-127">-Confirm</span></span>
<span data-ttu-id="5ceec-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ceec-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ceec-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ceec-129">-WhatIf</span></span>
<span data-ttu-id="5ceec-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ceec-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ceec-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ceec-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ceec-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ceec-132">-DefaultProfile</span></span>
<span data-ttu-id="5ceec-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ceec-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5ceec-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ceec-134">CommonParameters</span></span>
<span data-ttu-id="5ceec-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ceec-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ceec-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ceec-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ceec-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ceec-137">INPUTS</span></span>

## <span data-ttu-id="5ceec-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ceec-138">OUTPUTS</span></span>

### <span data-ttu-id="5ceec-139">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ceec-139">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="5ceec-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ceec-140">NOTES</span></span>

## <span data-ttu-id="5ceec-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ceec-141">RELATED LINKS</span></span>

[<span data-ttu-id="5ceec-142">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ceec-142">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="5ceec-143">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ceec-143">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="5ceec-144">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="5ceec-144">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
