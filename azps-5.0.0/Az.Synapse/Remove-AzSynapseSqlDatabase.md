---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 2525792f7696c69a03a926850eaea20267d14fbf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231606"
---
# <span data-ttu-id="5c6eb-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c6eb-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="5c6eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="5c6eb-103">Usuwa bazę danych SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="5c6eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c6eb-104">SYNTAX</span></span>

### <span data-ttu-id="5c6eb-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5c6eb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c6eb-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c6eb-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c6eb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c6eb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c6eb-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c6eb-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c6eb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5c6eb-109">DESCRIPTION</span></span>
<span data-ttu-id="5c6eb-110">Polecenie cmdlet **Remove-AzSynapseSqlPool** trwale usuwa bazę danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>


## <span data-ttu-id="5c6eb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c6eb-111">EXAMPLES</span></span>

### <span data-ttu-id="5c6eb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5c6eb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="5c6eb-113">To polecenie usuwa bazę danych SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="5c6eb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5c6eb-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="5c6eb-115">To polecenie usuwa bazę danych SQL usługi Azure Synapse Analiza za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="5c6eb-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="5c6eb-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="5c6eb-117">To polecenie usuwa bazę danych SQL usługi Azure Synapse Analiza za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="5c6eb-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="5c6eb-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="5c6eb-119">To polecenie usuwa bazę danych SQL Azure Synapse Analytics z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="5c6eb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c6eb-120">PARAMETERS</span></span>

### <span data-ttu-id="5c6eb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c6eb-121">-AsJob</span></span>
<span data-ttu-id="5c6eb-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="5c6eb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c6eb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c6eb-123">-DefaultProfile</span></span>
<span data-ttu-id="5c6eb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c6eb-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5c6eb-125">-InputObject</span></span>
<span data-ttu-id="5c6eb-126">Obiekt wejściowy SQL Database, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-126">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c6eb-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c6eb-127">-Name</span></span>
<span data-ttu-id="5c6eb-128">Nazwa bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-128">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="5c6eb-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c6eb-129">-PassThru</span></span>
<span data-ttu-id="5c6eb-130">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-130">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5c6eb-131">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-131">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5c6eb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c6eb-132">-ResourceGroupName</span></span>
<span data-ttu-id="5c6eb-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-133">Resource group name.</span></span>

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

### <span data-ttu-id="5c6eb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c6eb-134">-ResourceId</span></span>
<span data-ttu-id="5c6eb-135">Identyfikator zasobu bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-135">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="5c6eb-136">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="5c6eb-136">-WorkspaceName</span></span>
<span data-ttu-id="5c6eb-137">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5c6eb-138">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="5c6eb-138">-WorkspaceObject</span></span>
<span data-ttu-id="5c6eb-139">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5c6eb-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5c6eb-140">-Confirm</span></span>
<span data-ttu-id="5c6eb-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c6eb-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c6eb-142">-WhatIf</span></span>
<span data-ttu-id="5c6eb-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c6eb-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c6eb-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c6eb-145">CommonParameters</span></span>
<span data-ttu-id="5c6eb-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c6eb-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c6eb-147">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c6eb-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c6eb-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c6eb-148">INPUTS</span></span>

### <span data-ttu-id="5c6eb-149">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="5c6eb-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="5c6eb-150">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5c6eb-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="5c6eb-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5c6eb-151">System.String</span></span>

## <span data-ttu-id="5c6eb-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c6eb-152">OUTPUTS</span></span>

### <span data-ttu-id="5c6eb-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c6eb-153">System.Boolean</span></span>

## <span data-ttu-id="5c6eb-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c6eb-154">NOTES</span></span>

## <span data-ttu-id="5c6eb-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c6eb-155">RELATED LINKS</span></span>
