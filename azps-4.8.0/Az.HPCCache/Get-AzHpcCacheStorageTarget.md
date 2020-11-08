---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/get-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Get-AzHpcCacheStorageTarget.md
ms.openlocfilehash: c32b47b7300c7da0a6517ca5e3802af60bd0f571
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064093"
---
# <span data-ttu-id="71782-101">Get-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="71782-101">Get-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="71782-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="71782-102">SYNOPSIS</span></span>
<span data-ttu-id="71782-103">Pobierz docelowe miejsca do magazynowania w pamięci podręcznej HPC.</span><span class="sxs-lookup"><span data-stu-id="71782-103">Get HPC cache storage target(s).</span></span>

## <span data-ttu-id="71782-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="71782-104">SYNTAX</span></span>

### <span data-ttu-id="71782-105">ByFieldsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="71782-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71782-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="71782-106">ByResourceIdParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="71782-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="71782-107">ByObjectParameterSet</span></span>
```
Get-AzHpcCacheStorageTarget -CacheObject <PSHPCCache> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="71782-108">Opis</span><span class="sxs-lookup"><span data-stu-id="71782-108">DESCRIPTION</span></span>
<span data-ttu-id="71782-109">Polecenie cmdlet **Get-AzHpcCacheStorageTarget** Pobiera elementy docelowe magazynu, które istnieją w pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="71782-109">The **Get-AzHpcCacheStorageTarget** cmdlet gets storage target(s) that exist on cache.</span></span>

## <span data-ttu-id="71782-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="71782-110">EXAMPLES</span></span>

### <span data-ttu-id="71782-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="71782-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest
```

### <span data-ttu-id="71782-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="71782-112">Example 2</span></span>
```powershell
PS C:\> Get-AzHpcCacheStorageTarget -ResourceGroupName rgTest -CacheName cacheTest -StorageTargetName stTest
```

## <span data-ttu-id="71782-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="71782-113">PARAMETERS</span></span>

### <span data-ttu-id="71782-114">-CacheId</span><span class="sxs-lookup"><span data-stu-id="71782-114">-CacheId</span></span>
<span data-ttu-id="71782-115">Identyfikator zasobu w pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="71782-115">The resource id of the Cache</span></span>

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

### <span data-ttu-id="71782-116">-CacheName</span><span class="sxs-lookup"><span data-stu-id="71782-116">-CacheName</span></span>
<span data-ttu-id="71782-117">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="71782-117">Name of cache.</span></span>

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

### <span data-ttu-id="71782-118">-Cacheobject</span><span class="sxs-lookup"><span data-stu-id="71782-118">-CacheObject</span></span>
<span data-ttu-id="71782-119">Obiekt pamięci podręcznej, który ma zostać uruchomiony.</span><span class="sxs-lookup"><span data-stu-id="71782-119">The cache object to start.</span></span>

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

### <span data-ttu-id="71782-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71782-120">-DefaultProfile</span></span>
<span data-ttu-id="71782-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="71782-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71782-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="71782-122">-Name</span></span>
<span data-ttu-id="71782-123">Nazwa docelowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="71782-123">Name of storage target.</span></span>

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

### <span data-ttu-id="71782-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71782-124">-ResourceGroupName</span></span>
<span data-ttu-id="71782-125">Nazwa pamięci podręcznej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="71782-125">Name of resource group cache is in.</span></span>


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

### <span data-ttu-id="71782-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71782-126">CommonParameters</span></span>
<span data-ttu-id="71782-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71782-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71782-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="71782-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71782-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="71782-129">INPUTS</span></span>

### <span data-ttu-id="71782-130">System. String</span><span class="sxs-lookup"><span data-stu-id="71782-130">System.String</span></span>

## <span data-ttu-id="71782-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="71782-131">OUTPUTS</span></span>

### <span data-ttu-id="71782-132">Microsoft. Azure. PowerShell. polecenia. HPCCache. models. PSHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="71782-132">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHpcStorageTarget</span></span>

## <span data-ttu-id="71782-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="71782-133">NOTES</span></span>

## <span data-ttu-id="71782-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="71782-134">RELATED LINKS</span></span>
