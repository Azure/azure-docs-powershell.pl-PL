---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3702701E-428D-47E2-A227-0F38B055F881
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMUsage.md
ms.openlocfilehash: d22e36ad3cc4737be9c73d6b7cdc49329f904263
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200674"
---
# <span data-ttu-id="79bf5-101">Get-AzVMUsage</span><span class="sxs-lookup"><span data-stu-id="79bf5-101">Get-AzVMUsage</span></span>

## <span data-ttu-id="79bf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79bf5-102">SYNOPSIS</span></span>
<span data-ttu-id="79bf5-103">Pobiera użycie podstawowej liczby maszyn wirtualnych dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="79bf5-103">Gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="79bf5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79bf5-104">SYNTAX</span></span>

```
Get-AzVMUsage [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79bf5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="79bf5-105">DESCRIPTION</span></span>
<span data-ttu-id="79bf5-106">Polecenie **cmdlet Get-AzVMUsage** pobiera użycie podstawowej liczby maszyn wirtualnych dla lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="79bf5-106">The **Get-AzVMUsage** cmdlet gets the virtual machine core count usage for a location.</span></span>

## <span data-ttu-id="79bf5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79bf5-107">EXAMPLES</span></span>

### <span data-ttu-id="79bf5-108">Przykład 1. Uzyskiwanie użycia liczby podstawowych danych w lokalizacji</span><span class="sxs-lookup"><span data-stu-id="79bf5-108">Example 1: Get core count usage for a location</span></span>
```
PS C:\> Get-AzVMUsage -Location "Central US"
```

<span data-ttu-id="79bf5-109">To polecenie pobiera użycie podstawowej liczby maszyn wirtualnych dla lokalizacji w Centrum USA.</span><span class="sxs-lookup"><span data-stu-id="79bf5-109">This command gets the virtual machine core count usage for the location Central US.</span></span>

## <span data-ttu-id="79bf5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79bf5-110">PARAMETERS</span></span>

### <span data-ttu-id="79bf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bf5-111">-DefaultProfile</span></span>
<span data-ttu-id="79bf5-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79bf5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79bf5-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="79bf5-113">-Location</span></span>
<span data-ttu-id="79bf5-114">Określa lokalizację, w której to polecenie cmdlet uzyskuje użycie podstawowej liczby maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="79bf5-114">Specifies the location for which this cmdlet gets virtual machine core count usage.</span></span>

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

### <span data-ttu-id="79bf5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bf5-115">CommonParameters</span></span>
<span data-ttu-id="79bf5-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79bf5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bf5-117">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79bf5-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bf5-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79bf5-118">INPUTS</span></span>

### <span data-ttu-id="79bf5-119">System.String</span><span class="sxs-lookup"><span data-stu-id="79bf5-119">System.String</span></span>

## <span data-ttu-id="79bf5-120">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79bf5-120">OUTPUTS</span></span>

### <span data-ttu-id="79bf5-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span><span class="sxs-lookup"><span data-stu-id="79bf5-121">Microsoft.Azure.Commands.Compute.Models.PSUsage</span></span>

## <span data-ttu-id="79bf5-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79bf5-122">NOTES</span></span>

## <span data-ttu-id="79bf5-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79bf5-123">RELATED LINKS</span></span>

[<span data-ttu-id="79bf5-124">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="79bf5-124">Get-AzVM</span></span>](./Get-AzVM.md)


