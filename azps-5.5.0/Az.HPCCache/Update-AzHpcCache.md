---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237739"
---
# <span data-ttu-id="ca8c7-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="ca8c7-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="ca8c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ca8c7-103">Aktualizuje pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="ca8c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca8c7-104">SYNTAX</span></span>

### <span data-ttu-id="ca8c7-105">FlushParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca8c7-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8c7-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8c7-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8c7-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8c7-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca8c7-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca8c7-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca8c7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca8c7-109">DESCRIPTION</span></span>
<span data-ttu-id="ca8c7-110">Polecenie **cmdlet Update-azHpcCache** aktualizuje pamięć podręczną Azure HPC Cache.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="ca8c7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca8c7-111">EXAMPLES</span></span>

### <span data-ttu-id="ca8c7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca8c7-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="ca8c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca8c7-113">PARAMETERS</span></span>

### <span data-ttu-id="ca8c7-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ca8c7-114">-AsJob</span></span>
<span data-ttu-id="ca8c7-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ca8c7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca8c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca8c7-116">-DefaultProfile</span></span>
<span data-ttu-id="ca8c7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca8c7-118">— Opróżnij</span><span class="sxs-lookup"><span data-stu-id="ca8c7-118">-Flush</span></span>
<span data-ttu-id="ca8c7-119">Opróżnia pamięć podręczną HPC.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8c7-120">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ca8c7-120">-Force</span></span>
<span data-ttu-id="ca8c7-121">Wskazuje, że polecenie cmdlet nie wyświetla monitu o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="ca8c7-122">Domyślnie to polecenie cmdlet wyświetla monit o potwierdzenie, że chcesz zaktualizować pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="ca8c7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca8c7-123">-InputObject</span></span>
<span data-ttu-id="ca8c7-124">Obiekt pamięci podręcznej do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-124">The cache object to update.</span></span>

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

### <span data-ttu-id="ca8c7-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca8c7-125">-Name</span></span>
<span data-ttu-id="ca8c7-126">Nazwa pamięci podręcznej.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-126">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca8c7-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca8c7-127">-PassThru</span></span>
<span data-ttu-id="ca8c7-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ca8c7-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ca8c7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca8c7-130">-ResourceGroupName</span></span>
<span data-ttu-id="ca8c7-131">Nazwa grupy zasobów, w ramach której chcesz zaktualizować pamięć podręczną.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="ca8c7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca8c7-132">-ResourceId</span></span>
<span data-ttu-id="ca8c7-133">Identyfikator zasobu pamięci podręcznej</span><span class="sxs-lookup"><span data-stu-id="ca8c7-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="ca8c7-134">— uaktualnianie</span><span class="sxs-lookup"><span data-stu-id="ca8c7-134">-Upgrade</span></span>
<span data-ttu-id="ca8c7-135">Uaktualnij hpcCache.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca8c7-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ca8c7-136">-Confirm</span></span>
<span data-ttu-id="ca8c7-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca8c7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca8c7-138">-WhatIf</span></span>
<span data-ttu-id="ca8c7-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca8c7-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca8c7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca8c7-141">CommonParameters</span></span>
<span data-ttu-id="ca8c7-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca8c7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca8c7-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca8c7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca8c7-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca8c7-144">INPUTS</span></span>

### <span data-ttu-id="ca8c7-145">System.String</span><span class="sxs-lookup"><span data-stu-id="ca8c7-145">System.String</span></span>

## <span data-ttu-id="ca8c7-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ca8c7-146">OUTPUTS</span></span>

## <span data-ttu-id="ca8c7-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca8c7-147">NOTES</span></span>

## <span data-ttu-id="ca8c7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca8c7-148">RELATED LINKS</span></span>
