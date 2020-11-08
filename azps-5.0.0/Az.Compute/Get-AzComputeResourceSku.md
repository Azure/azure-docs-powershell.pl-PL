---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94224592"
---
# <span data-ttu-id="d9ac9-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="d9ac9-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="d9ac9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d9ac9-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ac9-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="d9ac9-103">List all compute resource Skus</span></span>

## <span data-ttu-id="d9ac9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d9ac9-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9ac9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d9ac9-105">DESCRIPTION</span></span>
<span data-ttu-id="d9ac9-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="d9ac9-106">List all compute resource Skus</span></span>

## <span data-ttu-id="d9ac9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d9ac9-107">EXAMPLES</span></span>

### <span data-ttu-id="d9ac9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d9ac9-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="d9ac9-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="d9ac9-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="d9ac9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d9ac9-110">PARAMETERS</span></span>

### <span data-ttu-id="d9ac9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ac9-111">-DefaultProfile</span></span>
<span data-ttu-id="d9ac9-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9ac9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9ac9-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9ac9-113">-Location</span></span>
<span data-ttu-id="d9ac9-114">Określa lokalizację dostępnych jednostek SKU do wylistowania.</span><span class="sxs-lookup"><span data-stu-id="d9ac9-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="d9ac9-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ac9-115">CommonParameters</span></span>
<span data-ttu-id="d9ac9-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9ac9-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ac9-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9ac9-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ac9-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9ac9-118">INPUTS</span></span>

### <span data-ttu-id="d9ac9-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d9ac9-119">System.String</span></span>

## <span data-ttu-id="d9ac9-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d9ac9-120">OUTPUTS</span></span>

### <span data-ttu-id="d9ac9-121">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="d9ac9-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="d9ac9-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d9ac9-122">NOTES</span></span>

## <span data-ttu-id="d9ac9-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9ac9-123">RELATED LINKS</span></span>
