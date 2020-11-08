---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062203"
---
# <span data-ttu-id="72bf4-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="72bf4-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="72bf4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72bf4-102">SYNOPSIS</span></span>
<span data-ttu-id="72bf4-103">Umożliwia zaktualizowanie miejsca docelowego magazynu.</span><span class="sxs-lookup"><span data-stu-id="72bf4-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="72bf4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72bf4-104">SYNTAX</span></span>

### <span data-ttu-id="72bf4-105">ClfsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72bf4-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="72bf4-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="72bf4-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="72bf4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="72bf4-107">DESCRIPTION</span></span>
<span data-ttu-id="72bf4-108">Polecenie cmdlet **Set-AzHpcCacheStorageTarget** umożliwia zaktualizowanie miejsca docelowego miejsca do magazynowania dołączonego do pamięci podręcznej Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="72bf4-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="72bf4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72bf4-109">EXAMPLES</span></span>

### <span data-ttu-id="72bf4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="72bf4-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="72bf4-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="72bf4-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="72bf4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72bf4-112">PARAMETERS</span></span>

### <span data-ttu-id="72bf4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="72bf4-113">-AsJob</span></span>
<span data-ttu-id="72bf4-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="72bf4-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="72bf4-115">-CacheName</span></span>
<span data-ttu-id="72bf4-116">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="72bf4-116">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="72bf4-117">-CLFS</span></span>
<span data-ttu-id="72bf4-118">Aktualizuj typ docelowy magazynu CLFS.</span><span class="sxs-lookup"><span data-stu-id="72bf4-118">Update CLFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72bf4-119">-DefaultProfile</span></span>
<span data-ttu-id="72bf4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72bf4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72bf4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="72bf4-121">-Force</span></span>
<span data-ttu-id="72bf4-122">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="72bf4-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="72bf4-123">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru Opróżnienia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="72bf4-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-124">-Połączenie</span><span class="sxs-lookup"><span data-stu-id="72bf4-124">-Junction</span></span>
<span data-ttu-id="72bf4-125">Połączenia.</span><span class="sxs-lookup"><span data-stu-id="72bf4-125">Junction.</span></span>

```yaml
Type: System.Collections.Hashtable[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="72bf4-126">-Name</span></span>
<span data-ttu-id="72bf4-127">Nazwa docelowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="72bf4-127">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="72bf4-128">-NFS</span></span>
<span data-ttu-id="72bf4-129">Aktualizowanie typu docelowego magazynu systemu plików NFS.</span><span class="sxs-lookup"><span data-stu-id="72bf4-129">Update NFS Storage Target type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72bf4-130">-ResourceGroupName</span></span>
<span data-ttu-id="72bf4-131">Nazwa grupy zasobów, pod którą chcesz zaktualizować miejsce docelowe magazynu.</span><span class="sxs-lookup"><span data-stu-id="72bf4-131">Name of resource group under which you want to update storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72bf4-132">-Confirm</span></span>
<span data-ttu-id="72bf4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72bf4-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72bf4-134">-WhatIf</span></span>
<span data-ttu-id="72bf4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72bf4-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="72bf4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72bf4-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72bf4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72bf4-137">CommonParameters</span></span>
<span data-ttu-id="72bf4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72bf4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72bf4-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72bf4-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72bf4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72bf4-140">INPUTS</span></span>

### <span data-ttu-id="72bf4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="72bf4-141">System.String</span></span>

## <span data-ttu-id="72bf4-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72bf4-142">OUTPUTS</span></span>

### <span data-ttu-id="72bf4-143">Microsoft. Azure. PowerShell. polecenia. HPCCache. models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="72bf4-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="72bf4-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72bf4-144">NOTES</span></span>

## <span data-ttu-id="72bf4-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72bf4-145">RELATED LINKS</span></span>
