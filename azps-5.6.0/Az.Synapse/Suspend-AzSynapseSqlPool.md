---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/suspend-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Suspend-AzSynapseSqlPool.md
ms.openlocfilehash: d0249098c8414a38adecc4112449174496656b78
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011274"
---
# <span data-ttu-id="1fe63-101">Suspend-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1fe63-101">Suspend-AzSynapseSqlPool</span></span>

## <span data-ttu-id="1fe63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fe63-102">SYNOPSIS</span></span>
<span data-ttu-id="1fe63-103">Zawiesza pulę języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1fe63-103">Suspends a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1fe63-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1fe63-104">SYNTAX</span></span>

### <span data-ttu-id="1fe63-105">SuspendByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1fe63-105">SuspendByNameParameterSet (Default)</span></span>
```
Suspend-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe63-106">SuspendByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe63-106">SuspendByParentObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe63-107">SuspendByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe63-107">SuspendByInputObjectParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fe63-108">SuspendByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fe63-108">SuspendByResourceIdParameterSet</span></span>
```
Suspend-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fe63-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1fe63-109">DESCRIPTION</span></span>
<span data-ttu-id="1fe63-110">Polecenie cmdlet **Suspend-AzSynapseSqlPool** zawiesza pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1fe63-110">The **Suspend-AzSynapseSqlPool** cmdlet suspends an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1fe63-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1fe63-111">EXAMPLES</span></span>

### <span data-ttu-id="1fe63-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fe63-112">Example 1</span></span>
```powershell
PS C:\> Suspend-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="1fe63-113">To polecenie zawiesza aktywną pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="1fe63-113">This command suspends an active Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="1fe63-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fe63-114">PARAMETERS</span></span>

### <span data-ttu-id="1fe63-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1fe63-115">-AsJob</span></span>
<span data-ttu-id="1fe63-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1fe63-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fe63-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fe63-117">-DefaultProfile</span></span>
<span data-ttu-id="1fe63-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fe63-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fe63-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1fe63-119">-InputObject</span></span>
<span data-ttu-id="1fe63-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="1fe63-120">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1fe63-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1fe63-121">-Name</span></span>
<span data-ttu-id="1fe63-122">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="1fe63-122">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="1fe63-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fe63-123">-PassThru</span></span>
<span data-ttu-id="1fe63-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="1fe63-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1fe63-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="1fe63-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="1fe63-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fe63-126">-ResourceGroupName</span></span>
<span data-ttu-id="1fe63-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1fe63-127">Resource group name.</span></span>

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

### <span data-ttu-id="1fe63-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fe63-128">-ResourceId</span></span>
<span data-ttu-id="1fe63-129">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="1fe63-129">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="1fe63-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1fe63-130">-WorkspaceName</span></span>
<span data-ttu-id="1fe63-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="1fe63-131">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="1fe63-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="1fe63-132">-WorkspaceObject</span></span>
<span data-ttu-id="1fe63-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="1fe63-133">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="1fe63-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fe63-134">-Confirm</span></span>
<span data-ttu-id="1fe63-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1fe63-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fe63-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fe63-136">-WhatIf</span></span>
<span data-ttu-id="1fe63-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fe63-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fe63-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1fe63-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fe63-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fe63-139">CommonParameters</span></span>
<span data-ttu-id="1fe63-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fe63-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fe63-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fe63-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fe63-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fe63-142">INPUTS</span></span>

### <span data-ttu-id="1fe63-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="1fe63-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="1fe63-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1fe63-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1fe63-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fe63-145">OUTPUTS</span></span>

### <span data-ttu-id="1fe63-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="1fe63-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="1fe63-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1fe63-147">NOTES</span></span>

## <span data-ttu-id="1fe63-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fe63-148">RELATED LINKS</span></span>
