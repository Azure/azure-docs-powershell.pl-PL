---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPool.md
ms.openlocfilehash: cd715bed20477fae4cbb17d033fd67fefa4e1cdc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222125"
---
# <span data-ttu-id="c8a32-101">Remove-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c8a32-101">Remove-AzSynapseSqlPool</span></span>

## <span data-ttu-id="c8a32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c8a32-102">SYNOPSIS</span></span>
<span data-ttu-id="c8a32-103">Usuwa pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8a32-103">Deletes a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c8a32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c8a32-104">SYNTAX</span></span>

### <span data-ttu-id="c8a32-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c8a32-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a32-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a32-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a32-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a32-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c8a32-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c8a32-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c8a32-109">Opis</span><span class="sxs-lookup"><span data-stu-id="c8a32-109">DESCRIPTION</span></span>
<span data-ttu-id="c8a32-110">Polecenie cmdlet **Remove-AzSynapseSqlPool** trwale usuwa pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8a32-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="c8a32-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c8a32-111">EXAMPLES</span></span>

### <span data-ttu-id="c8a32-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c8a32-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="c8a32-113">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="c8a32-113">This command deletes an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="c8a32-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c8a32-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlPool -Name ContosoSqlPool
```

<span data-ttu-id="c8a32-115">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="c8a32-115">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="c8a32-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="c8a32-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPool
```

<span data-ttu-id="c8a32-117">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics z rurociągiem.</span><span class="sxs-lookup"><span data-stu-id="c8a32-117">This command deletes an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="c8a32-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="c8a32-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool
```

<span data-ttu-id="c8a32-119">To polecenie usuwa pulę SQL usługi Azure Synapse Analytics o określonym IDENTYFIKATORze zasobu.</span><span class="sxs-lookup"><span data-stu-id="c8a32-119">This command deletes an Azure Synapse Analytics SQL pool with the specified resource ID.</span></span>

## <span data-ttu-id="c8a32-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c8a32-120">PARAMETERS</span></span>

### <span data-ttu-id="c8a32-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c8a32-121">-AsJob</span></span>
<span data-ttu-id="c8a32-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c8a32-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c8a32-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8a32-123">-DefaultProfile</span></span>
<span data-ttu-id="c8a32-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c8a32-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c8a32-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c8a32-125">-InputObject</span></span>
<span data-ttu-id="c8a32-126">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="c8a32-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c8a32-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c8a32-127">-Name</span></span>
<span data-ttu-id="c8a32-128">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8a32-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c8a32-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8a32-129">-PassThru</span></span>
<span data-ttu-id="c8a32-130">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="c8a32-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="c8a32-131">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="c8a32-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c8a32-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c8a32-132">-ResourceGroupName</span></span>
<span data-ttu-id="c8a32-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c8a32-133">Resource group name.</span></span>

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

### <span data-ttu-id="c8a32-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c8a32-134">-ResourceId</span></span>
<span data-ttu-id="c8a32-135">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8a32-135">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="c8a32-136">-Version</span><span class="sxs-lookup"><span data-stu-id="c8a32-136">-Version</span></span>
<span data-ttu-id="c8a32-137">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8a32-137">Version of Synapse SQL pool.</span></span> <span data-ttu-id="c8a32-138">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="c8a32-138">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="c8a32-139">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="c8a32-139">-WorkspaceName</span></span>
<span data-ttu-id="c8a32-140">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="c8a32-140">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c8a32-141">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="c8a32-141">-WorkspaceObject</span></span>
<span data-ttu-id="c8a32-142">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="c8a32-142">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c8a32-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c8a32-143">-Confirm</span></span>
<span data-ttu-id="c8a32-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a32-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c8a32-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c8a32-145">-WhatIf</span></span>
<span data-ttu-id="c8a32-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c8a32-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c8a32-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c8a32-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c8a32-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8a32-148">CommonParameters</span></span>
<span data-ttu-id="c8a32-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8a32-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8a32-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c8a32-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8a32-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c8a32-151">INPUTS</span></span>

### <span data-ttu-id="c8a32-152">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="c8a32-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="c8a32-153">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="c8a32-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="c8a32-154">System. String</span><span class="sxs-lookup"><span data-stu-id="c8a32-154">System.String</span></span>

## <span data-ttu-id="c8a32-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c8a32-155">OUTPUTS</span></span>

### <span data-ttu-id="c8a32-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c8a32-156">System.Boolean</span></span>

## <span data-ttu-id="c8a32-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c8a32-157">NOTES</span></span>

## <span data-ttu-id="c8a32-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c8a32-158">RELATED LINKS</span></span>
