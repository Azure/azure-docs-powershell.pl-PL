---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/update-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlPool.md
ms.openlocfilehash: 79bd39616f33a50684827276c6af919990b269ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225281"
---
# <span data-ttu-id="a0673-101">Update-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a0673-101">Update-AzSynapseSqlPool</span></span>

## <span data-ttu-id="a0673-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0673-102">SYNOPSIS</span></span>
<span data-ttu-id="a0673-103">Aktualizuje pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a0673-103">Updates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a0673-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0673-104">SYNTAX</span></span>

### <span data-ttu-id="a0673-105">UpdateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0673-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0673-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0673-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool -Name <String> [-Version <Int32>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PerformanceLevel <String>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0673-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0673-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -InputObject <PSSynapseSqlPool> [-Tag <Hashtable>]
 [-PerformanceLevel <String>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0673-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0673-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlPool [-Version <Int32>] -ResourceId <String> [-Tag <Hashtable>] [-PerformanceLevel <String>]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0673-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a0673-109">DESCRIPTION</span></span>
<span data-ttu-id="a0673-110">Polecenie cmdlet **Update-AzSynapseSqlPool** AKTUALIZUJE pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a0673-110">The **Update-AzSynapseSqlPool** cmdlet updates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="a0673-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0673-111">EXAMPLES</span></span>

### <span data-ttu-id="a0673-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0673-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -Tag @{'key'='value'} -PerformanceLevel DW300c
```

<span data-ttu-id="a0673-113">To polecenie aktualizuje pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a0673-113">This command updates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="a0673-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a0673-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Update-AzSynapseSqlPool -Name ContosoSqlPool -Tag @{'key'='value1'}
```

<span data-ttu-id="a0673-115">To polecenie umożliwia zaktualizowanie puli SQL usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="a0673-115">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="a0673-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a0673-116">Example 3</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Update-AzSynapseSqlPool -Tag @{'key'='value2'}
```

<span data-ttu-id="a0673-117">To polecenie umożliwia zaktualizowanie puli SQL usługi Azure Synapse Analytics za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="a0673-117">This command updates an Azure Synapse Analytics SQL pool through pipeline.</span></span>

### <span data-ttu-id="a0673-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a0673-118">Example 4</span></span>
```powershell
PS C:\> Update-AzSynapseSqlPool -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd3/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool -Tag @{'key'='value3'}
```

<span data-ttu-id="a0673-119">To polecenie aktualizuje pulę SQL usługi Azure Synapse z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="a0673-119">This command updates an Azure Synapse Analytics SQL pool with resource ID.</span></span>

## <span data-ttu-id="a0673-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0673-120">PARAMETERS</span></span>

### <span data-ttu-id="a0673-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0673-121">-AsJob</span></span>
<span data-ttu-id="a0673-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a0673-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0673-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0673-123">-DefaultProfile</span></span>
<span data-ttu-id="a0673-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0673-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0673-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a0673-125">-InputObject</span></span>
<span data-ttu-id="a0673-126">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a0673-126">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a0673-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a0673-127">-Name</span></span>
<span data-ttu-id="a0673-128">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0673-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0673-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0673-129">-PassThru</span></span>
<span data-ttu-id="a0673-130">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a0673-130">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a0673-131">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="a0673-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a0673-132">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="a0673-132">-PerformanceLevel</span></span>
<span data-ttu-id="a0673-133">Warstwa usług SQL i poziom wydajności, które mają zostać przypisane do puli SQL.</span><span class="sxs-lookup"><span data-stu-id="a0673-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="a0673-134">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="a0673-134">For example, DW2000c.</span></span>

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

### <span data-ttu-id="a0673-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0673-135">-ResourceGroupName</span></span>
<span data-ttu-id="a0673-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0673-136">Resource group name.</span></span>

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

### <span data-ttu-id="a0673-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0673-137">-ResourceId</span></span>
<span data-ttu-id="a0673-138">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0673-138">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="a0673-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="a0673-139">-Tag</span></span>
<span data-ttu-id="a0673-140">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="a0673-140">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="a0673-141">-Version</span><span class="sxs-lookup"><span data-stu-id="a0673-141">-Version</span></span>
<span data-ttu-id="a0673-142">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0673-142">Version of Synapse SQL pool.</span></span> <span data-ttu-id="a0673-143">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="a0673-143">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="a0673-144">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="a0673-144">-WorkspaceName</span></span>
<span data-ttu-id="a0673-145">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="a0673-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a0673-146">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="a0673-146">-WorkspaceObject</span></span>
<span data-ttu-id="a0673-147">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="a0673-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a0673-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0673-148">-Confirm</span></span>
<span data-ttu-id="a0673-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0673-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0673-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0673-150">-WhatIf</span></span>
<span data-ttu-id="a0673-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0673-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0673-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0673-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0673-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0673-153">CommonParameters</span></span>
<span data-ttu-id="a0673-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0673-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0673-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0673-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0673-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0673-156">INPUTS</span></span>

### <span data-ttu-id="a0673-157">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a0673-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a0673-158">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a0673-158">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a0673-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0673-159">OUTPUTS</span></span>

### <span data-ttu-id="a0673-160">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a0673-160">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a0673-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0673-161">NOTES</span></span>

## <span data-ttu-id="a0673-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0673-162">RELATED LINKS</span></span>
