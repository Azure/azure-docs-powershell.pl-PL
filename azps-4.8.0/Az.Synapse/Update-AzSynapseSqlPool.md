---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 62b1e0ef03d52337c03506d3bddc8bbfd3d5512d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222423"
---
# <span data-ttu-id="7fd4c-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7fd4c-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="7fd4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fd4c-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd4c-103">Aktualizuje pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7fd4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fd4c-104">SYNTAX</span></span>

### <span data-ttu-id="7fd4c-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7fd4c-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-106">PauseByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-106">PauseByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Suspend] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-107">ResumeByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-107">ResumeByNameParameterSet</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Resume] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-108">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-108">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-109">PauseByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-109">PauseByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Suspend] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-110">ResumeByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-110">ResumeByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] [-Resume] -WorkspaceObject <PSSynapseWorkspace>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-111">PauseByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-111">PauseByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-112">PauseByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-112">PauseByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Suspend] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-113">ResumeByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-113">ResumeByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-114">ResumeByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-114">ResumeByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] [-Resume] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-115">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-115">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fd4c-116">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fd4c-116">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fd4c-117">Opis</span><span class="sxs-lookup"><span data-stu-id="7fd4c-117">DESCRIPTION</span></span>
<span data-ttu-id="7fd4c-118">Polecenie cmdlet **Update-AzSynapseSqlPool** AKTUALIZUJE pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-118">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="7fd4c-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fd4c-119">EXAMPLES</span></span>

### <span data-ttu-id="7fd4c-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fd4c-120">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="7fd4c-121">To polecenie aktualizuje pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-121">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="7fd4c-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7fd4c-122">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="7fd4c-123">To polecenie umożliwia zaktualizowanie puli SQL usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-123">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="7fd4c-124">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7fd4c-124">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="7fd4c-125">To polecenie umożliwia zaktualizowanie puli SQL usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-125">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="7fd4c-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="7fd4c-126">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="7fd4c-127">To polecenie aktualizuje pulę SQL usługi Azure Synapse z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-127">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="7fd4c-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fd4c-128">PARAMETERS</span></span>

### <span data-ttu-id="7fd4c-129">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fd4c-129">-AsJob</span></span>
<span data-ttu-id="7fd4c-130">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="7fd4c-130">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7fd4c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd4c-131">-DefaultProfile</span></span>
<span data-ttu-id="7fd4c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd4c-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7fd4c-133">-InputObject</span></span>
<span data-ttu-id="7fd4c-134">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-134">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: PauseByInputObjectParameterSet, ResumeByInputObjectParameterSet, UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7fd4c-135">-Name</span></span>
<span data-ttu-id="7fd4c-136">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-136">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet, UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-137">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fd4c-137">-PassThru</span></span>
<span data-ttu-id="7fd4c-138">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-138">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="7fd4c-139">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-139">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="7fd4c-140">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="7fd4c-140">-PerformanceLevel</span></span>
<span data-ttu-id="7fd4c-141">Warstwa usług SQL i poziom wydajności, które mają zostać przypisane do puli SQL.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-141">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="7fd4c-142">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-142">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd4c-143">-ResourceGroupName</span></span>
<span data-ttu-id="7fd4c-144">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-144">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fd4c-145">-ResourceId</span></span>
<span data-ttu-id="7fd4c-146">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-146">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: PauseByResourceIdParameterSet, ResumeByResourceIdParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-147">-Życiorys</span><span class="sxs-lookup"><span data-stu-id="7fd4c-147">-Resume</span></span>
<span data-ttu-id="7fd4c-148">Wskazuje, że należy wznowić pulę SQL</span><span class="sxs-lookup"><span data-stu-id="7fd4c-148">Indicates to resume the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResumeByNameParameterSet, ResumeByParentObjectParameterSet, ResumeByInputObjectParameterSet, ResumeByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-149">-Suspend</span><span class="sxs-lookup"><span data-stu-id="7fd4c-149">-Suspend</span></span>
<span data-ttu-id="7fd4c-150">Wskazuje, że należy wstrzymać pulę SQL</span><span class="sxs-lookup"><span data-stu-id="7fd4c-150">Indicates to pause the SQL pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PauseByNameParameterSet, PauseByParentObjectParameterSet, PauseByInputObjectParameterSet, PauseByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-151">-Tag</span><span class="sxs-lookup"><span data-stu-id="7fd4c-151">-Tag</span></span>
<span data-ttu-id="7fd4c-152">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-152">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet, UpdateByInputObjectParameterSet, UpdateByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-153">-Version</span><span class="sxs-lookup"><span data-stu-id="7fd4c-153">-Version</span></span>
<span data-ttu-id="7fd4c-154">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-154">Version of Synapse SQL pool.</span></span> <span data-ttu-id="7fd4c-155">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-155">For example, 2 or 3.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-156">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="7fd4c-156">-WorkspaceName</span></span>
<span data-ttu-id="7fd4c-157">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-157">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, PauseByNameParameterSet, ResumeByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-158">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="7fd4c-158">-WorkspaceObject</span></span>
<span data-ttu-id="7fd4c-159">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-159">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet, PauseByParentObjectParameterSet, ResumeByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd4c-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7fd4c-160">-Confirm</span></span>
<span data-ttu-id="7fd4c-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-161">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd4c-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd4c-162">-WhatIf</span></span>
<span data-ttu-id="7fd4c-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd4c-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-164">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd4c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd4c-165">CommonParameters</span></span>
<span data-ttu-id="7fd4c-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd4c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd4c-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fd4c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd4c-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fd4c-168">INPUTS</span></span>

### <span data-ttu-id="7fd4c-169">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="7fd4c-169">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="7fd4c-170">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7fd4c-170">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7fd4c-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fd4c-171">OUTPUTS</span></span>

### <span data-ttu-id="7fd4c-172">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7fd4c-172">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7fd4c-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fd4c-173">NOTES</span></span>

## <span data-ttu-id="7fd4c-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fd4c-174">RELATED LINKS</span></span>
