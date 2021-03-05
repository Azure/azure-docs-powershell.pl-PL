---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/resume-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Resume-AzSynapseSqlPool.md
ms.openlocfilehash: cfcfb283887e221db02c894f7a7712203e516996
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967153"
---
# <span data-ttu-id="5e565-101">Resume-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5e565-101">Resume-AzSynapseSqlPool</span></span>

## <span data-ttu-id="5e565-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e565-102">SYNOPSIS</span></span>
<span data-ttu-id="5e565-103">Wznawia pulę języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e565-103">Resumes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5e565-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e565-104">SYNTAX</span></span>

### <span data-ttu-id="5e565-105">ResumeByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5e565-105">ResumeByNameParameterSet (Default)</span></span>
```
Resume-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e565-106">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e565-106">ResumeByParentObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e565-107">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e565-107">ResumeByInputObjectParameterSet</span></span>
```
Resume-AzSynapseSqlPool -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e565-108">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e565-108">ResumeByResourceIdParameterSet</span></span>
```
Resume-AzSynapseSqlPool -ResourceId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e565-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e565-109">DESCRIPTION</span></span>
<span data-ttu-id="5e565-110">Polecenie **cmdlet Resume-AzSynapseSqlPool** wznawia pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e565-110">The **Resume-AzSynapseSqlPool** cmdlet resumes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5e565-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e565-111">EXAMPLES</span></span>

### <span data-ttu-id="5e565-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e565-112">Example 1</span></span>
```powershell
PS C:\> Resume-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="5e565-113">To polecenie wznawia zawieszoną pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5e565-113">This command resumes a suspended Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="5e565-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e565-114">PARAMETERS</span></span>

### <span data-ttu-id="5e565-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="5e565-115">-AsJob</span></span>
<span data-ttu-id="5e565-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5e565-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e565-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e565-117">-DefaultProfile</span></span>
<span data-ttu-id="5e565-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e565-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e565-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e565-119">-InputObject</span></span>
<span data-ttu-id="5e565-120">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="5e565-120">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: ResumeByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e565-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5e565-121">-Name</span></span>
<span data-ttu-id="5e565-122">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="5e565-122">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e565-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e565-123">-PassThru</span></span>
<span data-ttu-id="5e565-124">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="5e565-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5e565-125">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="5e565-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5e565-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e565-126">-ResourceGroupName</span></span>
<span data-ttu-id="5e565-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5e565-127">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e565-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5e565-128">-ResourceId</span></span>
<span data-ttu-id="5e565-129">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="5e565-129">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e565-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5e565-130">-WorkspaceName</span></span>
<span data-ttu-id="5e565-131">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="5e565-131">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e565-132">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5e565-132">-WorkspaceObject</span></span>
<span data-ttu-id="5e565-133">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="5e565-133">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e565-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e565-134">-Confirm</span></span>
<span data-ttu-id="5e565-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e565-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e565-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e565-136">-WhatIf</span></span>
<span data-ttu-id="5e565-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e565-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e565-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e565-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e565-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e565-139">CommonParameters</span></span>
<span data-ttu-id="5e565-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e565-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e565-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e565-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e565-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e565-142">INPUTS</span></span>

### <span data-ttu-id="5e565-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5e565-143">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5e565-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5e565-144">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5e565-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e565-145">OUTPUTS</span></span>

### <span data-ttu-id="5e565-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5e565-146">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5e565-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e565-147">NOTES</span></span>

## <span data-ttu-id="5e565-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e565-148">RELATED LINKS</span></span>
