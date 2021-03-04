---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 297b862cb9491c0659d5fd2ec5ab0da4fc071e4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959009"
---
# <span data-ttu-id="c6152-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="c6152-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="c6152-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6152-102">SYNOPSIS</span></span>
<span data-ttu-id="c6152-103">Pobiera przydziały usługi wsadowej dla subskrypcji w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c6152-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="c6152-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c6152-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6152-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c6152-105">DESCRIPTION</span></span>
<span data-ttu-id="c6152-106">Pobiera przydziały usługi wsadowej dla określonej subskrypcji w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c6152-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="c6152-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c6152-107">EXAMPLES</span></span>

### <span data-ttu-id="c6152-108">Przykład 1. Uzyskiwanie przydziałów usługi wsadowej dla subskrypcji w regionie Zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="c6152-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="c6152-109">To polecenie pobiera przydziały dla bieżącej subskrypcji w regionie Zachód Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="c6152-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="c6152-110">Zwracana wartość wskazuje, że ta subskrypcja może utworzyć tylko jedno konto wsadowe w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="c6152-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="c6152-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6152-111">PARAMETERS</span></span>

### <span data-ttu-id="c6152-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6152-112">-DefaultProfile</span></span>
<span data-ttu-id="c6152-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6152-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6152-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c6152-114">-Location</span></span>
<span data-ttu-id="c6152-115">Określa region, dla którego to polecenie cmdlet sprawdza przydziały.</span><span class="sxs-lookup"><span data-stu-id="c6152-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="c6152-116">Aby uzyskać więcej informacji, zobacz Regiony platformy Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="c6152-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6152-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6152-117">CommonParameters</span></span>
<span data-ttu-id="c6152-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6152-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6152-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6152-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6152-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6152-120">INPUTS</span></span>

### <span data-ttu-id="c6152-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c6152-121">System.String</span></span>

## <span data-ttu-id="c6152-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6152-122">OUTPUTS</span></span>

### <span data-ttu-id="c6152-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="c6152-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="c6152-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c6152-124">NOTES</span></span>

## <span data-ttu-id="c6152-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6152-125">RELATED LINKS</span></span>
