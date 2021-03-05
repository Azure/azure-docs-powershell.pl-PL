---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlDatabase.md
ms.openlocfilehash: a60bcb20610449b9f76ff3e62684da43a2a792c8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959978"
---
# <span data-ttu-id="a45ff-101">Remove-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a45ff-101">Remove-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="a45ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a45ff-102">SYNOPSIS</span></span>
<span data-ttu-id="a45ff-103">Usuwa bazę danych Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="a45ff-103">Deletes a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a45ff-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a45ff-104">SYNTAX</span></span>

### <span data-ttu-id="a45ff-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a45ff-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-PassThru]
 [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a45ff-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45ff-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a45ff-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45ff-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a45ff-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a45ff-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlDatabase -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a45ff-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a45ff-109">DESCRIPTION</span></span>
<span data-ttu-id="a45ff-110">Polecenie **cmdlet Remove-AzSynapseSqlPool** trwale usuwa bazę danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="a45ff-110">The **Remove-AzSynapseSqlPool** cmdlet permanently deletes an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="a45ff-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a45ff-111">EXAMPLES</span></span>

### <span data-ttu-id="a45ff-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a45ff-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
```

<span data-ttu-id="a45ff-113">To polecenie usuwa bazę danych AZURE Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="a45ff-113">This command deletes an Azure Synapse Analytics SQL database.</span></span>

### <span data-ttu-id="a45ff-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a45ff-114">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseSqlDatabase -Name ContosoSqlDatabase
```

<span data-ttu-id="a45ff-115">To polecenie usuwa bazę danych Azure Synapse Analytics SQL w potoku.</span><span class="sxs-lookup"><span data-stu-id="a45ff-115">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="a45ff-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a45ff-116">Example 3</span></span>
```powershell
PS C:\> $database = Get-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase
PS C:\> $database | Remove-AzSynapseSqlDatabase
```

<span data-ttu-id="a45ff-117">To polecenie usuwa bazę danych Azure Synapse Analytics SQL w potoku.</span><span class="sxs-lookup"><span data-stu-id="a45ff-117">This command deletes an Azure Synapse Analytics SQL database through pipeline.</span></span>

### <span data-ttu-id="a45ff-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="a45ff-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlDatabase -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlDatabases/ContosoSqlDatabase
```

<span data-ttu-id="a45ff-119">To polecenie usuwa bazę danych AZURE Synapse Analytics SQL o określonym identyfikatorze zasobu.</span><span class="sxs-lookup"><span data-stu-id="a45ff-119">This command deletes an Azure Synapse Analytics SQL database with the specified resource ID.</span></span>

## <span data-ttu-id="a45ff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a45ff-120">PARAMETERS</span></span>

### <span data-ttu-id="a45ff-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="a45ff-121">-AsJob</span></span>
<span data-ttu-id="a45ff-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a45ff-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a45ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a45ff-123">-DefaultProfile</span></span>
<span data-ttu-id="a45ff-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a45ff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a45ff-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a45ff-125">-Force</span></span>
<span data-ttu-id="a45ff-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a45ff-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a45ff-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a45ff-127">-InputObject</span></span>
<span data-ttu-id="a45ff-128">Obiekt wejściowy bazy danych SQL, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a45ff-128">SQL Database input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a45ff-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a45ff-129">-Name</span></span>
<span data-ttu-id="a45ff-130">Nazwa bazy danych Synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a45ff-130">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="a45ff-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a45ff-131">-PassThru</span></span>
<span data-ttu-id="a45ff-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a45ff-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a45ff-133">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="a45ff-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a45ff-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a45ff-134">-ResourceGroupName</span></span>
<span data-ttu-id="a45ff-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a45ff-135">Resource group name.</span></span>

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

### <span data-ttu-id="a45ff-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a45ff-136">-ResourceId</span></span>
<span data-ttu-id="a45ff-137">Identyfikator zasobu synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="a45ff-137">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="a45ff-138">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a45ff-138">-WorkspaceName</span></span>
<span data-ttu-id="a45ff-139">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="a45ff-139">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a45ff-140">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a45ff-140">-WorkspaceObject</span></span>
<span data-ttu-id="a45ff-141">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="a45ff-141">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a45ff-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a45ff-142">-Confirm</span></span>
<span data-ttu-id="a45ff-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a45ff-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a45ff-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a45ff-144">-WhatIf</span></span>
<span data-ttu-id="a45ff-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a45ff-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a45ff-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a45ff-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a45ff-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a45ff-147">CommonParameters</span></span>
<span data-ttu-id="a45ff-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a45ff-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a45ff-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a45ff-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a45ff-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a45ff-150">INPUTS</span></span>

### <span data-ttu-id="a45ff-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a45ff-151">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="a45ff-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a45ff-152">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

### <span data-ttu-id="a45ff-153">System.String</span><span class="sxs-lookup"><span data-stu-id="a45ff-153">System.String</span></span>

## <span data-ttu-id="a45ff-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a45ff-154">OUTPUTS</span></span>

### <span data-ttu-id="a45ff-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a45ff-155">System.Boolean</span></span>

## <span data-ttu-id="a45ff-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a45ff-156">NOTES</span></span>

## <span data-ttu-id="a45ff-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a45ff-157">RELATED LINKS</span></span>
