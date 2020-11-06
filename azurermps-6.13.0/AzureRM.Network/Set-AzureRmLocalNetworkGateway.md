---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmLocalNetworkGateway.md
ms.openlocfilehash: a37cb732aed95a2c31c970d83558a3eff8ab31c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524377"
---
# <span data-ttu-id="fe959-101">Set-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-101">Set-AzureRmLocalNetworkGateway</span></span>

## <span data-ttu-id="fe959-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe959-102">SYNOPSIS</span></span>
<span data-ttu-id="fe959-103">Modyfikuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="fe959-103">Modifies a local network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe959-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe959-104">SYNTAX</span></span>

```
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe959-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe959-105">DESCRIPTION</span></span>
<span data-ttu-id="fe959-106">Polecenie cmdlet **Set-AzureRmLocalNetworkGateway** modyfikuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="fe959-106">The **Set-AzureRmLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="fe959-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe959-107">EXAMPLES</span></span>

### <span data-ttu-id="fe959-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe959-108">Example 1</span></span>
<span data-ttu-id="fe959-109">Ustawianie konfiguracji dla istniejącej bramy</span><span class="sxs-lookup"><span data-stu-id="fe959-109">Set configuration for an existing gateway</span></span>


```
$lgw = Get-AzureRmLocalNetworkGateway -Name myLocalGW -ResourceGroupName myRG
Set-AzureRmLocalNetworkGateway -LocalNetworkGateway $lgw

Name                     : myLocalGW
ResourceGroupName        : TestRG1
Location                 : westus
Id                       : /subscriptions/81ab786c-56eb-4a4d-bb5f-f60329772466/resourceGroups/TestRG1/providers/Microso
                           ft.Network/localNetworkGateways/myLocalGW
Etag                     : W/"d2de6968-315e-411d-a4b8-a8c335abe61b"
ResourceGuid             : 393acf8b-dbb8-4b08-a9ea-c714570710e1
ProvisioningState        : Succeeded
Tags                     :
GatewayIpAddress         : 1.2.3.4
LocalNetworkAddressSpace : {
                             "AddressPrefixes": []
                           }
BgpSettings              : null
```

## <span data-ttu-id="fe959-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe959-110">PARAMETERS</span></span>

### <span data-ttu-id="fe959-111">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="fe959-111">-AddressPrefix</span></span>
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

### <span data-ttu-id="fe959-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe959-112">-AsJob</span></span>
<span data-ttu-id="fe959-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="fe959-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe959-114">-ASN</span><span class="sxs-lookup"><span data-stu-id="fe959-114">-Asn</span></span>
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

### <span data-ttu-id="fe959-115">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="fe959-115">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="fe959-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe959-116">-DefaultProfile</span></span>
<span data-ttu-id="fe959-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe959-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe959-118">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-118">-LocalNetworkGateway</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe959-119">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="fe959-119">-PeerWeight</span></span>
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

### <span data-ttu-id="fe959-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe959-120">CommonParameters</span></span>
<span data-ttu-id="fe959-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe959-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe959-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe959-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe959-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe959-123">INPUTS</span></span>

### <span data-ttu-id="fe959-124">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-124">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>
<span data-ttu-id="fe959-125">Parametry: LocalNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fe959-125">Parameters: LocalNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="fe959-126">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="fe959-126">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="fe959-127">System. UInt32</span><span class="sxs-lookup"><span data-stu-id="fe959-127">System.UInt32</span></span>

### <span data-ttu-id="fe959-128">System. String</span><span class="sxs-lookup"><span data-stu-id="fe959-128">System.String</span></span>

### <span data-ttu-id="fe959-129">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fe959-129">System.Int32</span></span>

## <span data-ttu-id="fe959-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe959-130">OUTPUTS</span></span>

### <span data-ttu-id="fe959-131">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-131">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="fe959-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe959-132">NOTES</span></span>

## <span data-ttu-id="fe959-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe959-133">RELATED LINKS</span></span>

[<span data-ttu-id="fe959-134">Get-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-134">Get-AzureRmLocalNetworkGateway</span></span>](./Get-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="fe959-135">Nowe — AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-135">New-AzureRmLocalNetworkGateway</span></span>](./New-AzureRmLocalNetworkGateway.md)

[<span data-ttu-id="fe959-136">Remove-AzureRmLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="fe959-136">Remove-AzureRmLocalNetworkGateway</span></span>](./Remove-AzureRmLocalNetworkGateway.md)


