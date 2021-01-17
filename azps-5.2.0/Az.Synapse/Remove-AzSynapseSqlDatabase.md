---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: 4951fbe707dbae8c1fdff34e828e468a2d3168bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337174"
---
# <span data-ttu-id="f9455-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9455-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="f9455-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9455-102">SYNOPSIS</span></span>
<span data-ttu-id="f9455-103">Usuwa bazę danych SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9455-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f9455-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9455-104">SYNTAX</span></span>

### <span data-ttu-id="f9455-105">DeleteByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9455-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9455-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9455-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9455-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9455-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9455-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9455-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9455-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f9455-109">DESCRIPTION</span></span>
<span data-ttu-id="f9455-110">Polecenie cmdlet **Remove-AzSynapseSqlPool** trwale usuwa bazę danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9455-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="f9455-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9455-111">EXAMPLES</span></span>

### <span data-ttu-id="f9455-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9455-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="f9455-113">To polecenie usuwa bazę danych SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f9455-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="f9455-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9455-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="f9455-115">To polecenie usuwa bazę danych SQL usługi Azure Synapse Analiza za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="f9455-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="f9455-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f9455-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="f9455-117">To polecenie usuwa bazę danych SQL usługi Azure Synapse Analiza za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="f9455-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="f9455-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f9455-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="f9455-119">To polecenie usuwa bazę danych SQL Azure Synapse Analytics z określonym IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="f9455-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="f9455-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9455-120">PARAMETERS</span></span>

### <span data-ttu-id="f9455-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9455-121">-AsJob</span></span>
<span data-ttu-id="f9455-122">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f9455-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9455-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9455-123">-DefaultProfile</span></span>
<span data-ttu-id="f9455-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9455-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9455-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f9455-125">-Force</span></span>
<span data-ttu-id="f9455-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f9455-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f9455-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9455-127">-InputObject</span></span>
<span data-ttu-id="f9455-128">Obiekt wejściowy SQL Database, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f9455-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f9455-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9455-129">-Name</span></span>
<span data-ttu-id="f9455-130">Nazwa bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f9455-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="f9455-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9455-131">-PassThru</span></span>
<span data-ttu-id="f9455-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f9455-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f9455-133">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="f9455-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f9455-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9455-134">-ResourceGroupName</span></span>
<span data-ttu-id="f9455-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9455-135">Resource group name.</span></span>

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

### <span data-ttu-id="f9455-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9455-136">-ResourceId</span></span>
<span data-ttu-id="f9455-137">Identyfikator zasobu bazy danych SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="f9455-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="f9455-138">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f9455-138">-WorkspaceName</span></span>
<span data-ttu-id="f9455-139">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f9455-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f9455-140">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="f9455-140">-WorkspaceObject</span></span>
<span data-ttu-id="f9455-141">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f9455-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f9455-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f9455-142">-Confirm</span></span>
<span data-ttu-id="f9455-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9455-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9455-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9455-144">-WhatIf</span></span>
<span data-ttu-id="f9455-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f9455-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f9455-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f9455-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9455-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9455-147">CommonParameters</span></span>
<span data-ttu-id="f9455-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9455-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9455-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f9455-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9455-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9455-150">INPUTS</span></span>

### <span data-ttu-id="f9455-151">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f9455-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="f9455-152">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f9455-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="f9455-153">System. String</span><span class="sxs-lookup"><span data-stu-id="f9455-153">System.String</span></span>

## <span data-ttu-id="f9455-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9455-154">OUTPUTS</span></span>

### <span data-ttu-id="f9455-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f9455-155">System.Boolean</span></span>

## <span data-ttu-id="f9455-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9455-156">NOTES</span></span>

## <span data-ttu-id="f9455-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9455-157">RELATED LINKS</span></span>
