---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: F8C1DF39-1DAF-4BDB-8B0E-1BC3B5E82185
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azlocalnetworkgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzLocalNetworkGateway.md
ms.openlocfilehash: 61e2fd8a4f6c073bbb900586b0d73dec97c3b662
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892774"
---
# <span data-ttu-id="20f27-101">Set-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-101">Set-AzLocalNetworkGateway</span></span>

## <span data-ttu-id="20f27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20f27-102">SYNOPSIS</span></span>
<span data-ttu-id="20f27-103">Modyfikuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="20f27-103">Modifies a local network gateway.</span></span>

## <span data-ttu-id="20f27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20f27-104">SYNTAX</span></span>

```
Set-AzLocalNetworkGateway -LocalNetworkGateway <PSLocalNetworkGateway>
 [-AddressPrefix <System.Collections.Generic.List`1[System.String]>] [-Asn <UInt32>]
 [-BgpPeeringAddress <String>] [-PeerWeight <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20f27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20f27-105">DESCRIPTION</span></span>
<span data-ttu-id="20f27-106">Polecenie cmdlet **Set-AzLocalNetworkGateway** modyfikuje bramę sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="20f27-106">The **Set-AzLocalNetworkGateway** cmdlet modifies a local network gateway.</span></span>

## <span data-ttu-id="20f27-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20f27-107">EXAMPLES</span></span>

### <span data-ttu-id="20f27-108">1:1</span><span class="sxs-lookup"><span data-stu-id="20f27-108">1:</span></span>
```

```

## <span data-ttu-id="20f27-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20f27-109">PARAMETERS</span></span>

### <span data-ttu-id="20f27-110">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="20f27-110">-AddressPrefix</span></span>
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

### <span data-ttu-id="20f27-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20f27-111">-AsJob</span></span>
<span data-ttu-id="20f27-112">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="20f27-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20f27-113">-ASN</span><span class="sxs-lookup"><span data-stu-id="20f27-113">-Asn</span></span>
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

### <span data-ttu-id="20f27-114">-BgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="20f27-114">-BgpPeeringAddress</span></span>
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

### <span data-ttu-id="20f27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f27-115">-DefaultProfile</span></span>
<span data-ttu-id="20f27-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20f27-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f27-117">-LocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-117">-LocalNetworkGateway</span></span>
```yaml
Type: PSLocalNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="20f27-118">-PeerWeight</span><span class="sxs-lookup"><span data-stu-id="20f27-118">-PeerWeight</span></span>
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

### <span data-ttu-id="20f27-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f27-119">CommonParameters</span></span>
<span data-ttu-id="20f27-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20f27-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f27-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f27-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f27-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20f27-122">INPUTS</span></span>

### <span data-ttu-id="20f27-123">PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-123">PSLocalNetworkGateway</span></span>
<span data-ttu-id="20f27-124">Parametr "LocalNetworkGateway" akceptuje wartość typu "PSLocalNetworkGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="20f27-124">Parameter 'LocalNetworkGateway' accepts value of type 'PSLocalNetworkGateway' from the pipeline</span></span>

## <span data-ttu-id="20f27-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20f27-125">OUTPUTS</span></span>

### <span data-ttu-id="20f27-126">Microsoft. Azure. Commands. Network. models. PSLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-126">Microsoft.Azure.Commands.Network.Models.PSLocalNetworkGateway</span></span>

## <span data-ttu-id="20f27-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20f27-127">NOTES</span></span>

## <span data-ttu-id="20f27-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20f27-128">RELATED LINKS</span></span>

[<span data-ttu-id="20f27-129">Get-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-129">Get-AzLocalNetworkGateway</span></span>](./Get-AzLocalNetworkGateway.md)

[<span data-ttu-id="20f27-130">Nowe — AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-130">New-AzLocalNetworkGateway</span></span>](./New-AzLocalNetworkGateway.md)

[<span data-ttu-id="20f27-131">Remove-AzLocalNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20f27-131">Remove-AzLocalNetworkGateway</span></span>](./Remove-AzLocalNetworkGateway.md)


