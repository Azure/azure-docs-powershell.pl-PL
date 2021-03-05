---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 6fb1e00f74bcd170d8117e4e37655da6c275a62f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988226"
---
# <span data-ttu-id="050b4-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="050b4-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="050b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050b4-102">SYNOPSIS</span></span>
<span data-ttu-id="050b4-103">Uzyskaj wartości docelowe pamięci podręcznej HPC.</span><span class="sxs-lookup"><span data-stu-id="050b4-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="050b4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="050b4-104">SYNTAX</span></span>

### <span data-ttu-id="050b4-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="050b4-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050b4-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="050b4-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="050b4-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="050b4-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="050b4-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="050b4-108">DESCRIPTION</span></span>
<span data-ttu-id="050b4-109">Polecenie **cmdlet Get-AzHpcCacheStorageTarget** pobiera wartości docelowe magazynu istniejące w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="050b4-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="050b4-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="050b4-110">EXAMPLES</span></span>

### <span data-ttu-id="050b4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="050b4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="050b4-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="050b4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="050b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="050b4-113">PARAMETERS</span></span>

### <span data-ttu-id="050b4-114">- CacheId</span><span class="sxs-lookup"><span data-stu-id="050b4-114">-CacheId</span></span>
<span data-ttu-id="050b4-115">Identyfikator zasobu pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="050b4-115">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050b4-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="050b4-116">-CacheName</span></span>
<span data-ttu-id="050b4-117">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="050b4-117">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050b4-118">-CacheObject</span><span class="sxs-lookup"><span data-stu-id="050b4-118">-CacheObject</span></span>
<span data-ttu-id="050b4-119">Obiekt pamięci podręcznej, który ma się rozpocząć.</span><span class="sxs-lookup"><span data-stu-id="050b4-119">The cache object to start.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="050b4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050b4-120">-DefaultProfile</span></span>
<span data-ttu-id="050b4-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="050b4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="050b4-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="050b4-122">-Name</span></span>
<span data-ttu-id="050b4-123">Nazwa miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="050b4-123">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: StorageTargetName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050b4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050b4-124">-ResourceGroupName</span></span>
<span data-ttu-id="050b4-125">Nazwa pamięci podręcznej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="050b4-125">Name of resource group cache is in.</span></span>


```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050b4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050b4-126">CommonParameters</span></span>
<span data-ttu-id="050b4-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="050b4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050b4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="050b4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050b4-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="050b4-129">INPUTS</span></span>

### <span data-ttu-id="050b4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="050b4-130">System.String</span></span>

## <span data-ttu-id="050b4-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="050b4-131">OUTPUTS</span></span>

### <span data-ttu-id="050b4-132">Microsoft.Azure.PowerShell.Cmdlet.HPCCache.Models.PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="050b4-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="050b4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="050b4-133">NOTES</span></span>

## <span data-ttu-id="050b4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="050b4-134">RELATED LINKS</span></span>
