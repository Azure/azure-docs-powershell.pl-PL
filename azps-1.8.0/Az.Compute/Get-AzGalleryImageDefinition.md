---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: 86da7a6f991bf7eeead14ad3414f9210eb7e175d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869119"
---
# <span data-ttu-id="73f65-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="73f65-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="73f65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="73f65-102">SYNOPSIS</span></span>
<span data-ttu-id="73f65-103">Definicje obrazów galerii get lub list.</span><span class="sxs-lookup"><span data-stu-id="73f65-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="73f65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="73f65-104">SYNTAX</span></span>

### <span data-ttu-id="73f65-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="73f65-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="73f65-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="73f65-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="73f65-107">Opis</span><span class="sxs-lookup"><span data-stu-id="73f65-107">DESCRIPTION</span></span>
<span data-ttu-id="73f65-108">Definicje obrazów galerii get lub list.</span><span class="sxs-lookup"><span data-stu-id="73f65-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="73f65-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="73f65-109">EXAMPLES</span></span>

### <span data-ttu-id="73f65-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="73f65-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="73f65-111">Pobierz definicję Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="73f65-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="73f65-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="73f65-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image*

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="73f65-113">Pobierz definicję Zdjęcia z galerii, która rozpoczyna się od tekstu "obraz".</span><span class="sxs-lookup"><span data-stu-id="73f65-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="73f65-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="73f65-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageDefinition -ResourceGroupName rg1 -GalleryName gallery1

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image1
Name                : image1
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}

ResourceGroupName   : rg1
Eula                : eula
PrivacyStatementUri : Https://www.microsoft.com
ReleaseNoteUri      : https://www.microsoft.com
OsType              : Windows
OsState             : Generalized
EndOfLifeDate       : 2/18/2025 12:07:00 PM
Identifier          :
  Publisher         : PsSDKTeamTest
  Offer             : testgalleryoffer1
  Sku               : testgallerysku1
Recommended         :
  VCPUs             :
    Min             : 2
    Max             : 32
  Memory            :
    Min             : 1
    Max             : 100
Disallowed          :
  DiskTypes[0]      : Standard_LRS
PurchasePlan        :
  Name              : PsSDKTestPlan
  Publisher         : PSSDKTeam
  Product           : PsSDKTestProductWindowsVm
ProvisioningState   : Succeeded
Id                  : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/provi
ders/Microsoft.Compute/galleries/gallery1/images/image2
Name                : image2
Type                : Microsoft.Compute/galleries/images
Location            : eastus2
Tags                : {}
```

<span data-ttu-id="73f65-115">Pobierz definicje zdjęć z galerii w gallery1.</span><span class="sxs-lookup"><span data-stu-id="73f65-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="73f65-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="73f65-116">PARAMETERS</span></span>

### <span data-ttu-id="73f65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73f65-117">-DefaultProfile</span></span>
<span data-ttu-id="73f65-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="73f65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73f65-119">-Gallery</span><span class="sxs-lookup"><span data-stu-id="73f65-119">-GalleryName</span></span>
<span data-ttu-id="73f65-120">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="73f65-120">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f65-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="73f65-121">-Name</span></span>
<span data-ttu-id="73f65-122">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="73f65-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="73f65-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73f65-123">-ResourceGroupName</span></span>
<span data-ttu-id="73f65-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="73f65-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73f65-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="73f65-125">-ResourceId</span></span>
<span data-ttu-id="73f65-126">Identyfikator zasobu definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="73f65-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="73f65-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73f65-127">CommonParameters</span></span>
<span data-ttu-id="73f65-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73f65-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73f65-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="73f65-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73f65-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="73f65-130">INPUTS</span></span>

### <span data-ttu-id="73f65-131">System. String</span><span class="sxs-lookup"><span data-stu-id="73f65-131">System.String</span></span>

## <span data-ttu-id="73f65-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="73f65-132">OUTPUTS</span></span>

### <span data-ttu-id="73f65-133">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="73f65-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="73f65-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="73f65-134">NOTES</span></span>

## <span data-ttu-id="73f65-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="73f65-135">RELATED LINKS</span></span>
