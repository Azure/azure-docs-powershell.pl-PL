---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198346"
---
# <span data-ttu-id="11d19-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11d19-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="11d19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11d19-102">SYNOPSIS</span></span>
<span data-ttu-id="11d19-103">Usuwa pulę języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="11d19-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="11d19-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11d19-104">SYNTAX</span></span>

### <span data-ttu-id="11d19-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="11d19-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11d19-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d19-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d19-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d19-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11d19-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11d19-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11d19-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="11d19-109">DESCRIPTION</span></span>
<span data-ttu-id="11d19-110">Polecenie **cmdlet Remove-AzSynapseSqlPool** trwale usuwa pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="11d19-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="11d19-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11d19-111">EXAMPLES</span></span>

### <span data-ttu-id="11d19-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11d19-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="11d19-113">To polecenie usuwa pulę sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="11d19-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="11d19-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11d19-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="11d19-115">To polecenie usuwa pulę języka SQL Synapse Analytics platformy Azure w potoku.</span><span class="sxs-lookup"><span data-stu-id="11d19-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="11d19-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="11d19-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="11d19-117">To polecenie usuwa pulę sql usługi Azure Synapse Analytics z potoku.</span><span class="sxs-lookup"><span data-stu-id="11d19-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="11d19-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="11d19-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="11d19-119">To polecenie usuwa pulę sql usługi Azure Synapse Analytics z określonym identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="11d19-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="11d19-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11d19-120">PARAMETERS</span></span>

### <span data-ttu-id="11d19-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11d19-121">-AsJob</span></span>
<span data-ttu-id="11d19-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="11d19-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11d19-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11d19-123">-DefaultProfile</span></span>
<span data-ttu-id="11d19-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11d19-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11d19-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="11d19-125">-Force</span></span>
<span data-ttu-id="11d19-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11d19-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="11d19-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="11d19-127">-InputObject</span></span>
<span data-ttu-id="11d19-128">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="11d19-128">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11d19-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11d19-129">-Name</span></span>
<span data-ttu-id="11d19-130">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="11d19-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d19-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="11d19-131">-PassThru</span></span>
<span data-ttu-id="11d19-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="11d19-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="11d19-133">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="11d19-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="11d19-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11d19-134">-ResourceGroupName</span></span>
<span data-ttu-id="11d19-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11d19-135">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d19-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11d19-136">-ResourceId</span></span>
<span data-ttu-id="11d19-137">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="11d19-137">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11d19-138">— Wersja</span><span class="sxs-lookup"><span data-stu-id="11d19-138">-Version</span></span>
<span data-ttu-id="11d19-139">Wersja puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="11d19-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="11d19-140">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="11d19-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="11d19-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11d19-141">-WorkspaceName</span></span>
<span data-ttu-id="11d19-142">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="11d19-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11d19-143">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11d19-143">-WorkspaceObject</span></span>
<span data-ttu-id="11d19-144">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="11d19-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11d19-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11d19-145">-Confirm</span></span>
<span data-ttu-id="11d19-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11d19-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11d19-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11d19-147">-WhatIf</span></span>
<span data-ttu-id="11d19-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11d19-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11d19-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11d19-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11d19-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11d19-150">CommonParameters</span></span>
<span data-ttu-id="11d19-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11d19-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11d19-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11d19-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11d19-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11d19-153">INPUTS</span></span>

### <span data-ttu-id="11d19-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11d19-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="11d19-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11d19-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="11d19-156">System.String</span><span class="sxs-lookup"><span data-stu-id="11d19-156">System.String</span></span>

## <span data-ttu-id="11d19-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="11d19-157">OUTPUTS</span></span>

### <span data-ttu-id="11d19-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="11d19-158">System.Boolean</span></span>

## <span data-ttu-id="11d19-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11d19-159">NOTES</span></span>

## <span data-ttu-id="11d19-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11d19-160">RELATED LINKS</span></span>
