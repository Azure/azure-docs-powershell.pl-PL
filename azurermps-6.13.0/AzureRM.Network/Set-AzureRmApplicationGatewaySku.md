---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 487a3cd096f1d27852f4472d478977ac0cbe2ccc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718791"
---
# <span data-ttu-id="475f8-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="475f8-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="475f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="475f8-102">SYNOPSIS</span></span>
<span data-ttu-id="475f8-103">Modyfikuje jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="475f8-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="475f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="475f8-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 [-Capacity <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="475f8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="475f8-105">DESCRIPTION</span></span>
<span data-ttu-id="475f8-106">Polecenie cmdlet **Set-AzureRmApplicationGatewaySku** modyfikuje jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="475f8-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="475f8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="475f8-107">EXAMPLES</span></span>

### <span data-ttu-id="475f8-108">Przykład 1: Aktualizowanie wersji SKU bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="475f8-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="475f8-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="475f8-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="475f8-110">Drugie polecenie aktualizuje jednostkę SKU bramy Application.</span><span class="sxs-lookup"><span data-stu-id="475f8-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="475f8-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="475f8-111">PARAMETERS</span></span>

### <span data-ttu-id="475f8-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="475f8-112">-ApplicationGateway</span></span>
<span data-ttu-id="475f8-113">Określa obiekt bramy aplikacji, z którym ten polecenie cmdlet kojarzy jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="475f8-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="475f8-114">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="475f8-114">-Capacity</span></span>
<span data-ttu-id="475f8-115">Określa liczbę wystąpień bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="475f8-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="475f8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="475f8-116">-DefaultProfile</span></span>
<span data-ttu-id="475f8-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="475f8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="475f8-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="475f8-118">-Name</span></span>
<span data-ttu-id="475f8-119">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="475f8-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="475f8-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="475f8-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="475f8-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="475f8-121">Standard_Small</span></span>
- <span data-ttu-id="475f8-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="475f8-122">Standard_Medium</span></span>
- <span data-ttu-id="475f8-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="475f8-123">Standard_Large</span></span>
- <span data-ttu-id="475f8-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="475f8-124">WAF_Medium</span></span>
- <span data-ttu-id="475f8-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="475f8-125">WAF_Large</span></span>

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

### <span data-ttu-id="475f8-126">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="475f8-126">-Tier</span></span>
<span data-ttu-id="475f8-127">Określa poziom bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="475f8-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="475f8-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="475f8-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="475f8-129">Standard</span><span class="sxs-lookup"><span data-stu-id="475f8-129">Standard</span></span>
- <span data-ttu-id="475f8-130">WAF</span><span class="sxs-lookup"><span data-stu-id="475f8-130">WAF</span></span>

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

### <span data-ttu-id="475f8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475f8-131">CommonParameters</span></span>
<span data-ttu-id="475f8-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475f8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475f8-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475f8-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475f8-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="475f8-134">INPUTS</span></span>

### <span data-ttu-id="475f8-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="475f8-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="475f8-136">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="475f8-136">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="475f8-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="475f8-137">OUTPUTS</span></span>

### <span data-ttu-id="475f8-138">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="475f8-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="475f8-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="475f8-139">NOTES</span></span>

## <span data-ttu-id="475f8-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="475f8-140">RELATED LINKS</span></span>

[<span data-ttu-id="475f8-141">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="475f8-141">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="475f8-142">Nowe — AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="475f8-142">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


