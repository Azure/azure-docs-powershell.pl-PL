---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzGalleryImageVersion.md
ms.openlocfilehash: 1385d4fe93157715ffdd521cfb62ed963b86e1ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94318127"
---
# <span data-ttu-id="33e7a-101">Get-AzGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="33e7a-101">Get-AzGalleryImageVersion</span></span>

## <span data-ttu-id="33e7a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="33e7a-103">Wersje obrazów galerii pobieranie lub wyświetlanie.</span><span class="sxs-lookup"><span data-stu-id="33e7a-103">Get or list gallery image versions.</span></span>

## <span data-ttu-id="33e7a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33e7a-104">SYNTAX</span></span>

### <span data-ttu-id="33e7a-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="33e7a-105">DefaultParameter (Default)</span></span>
```
Get-AzGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33e7a-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="33e7a-106">ResourceIdParameter</span></span>
```
Get-AzGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33e7a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="33e7a-107">DESCRIPTION</span></span>
<span data-ttu-id="33e7a-108">Wersje obrazów galerii pobieranie lub wyświetlanie.</span><span class="sxs-lookup"><span data-stu-id="33e7a-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="33e7a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33e7a-109">EXAMPLES</span></span>

### <span data-ttu-id="33e7a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33e7a-110">Example 1</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1.0.0

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="33e7a-111">Pobierz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="33e7a-111">Get the gallery image version.</span></span>

### <span data-ttu-id="33e7a-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33e7a-112">Example 2</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1 -GalleryImageVersionName 1*

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="33e7a-113">Pobierz wersje zdjęć z galerii zaczynające się od "1".</span><span class="sxs-lookup"><span data-stu-id="33e7a-113">Get the gallery image versions that starts with "1".</span></span>

### <span data-ttu-id="33e7a-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="33e7a-114">Example 3</span></span>
```powershell
PS C:\> Get-AzGalleryImageVersion -ResourceGroupName rg1 -GalleryName gallery1 -GalleryImageDefinitionName image1

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.0.0
Name                     : 1.0.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}

ResourceGroupName        : rg1
PublishingProfile        :
  TargetRegions[0]       :
    Name                 : South Central US
    RegionalReplicaCount : 1
  TargetRegions[1]       :
    Name                 : East US 2
    RegionalReplicaCount : 2
  TargetRegions[2]       :
    Name                 : Central US
    RegionalReplicaCount : 1
  Source                 :
    ManagedImage         :
      Id                 : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/images/test1
  ReplicaCount           : 1
  ExcludeFromLatest      : False
  PublishedDate          : 11/14/2018 12:00:00 AM
  EndOfLifeDate          : 2/18/2025 12:07:00 PM
ProvisioningState        : Succeeded
StorageProfile           :
  OsDiskImage            :
    SizeInGB             : 127
    HostCaching          : ReadWrite
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/rg1/
providers/Microsoft.Compute/galleries/gallery1/images/image1/versions/1.1.0
Name                     : 1.1.0
Type                     : Microsoft.Compute/galleries/images/versions
Location                 : eastus2
Tags                     : {}
```

<span data-ttu-id="33e7a-115">Pobierz wszystkie wersje zdjęć z galerii.</span><span class="sxs-lookup"><span data-stu-id="33e7a-115">Get all gallery image versions.</span></span>

## <span data-ttu-id="33e7a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33e7a-116">PARAMETERS</span></span>

### <span data-ttu-id="33e7a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e7a-117">-DefaultProfile</span></span>
<span data-ttu-id="33e7a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33e7a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33e7a-119">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="33e7a-119">-ExpandReplicationStatus</span></span>
<span data-ttu-id="33e7a-120">Pokaż stan replikacji.</span><span class="sxs-lookup"><span data-stu-id="33e7a-120">Show replication status.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e7a-121">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="33e7a-121">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="33e7a-122">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="33e7a-122">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33e7a-123">-Gallery</span><span class="sxs-lookup"><span data-stu-id="33e7a-123">-GalleryName</span></span>
<span data-ttu-id="33e7a-124">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="33e7a-124">The name of the gallery.</span></span>

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

### <span data-ttu-id="33e7a-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="33e7a-125">-Name</span></span>
<span data-ttu-id="33e7a-126">Nazwa wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="33e7a-126">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="33e7a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33e7a-127">-ResourceGroupName</span></span>
<span data-ttu-id="33e7a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="33e7a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="33e7a-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33e7a-129">-ResourceId</span></span>
<span data-ttu-id="33e7a-130">Identyfikator zasobu dla wersji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="33e7a-130">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="33e7a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e7a-131">CommonParameters</span></span>
<span data-ttu-id="33e7a-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33e7a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e7a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="33e7a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e7a-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33e7a-134">INPUTS</span></span>

### <span data-ttu-id="33e7a-135">System. String</span><span class="sxs-lookup"><span data-stu-id="33e7a-135">System.String</span></span>

### <span data-ttu-id="33e7a-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="33e7a-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="33e7a-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33e7a-137">OUTPUTS</span></span>

### <span data-ttu-id="33e7a-138">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="33e7a-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="33e7a-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33e7a-139">NOTES</span></span>

## <span data-ttu-id="33e7a-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33e7a-140">RELATED LINKS</span></span>
