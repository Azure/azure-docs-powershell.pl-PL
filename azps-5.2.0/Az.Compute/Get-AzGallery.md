---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGallery.md
ms.openlocfilehash: baa3730ee03dd8f871e64e7964659c62f60e8032
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332785"
---
# <span data-ttu-id="ffd50-101">Get-AzGallery</span><span class="sxs-lookup"><span data-stu-id="ffd50-101">Get-AzGallery</span></span>

## <span data-ttu-id="ffd50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ffd50-102">SYNOPSIS</span></span>
<span data-ttu-id="ffd50-103">Uzyskaj lub Wyświetl galerie.</span><span class="sxs-lookup"><span data-stu-id="ffd50-103">Get or list galleries.</span></span>

## <span data-ttu-id="ffd50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ffd50-104">SYNTAX</span></span>

### <span data-ttu-id="ffd50-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ffd50-105">DefaultParameter (Default)</span></span>
```
Get-AzGallery [[-ResourceGroupName] <String>] [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffd50-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="ffd50-106">ResourceIdParameter</span></span>
```
Get-AzGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ffd50-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ffd50-107">DESCRIPTION</span></span>
<span data-ttu-id="ffd50-108">Uzyskaj lub Wyświetl galerie.</span><span class="sxs-lookup"><span data-stu-id="ffd50-108">Get or list galleries.</span></span>

## <span data-ttu-id="ffd50-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ffd50-109">EXAMPLES</span></span>

### <span data-ttu-id="ffd50-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ffd50-110">Example 1</span></span>
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

<span data-ttu-id="ffd50-111">Uzyskiwanie galerii "gallery1"</span><span class="sxs-lookup"><span data-stu-id="ffd50-111">Get the gallery "gallery1"</span></span>

### <span data-ttu-id="ffd50-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ffd50-112">Example 2</span></span>
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

<span data-ttu-id="ffd50-113">Pobierz wszystkie galerie w RG1.</span><span class="sxs-lookup"><span data-stu-id="ffd50-113">Get all galleries in rg1.</span></span>

### <span data-ttu-id="ffd50-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ffd50-114">Example 3</span></span>
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

<span data-ttu-id="ffd50-115">Pobierz wszystkie galerie w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ffd50-115">Get all galleries in subscription.</span></span>

### <span data-ttu-id="ffd50-116">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="ffd50-116">Example 4</span></span>
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

<span data-ttu-id="ffd50-117">Pobierz wszystkie galerie w ramach subskrypcji, rozpoczynając od "galerii".</span><span class="sxs-lookup"><span data-stu-id="ffd50-117">Get all galleries in subscription that start with "gallery".</span></span>

## <span data-ttu-id="ffd50-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ffd50-118">PARAMETERS</span></span>

### <span data-ttu-id="ffd50-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffd50-119">-DefaultProfile</span></span>
<span data-ttu-id="ffd50-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ffd50-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffd50-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ffd50-121">-Name</span></span>
<span data-ttu-id="ffd50-122">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="ffd50-122">The name of the gallery.</span></span>

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

### <span data-ttu-id="ffd50-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffd50-123">-ResourceGroupName</span></span>
<span data-ttu-id="ffd50-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ffd50-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="ffd50-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffd50-125">-ResourceId</span></span>
<span data-ttu-id="ffd50-126">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="ffd50-126">The resource id for Gallery</span></span>

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

### <span data-ttu-id="ffd50-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffd50-127">CommonParameters</span></span>
<span data-ttu-id="ffd50-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffd50-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffd50-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ffd50-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffd50-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ffd50-130">INPUTS</span></span>

### <span data-ttu-id="ffd50-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ffd50-131">System.String</span></span>

## <span data-ttu-id="ffd50-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ffd50-132">OUTPUTS</span></span>

### <span data-ttu-id="ffd50-133">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="ffd50-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="ffd50-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ffd50-134">NOTES</span></span>

## <span data-ttu-id="ffd50-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ffd50-135">RELATED LINKS</span></span>
