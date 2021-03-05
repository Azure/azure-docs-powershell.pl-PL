---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: fe13a82a6662b0f8e9578f4f0fd5143b350538c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959953"
---
# <span data-ttu-id="25e89-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="25e89-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="25e89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e89-102">SYNOPSIS</span></span>
<span data-ttu-id="25e89-103">Aktualizuje pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="25e89-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="25e89-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="25e89-104">SYNTAX</span></span>

### <span data-ttu-id="25e89-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="25e89-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e89-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25e89-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e89-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="25e89-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25e89-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="25e89-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e89-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="25e89-109">DESCRIPTION</span></span>
<span data-ttu-id="25e89-110">Polecenie **cmdlet Update-AzSynapseSqlPool** aktualizuje pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="25e89-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="25e89-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="25e89-111">EXAMPLES</span></span>

### <span data-ttu-id="25e89-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="25e89-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="25e89-113">To polecenie aktualizuje pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="25e89-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="25e89-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="25e89-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="25e89-115">To polecenie aktualizuje pulę języka SQL Azure Synapse Analytics za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="25e89-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="25e89-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="25e89-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="25e89-117">To polecenie aktualizuje pulę języka SQL Azure Synapse Analytics za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="25e89-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="25e89-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="25e89-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="25e89-119">To polecenie aktualizuje pulę sql usługi Azure Synapse Analytics o identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="25e89-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="25e89-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e89-120">PARAMETERS</span></span>

### <span data-ttu-id="25e89-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="25e89-121">-AsJob</span></span>
<span data-ttu-id="25e89-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="25e89-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25e89-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e89-123">-DefaultProfile</span></span>
<span data-ttu-id="25e89-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="25e89-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e89-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="25e89-125">-InputObject</span></span>
<span data-ttu-id="25e89-126">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="25e89-126">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="25e89-127">-Name</span></span>
<span data-ttu-id="25e89-128">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="25e89-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e89-129">-PassThru</span></span>
<span data-ttu-id="25e89-130">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="25e89-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="25e89-131">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="25e89-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="25e89-132">- PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="25e89-132">-PerformanceLevel</span></span>
<span data-ttu-id="25e89-133">Warstwa i poziom wydajności usługi SQL, które można przypisać do puli sql.</span><span class="sxs-lookup"><span data-stu-id="25e89-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="25e89-134">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="25e89-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e89-135">-ResourceGroupName</span></span>
<span data-ttu-id="25e89-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25e89-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25e89-137">-ResourceId</span></span>
<span data-ttu-id="25e89-138">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="25e89-138">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-139">— Tag</span><span class="sxs-lookup"><span data-stu-id="25e89-139">-Tag</span></span>
<span data-ttu-id="25e89-140">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="25e89-140">A string,string dictionary of tags associated with the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-141">— Wersja</span><span class="sxs-lookup"><span data-stu-id="25e89-141">-Version</span></span>
<span data-ttu-id="25e89-142">Wersja puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="25e89-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="25e89-143">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="25e89-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="25e89-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="25e89-144">-WorkspaceName</span></span>
<span data-ttu-id="25e89-145">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="25e89-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-146">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="25e89-146">-WorkspaceObject</span></span>
<span data-ttu-id="25e89-147">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="25e89-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="25e89-148">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25e89-148">-Confirm</span></span>
<span data-ttu-id="25e89-149">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25e89-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e89-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e89-150">-WhatIf</span></span>
<span data-ttu-id="25e89-151">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25e89-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e89-152">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="25e89-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e89-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e89-153">CommonParameters</span></span>
<span data-ttu-id="25e89-154">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e89-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e89-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25e89-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e89-156">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25e89-156">INPUTS</span></span>

### <span data-ttu-id="25e89-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="25e89-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="25e89-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="25e89-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="25e89-159">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25e89-159">OUTPUTS</span></span>

### <span data-ttu-id="25e89-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="25e89-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="25e89-161">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="25e89-161">NOTES</span></span>

## <span data-ttu-id="25e89-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25e89-162">RELATED LINKS</span></span>
