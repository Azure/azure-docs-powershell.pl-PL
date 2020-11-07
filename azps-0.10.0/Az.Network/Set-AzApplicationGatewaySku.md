---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewaySku.md
ms.openlocfilehash: a0a8c3d3f2e058fa51283a02ecb53df62c0b8970
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892821"
---
# <span data-ttu-id="9b5dc-101">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9b5dc-101">Set-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="9b5dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b5dc-102">SYNOPSIS</span></span>
<span data-ttu-id="9b5dc-103">Modyfikuje jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-103">Modifies the SKU of an application gateway.</span></span>

## <span data-ttu-id="9b5dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b5dc-104">SYNTAX</span></span>

```
Set-AzApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b5dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9b5dc-105">DESCRIPTION</span></span>
<span data-ttu-id="9b5dc-106">Polecenie cmdlet **Set-AzApplicationGatewaySku** modyfikuje jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-106">The **Set-AzApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="9b5dc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b5dc-107">EXAMPLES</span></span>

### <span data-ttu-id="9b5dc-108">Przykład 1: Aktualizowanie wersji SKU bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="9b5dc-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="9b5dc-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="9b5dc-110">Drugie polecenie aktualizuje jednostkę SKU bramy Application.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="9b5dc-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b5dc-111">PARAMETERS</span></span>

### <span data-ttu-id="9b5dc-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b5dc-112">-ApplicationGateway</span></span>
<span data-ttu-id="9b5dc-113">Określa obiekt bramy aplikacji, z którym ten polecenie cmdlet kojarzy jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b5dc-114">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="9b5dc-114">-Capacity</span></span>
<span data-ttu-id="9b5dc-115">Określa liczbę wystąpień bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-115">Specifies the instance count of the application gateway.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b5dc-116">-DefaultProfile</span></span>
<span data-ttu-id="9b5dc-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b5dc-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b5dc-118">-Name</span></span>
<span data-ttu-id="9b5dc-119">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="9b5dc-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9b5dc-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b5dc-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="9b5dc-121">Standard_Small</span></span>
- <span data-ttu-id="9b5dc-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="9b5dc-122">Standard_Medium</span></span>
- <span data-ttu-id="9b5dc-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="9b5dc-123">Standard_Large</span></span>
- <span data-ttu-id="9b5dc-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="9b5dc-124">WAF_Medium</span></span>
- <span data-ttu-id="9b5dc-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="9b5dc-125">WAF_Large</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5dc-126">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="9b5dc-126">-Tier</span></span>
<span data-ttu-id="9b5dc-127">Określa poziom bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="9b5dc-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9b5dc-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9b5dc-129">Standard</span><span class="sxs-lookup"><span data-stu-id="9b5dc-129">Standard</span></span>
- <span data-ttu-id="9b5dc-130">WAF</span><span class="sxs-lookup"><span data-stu-id="9b5dc-130">WAF</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b5dc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b5dc-131">CommonParameters</span></span>
<span data-ttu-id="9b5dc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b5dc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b5dc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b5dc-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b5dc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b5dc-134">INPUTS</span></span>

### <span data-ttu-id="9b5dc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="9b5dc-135">System.String</span></span>

## <span data-ttu-id="9b5dc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b5dc-136">OUTPUTS</span></span>

### <span data-ttu-id="9b5dc-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="9b5dc-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="9b5dc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b5dc-138">NOTES</span></span>

## <span data-ttu-id="9b5dc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b5dc-139">RELATED LINKS</span></span>

[<span data-ttu-id="9b5dc-140">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9b5dc-140">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="9b5dc-141">Nowe — AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="9b5dc-141">New-AzApplicationGatewaySku</span></span>](./New-AzApplicationGatewaySku.md)


