---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 212ba438a701b9abbd2fd290f4fb0f867b551497
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240874"
---
# <span data-ttu-id="3c685-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3c685-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="3c685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c685-102">SYNOPSIS</span></span>
<span data-ttu-id="3c685-103">Tworzy sku dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3c685-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="3c685-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3c685-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c685-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3c685-105">DESCRIPTION</span></span>
<span data-ttu-id="3c685-106">Polecenie **cmdlet New-AzApplicationGatewaySku** tworzy jednostkę przechowywania akcji (SKU) dla bramy aplikacji azure.</span><span class="sxs-lookup"><span data-stu-id="3c685-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="3c685-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3c685-107">EXAMPLES</span></span>

### <span data-ttu-id="3c685-108">Przykład 1. Tworzenie wersji SKU dla bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3c685-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="3c685-109">To polecenie tworzy sku o nazwie Standard_Small bramy aplikacji Azure i zapisuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="3c685-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="3c685-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c685-110">PARAMETERS</span></span>

### <span data-ttu-id="3c685-111">— Pojemność</span><span class="sxs-lookup"><span data-stu-id="3c685-111">-Capacity</span></span>
<span data-ttu-id="3c685-112">Określa liczbę wystąpień bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3c685-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="3c685-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c685-113">-DefaultProfile</span></span>
<span data-ttu-id="3c685-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c685-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c685-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="3c685-115">-Name</span></span>
<span data-ttu-id="3c685-116">Określa nazwę sku.</span><span class="sxs-lookup"><span data-stu-id="3c685-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="3c685-117">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3c685-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3c685-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="3c685-118">Standard_Small</span></span>
- <span data-ttu-id="3c685-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="3c685-119">Standard_Medium</span></span>
- <span data-ttu-id="3c685-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="3c685-120">Standard_Large</span></span>
- <span data-ttu-id="3c685-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="3c685-121">WAF_Medium</span></span>
- <span data-ttu-id="3c685-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="3c685-122">WAF_Large</span></span>
- <span data-ttu-id="3c685-123">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="3c685-123">Standard_v2</span></span>
- <span data-ttu-id="3c685-124">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3c685-124">WAF_v2</span></span>

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

### <span data-ttu-id="3c685-125">- Warstwa</span><span class="sxs-lookup"><span data-stu-id="3c685-125">-Tier</span></span>
<span data-ttu-id="3c685-126">Określa warstwę sku.</span><span class="sxs-lookup"><span data-stu-id="3c685-126">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="3c685-127">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3c685-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3c685-128">Standardowe</span><span class="sxs-lookup"><span data-stu-id="3c685-128">Standard</span></span>
- <span data-ttu-id="3c685-129">WAF</span><span class="sxs-lookup"><span data-stu-id="3c685-129">WAF</span></span>
- <span data-ttu-id="3c685-130">Standard_v2</span><span class="sxs-lookup"><span data-stu-id="3c685-130">Standard_v2</span></span>
- <span data-ttu-id="3c685-131">WAF_v2</span><span class="sxs-lookup"><span data-stu-id="3c685-131">WAF_v2</span></span>

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

### <span data-ttu-id="3c685-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c685-132">CommonParameters</span></span>
<span data-ttu-id="3c685-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c685-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c685-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c685-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c685-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c685-135">INPUTS</span></span>

### <span data-ttu-id="3c685-136">Brak</span><span class="sxs-lookup"><span data-stu-id="3c685-136">None</span></span>

## <span data-ttu-id="3c685-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c685-137">OUTPUTS</span></span>

### <span data-ttu-id="3c685-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3c685-138">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="3c685-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3c685-139">NOTES</span></span>

## <span data-ttu-id="3c685-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c685-140">RELATED LINKS</span></span>

[<span data-ttu-id="3c685-141">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3c685-141">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="3c685-142">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="3c685-142">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


