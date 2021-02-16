---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195058"
---
# <span data-ttu-id="3496c-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="3496c-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="3496c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3496c-102">SYNOPSIS</span></span>
<span data-ttu-id="3496c-103">Lista wszystkich jednostki SKU zasobu obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="3496c-103">List all compute resource Skus</span></span>

## <span data-ttu-id="3496c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="3496c-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3496c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="3496c-105">DESCRIPTION</span></span>
<span data-ttu-id="3496c-106">Lista wszystkich jednostki SKU zasobu obliczeniowego</span><span class="sxs-lookup"><span data-stu-id="3496c-106">List all compute resource Skus</span></span>

## <span data-ttu-id="3496c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="3496c-107">EXAMPLES</span></span>

### <span data-ttu-id="3496c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3496c-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="3496c-109">Lista wszystkich jednostki SKU zasobów obliczeniowych w regionie Stanów Zjednoczonych Zachód</span><span class="sxs-lookup"><span data-stu-id="3496c-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="3496c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3496c-110">PARAMETERS</span></span>

### <span data-ttu-id="3496c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3496c-111">-DefaultProfile</span></span>
<span data-ttu-id="3496c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="3496c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3496c-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3496c-113">-Location</span></span>
<span data-ttu-id="3496c-114">Określa lokalizację dostępnych jednostki SKU do listy.</span><span class="sxs-lookup"><span data-stu-id="3496c-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="3496c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3496c-115">CommonParameters</span></span>
<span data-ttu-id="3496c-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3496c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3496c-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3496c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3496c-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3496c-118">INPUTS</span></span>

### <span data-ttu-id="3496c-119">System.String</span><span class="sxs-lookup"><span data-stu-id="3496c-119">System.String</span></span>

## <span data-ttu-id="3496c-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3496c-120">OUTPUTS</span></span>

### <span data-ttu-id="3496c-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="3496c-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="3496c-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="3496c-122">NOTES</span></span>

## <span data-ttu-id="3496c-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3496c-123">RELATED LINKS</span></span>
