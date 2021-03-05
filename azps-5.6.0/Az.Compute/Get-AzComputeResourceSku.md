---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983754"
---
# <span data-ttu-id="2f6e5-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="2f6e5-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="2f6e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f6e5-102">SYNOPSIS</span></span>
<span data-ttu-id="2f6e5-103">Lista wszystkich jednostki SKU zasobu obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="2f6e5-103">List all compute resource Skus</span></span>

## <span data-ttu-id="2f6e5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f6e5-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f6e5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f6e5-105">DESCRIPTION</span></span>
<span data-ttu-id="2f6e5-106">Lista wszystkich jednostki SKU zasobu obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="2f6e5-106">List all compute resource Skus</span></span>

## <span data-ttu-id="2f6e5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f6e5-107">EXAMPLES</span></span>

### <span data-ttu-id="2f6e5-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2f6e5-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="2f6e5-109">Lista wszystkich jednostki SKU zasobów obliczeniowych w regionie Stanów Zjednoczonych Zachód</span><span class="sxs-lookup"><span data-stu-id="2f6e5-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="2f6e5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f6e5-110">PARAMETERS</span></span>

### <span data-ttu-id="2f6e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f6e5-111">-DefaultProfile</span></span>
<span data-ttu-id="2f6e5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2f6e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f6e5-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f6e5-113">-Location</span></span>
<span data-ttu-id="2f6e5-114">Określa lokalizację dostępnych jednostki SKU do listy.</span><span class="sxs-lookup"><span data-stu-id="2f6e5-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f6e5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f6e5-115">CommonParameters</span></span>
<span data-ttu-id="2f6e5-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f6e5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f6e5-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f6e5-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f6e5-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f6e5-118">INPUTS</span></span>

### <span data-ttu-id="2f6e5-119">System.String</span><span class="sxs-lookup"><span data-stu-id="2f6e5-119">System.String</span></span>

## <span data-ttu-id="2f6e5-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f6e5-120">OUTPUTS</span></span>

### <span data-ttu-id="2f6e5-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="2f6e5-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="2f6e5-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f6e5-122">NOTES</span></span>

## <span data-ttu-id="2f6e5-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f6e5-123">RELATED LINKS</span></span>
