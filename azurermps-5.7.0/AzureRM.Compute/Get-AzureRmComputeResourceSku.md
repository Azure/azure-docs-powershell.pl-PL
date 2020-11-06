---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526990"
---
# <span data-ttu-id="2b47b-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="2b47b-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="2b47b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b47b-102">SYNOPSIS</span></span>
<span data-ttu-id="2b47b-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="2b47b-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b47b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b47b-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="2b47b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b47b-105">DESCRIPTION</span></span>
<span data-ttu-id="2b47b-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="2b47b-106">List all compute resource Skus</span></span>

## <span data-ttu-id="2b47b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b47b-107">EXAMPLES</span></span>

### <span data-ttu-id="2b47b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b47b-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="2b47b-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="2b47b-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="2b47b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b47b-110">PARAMETERS</span></span>

### <span data-ttu-id="2b47b-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b47b-111">CommonParameters</span></span>
<span data-ttu-id="2b47b-112">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b47b-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b47b-113">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b47b-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b47b-114">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b47b-114">INPUTS</span></span>

### <span data-ttu-id="2b47b-115">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2b47b-115">None</span></span>


## <span data-ttu-id="2b47b-116">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b47b-116">OUTPUTS</span></span>

### <span data-ttu-id="2b47b-117">System. Object</span><span class="sxs-lookup"><span data-stu-id="2b47b-117">System.Object</span></span>

## <span data-ttu-id="2b47b-118">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b47b-118">NOTES</span></span>

## <span data-ttu-id="2b47b-119">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b47b-119">RELATED LINKS</span></span>

