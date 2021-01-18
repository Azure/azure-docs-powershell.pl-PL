---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499077"
---
# <span data-ttu-id="6471e-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="6471e-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="6471e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6471e-102">SYNOPSIS</span></span>
<span data-ttu-id="6471e-103">Tworzy miejsce docelowe magazynu.</span><span class="sxs-lookup"><span data-stu-id="6471e-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="6471e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6471e-104">SYNTAX</span></span>

### <span data-ttu-id="6471e-105">ClfsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6471e-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6471e-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="6471e-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6471e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6471e-107">DESCRIPTION</span></span>
<span data-ttu-id="6471e-108">Polecenie cmdlet **New-AzHpcCacheStorageTarget** umożliwia dodanie miejsca docelowego magazynu do pamięci podręcznej platformy Azure HPC.</span><span class="sxs-lookup"><span data-stu-id="6471e-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="6471e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6471e-109">EXAMPLES</span></span>

### <span data-ttu-id="6471e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6471e-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="6471e-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6471e-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="6471e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6471e-112">PARAMETERS</span></span>

### <span data-ttu-id="6471e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6471e-113">-AsJob</span></span>
<span data-ttu-id="6471e-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6471e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6471e-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="6471e-115">-CacheName</span></span>
<span data-ttu-id="6471e-116">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="6471e-116">Name of cache.</span></span>

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

### <span data-ttu-id="6471e-117">-CLFS</span><span class="sxs-lookup"><span data-stu-id="6471e-117">-CLFS</span></span>
<span data-ttu-id="6471e-118">Aktualizuj typ docelowy magazynu CLFS.</span><span class="sxs-lookup"><span data-stu-id="6471e-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="6471e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6471e-119">-DefaultProfile</span></span>
<span data-ttu-id="6471e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6471e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6471e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6471e-121">-Force</span></span>
<span data-ttu-id="6471e-122">Wskazuje, że polecenie cmdlet nie monituje o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6471e-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="6471e-123">Domyślnie to polecenie cmdlet monituje o potwierdzenie zamiaru Opróżnienia pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="6471e-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="6471e-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="6471e-124">-HostName</span></span>
<span data-ttu-id="6471e-125">Nazwa hosta NFS.</span><span class="sxs-lookup"><span data-stu-id="6471e-125">NFS host name.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6471e-126">-Połączenie</span><span class="sxs-lookup"><span data-stu-id="6471e-126">-Junction</span></span>
<span data-ttu-id="6471e-127">Połączenia.</span><span class="sxs-lookup"><span data-stu-id="6471e-127">Junction.</span></span>

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

### <span data-ttu-id="6471e-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6471e-128">-Name</span></span>
<span data-ttu-id="6471e-129">Nazwa docelowego miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="6471e-129">Name of storage target.</span></span>

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

### <span data-ttu-id="6471e-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="6471e-130">-NFS</span></span>
<span data-ttu-id="6471e-131">Aktualizowanie typu docelowego magazynu systemu plików NFS.</span><span class="sxs-lookup"><span data-stu-id="6471e-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="6471e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6471e-132">-ResourceGroupName</span></span>
<span data-ttu-id="6471e-133">"Nazwa grupy zasobów, pod którą chcesz utworzyć miejsce docelowe miejsca do magazynowania dla danej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="6471e-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="6471e-134">-StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="6471e-134">-StorageContainerID</span></span>
<span data-ttu-id="6471e-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="6471e-135">StorageContainerID</span></span>

```yaml
Type: System.String
Parameter Sets: ClfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6471e-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="6471e-136">-UsageModel</span></span>
<span data-ttu-id="6471e-137">Model użycia systemu plików NFS.</span><span class="sxs-lookup"><span data-stu-id="6471e-137">NFS usage model.</span></span>

```yaml
Type: System.String
Parameter Sets: NfsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6471e-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6471e-138">-Confirm</span></span>
<span data-ttu-id="6471e-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6471e-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6471e-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6471e-140">-WhatIf</span></span>
<span data-ttu-id="6471e-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6471e-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6471e-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6471e-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6471e-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6471e-143">CommonParameters</span></span>
<span data-ttu-id="6471e-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6471e-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6471e-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6471e-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6471e-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6471e-146">INPUTS</span></span>

### <span data-ttu-id="6471e-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6471e-147">System.String</span></span>

## <span data-ttu-id="6471e-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6471e-148">OUTPUTS</span></span>

### <span data-ttu-id="6471e-149">Microsoft. Azure. PowerShell. polecenia. HPCCache. models. PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="6471e-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="6471e-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6471e-150">NOTES</span></span>

## <span data-ttu-id="6471e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6471e-151">RELATED LINKS</span></span>
