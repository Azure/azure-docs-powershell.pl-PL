---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706448"
---
# <span data-ttu-id="3c9ba-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="3c9ba-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="3c9ba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c9ba-102">SYNOPSIS</span></span>
<span data-ttu-id="3c9ba-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="3c9ba-103">List all compute resource Skus</span></span>

## <span data-ttu-id="3c9ba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c9ba-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c9ba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c9ba-105">DESCRIPTION</span></span>
<span data-ttu-id="3c9ba-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="3c9ba-106">List all compute resource Skus</span></span>

## <span data-ttu-id="3c9ba-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c9ba-107">EXAMPLES</span></span>

### <span data-ttu-id="3c9ba-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c9ba-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="3c9ba-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="3c9ba-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="3c9ba-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c9ba-110">PARAMETERS</span></span>

### <span data-ttu-id="3c9ba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c9ba-111">-DefaultProfile</span></span>
<span data-ttu-id="3c9ba-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c9ba-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c9ba-113">CommonParameters</span></span>
<span data-ttu-id="3c9ba-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c9ba-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c9ba-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c9ba-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c9ba-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c9ba-116">INPUTS</span></span>

### <span data-ttu-id="3c9ba-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3c9ba-117">None</span></span>

## <span data-ttu-id="3c9ba-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c9ba-118">OUTPUTS</span></span>

### <span data-ttu-id="3c9ba-119">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="3c9ba-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="3c9ba-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c9ba-120">NOTES</span></span>

## <span data-ttu-id="3c9ba-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c9ba-121">RELATED LINKS</span></span>
