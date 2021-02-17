---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239349"
---
# <span data-ttu-id="d9b8a-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="d9b8a-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="d9b8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9b8a-102">SYNOPSIS</span></span>
<span data-ttu-id="d9b8a-103">Pobiera przydziały usługi wsadowej dla subskrypcji w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="d9b8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9b8a-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9b8a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9b8a-105">DESCRIPTION</span></span>
<span data-ttu-id="d9b8a-106">Pobiera przydziały usługi wsadowej dla określonej subskrypcji w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="d9b8a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9b8a-107">EXAMPLES</span></span>

### <span data-ttu-id="d9b8a-108">Przykład 1. Uzyskiwanie przydziałów usługi wsadowej dla subskrypcji w regionie Zachód Stanów Zjednoczonych</span><span class="sxs-lookup"><span data-stu-id="d9b8a-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="d9b8a-109">To polecenie pobiera przydziały dla bieżącej subskrypcji w regionie Zachód Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="d9b8a-110">Zwracana wartość wskazuje, że ta subskrypcja może utworzyć tylko jedno konto wsadowe w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="d9b8a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9b8a-111">PARAMETERS</span></span>

### <span data-ttu-id="d9b8a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9b8a-112">-DefaultProfile</span></span>
<span data-ttu-id="d9b8a-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d9b8a-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d9b8a-114">-Location</span></span>
<span data-ttu-id="d9b8a-115">Określa region, dla którego to polecenie cmdlet sprawdza przydziały.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="d9b8a-116">Aby uzyskać więcej informacji, zobacz Regiony platformy Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="d9b8a-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="d9b8a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9b8a-117">CommonParameters</span></span>
<span data-ttu-id="d9b8a-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9b8a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9b8a-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9b8a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9b8a-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9b8a-120">INPUTS</span></span>

### <span data-ttu-id="d9b8a-121">System.String</span><span class="sxs-lookup"><span data-stu-id="d9b8a-121">System.String</span></span>

## <span data-ttu-id="d9b8a-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9b8a-122">OUTPUTS</span></span>

### <span data-ttu-id="d9b8a-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="d9b8a-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="d9b8a-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9b8a-124">NOTES</span></span>

## <span data-ttu-id="d9b8a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9b8a-125">RELATED LINKS</span></span>
