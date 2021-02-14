---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.CloudService/new-AzCloudServiceRoleProfilePropertiesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceRoleProfilePropertiesObject.md
ms.openlocfilehash: c9e41a6a4fa7a89db31304dc343da466e8632a74
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181787"
---
# <span data-ttu-id="9193c-101">New-AzCloudServiceRoleProfilePropertiesObject</span><span class="sxs-lookup"><span data-stu-id="9193c-101">New-AzCloudServiceRoleProfilePropertiesObject</span></span>

## <span data-ttu-id="9193c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9193c-102">SYNOPSIS</span></span>
<span data-ttu-id="9193c-103">Tworzenie obiektu w pamięci dla właściwości CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9193c-103">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9193c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9193c-104">SYNTAX</span></span>

```
New-AzCloudServiceRoleProfilePropertiesObject [-Name <String>] [-SkuCapacity <Int64>] [-SkuName <String>]
 [-SkuTier <String>] [<CommonParameters>]
```

## <span data-ttu-id="9193c-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9193c-105">DESCRIPTION</span></span>
<span data-ttu-id="9193c-106">Tworzenie obiektu w pamięci dla właściwości CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9193c-106">Create a in-memory object for CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9193c-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9193c-107">EXAMPLES</span></span>

### <span data-ttu-id="9193c-108">Przykład 1. Tworzenie obiektu właściwości profilu roli</span><span class="sxs-lookup"><span data-stu-id="9193c-108">Example 1: Create role profile properties object</span></span>
```powershell
$role = New-AzCloudServiceRoleProfilePropertiesObject -Name 'WebRole' -SkuName 'Standard_D1_v2' -SkuTier 'Standard' -SkuCapacity 2
```

<span data-ttu-id="9193c-109">To polecenie tworzy obiekt właściwości profilu roli, który jest używany do tworzenia lub aktualizowania usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="9193c-109">This command creates role profile properties object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="9193c-110">Aby uzyskać więcej szczegółowych informacji, zobacz New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="9193c-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="9193c-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9193c-111">PARAMETERS</span></span>

### <span data-ttu-id="9193c-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9193c-112">-Name</span></span>
<span data-ttu-id="9193c-113">Nazwa profilu roli.</span><span class="sxs-lookup"><span data-stu-id="9193c-113">Name of role profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9193c-114">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="9193c-114">-SkuCapacity</span></span>
<span data-ttu-id="9193c-115">Określa liczbę wystąpień ról w usłudze w chmurze.</span><span class="sxs-lookup"><span data-stu-id="9193c-115">Specifies the number of role instances in the cloud service.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9193c-116">-SKUName</span><span class="sxs-lookup"><span data-stu-id="9193c-116">-SkuName</span></span>
<span data-ttu-id="9193c-117">Nazwa sKU.</span><span class="sxs-lookup"><span data-stu-id="9193c-117">The sku name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9193c-118">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="9193c-118">-SkuTier</span></span>
<span data-ttu-id="9193c-119">SkuTier.</span><span class="sxs-lookup"><span data-stu-id="9193c-119">SkuTier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9193c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9193c-120">CommonParameters</span></span>
<span data-ttu-id="9193c-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9193c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9193c-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9193c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9193c-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9193c-123">INPUTS</span></span>

## <span data-ttu-id="9193c-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9193c-124">OUTPUTS</span></span>

### <span data-ttu-id="9193c-125">Microsoft.Azure.PowerShell.cmdlet.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span><span class="sxs-lookup"><span data-stu-id="9193c-125">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.CloudServiceRoleProfileProperties</span></span>

## <span data-ttu-id="9193c-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9193c-126">NOTES</span></span>

<span data-ttu-id="9193c-127">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9193c-127">ALIASES</span></span>

## <span data-ttu-id="9193c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9193c-128">RELATED LINKS</span></span>

