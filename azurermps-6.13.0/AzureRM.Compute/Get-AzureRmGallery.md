---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermgallery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmGallery.md
ms.openlocfilehash: cdb703144daa6f9abd62aee41eaad94b2cfa50e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541891"
---
# <span data-ttu-id="1e63c-101">Get-AzureRmGallery</span><span class="sxs-lookup"><span data-stu-id="1e63c-101">Get-AzureRmGallery</span></span>

## <span data-ttu-id="1e63c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e63c-102">SYNOPSIS</span></span>
<span data-ttu-id="1e63c-103">Uzyskaj lub Wyświetl galerie.</span><span class="sxs-lookup"><span data-stu-id="1e63c-103">Get or list galleries.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e63c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e63c-104">SYNTAX</span></span>

### <span data-ttu-id="1e63c-105">DefaultParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1e63c-105">DefaultParameter (Default)</span></span>
```
Get-AzureRmGallery [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1e63c-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="1e63c-106">ResourceIdParameter</span></span>
```
Get-AzureRmGallery [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e63c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1e63c-107">DESCRIPTION</span></span>
<span data-ttu-id="1e63c-108">Uzyskaj lub Wyświetl galerie.</span><span class="sxs-lookup"><span data-stu-id="1e63c-108">Get or list galleries.</span></span>

## <span data-ttu-id="1e63c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e63c-109">EXAMPLES</span></span>

### <span data-ttu-id="1e63c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e63c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmGallery -ResourceGroupName $rgname -GalleryName $galleryName

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

<span data-ttu-id="1e63c-111">Zapoznaj się z galerią.</span><span class="sxs-lookup"><span data-stu-id="1e63c-111">Get the gallery.</span></span>

## <span data-ttu-id="1e63c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e63c-112">PARAMETERS</span></span>

### <span data-ttu-id="1e63c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e63c-113">-DefaultProfile</span></span>
<span data-ttu-id="1e63c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e63c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e63c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1e63c-115">-Name</span></span>
<span data-ttu-id="1e63c-116">Nazwa galerii.</span><span class="sxs-lookup"><span data-stu-id="1e63c-116">The name of the gallery.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: GalleryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e63c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e63c-117">-ResourceGroupName</span></span>
<span data-ttu-id="1e63c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e63c-118">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e63c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e63c-119">-ResourceId</span></span>
<span data-ttu-id="1e63c-120">Identyfikator zasobu galerii</span><span class="sxs-lookup"><span data-stu-id="1e63c-120">The resource id for Gallery</span></span>

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

### <span data-ttu-id="1e63c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e63c-121">CommonParameters</span></span>
<span data-ttu-id="1e63c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e63c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e63c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e63c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e63c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e63c-124">INPUTS</span></span>

### <span data-ttu-id="1e63c-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1e63c-125">System.String</span></span>

### <span data-ttu-id="1e63c-126">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="1e63c-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="1e63c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e63c-127">OUTPUTS</span></span>

### <span data-ttu-id="1e63c-128">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSGallery</span><span class="sxs-lookup"><span data-stu-id="1e63c-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSGallery</span></span>

## <span data-ttu-id="1e63c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e63c-129">NOTES</span></span>

## <span data-ttu-id="1e63c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e63c-130">RELATED LINKS</span></span>
