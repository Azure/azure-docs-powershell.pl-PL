---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/update-azsynapsesqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Update-AzSynapseSqlDatabase.md
ms.openlocfilehash: a939ef485976a746e705de10a4706b03c63f910e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991887"
---
# <span data-ttu-id="6d005-101">Update-AzSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d005-101">Update-AzSynapseSqlDatabase</span></span>

## <span data-ttu-id="6d005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d005-102">SYNOPSIS</span></span>
<span data-ttu-id="6d005-103">Aktualizuje bazę danych Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="6d005-103">Updates a Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6d005-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6d005-104">SYNTAX</span></span>

### <span data-ttu-id="6d005-105">UpdateByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6d005-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzSynapseSqlDatabase [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-MaxSizeInBytes <Int64>] [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d005-106">UpdateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d005-106">UpdateByParentObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -Name <String> [-MaxSizeInBytes <Int64>] -WorkspaceObject <PSSynapseWorkspace>
 [-Tag <Hashtable>] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d005-107">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d005-107">UpdateByInputObjectParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -InputObject <PSSynapseSqlDatabase> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d005-108">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6d005-108">UpdateByResourceIdParameterSet</span></span>
```
Update-AzSynapseSqlDatabase -ResourceId <String> [-Tag <Hashtable>] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d005-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="6d005-109">DESCRIPTION</span></span>
<span data-ttu-id="6d005-110">Polecenie **cmdlet Update-AzSynapseSqlDatabase** aktualizuje bazę danych SQL Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="6d005-110">The **Update-AzSynapseSqlDatabase** cmdlet updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6d005-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6d005-111">EXAMPLES</span></span>

### <span data-ttu-id="6d005-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6d005-112">Example 1</span></span>
```powershell
PS C:\> Update-AzSynapseSqlDatabase -WorkspaceName ContosoWorkspace -Name ContosoSqlDatabase -Tag @{'key'='value'}
```

<span data-ttu-id="6d005-113">To polecenie aktualizuje bazę danych Azure Synapse Analytics SQL.</span><span class="sxs-lookup"><span data-stu-id="6d005-113">This command updates an Azure Synapse Analytics SQL database.</span></span>

## <span data-ttu-id="6d005-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d005-114">PARAMETERS</span></span>

### <span data-ttu-id="6d005-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6d005-115">-AsJob</span></span>
<span data-ttu-id="6d005-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6d005-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d005-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d005-117">-DefaultProfile</span></span>
<span data-ttu-id="6d005-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6d005-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d005-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d005-119">-InputObject</span></span>
<span data-ttu-id="6d005-120">Obiekt wejściowy bazy danych SQL, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="6d005-120">SQL Database input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d005-121">-MaxSizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6d005-121">-MaxSizeInBytes</span></span>
<span data-ttu-id="6d005-122">Określa maksymalny rozmiar bazy danych (w bajtach).</span><span class="sxs-lookup"><span data-stu-id="6d005-122">Specifies the maximum size of the database in bytes.</span></span>

```yaml
Type: System.Int64
Parameter Sets: UpdateByNameParameterSet, UpdateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d005-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6d005-123">-Name</span></span>
<span data-ttu-id="6d005-124">Nazwa bazy danych Synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6d005-124">Name of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="6d005-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d005-125">-PassThru</span></span>
<span data-ttu-id="6d005-126">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="6d005-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="6d005-127">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="6d005-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6d005-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d005-128">-ResourceGroupName</span></span>
<span data-ttu-id="6d005-129">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6d005-129">Resource group name.</span></span>

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

### <span data-ttu-id="6d005-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6d005-130">-ResourceId</span></span>
<span data-ttu-id="6d005-131">Identyfikator zasobu synapse SQL Database.</span><span class="sxs-lookup"><span data-stu-id="6d005-131">Resource identifier of Synapse SQL Database.</span></span>

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

### <span data-ttu-id="6d005-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="6d005-132">-Tag</span></span>
<span data-ttu-id="6d005-133">A string,string dictionary of tags associated with the resource.</span><span class="sxs-lookup"><span data-stu-id="6d005-133">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="6d005-134">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6d005-134">-WorkspaceName</span></span>
<span data-ttu-id="6d005-135">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="6d005-135">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="6d005-136">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6d005-136">-WorkspaceObject</span></span>
<span data-ttu-id="6d005-137">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="6d005-137">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="6d005-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6d005-138">-Confirm</span></span>
<span data-ttu-id="6d005-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6d005-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d005-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d005-140">-WhatIf</span></span>
<span data-ttu-id="6d005-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d005-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d005-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6d005-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d005-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d005-143">CommonParameters</span></span>
<span data-ttu-id="6d005-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d005-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d005-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d005-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d005-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d005-146">INPUTS</span></span>

### <span data-ttu-id="6d005-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="6d005-147">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="6d005-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d005-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="6d005-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6d005-149">OUTPUTS</span></span>

### <span data-ttu-id="6d005-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6d005-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlDatabase</span></span>

## <span data-ttu-id="6d005-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6d005-151">NOTES</span></span>

## <span data-ttu-id="6d005-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6d005-152">RELATED LINKS</span></span>
