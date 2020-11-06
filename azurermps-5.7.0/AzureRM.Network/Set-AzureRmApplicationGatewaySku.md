---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3D88F561-7FE4-4017-BAC4-8F085AD037A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: 0d4e1977e0985dbe82731376bd78547ce21251e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550619"
---
# <span data-ttu-id="e448f-101">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e448f-101">Set-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="e448f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e448f-102">SYNOPSIS</span></span>
<span data-ttu-id="e448f-103">Modyfikuje jednostkę SKU bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e448f-103">Modifies the SKU of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e448f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e448f-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewaySku -ApplicationGateway <PSApplicationGateway> -Name <String> -Tier <String>
 -Capacity <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e448f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e448f-105">DESCRIPTION</span></span>
<span data-ttu-id="e448f-106">Polecenie cmdlet **Set-AzureRmApplicationGatewaySku** modyfikuje jednostkę składowania zapasu (SKU) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e448f-106">The **Set-AzureRmApplicationGatewaySku** cmdlet modifies the stock keeping unit (SKU) of an application gateway.</span></span>

## <span data-ttu-id="e448f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e448f-107">EXAMPLES</span></span>

### <span data-ttu-id="e448f-108">Przykład 1: Aktualizowanie wersji SKU bramy Application Gateway</span><span class="sxs-lookup"><span data-stu-id="e448f-108">Example 1: Update the application gateway SKU</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewaySku -ApplicationGateway $AppGw -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="e448f-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="e448f-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="e448f-110">Drugie polecenie aktualizuje jednostkę SKU bramy Application.</span><span class="sxs-lookup"><span data-stu-id="e448f-110">The second command updates the SKU of the application gateway.</span></span>

## <span data-ttu-id="e448f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e448f-111">PARAMETERS</span></span>

### <span data-ttu-id="e448f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e448f-112">-ApplicationGateway</span></span>
<span data-ttu-id="e448f-113">Określa obiekt bramy aplikacji, z którym ten polecenie cmdlet kojarzy jednostkę SKU.</span><span class="sxs-lookup"><span data-stu-id="e448f-113">Specifies the application gateway object with which this cmdlet associates the SKU.</span></span>

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

### <span data-ttu-id="e448f-114">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="e448f-114">-Capacity</span></span>
<span data-ttu-id="e448f-115">Określa liczbę wystąpień bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="e448f-115">Specifies the instance count of the application gateway.</span></span>

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

### <span data-ttu-id="e448f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e448f-116">-DefaultProfile</span></span>
<span data-ttu-id="e448f-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e448f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e448f-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e448f-118">-Name</span></span>
<span data-ttu-id="e448f-119">Określa nazwę bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e448f-119">Specifies the name of the application gateway.</span></span>
<span data-ttu-id="e448f-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e448f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e448f-121">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="e448f-121">Standard_Small</span></span>
- <span data-ttu-id="e448f-122">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="e448f-122">Standard_Medium</span></span>
- <span data-ttu-id="e448f-123">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="e448f-123">Standard_Large</span></span>
- <span data-ttu-id="e448f-124">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="e448f-124">WAF_Medium</span></span>
- <span data-ttu-id="e448f-125">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="e448f-125">WAF_Large</span></span>

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

### <span data-ttu-id="e448f-126">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="e448f-126">-Tier</span></span>
<span data-ttu-id="e448f-127">Określa poziom bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="e448f-127">Specifies the tier of the application gateway.</span></span>
<span data-ttu-id="e448f-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e448f-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e448f-129">Standard</span><span class="sxs-lookup"><span data-stu-id="e448f-129">Standard</span></span>
- <span data-ttu-id="e448f-130">WAF</span><span class="sxs-lookup"><span data-stu-id="e448f-130">WAF</span></span>

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

### <span data-ttu-id="e448f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e448f-131">CommonParameters</span></span>
<span data-ttu-id="e448f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e448f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e448f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e448f-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e448f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e448f-134">INPUTS</span></span>

### <span data-ttu-id="e448f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e448f-135">System.String</span></span>

## <span data-ttu-id="e448f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e448f-136">OUTPUTS</span></span>

### <span data-ttu-id="e448f-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e448f-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e448f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e448f-138">NOTES</span></span>

## <span data-ttu-id="e448f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e448f-139">RELATED LINKS</span></span>

[<span data-ttu-id="e448f-140">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e448f-140">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="e448f-141">Nowe — AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="e448f-141">New-AzureRmApplicationGatewaySku</span></span>](./New-AzureRmApplicationGatewaySku.md)


