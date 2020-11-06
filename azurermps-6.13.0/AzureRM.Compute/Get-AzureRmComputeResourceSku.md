---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: cf10674f3140e618b82b40e6c8288126cb941c3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541900"
---
# <span data-ttu-id="b3cc0-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="b3cc0-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="b3cc0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3cc0-102">SYNOPSIS</span></span>
<span data-ttu-id="b3cc0-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="b3cc0-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3cc0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3cc0-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3cc0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b3cc0-105">DESCRIPTION</span></span>
<span data-ttu-id="b3cc0-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="b3cc0-106">List all compute resource Skus</span></span>

## <span data-ttu-id="b3cc0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3cc0-107">EXAMPLES</span></span>

### <span data-ttu-id="b3cc0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b3cc0-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="b3cc0-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="b3cc0-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="b3cc0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3cc0-110">PARAMETERS</span></span>

### <span data-ttu-id="b3cc0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3cc0-111">-DefaultProfile</span></span>
<span data-ttu-id="b3cc0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3cc0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3cc0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3cc0-113">CommonParameters</span></span>
<span data-ttu-id="b3cc0-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3cc0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3cc0-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3cc0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3cc0-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3cc0-116">INPUTS</span></span>

### <span data-ttu-id="b3cc0-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b3cc0-117">None</span></span>

## <span data-ttu-id="b3cc0-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3cc0-118">OUTPUTS</span></span>

### <span data-ttu-id="b3cc0-119">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="b3cc0-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="b3cc0-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3cc0-120">NOTES</span></span>

## <span data-ttu-id="b3cc0-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3cc0-121">RELATED LINKS</span></span>
