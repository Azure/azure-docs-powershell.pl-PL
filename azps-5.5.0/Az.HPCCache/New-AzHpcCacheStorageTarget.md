---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCacheStorageTarget.md
ms.openlocfilehash: eee07c01b0c9e0e2b072787d0d37a6a868fbf150
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243443"
---
# <span data-ttu-id="b257b-101">New-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b257b-101">New-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="b257b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b257b-102">SYNOPSIS</span></span>
<span data-ttu-id="b257b-103">Tworzy miejsce docelowe miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="b257b-103">Creates a Storage Target.</span></span>

## <span data-ttu-id="b257b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b257b-104">SYNTAX</span></span>

### <span data-ttu-id="b257b-105">ClfsParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b257b-105">ClfsParameterSet (Default)</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-StorageContainerID <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b257b-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="b257b-106">NfsParameterSet</span></span>
```
New-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-HostName <String>] [-UsageModel <String>] [-Junction <Hashtable[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b257b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b257b-107">DESCRIPTION</span></span>
<span data-ttu-id="b257b-108">Polecenie **cmdlet New-azHpcCacheStorageTarget** dodaje element docelowy magazynu do pamięci podręcznej Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="b257b-108">The **New-AzHpcCacheStorageTarget** cmdlet adds a Storage Target to Azure HPC Cache.</span></span>

## <span data-ttu-id="b257b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b257b-109">EXAMPLES</span></span>

### <span data-ttu-id="b257b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b257b-110">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -StorageContainerID "/subscriptions/testsub/resourceGroups/testRG/providers/Microsoft.Storage/storageAccounts/testdstorageaccount/blobServices/default/containers/testcontainer" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="b257b-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b257b-111">Example 2</span></span>
```powershell
PS C:\> New-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -UsageModel "READ_HEAVY_INFREQ" -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

## <span data-ttu-id="b257b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b257b-112">PARAMETERS</span></span>

### <span data-ttu-id="b257b-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b257b-113">-AsJob</span></span>
<span data-ttu-id="b257b-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b257b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b257b-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="b257b-115">-CacheName</span></span>
<span data-ttu-id="b257b-116">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b257b-116">Name of cache.</span></span>

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

### <span data-ttu-id="b257b-117">— CLFS</span><span class="sxs-lookup"><span data-stu-id="b257b-117">-CLFS</span></span>
<span data-ttu-id="b257b-118">Aktualizowanie typu docelowego magazynu usługi CLFS.</span><span class="sxs-lookup"><span data-stu-id="b257b-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="b257b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b257b-119">-DefaultProfile</span></span>
<span data-ttu-id="b257b-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b257b-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b257b-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b257b-121">-Force</span></span>
<span data-ttu-id="b257b-122">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b257b-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="b257b-123">Domyślnie to polecenie cmdlet monituje o potwierdzenie, że chcesz opróżnić pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="b257b-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="b257b-124">-HostName</span><span class="sxs-lookup"><span data-stu-id="b257b-124">-HostName</span></span>
<span data-ttu-id="b257b-125">Nazwa hosta systemu NFS.</span><span class="sxs-lookup"><span data-stu-id="b257b-125">NFS host name.</span></span>

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

### <span data-ttu-id="b257b-126">— Skrzyżowań</span><span class="sxs-lookup"><span data-stu-id="b257b-126">-Junction</span></span>
<span data-ttu-id="b257b-127">Skrzyżowań.</span><span class="sxs-lookup"><span data-stu-id="b257b-127">Junction.</span></span>

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

### <span data-ttu-id="b257b-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b257b-128">-Name</span></span>
<span data-ttu-id="b257b-129">Nazwa miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="b257b-129">Name of storage target.</span></span>

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

### <span data-ttu-id="b257b-130">-NFS</span><span class="sxs-lookup"><span data-stu-id="b257b-130">-NFS</span></span>
<span data-ttu-id="b257b-131">Aktualizowanie typu docelowego miejsca do magazynowania systemu NFS.</span><span class="sxs-lookup"><span data-stu-id="b257b-131">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="b257b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b257b-132">-ResourceGroupName</span></span>
<span data-ttu-id="b257b-133">"Nazwa grupy zasobów, w ramach której chcesz utworzyć miejsce docelowe miejsca do magazynowania dla danej pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="b257b-133">"Name of resource group under which you want to create storage target for given cache.</span></span>

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

### <span data-ttu-id="b257b-134">- StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="b257b-134">-StorageContainerID</span></span>
<span data-ttu-id="b257b-135">StorageContainerID</span><span class="sxs-lookup"><span data-stu-id="b257b-135">StorageContainerID</span></span>

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

### <span data-ttu-id="b257b-136">-UsageModel</span><span class="sxs-lookup"><span data-stu-id="b257b-136">-UsageModel</span></span>
<span data-ttu-id="b257b-137">Model użycia systemu NFS.</span><span class="sxs-lookup"><span data-stu-id="b257b-137">NFS usage model.</span></span>

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

### <span data-ttu-id="b257b-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b257b-138">-Confirm</span></span>
<span data-ttu-id="b257b-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b257b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b257b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b257b-140">-WhatIf</span></span>
<span data-ttu-id="b257b-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b257b-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b257b-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b257b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b257b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b257b-143">CommonParameters</span></span>
<span data-ttu-id="b257b-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b257b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b257b-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b257b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b257b-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b257b-146">INPUTS</span></span>

### <span data-ttu-id="b257b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="b257b-147">System.String</span></span>

## <span data-ttu-id="b257b-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b257b-148">OUTPUTS</span></span>

### <span data-ttu-id="b257b-149">Microsoft.Azure.PowerShell.Cmdlet.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="b257b-149">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="b257b-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b257b-150">NOTES</span></span>

## <span data-ttu-id="b257b-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b257b-151">RELATED LINKS</span></span>
