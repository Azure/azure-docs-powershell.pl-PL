---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: d60997647ed4f6bb1317148daadcbe4c0e00a5c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013489"
---
# <span data-ttu-id="1f380-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="1f380-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="1f380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f380-102">SYNOPSIS</span></span>
<span data-ttu-id="1f380-103">Aktualizacja miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1f380-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="1f380-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f380-104">SYNTAX</span></span>

### <span data-ttu-id="1f380-105">ClfsParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1f380-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1f380-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f380-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1f380-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f380-107">DESCRIPTION</span></span>
<span data-ttu-id="1f380-108">Polecenie **cmdlet Set-AzHpcCacheStorageTarget** aktualizuje element docelowy magazynu dołączony do pamięci podręcznej AZURE HPC.</span><span class="sxs-lookup"><span data-stu-id="1f380-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="1f380-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f380-109">EXAMPLES</span></span>

### <span data-ttu-id="1f380-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f380-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="1f380-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1f380-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="1f380-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f380-112">PARAMETERS</span></span>

### <span data-ttu-id="1f380-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1f380-113">-AsJob</span></span>
<span data-ttu-id="1f380-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1f380-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1f380-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="1f380-115">-CacheName</span></span>
<span data-ttu-id="1f380-116">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="1f380-116">Name of cache.</span></span>

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

### <span data-ttu-id="1f380-117">— CLFS</span><span class="sxs-lookup"><span data-stu-id="1f380-117">-CLFS</span></span>
<span data-ttu-id="1f380-118">Aktualizowanie typu docelowego magazynu usługi CLFS.</span><span class="sxs-lookup"><span data-stu-id="1f380-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="1f380-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f380-119">-DefaultProfile</span></span>
<span data-ttu-id="1f380-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1f380-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f380-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1f380-121">-Force</span></span>
<span data-ttu-id="1f380-122">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f380-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="1f380-123">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie, że chcesz opróżnić pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="1f380-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="1f380-124">— Skrzyżowań</span><span class="sxs-lookup"><span data-stu-id="1f380-124">-Junction</span></span>
<span data-ttu-id="1f380-125">Skrzyżowań.</span><span class="sxs-lookup"><span data-stu-id="1f380-125">Junction.</span></span>

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

### <span data-ttu-id="1f380-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f380-126">-Name</span></span>
<span data-ttu-id="1f380-127">Nazwa miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1f380-127">Name of storage target.</span></span>

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

### <span data-ttu-id="1f380-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="1f380-128">-NFS</span></span>
<span data-ttu-id="1f380-129">Aktualizowanie typu docelowego miejsca do magazynowania systemu NFS.</span><span class="sxs-lookup"><span data-stu-id="1f380-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="1f380-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f380-130">-ResourceGroupName</span></span>
<span data-ttu-id="1f380-131">Nazwa grupy zasobów, w ramach której chcesz zaktualizować miejsce docelowe magazynu.</span><span class="sxs-lookup"><span data-stu-id="1f380-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="1f380-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1f380-132">-Confirm</span></span>
<span data-ttu-id="1f380-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1f380-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f380-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f380-134">-WhatIf</span></span>
<span data-ttu-id="1f380-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f380-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f380-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1f380-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f380-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f380-137">CommonParameters</span></span>
<span data-ttu-id="1f380-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f380-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f380-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1f380-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f380-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f380-140">INPUTS</span></span>

### <span data-ttu-id="1f380-141">System.String</span><span class="sxs-lookup"><span data-stu-id="1f380-141">System.String</span></span>

## <span data-ttu-id="1f380-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f380-142">OUTPUTS</span></span>

### <span data-ttu-id="1f380-143">Microsoft.Azure.PowerShell.Cmdlet.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="1f380-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="1f380-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f380-144">NOTES</span></span>

## <span data-ttu-id="1f380-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f380-145">RELATED LINKS</span></span>
