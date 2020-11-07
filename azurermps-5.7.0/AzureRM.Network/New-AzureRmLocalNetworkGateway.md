---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 59BE802E-C061-4E25-A446-B00B0BA36019
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: 6db2d9defaed434aa74f64d6f13af4f029edf482
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717200"
---
# <span data-ttu-id="05e9c-101">New-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05e9c-101">New-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="05e9c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05e9c-102">SYNOPSIS</span></span>
<span data-ttu-id="05e9c-103">Tworzy bramę sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="05e9c-103">Creates a Local Network Gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05e9c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05e9c-104">SYNTAX</span></span>

```
New-AzureRmLocalNetworkGateway -Name <String> -ResourceGroupName <String> -Location <String>
 [-GatewayIpAddress <String>] [-AddressPrefix <System.Collections.Generic.List`1[System.String]>]
 [-Asn <UInt32>] [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05e9c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05e9c-105">DESCRIPTION</span></span>
<span data-ttu-id="05e9c-106">Lokalna Brama sieci to obiekt reprezentujący urządzenie VPN.</span><span class="sxs-lookup"><span data-stu-id="05e9c-106">The Local Network Gateway is the object representing your VPN device On-Premises.</span></span>

<span data-ttu-id="05e9c-107">Polecenie cmdlet **New-AzureRmLocalNetworkGateway** tworzy obiekt reprezentujący bramę on-środowisku na podstawie nazwy, nazwy, lokalizacji i adresu IP bramy oraz prefiksu adresu sieci lokalnej, który będzie łączyć się z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05e9c-107">The **New-AzureRmLocalNetworkGateway** cmdlet creates the object representing your on-prem gateway based on the Name, Resource Group Name, Location, and IP Address of the gateway, as well as the Address Prefix of the On-Premises network which will be connecting to Azure.</span></span>

## <span data-ttu-id="05e9c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05e9c-108">EXAMPLES</span></span>

### <span data-ttu-id="05e9c-109">1: Tworzenie bramy sieci lokalnej</span><span class="sxs-lookup"><span data-stu-id="05e9c-109">1: Create a Local Network Gateway</span></span>
```
New-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG -Location "West US" -GatewayIpAddress 23.99.221.164 -AddressPrefix "10.5.51.0/24"
```

<span data-ttu-id="05e9c-110">Tworzy obiekt bramy sieci lokalnej o nazwie "myLocalGW" w grupie zasobów "myRG" w lokalizacji "Zachodnia USA" z adresem IP "23.99.221.164" oraz prefiksem adresu "10.5.51.0/24" on-środowisku.</span><span class="sxs-lookup"><span data-stu-id="05e9c-110">Creates the object of the Local Network Gateway with the name "myLocalGW" within the resource group "myRG" in location "West US" with the IP address "23.99.221.164" and the address prefix "10.5.51.0/24" on-prem.</span></span>

## <span data-ttu-id="05e9c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05e9c-111">PARAMETERS</span></span>

### <span data-ttu-id="05e9c-112">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="05e9c-112">-AddressPrefix</span></span>
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

### <span data-ttu-id="05e9c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05e9c-113">-AsJob</span></span>
<span data-ttu-id="05e9c-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="05e9c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="05e9c-115">-ASN</span><span class="sxs-lookup"><span data-stu-id="05e9c-115">-Asn</span></span>
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

### <span data-ttu-id="05e9c-116">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="05e9c-116">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="05e9c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05e9c-117">-DefaultProfile</span></span>
<span data-ttu-id="05e9c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05e9c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05e9c-119">-Force</span><span class="sxs-lookup"><span data-stu-id="05e9c-119">-Force</span></span>
<span data-ttu-id="05e9c-120">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="05e9c-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="05e9c-121">-GatewayIpAddress</span><span class="sxs-lookup"><span data-stu-id="05e9c-121">-GatewayIpAddress</span></span>
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

### <span data-ttu-id="05e9c-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="05e9c-122">-Location</span></span>
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

### <span data-ttu-id="05e9c-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05e9c-123">-Name</span></span>
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

### <span data-ttu-id="05e9c-124">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="05e9c-124">-PeerWeight</span></span>
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

### <span data-ttu-id="05e9c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05e9c-125">-ResourceGroupName</span></span>
<span data-ttu-id="05e9c-126">Określa grupę zasobów, do której należy lokalna Brama sieci.</span><span class="sxs-lookup"><span data-stu-id="05e9c-126">Specifies the resource group that the local network gateway belongs to.</span></span>

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

### <span data-ttu-id="05e9c-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="05e9c-127">-Tag</span></span>
<span data-ttu-id="05e9c-128">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="05e9c-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="05e9c-129">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="05e9c-129">For example:</span></span>

<span data-ttu-id="05e9c-130">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="05e9c-130">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="05e9c-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05e9c-131">-Confirm</span></span>
<span data-ttu-id="05e9c-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e9c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05e9c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05e9c-133">-WhatIf</span></span>
<span data-ttu-id="05e9c-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05e9c-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05e9c-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05e9c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05e9c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05e9c-136">CommonParameters</span></span>
<span data-ttu-id="05e9c-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05e9c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05e9c-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05e9c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05e9c-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05e9c-139">INPUTS</span></span>

### <span data-ttu-id="05e9c-140">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="05e9c-140">None</span></span>
<span data-ttu-id="05e9c-141">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="05e9c-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05e9c-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05e9c-142">OUTPUTS</span></span>

### <span data-ttu-id="05e9c-143">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05e9c-143">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="05e9c-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05e9c-144">NOTES</span></span>

## <span data-ttu-id="05e9c-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05e9c-145">RELATED LINKS</span></span>

[<span data-ttu-id="05e9c-146">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05e9c-146">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="05e9c-147">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05e9c-147">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="05e9c-148">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="05e9c-148">Set-AzureRmLocalNetworkGateway</span></span>](./Set-AzureRmLocalNetworkGateway.md)
