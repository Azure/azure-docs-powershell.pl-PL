---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCacheStorageTarget.md
ms.openlocfilehash: fa799a05b76f9f6941b19bf171beb77318b77d39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196274"
---
# <span data-ttu-id="91a65-101">Set-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="91a65-101">Set-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="91a65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91a65-102">SYNOPSIS</span></span>
<span data-ttu-id="91a65-103">Aktualizacja miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="91a65-103">Updates a Storage Target.</span></span>

## <span data-ttu-id="91a65-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91a65-104">SYNTAX</span></span>

### <span data-ttu-id="91a65-105">ClfsParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="91a65-105">ClfsParameterSet (Default)</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-CLFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91a65-106">NfsParameterSet</span><span class="sxs-lookup"><span data-stu-id="91a65-106">NfsParameterSet</span></span>
```
Set-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-NFS]
 [-Junction <Hashtable[]>] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="91a65-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="91a65-107">DESCRIPTION</span></span>
<span data-ttu-id="91a65-108">Polecenie **cmdlet Set-AzHpcCacheStorageTarget** aktualizuje element docelowy magazynu dołączony do pamięci podręcznej HPC platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="91a65-108">The **Set-AzHpcCacheStorageTarget** cmdlet updates a Storage Target attached to Azure HPC cache.</span></span>

## <span data-ttu-id="91a65-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91a65-109">EXAMPLES</span></span>

### <span data-ttu-id="91a65-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="91a65-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -CLFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/"})
```

### <span data-ttu-id="91a65-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="91a65-111">Example 2</span></span>
```powershell
PS C:\> Set-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST -NFS -Junction @(@{"namespacePath"="/msazure";"targetPath"="/";"nfsExport"="/export"})
```

## <span data-ttu-id="91a65-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91a65-112">PARAMETERS</span></span>

### <span data-ttu-id="91a65-113">— AsJob</span><span class="sxs-lookup"><span data-stu-id="91a65-113">-AsJob</span></span>
<span data-ttu-id="91a65-114">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="91a65-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="91a65-115">-CacheName</span><span class="sxs-lookup"><span data-stu-id="91a65-115">-CacheName</span></span>
<span data-ttu-id="91a65-116">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="91a65-116">Name of cache.</span></span>

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

### <span data-ttu-id="91a65-117">— CLFS</span><span class="sxs-lookup"><span data-stu-id="91a65-117">-CLFS</span></span>
<span data-ttu-id="91a65-118">Aktualizowanie typu docelowego magazynu usługi CLFS.</span><span class="sxs-lookup"><span data-stu-id="91a65-118">Update CLFS Storage Target type.</span></span>

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

### <span data-ttu-id="91a65-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91a65-119">-DefaultProfile</span></span>
<span data-ttu-id="91a65-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91a65-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91a65-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="91a65-121">-Force</span></span>
<span data-ttu-id="91a65-122">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91a65-122">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="91a65-123">Domyślnie to polecenie cmdlet monituje o potwierdzenie, że chcesz opróżnić pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="91a65-123">By default, this cmdlet prompts you to confirm that you want to flush the cache.</span></span>

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

### <span data-ttu-id="91a65-124">— Skrzyżowań</span><span class="sxs-lookup"><span data-stu-id="91a65-124">-Junction</span></span>
<span data-ttu-id="91a65-125">Skrzyżowań.</span><span class="sxs-lookup"><span data-stu-id="91a65-125">Junction.</span></span>

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

### <span data-ttu-id="91a65-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91a65-126">-Name</span></span>
<span data-ttu-id="91a65-127">Nazwa miejsca docelowego magazynowania.</span><span class="sxs-lookup"><span data-stu-id="91a65-127">Name of storage target.</span></span>

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

### <span data-ttu-id="91a65-128">-NFS</span><span class="sxs-lookup"><span data-stu-id="91a65-128">-NFS</span></span>
<span data-ttu-id="91a65-129">Aktualizowanie typu docelowego miejsca do magazynowania systemu NFS.</span><span class="sxs-lookup"><span data-stu-id="91a65-129">Update NFS Storage Target type.</span></span>

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

### <span data-ttu-id="91a65-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91a65-130">-ResourceGroupName</span></span>
<span data-ttu-id="91a65-131">Nazwa grupy zasobów, w ramach której chcesz zaktualizować miejsce docelowe magazynu.</span><span class="sxs-lookup"><span data-stu-id="91a65-131">Name of resource group under which you want to update storage target.</span></span>

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

### <span data-ttu-id="91a65-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91a65-132">-Confirm</span></span>
<span data-ttu-id="91a65-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="91a65-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91a65-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91a65-134">-WhatIf</span></span>
<span data-ttu-id="91a65-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91a65-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91a65-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="91a65-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91a65-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91a65-137">CommonParameters</span></span>
<span data-ttu-id="91a65-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91a65-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91a65-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91a65-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91a65-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91a65-140">INPUTS</span></span>

### <span data-ttu-id="91a65-141">System.String</span><span class="sxs-lookup"><span data-stu-id="91a65-141">System.String</span></span>

## <span data-ttu-id="91a65-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91a65-142">OUTPUTS</span></span>

### <span data-ttu-id="91a65-143">Microsoft.Azure.PowerShell.Cmdlet.HPCCache.Models.PsHpcStorageTarget</span><span class="sxs-lookup"><span data-stu-id="91a65-143">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PsHpcStorageTarget</span></span>

## <span data-ttu-id="91a65-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91a65-144">NOTES</span></span>

## <span data-ttu-id="91a65-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91a65-145">RELATED LINKS</span></span>
