---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 48C33FAF-83C1-4725-AD2A-CF48D0718182
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewaySku.md
ms.openlocfilehash: eb1f0dadd905ff4b57a58c46f763f3c2dd51f256
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551811"
---
# <span data-ttu-id="d2056-101">New-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d2056-101">New-AzureRmApplicationGatewaySku</span></span>

## <span data-ttu-id="d2056-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d2056-102">SYNOPSIS</span></span>
<span data-ttu-id="d2056-103">Tworzy jednostkę SKU dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d2056-103">Creates a SKU for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2056-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d2056-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewaySku -Name <String> -Tier <String> -Capacity <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2056-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d2056-105">DESCRIPTION</span></span>
<span data-ttu-id="d2056-106">Polecenie cmdlet **New-AzureRmApplicationGatewaySku** umożliwia utworzenie jednostki składowania zapasu (SKU) dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d2056-106">The **New-AzureRmApplicationGatewaySku** cmdlet creates a stock keeping unit (SKU) for an Azure application gateway.</span></span>

## <span data-ttu-id="d2056-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d2056-107">EXAMPLES</span></span>

### <span data-ttu-id="d2056-108">Przykład 1. Tworzenie jednostki SKU dla bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="d2056-108">Example 1: Create a SKU for an Azure application gateway</span></span>
```
PS C:\>$SKU = New-AzureRmApplicationGatewaySku -Name "Standard_Small" -Tier "Standard" -Capacity 2
```

<span data-ttu-id="d2056-109">To polecenie tworzy jednostkę SKU o nazwie Standard_Small dla bramy aplikacji platformy Azure i zapisuje wynik w zmiennej o nazwie $SKU.</span><span class="sxs-lookup"><span data-stu-id="d2056-109">This command creates a SKU named Standard_Small for an Azure application gateway and stores the result in the variable named $SKU.</span></span>

## <span data-ttu-id="d2056-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d2056-110">PARAMETERS</span></span>

### <span data-ttu-id="d2056-111">-Pojemność</span><span class="sxs-lookup"><span data-stu-id="d2056-111">-Capacity</span></span>
<span data-ttu-id="d2056-112">Określa liczbę wystąpień bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="d2056-112">Specifies the number of instances of an application gateway.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2056-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d2056-113">-Name</span></span>
<span data-ttu-id="d2056-114">Określa nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="d2056-114">Specifies the name of the SKU.</span></span>

<span data-ttu-id="d2056-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2056-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2056-116">Standard_Small</span><span class="sxs-lookup"><span data-stu-id="d2056-116">Standard_Small</span></span>
- <span data-ttu-id="d2056-117">Standard_Medium</span><span class="sxs-lookup"><span data-stu-id="d2056-117">Standard_Medium</span></span>
- <span data-ttu-id="d2056-118">Standard_Large</span><span class="sxs-lookup"><span data-stu-id="d2056-118">Standard_Large</span></span>
- <span data-ttu-id="d2056-119">WAF_Medium</span><span class="sxs-lookup"><span data-stu-id="d2056-119">WAF_Medium</span></span>
- <span data-ttu-id="d2056-120">WAF_Large</span><span class="sxs-lookup"><span data-stu-id="d2056-120">WAF_Large</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard_Small, Standard_Medium, Standard_Large, WAF_Medium, WAF_Large

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2056-121">-Warstwowy</span><span class="sxs-lookup"><span data-stu-id="d2056-121">-Tier</span></span>
<span data-ttu-id="d2056-122">Określa poziom jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="d2056-122">Specifies the tier of the SKU.</span></span>
<span data-ttu-id="d2056-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d2056-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d2056-124">Standard</span><span class="sxs-lookup"><span data-stu-id="d2056-124">Standard</span></span>
- <span data-ttu-id="d2056-125">WAF</span><span class="sxs-lookup"><span data-stu-id="d2056-125">WAF</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, WAF

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2056-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2056-126">-DefaultProfile</span></span>
<span data-ttu-id="d2056-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d2056-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2056-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2056-128">CommonParameters</span></span>
<span data-ttu-id="d2056-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2056-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2056-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2056-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2056-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d2056-131">INPUTS</span></span>

### <span data-ttu-id="d2056-132">System. String</span><span class="sxs-lookup"><span data-stu-id="d2056-132">System.String</span></span>

## <span data-ttu-id="d2056-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d2056-133">OUTPUTS</span></span>

### <span data-ttu-id="d2056-134">Microsoft. Azure. Commands. Network. models. PSApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d2056-134">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewaySku</span></span>

## <span data-ttu-id="d2056-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d2056-135">NOTES</span></span>

## <span data-ttu-id="d2056-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d2056-136">RELATED LINKS</span></span>

[<span data-ttu-id="d2056-137">Get-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d2056-137">Get-AzureRmApplicationGatewaySku</span></span>](./Get-AzureRmApplicationGatewaySku.md)

[<span data-ttu-id="d2056-138">Set-AzureRmApplicationGatewaySku</span><span class="sxs-lookup"><span data-stu-id="d2056-138">Set-AzureRmApplicationGatewaySku</span></span>](./Set-AzureRmApplicationGatewaySku.md)


