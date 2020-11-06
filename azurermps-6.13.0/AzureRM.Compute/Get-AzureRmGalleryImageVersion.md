---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimageversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageVersion.md
ms.openlocfilehash: bff748b8c867b272208469d34229cc2724bc8610
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541875"
---
# <span data-ttu-id="62a90-101">Get-AzureRmGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="62a90-101">Get-AzureRmGalleryImageVersion</span></span>

## <span data-ttu-id="62a90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62a90-102">SYNOPSIS</span></span>
<span data-ttu-id="62a90-103">Wersje obrazów galerii pobieranie lub wyświetlanie.</span><span class="sxs-lookup"><span data-stu-id="62a90-103">Get or list gallery image versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62a90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62a90-104">SYNTAX</span></span>

### <span data-ttu-id="62a90-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="62a90-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceGroupName] <String> [-GalleryName] <String>
 [-GalleryImageDefinitionName] <String> [[-Name] <String>] [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62a90-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="62a90-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageVersion [-ResourceId] <String> [-ExpandReplicationStatus]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62a90-107">Opis</span><span class="sxs-lookup"><span data-stu-id="62a90-107">DESCRIPTION</span></span>
<span data-ttu-id="62a90-108">Wersje obrazów galerii pobieranie lub wyświetlanie.</span><span class="sxs-lookup"><span data-stu-id="62a90-108">Get or list gallery image versions.</span></span>

## <span data-ttu-id="62a90-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62a90-109">EXAMPLES</span></span>

### <span data-ttu-id="62a90-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62a90-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageVersion -ResourceGroupName $rgname -GalleryName $gallery -ImageDefinitionName $image -GalleryImageVersionName $version
```

<span data-ttu-id="62a90-111">Pobierz wersję zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="62a90-111">Get the gallery image version.</span></span>

## <span data-ttu-id="62a90-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62a90-112">PARAMETERS</span></span>

### <span data-ttu-id="62a90-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62a90-113">-DefaultProfile</span></span>
<span data-ttu-id="62a90-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62a90-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62a90-115">-ExpandReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="62a90-115">-ExpandReplicationStatus</span></span>
<span data-ttu-id="62a90-116">Pokaż stan replikacji.</span><span class="sxs-lookup"><span data-stu-id="62a90-116">Show replication status.</span></span>

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

### <span data-ttu-id="62a90-117">-GalleryImageDefinitionName</span><span class="sxs-lookup"><span data-stu-id="62a90-117">-GalleryImageDefinitionName</span></span>
<span data-ttu-id="62a90-118">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="62a90-118">The name of the gallery image definition.</span></span>

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

### <span data-ttu-id="62a90-119">-Gallery</span><span class="sxs-lookup"><span data-stu-id="62a90-119">-GalleryName</span></span>
<span data-ttu-id="62a90-120">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="62a90-120">The name of the gallery.</span></span>

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

### <span data-ttu-id="62a90-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62a90-121">-Name</span></span>
<span data-ttu-id="62a90-122">Nazwa wersji zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="62a90-122">The name of the gallery image version.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageVersionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62a90-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62a90-123">-ResourceGroupName</span></span>
<span data-ttu-id="62a90-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62a90-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="62a90-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62a90-125">-ResourceId</span></span>
<span data-ttu-id="62a90-126">Identyfikator zasobu dla wersji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="62a90-126">The resource ID for the gallery image version</span></span>

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

### <span data-ttu-id="62a90-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62a90-127">CommonParameters</span></span>
<span data-ttu-id="62a90-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62a90-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62a90-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62a90-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62a90-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62a90-130">INPUTS</span></span>

### <span data-ttu-id="62a90-131">System. String</span><span class="sxs-lookup"><span data-stu-id="62a90-131">System.String</span></span>

### <span data-ttu-id="62a90-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="62a90-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="62a90-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62a90-133">OUTPUTS</span></span>

### <span data-ttu-id="62a90-134">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImageVersion</span><span class="sxs-lookup"><span data-stu-id="62a90-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImageVersion</span></span>

## <span data-ttu-id="62a90-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62a90-135">NOTES</span></span>

## <span data-ttu-id="62a90-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62a90-136">RELATED LINKS</span></span>
