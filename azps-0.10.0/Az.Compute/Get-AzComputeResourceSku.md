---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893822"
---
# <span data-ttu-id="39a6b-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="39a6b-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="39a6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="39a6b-102">SYNOPSIS</span></span>
<span data-ttu-id="39a6b-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="39a6b-103">List all compute resource Skus</span></span>

## <span data-ttu-id="39a6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="39a6b-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="39a6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="39a6b-105">DESCRIPTION</span></span>
<span data-ttu-id="39a6b-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="39a6b-106">List all compute resource Skus</span></span>

## <span data-ttu-id="39a6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="39a6b-107">EXAMPLES</span></span>

### <span data-ttu-id="39a6b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="39a6b-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="39a6b-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="39a6b-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="39a6b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="39a6b-110">PARAMETERS</span></span>

### <span data-ttu-id="39a6b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39a6b-111">-DefaultProfile</span></span>
<span data-ttu-id="39a6b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="39a6b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39a6b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39a6b-113">CommonParameters</span></span>
<span data-ttu-id="39a6b-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39a6b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39a6b-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39a6b-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39a6b-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="39a6b-116">INPUTS</span></span>

### <span data-ttu-id="39a6b-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="39a6b-117">None</span></span>

## <span data-ttu-id="39a6b-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="39a6b-118">OUTPUTS</span></span>

### <span data-ttu-id="39a6b-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="39a6b-119">System.Object</span></span>

## <span data-ttu-id="39a6b-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="39a6b-120">NOTES</span></span>

## <span data-ttu-id="39a6b-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="39a6b-121">RELATED LINKS</span></span>

