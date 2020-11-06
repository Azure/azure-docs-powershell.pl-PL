---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgalleryimagedefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGalleryImageDefinition.md
ms.openlocfilehash: 75d30165c5dc5d69eabd08e89ad2577df82f7ebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541876"
---
# <span data-ttu-id="4c373-101">Get-AzureRmGalleryImageDefinition</span><span class="sxs-lookup"><span data-stu-id="4c373-101">Get-AzureRmGalleryImageDefinition</span></span>

## <span data-ttu-id="4c373-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4c373-102">SYNOPSIS</span></span>
<span data-ttu-id="4c373-103">Definicje obrazów galerii get lub list.</span><span class="sxs-lookup"><span data-stu-id="4c373-103">Get or list gallery image definitions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c373-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4c373-104">SYNTAX</span></span>

### <span data-ttu-id="4c373-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4c373-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceGroupName] <String> [-GalleryName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c373-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4c373-106">ResourceIdParameter</span></span>
```
Get-AzureRmGalleryImageDefinition [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4c373-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4c373-107">DESCRIPTION</span></span>
<span data-ttu-id="4c373-108">Definicje obrazów galerii get lub list.</span><span class="sxs-lookup"><span data-stu-id="4c373-108">Get or list gallery image definitions.</span></span>

## <span data-ttu-id="4c373-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4c373-109">EXAMPLES</span></span>

### <span data-ttu-id="4c373-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c373-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGalleryImageDefinition -ResourceGroupName $rgname -GalleryName $gallery -GalleryImageDefinitionName $image
```

<span data-ttu-id="4c373-111">Pobierz definicję Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="4c373-111">Get the gallery image definition.</span></span>

## <span data-ttu-id="4c373-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4c373-112">PARAMETERS</span></span>

### <span data-ttu-id="4c373-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c373-113">-DefaultProfile</span></span>
<span data-ttu-id="4c373-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c373-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c373-115">-Gallery</span><span class="sxs-lookup"><span data-stu-id="4c373-115">-GalleryName</span></span>
<span data-ttu-id="4c373-116">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="4c373-116">The name of the gallery.</span></span>

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

### <span data-ttu-id="4c373-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4c373-117">-Name</span></span>
<span data-ttu-id="4c373-118">Nazwa definicji Zdjęcia z galerii.</span><span class="sxs-lookup"><span data-stu-id="4c373-118">The name of the gallery image definition.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryImageDefinitionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c373-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c373-119">-ResourceGroupName</span></span>
<span data-ttu-id="4c373-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c373-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="4c373-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c373-121">-ResourceId</span></span>
<span data-ttu-id="4c373-122">Identyfikator zasobu definicji obrazu galerii</span><span class="sxs-lookup"><span data-stu-id="4c373-122">The resource ID for the gallery image definition</span></span>

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

### <span data-ttu-id="4c373-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c373-123">CommonParameters</span></span>
<span data-ttu-id="4c373-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c373-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c373-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c373-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c373-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c373-126">INPUTS</span></span>

### <span data-ttu-id="4c373-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4c373-127">System.String</span></span>

## <span data-ttu-id="4c373-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4c373-128">OUTPUTS</span></span>

### <span data-ttu-id="4c373-129">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGalleryImage</span><span class="sxs-lookup"><span data-stu-id="4c373-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSGalleryImage</span></span>

## <span data-ttu-id="4c373-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4c373-130">NOTES</span></span>

## <span data-ttu-id="4c373-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c373-131">RELATED LINKS</span></span>
