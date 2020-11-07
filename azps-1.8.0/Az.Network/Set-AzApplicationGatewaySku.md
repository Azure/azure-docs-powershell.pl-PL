---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: ccc78a65041cac5cb471ac1f1bfa8d3ea3248ba1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709003"
---
# <span data-ttu-id="f87ad-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f87ad-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="f87ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f87ad-102">SYNOPSIS</span></span>
<span data-ttu-id="f87ad-103">Modyfikuje jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f87ad-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="f87ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f87ad-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f87ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f87ad-105">DESCRIPTION</span></span>
<span data-ttu-id="f87ad-106">Polecenie cmdlet **Set-AzApplicationGatewaySku** modyfikuje jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f87ad-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="f87ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f87ad-107">EXAMPLES</span></span>

### <span data-ttu-id="f87ad-108">Przykład 1: Aktualizowanie wersji SKU bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="f87ad-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="f87ad-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f87ad-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="f87ad-110">Drugie polecenie aktualizuje jednostkę SKU bramy Application.</span><span class="sxs-lookup"><span data-stu-id="f87ad-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="f87ad-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f87ad-111">PARAMETERS</span></span>

### <span data-ttu-id="f87ad-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f87ad-112">-ApplicationGateway</span></span>
<span data-ttu-id="f87ad-113">Określa obiekt bramy aplikacji, z którym ten polecenie cmdlet kojarzy jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="f87ad-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f87ad-114">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="f87ad-114">-Capacity</span></span>
<span data-ttu-id="f87ad-115">Określa liczbę wystąpień bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f87ad-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87ad-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f87ad-116">-DefaultProfile</span></span>
<span data-ttu-id="f87ad-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f87ad-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f87ad-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f87ad-118">-Name</span></span>
<span data-ttu-id="f87ad-119">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f87ad-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="f87ad-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f87ad-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f87ad-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="f87ad-121">Standard_Small</span></span>
- <span data-ttu-id="f87ad-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="f87ad-122">Standard_Medium</span></span>
- <span data-ttu-id="f87ad-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="f87ad-123">Standard_Large</span></span>
- <span data-ttu-id="f87ad-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="f87ad-124">WAF_Medium</span></span>
- <span data-ttu-id="f87ad-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="f87ad-125">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87ad-126">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="f87ad-126">-Tier</span></span>
<span data-ttu-id="f87ad-127">Określa poziom bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f87ad-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="f87ad-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f87ad-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f87ad-129">Standard</span><span class="sxs-lookup"><span data-stu-id="f87ad-129">Standard</span></span>
- <span data-ttu-id="f87ad-130">WAF</span><span class="sxs-lookup"><span data-stu-id="f87ad-130">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, WAF, Standard_v2, WAF_v2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f87ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f87ad-131">CommonParameters</span></span>
<span data-ttu-id="f87ad-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f87ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f87ad-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f87ad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f87ad-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f87ad-134">INPUTS</span></span>

### <span data-ttu-id="f87ad-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f87ad-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f87ad-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f87ad-136">OUTPUTS</span></span>

### <span data-ttu-id="f87ad-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f87ad-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f87ad-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f87ad-138">NOTES</span></span>

## <span data-ttu-id="f87ad-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f87ad-139">RELATED LINKS</span></span>

[<span data-ttu-id="f87ad-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f87ad-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="f87ad-141">Nowe — AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="f87ad-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


