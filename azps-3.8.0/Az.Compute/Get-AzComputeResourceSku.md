---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052657"
---
# <span data-ttu-id="8ef27-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="8ef27-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="8ef27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ef27-102">SYNOPSIS</span></span>
<span data-ttu-id="8ef27-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="8ef27-103">List all compute resource Skus</span></span>

## <span data-ttu-id="8ef27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ef27-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ef27-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8ef27-105">DESCRIPTION</span></span>
<span data-ttu-id="8ef27-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="8ef27-106">List all compute resource Skus</span></span>

## <span data-ttu-id="8ef27-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ef27-107">EXAMPLES</span></span>

### <span data-ttu-id="8ef27-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8ef27-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="8ef27-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="8ef27-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="8ef27-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ef27-110">PARAMETERS</span></span>

### <span data-ttu-id="8ef27-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ef27-111">-DefaultProfile</span></span>
<span data-ttu-id="8ef27-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ef27-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ef27-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ef27-113">CommonParameters</span></span>
<span data-ttu-id="8ef27-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ef27-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ef27-115">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ef27-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ef27-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ef27-116">INPUTS</span></span>

### <span data-ttu-id="8ef27-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8ef27-117">None</span></span>

## <span data-ttu-id="8ef27-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ef27-118">OUTPUTS</span></span>

### <span data-ttu-id="8ef27-119">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="8ef27-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="8ef27-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ef27-120">NOTES</span></span>

## <span data-ttu-id="8ef27-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ef27-121">RELATED LINKS</span></span>
