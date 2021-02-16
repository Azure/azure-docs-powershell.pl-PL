---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: f0d06956c15b83511989b0ec5917918773f92293
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100243018"
---
# <span data-ttu-id="bb581-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bb581-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="bb581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb581-102">SYNOPSIS</span></span>
<span data-ttu-id="bb581-103">Zawiesza pulę języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb581-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bb581-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb581-104">SYNTAX</span></span>

### <span data-ttu-id="bb581-105">SuspendByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bb581-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb581-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb581-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb581-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb581-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bb581-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bb581-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bb581-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb581-109">DESCRIPTION</span></span>
<span data-ttu-id="bb581-110">Polecenie cmdlet **Suspend-AzSynapseSqlPool** zawiesza pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb581-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bb581-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb581-111">EXAMPLES</span></span>

### <span data-ttu-id="bb581-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bb581-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="bb581-113">To polecenie zawiesza aktywną pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="bb581-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bb581-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb581-114">PARAMETERS</span></span>

### <span data-ttu-id="bb581-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="bb581-115">-AsJob</span></span>
<span data-ttu-id="bb581-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bb581-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bb581-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb581-117">-DefaultProfile</span></span>
<span data-ttu-id="bb581-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb581-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb581-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bb581-119">-InputObject</span></span>
<span data-ttu-id="bb581-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="bb581-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SuspendByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb581-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb581-121">-Name</span></span>
<span data-ttu-id="bb581-122">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="bb581-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet, SuspendByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb581-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bb581-123">-PassThru</span></span>
<span data-ttu-id="bb581-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="bb581-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="bb581-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="bb581-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="bb581-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb581-126">-ResourceGroupName</span></span>
<span data-ttu-id="bb581-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bb581-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb581-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bb581-128">-ResourceId</span></span>
<span data-ttu-id="bb581-129">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="bb581-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb581-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bb581-130">-WorkspaceName</span></span>
<span data-ttu-id="bb581-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="bb581-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SuspendByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bb581-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bb581-132">-WorkspaceObject</span></span>
<span data-ttu-id="bb581-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="bb581-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SuspendByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bb581-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bb581-134">-Confirm</span></span>
<span data-ttu-id="bb581-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bb581-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bb581-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bb581-136">-WhatIf</span></span>
<span data-ttu-id="bb581-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb581-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bb581-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="bb581-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bb581-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb581-139">CommonParameters</span></span>
<span data-ttu-id="bb581-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb581-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb581-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bb581-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb581-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb581-142">INPUTS</span></span>

### <span data-ttu-id="bb581-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bb581-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bb581-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bb581-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bb581-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bb581-145">OUTPUTS</span></span>

### <span data-ttu-id="bb581-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bb581-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bb581-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb581-147">NOTES</span></span>

## <span data-ttu-id="bb581-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb581-148">RELATED LINKS</span></span>
