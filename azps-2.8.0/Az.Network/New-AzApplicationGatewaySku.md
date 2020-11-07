---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaysku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewaySku.md
ms.openlocfilehash: 1d737733deb167510196555af4ad7b357cc60154
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869984"
---
# <span data-ttu-id="753b0-101">New-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="753b0-101">New-AzApplicationGatewaySku</span></span>

## <span data-ttu-id="753b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="753b0-102">SYNOPSIS</span></span>
<span data-ttu-id="753b0-103">Tworzy jednostkę SKU dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="753b0-103">Creates a SKU for an application gateway.</span></span>

## <span data-ttu-id="753b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="753b0-104">SYNTAX</span></span>

```
New-AzApplicationGatewaySku -Name <String> -Tier <String> [-Capacity <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="753b0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="753b0-105">DESCRIPTION</span></span>
<span data-ttu-id="753b0-106">Polecenie cmdlet **New-AzApplicationGatewaySku** umożliwia utworzenie jednostki składowania zapasu (SKU) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="753b0-106">The **New-AzApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="753b0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="753b0-107">EXAMPLES</span></span>

### <span data-ttu-id="753b0-108">Przykład 1. Tworzenie jednostki SKU dla bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="753b0-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="753b0-109">To polecenie tworzy jednostkę SKU o nazwie Standard_Small dla bramy aplikacji platformy Azure i zapisuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="753b0-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="753b0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="753b0-110">PARAMETERS</span></span>

### <span data-ttu-id="753b0-111">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="753b0-111">-Capacity</span></span>
<span data-ttu-id="753b0-112">Określa liczbę wystąpień bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="753b0-112">Specifies the number of instances of an application gateway.</span></span>

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

### <span data-ttu-id="753b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753b0-113">-DefaultProfile</span></span>
<span data-ttu-id="753b0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="753b0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="753b0-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="753b0-115">-Name</span></span>
<span data-ttu-id="753b0-116">Określa nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="753b0-116">Specifies the name of the SKU.</span></span>
<span data-ttu-id="753b0-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="753b0-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="753b0-118">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="753b0-118">Standard_Small</span></span>
- <span data-ttu-id="753b0-119">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="753b0-119">Standard_Medium</span></span>
- <span data-ttu-id="753b0-120">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="753b0-120">Standard_Large</span></span>
- <span data-ttu-id="753b0-121">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="753b0-121">WAF_Medium</span></span>
- <span data-ttu-id="753b0-122">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="753b0-122">WAF_Large</span></span>

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

### <span data-ttu-id="753b0-123">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="753b0-123">-Tier</span></span>
<span data-ttu-id="753b0-124">Określa poziom jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="753b0-124">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="753b0-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="753b0-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="753b0-126">Standard</span><span class="sxs-lookup"><span data-stu-id="753b0-126">Standard</span></span>
- <span data-ttu-id="753b0-127">WAF</span><span class="sxs-lookup"><span data-stu-id="753b0-127">WAF</span></span>

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

### <span data-ttu-id="753b0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753b0-128">CommonParameters</span></span>
<span data-ttu-id="753b0-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753b0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753b0-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="753b0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753b0-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="753b0-131">INPUTS</span></span>

### <span data-ttu-id="753b0-132">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="753b0-132">None</span></span>

## <span data-ttu-id="753b0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="753b0-133">OUTPUTS</span></span>

### <span data-ttu-id="753b0-134">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="753b0-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="753b0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="753b0-135">NOTES</span></span>

## <span data-ttu-id="753b0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="753b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="753b0-137">Get-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="753b0-137">Get-AzApplicationGatewaySku</span></span>](./Get-AzApplicationGatewaySku.md)

[<span data-ttu-id="753b0-138">Set-AzApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="753b0-138">Set-AzApplicationGatewaySku</span></span>](./Set-AzApplicationGatewaySku.md)


