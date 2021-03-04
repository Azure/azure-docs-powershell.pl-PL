---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: 7764ee4cd151e3de7cca2af84ed0cf670c52a6a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969290"
---
# <span data-ttu-id="06ec9-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="06ec9-101">Get-AzGallery</span></span>

## <span data-ttu-id="06ec9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="06ec9-103">Pobierz galerie lub wybierz galerie list.</span><span class="sxs-lookup"><span data-stu-id="06ec9-103">Get or list galleries.</span></span>

## <span data-ttu-id="06ec9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06ec9-104">SYNTAX</span></span>

### <span data-ttu-id="06ec9-105">DefaultParameters (domyślny)</span><span class="sxs-lookup"><span data-stu-id="06ec9-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06ec9-106">ResourceIdParameters</span><span class="sxs-lookup"><span data-stu-id="06ec9-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ec9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="06ec9-107">DESCRIPTION</span></span>
<span data-ttu-id="06ec9-108">Pobierz galerie lub wybierz galerie list.</span><span class="sxs-lookup"><span data-stu-id="06ec9-108">Get or list galleries.</span></span>

## <span data-ttu-id="06ec9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06ec9-109">EXAMPLES</span></span>

### <span data-ttu-id="06ec9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06ec9-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="06ec9-111">Uzyskiwanie galerii "galeria1"</span><span class="sxs-lookup"><span data-stu-id="06ec9-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="06ec9-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06ec9-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGallery -ResourceGroupName rg1

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="06ec9-113">Pobierz wszystkie galerie w rg1.</span><span class="sxs-lookup"><span data-stu-id="06ec9-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="06ec9-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="06ec9-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGallery

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="06ec9-115">Pobierz wszystkie galerie w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="06ec9-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="06ec9-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="06ec9-116">Example 4</span></span>
```powershell
PS C:\> Get-AzGallery -Name gallery*

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery1
Name              : gallery1
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg1
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/providers/Microsoft.Compute/galleries/gallery2
Name              : gallery2
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}

ResourceGroupName : rg2
Description       : Gallery created by Powershell.
Identifier        : 
  UniqueName      : 00000000-0000-0000-0000-000000000000-gallery1
ProvisioningState : Succeeded
Id                : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg2/providers/Microsoft.Compute/galleries/gallery3
Name              : gallery3
Type              : Microsoft.Compute/galleries
Location          : southcentralus
Tags              : {}
```

<span data-ttu-id="06ec9-117">Uzyskaj wszystkie galerie w subskrypcji, które zaczynają się od "galerii".</span><span class="sxs-lookup"><span data-stu-id="06ec9-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="06ec9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06ec9-118">PARAMETERS</span></span>

### <span data-ttu-id="06ec9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ec9-119">-DefaultProfile</span></span>
<span data-ttu-id="06ec9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06ec9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="06ec9-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06ec9-121">-Name</span></span>
<span data-ttu-id="06ec9-122">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="06ec9-122">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="06ec9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ec9-123">-ResourceGroupName</span></span>
<span data-ttu-id="06ec9-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="06ec9-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="06ec9-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="06ec9-125">-ResourceId</span></span>
<span data-ttu-id="06ec9-126">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="06ec9-126">The resource id for Gallery</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="06ec9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ec9-127">CommonParameters</span></span>
<span data-ttu-id="06ec9-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ec9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ec9-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06ec9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ec9-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ec9-130">INPUTS</span></span>

### <span data-ttu-id="06ec9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="06ec9-131">System.String</span></span>

## <span data-ttu-id="06ec9-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ec9-132">OUTPUTS</span></span>

### <span data-ttu-id="06ec9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span><span class="sxs-lookup"><span data-stu-id="06ec9-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="06ec9-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06ec9-134">NOTES</span></span>

## <span data-ttu-id="06ec9-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06ec9-135">RELATED LINKS</span></span>
