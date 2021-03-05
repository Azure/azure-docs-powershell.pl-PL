---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: ef13cdfc9a137790c0d9aa842a0ba31841baa99b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013729"
---
# <span data-ttu-id="8383c-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="8383c-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="8383c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8383c-102">SYNOPSIS</span></span>
<span data-ttu-id="8383c-103">Pobiera użycie podstawowej liczby maszyn wirtualnych dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8383c-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="8383c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8383c-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8383c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8383c-105">DESCRIPTION</span></span>
<span data-ttu-id="8383c-106">Polecenie **cmdlet Get-AzVMUsage** pobiera użycie podstawowej liczby maszyn wirtualnych dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8383c-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="8383c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8383c-107">EXAMPLES</span></span>

### <span data-ttu-id="8383c-108">Przykład 1. Uzyskiwanie użycia liczby podstawowych danych w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="8383c-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="8383c-109">To polecenie pobiera użycie podstawowej liczby maszyn wirtualnych dla lokalizacji w Centrum USA.</span><span class="sxs-lookup"><span data-stu-id="8383c-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="8383c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8383c-110">PARAMETERS</span></span>

### <span data-ttu-id="8383c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8383c-111">-DefaultProfile</span></span>
<span data-ttu-id="8383c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8383c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8383c-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8383c-113">-Location</span></span>
<span data-ttu-id="8383c-114">Określa lokalizację, w której to polecenie cmdlet uzyskuje użycie podstawowej liczby maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="8383c-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="8383c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8383c-115">CommonParameters</span></span>
<span data-ttu-id="8383c-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8383c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8383c-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8383c-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8383c-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8383c-118">INPUTS</span></span>

### <span data-ttu-id="8383c-119">System.String</span><span class="sxs-lookup"><span data-stu-id="8383c-119">System.String</span></span>

## <span data-ttu-id="8383c-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8383c-120">OUTPUTS</span></span>

### <span data-ttu-id="8383c-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="8383c-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="8383c-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8383c-122">NOTES</span></span>

## <span data-ttu-id="8383c-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8383c-123">RELATED LINKS</span></span>

[<span data-ttu-id="8383c-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8383c-124">Get-AzVM</span></span>](./Get-AzVM.md)


