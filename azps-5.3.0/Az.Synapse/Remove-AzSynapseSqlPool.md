---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: 37ece1d86c4b41dbf8a185c0d4ed5d7117db8b2d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383369"
---
# <span data-ttu-id="2aafe-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2aafe-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="2aafe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2aafe-102">SYNOPSIS</span></span>
<span data-ttu-id="2aafe-103">Usuwa pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2aafe-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2aafe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2aafe-104">SYNTAX</span></span>

### <span data-ttu-id="2aafe-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2aafe-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2aafe-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aafe-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aafe-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aafe-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2aafe-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2aafe-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2aafe-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2aafe-109">DESCRIPTION</span></span>
<span data-ttu-id="2aafe-110">Polecenie cmdlet **Remove-AzSynapseSqlPool** trwale usuwa pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2aafe-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="2aafe-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2aafe-111">EXAMPLES</span></span>

### <span data-ttu-id="2aafe-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2aafe-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="2aafe-113">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="2aafe-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="2aafe-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2aafe-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="2aafe-115">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="2aafe-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="2aafe-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2aafe-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="2aafe-117">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="2aafe-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="2aafe-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="2aafe-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="2aafe-119">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics o określonym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="2aafe-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="2aafe-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2aafe-120">PARAMETERS</span></span>

### <span data-ttu-id="2aafe-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2aafe-121">-AsJob</span></span>
<span data-ttu-id="2aafe-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2aafe-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2aafe-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aafe-123">-DefaultProfile</span></span>
<span data-ttu-id="2aafe-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2aafe-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2aafe-125">-Force</span><span class="sxs-lookup"><span data-stu-id="2aafe-125">-Force</span></span>
<span data-ttu-id="2aafe-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2aafe-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2aafe-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2aafe-127">-InputObject</span></span>
<span data-ttu-id="2aafe-128">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2aafe-128">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2aafe-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2aafe-129">-Name</span></span>
<span data-ttu-id="2aafe-130">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2aafe-130">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="2aafe-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2aafe-131">-PassThru</span></span>
<span data-ttu-id="2aafe-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="2aafe-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="2aafe-133">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="2aafe-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="2aafe-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2aafe-134">-ResourceGroupName</span></span>
<span data-ttu-id="2aafe-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2aafe-135">Resource group name.</span></span>

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

### <span data-ttu-id="2aafe-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2aafe-136">-ResourceId</span></span>
<span data-ttu-id="2aafe-137">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2aafe-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="2aafe-138">-Version</span><span class="sxs-lookup"><span data-stu-id="2aafe-138">-Version</span></span>
<span data-ttu-id="2aafe-139">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="2aafe-139">Version of Synapse SQL pool.</span></span> <span data-ttu-id="2aafe-140">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="2aafe-140">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="2aafe-141">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="2aafe-141">-WorkspaceName</span></span>
<span data-ttu-id="2aafe-142">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="2aafe-142">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="2aafe-143">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="2aafe-143">-WorkspaceObject</span></span>
<span data-ttu-id="2aafe-144">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="2aafe-144">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="2aafe-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2aafe-145">-Confirm</span></span>
<span data-ttu-id="2aafe-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aafe-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2aafe-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2aafe-147">-WhatIf</span></span>
<span data-ttu-id="2aafe-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2aafe-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2aafe-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2aafe-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2aafe-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aafe-150">CommonParameters</span></span>
<span data-ttu-id="2aafe-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aafe-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aafe-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2aafe-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aafe-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aafe-153">INPUTS</span></span>

### <span data-ttu-id="2aafe-154">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="2aafe-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="2aafe-155">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="2aafe-155">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="2aafe-156">System. String</span><span class="sxs-lookup"><span data-stu-id="2aafe-156">System.String</span></span>

## <span data-ttu-id="2aafe-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2aafe-157">OUTPUTS</span></span>

### <span data-ttu-id="2aafe-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2aafe-158">System.Boolean</span></span>

## <span data-ttu-id="2aafe-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2aafe-159">NOTES</span></span>

## <span data-ttu-id="2aafe-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aafe-160">RELATED LINKS</span></span>
