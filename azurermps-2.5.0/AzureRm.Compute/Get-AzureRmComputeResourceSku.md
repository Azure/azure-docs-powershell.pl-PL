---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899388"
---
# <span data-ttu-id="20d67-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="20d67-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="20d67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20d67-102">SYNOPSIS</span></span>
<span data-ttu-id="20d67-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="20d67-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20d67-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20d67-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20d67-105">Opis</span><span class="sxs-lookup"><span data-stu-id="20d67-105">DESCRIPTION</span></span>
<span data-ttu-id="20d67-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="20d67-106">List all compute resource Skus</span></span>

## <span data-ttu-id="20d67-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20d67-107">EXAMPLES</span></span>

### <span data-ttu-id="20d67-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="20d67-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="20d67-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="20d67-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="20d67-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20d67-110">PARAMETERS</span></span>

### <span data-ttu-id="20d67-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20d67-111">-DefaultProfile</span></span>
<span data-ttu-id="20d67-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20d67-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20d67-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d67-113">CommonParameters</span></span>
<span data-ttu-id="20d67-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d67-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d67-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d67-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d67-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20d67-116">INPUTS</span></span>

### <span data-ttu-id="20d67-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="20d67-117">None</span></span>

## <span data-ttu-id="20d67-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20d67-118">OUTPUTS</span></span>

### <span data-ttu-id="20d67-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="20d67-119">System.Object</span></span>

## <span data-ttu-id="20d67-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20d67-120">NOTES</span></span>

## <span data-ttu-id="20d67-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20d67-121">RELATED LINKS</span></span>

