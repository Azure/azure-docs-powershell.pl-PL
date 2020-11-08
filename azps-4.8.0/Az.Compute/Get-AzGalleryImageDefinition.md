---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageDefinition.md
ms.openlocfilehash: c6c689ce2c9ccda71150f221bdea4ae5dd2a20fc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062612"
---
# <span data-ttu-id="b2aa6-101">Get-AzGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="b2aa6-101">Get-AzGalleryImageDefinition</span></span>

## <span data-ttu-id="b2aa6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="b2aa6-103">Definicje obrazów galerii get lub list.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-103">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="b2aa6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2aa6-104">SYNTAX</span></span>

### <span data-ttu-id="b2aa6-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2aa6-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2aa6-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="b2aa6-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b2aa6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b2aa6-107">DESCRIPTION</span></span>
<span data-ttu-id="b2aa6-108">Definicje obrazów galerii get lub list.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="b2aa6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2aa6-109">EXAMPLES</span></span>

### <span data-ttu-id="b2aa6-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2aa6-110">Example 1</span></span>
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

<span data-ttu-id="b2aa6-111">Pobierz definicję Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-111">Get the gallery image definition.</span></span>

### <span data-ttu-id="b2aa6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b2aa6-112">Example 2</span></span>
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

<span data-ttu-id="b2aa6-113">Pobierz definicję Zdjęcia z galerii, która rozpoczyna się od tekstu "obraz".</span><span class="sxs-lookup"><span data-stu-id="b2aa6-113">Get the gallery image definition that starts with "image".</span></span>

### <span data-ttu-id="b2aa6-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b2aa6-114">Example 3</span></span>
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

<span data-ttu-id="b2aa6-115">Pobierz definicje zdjęć z galerii w gallery1.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-115">Get the gallery image definitions in gallery1.</span></span>

## <span data-ttu-id="b2aa6-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2aa6-116">PARAMETERS</span></span>

### <span data-ttu-id="b2aa6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2aa6-117">-DefaultProfile</span></span>
<span data-ttu-id="b2aa6-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2aa6-119">-Gallery</span><span class="sxs-lookup"><span data-stu-id="b2aa6-119">-GalleryName</span></span>
<span data-ttu-id="b2aa6-120">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="b2aa6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2aa6-121">-Name</span></span>
<span data-ttu-id="b2aa6-122">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-122">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="b2aa6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b2aa6-123">-ResourceGroupName</span></span>
<span data-ttu-id="b2aa6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="b2aa6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2aa6-125">-ResourceId</span></span>
<span data-ttu-id="b2aa6-126">Identyfikator zasobu definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="b2aa6-126">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="b2aa6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2aa6-127">CommonParameters</span></span>
<span data-ttu-id="b2aa6-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2aa6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2aa6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b2aa6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2aa6-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2aa6-130">INPUTS</span></span>

### <span data-ttu-id="b2aa6-131">System. String</span><span class="sxs-lookup"><span data-stu-id="b2aa6-131">System.String</span></span>

## <span data-ttu-id="b2aa6-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2aa6-132">OUTPUTS</span></span>

### <span data-ttu-id="b2aa6-133">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="b2aa6-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="b2aa6-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2aa6-134">NOTES</span></span>

## <span data-ttu-id="b2aa6-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2aa6-135">RELATED LINKS</span></span>
