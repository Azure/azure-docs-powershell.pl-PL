---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553376"
---
# <span data-ttu-id="2fce2-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="2fce2-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="2fce2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fce2-102">SYNOPSIS</span></span>
<span data-ttu-id="2fce2-103">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="2fce2-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fce2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fce2-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fce2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2fce2-105">DESCRIPTION</span></span>
<span data-ttu-id="2fce2-106">Lista wszystkich jednostek SKU zasobu COMPUTE</span><span class="sxs-lookup"><span data-stu-id="2fce2-106">List all compute resource Skus</span></span>

## <span data-ttu-id="2fce2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fce2-107">EXAMPLES</span></span>

### <span data-ttu-id="2fce2-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2fce2-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="2fce2-109">Lista wszystkich jednostek obliczeniowych zasobów w regionie zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="2fce2-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="2fce2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fce2-110">PARAMETERS</span></span>

### <span data-ttu-id="2fce2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fce2-111">-DefaultProfile</span></span>
<span data-ttu-id="2fce2-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2fce2-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fce2-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fce2-113">CommonParameters</span></span>
<span data-ttu-id="2fce2-114">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fce2-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fce2-115">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fce2-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fce2-116">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fce2-116">INPUTS</span></span>

### <span data-ttu-id="2fce2-117">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2fce2-117">None</span></span>

## <span data-ttu-id="2fce2-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fce2-118">OUTPUTS</span></span>

### <span data-ttu-id="2fce2-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="2fce2-119">System.Object</span></span>

## <span data-ttu-id="2fce2-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fce2-120">NOTES</span></span>

## <span data-ttu-id="2fce2-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fce2-121">RELATED LINKS</span></span>

