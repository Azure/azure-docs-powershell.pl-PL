---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapsesqlpoolrestorepoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolRestorePoint.md
ms.openlocfilehash: 6105b043ee1e21ddbf2f29ce6bf0819639a133d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971610"
---
# <span data-ttu-id="ba358-101">Remove-AzSynapseSqlPoolRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ba358-101">Remove-AzSynapseSqlPoolRestorePoint</span></span>

## <span data-ttu-id="ba358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba358-102">SYNOPSIS</span></span>
<span data-ttu-id="ba358-103">Usuwa punkt przywracania puli języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ba358-103">Deletes a Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="ba358-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba358-104">SYNTAX</span></span>

### <span data-ttu-id="ba358-105">DeleteByNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ba358-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -RestorePointCreationDate <DateTime> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba358-106">DeleteByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba358-106">DeleteByParentObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -RestorePointCreationDate <DateTime> -SqlPoolObject <PSSynapseSqlPool>
 [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ba358-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba358-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -InputObject <PSRestorePoint> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba358-108">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba358-108">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzSynapseSqlPoolRestorePoint -ResourceId <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba358-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba358-109">DESCRIPTION</span></span>
<span data-ttu-id="ba358-110">Polecenie cmdlet **Remove-AzSynapseSqlPoolRestorePoint** trwale usuwa punkt przywracania puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ba358-110">The **Remove-AzSynapseSqlPoolRestorePoint** cmdlet permanently deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

## <span data-ttu-id="ba358-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba358-111">EXAMPLES</span></span>

### <span data-ttu-id="ba358-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba358-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="ba358-113">To polecenie usuwa punkt przywracania puli sql usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="ba358-113">This command deletes an Azure Synapse Analytics SQL pool restore point.</span></span>

### <span data-ttu-id="ba358-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ba358-114">Example 2</span></span>
```powershell
PS C:\> $pool = Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $pool | Remove-AzSynapseSqlPoolRestorePoint -Name ContosoSqlPoolRestorePointCreationDate
```

<span data-ttu-id="ba358-115">To polecenie usuwa punkt przywracania puli sql usługi Azure Synapse Analytics z potoku.</span><span class="sxs-lookup"><span data-stu-id="ba358-115">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="ba358-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ba358-116">Example 3</span></span>
```powershell
PS C:\> $points = Get-AzSynapseSqlPoolRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
PS C:\> $points[index] | Remove-AzSynapseSqlPoolRestorePoint
```

<span data-ttu-id="ba358-117">To polecenie usuwa punkt przywracania puli sql usługi Azure Synapse Analytics z potoku.</span><span class="sxs-lookup"><span data-stu-id="ba358-117">This command deletes an Azure Synapse Analytics SQL pool restore point through pipeline.</span></span>

### <span data-ttu-id="ba358-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="ba358-118">Example 4</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolRestorePoint -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlPools/ContosoSqlPool/SqlPoolRestorePoints/RestorePointCreationDate
```

<span data-ttu-id="ba358-119">To polecenie usuwa punkt przywracania puli sql usługi Azure Synapse Analytics z określonym identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="ba358-119">This command deletes an Azure Synapse Analytics SQL pool restore point with the specified resource ID.</span></span>

## <span data-ttu-id="ba358-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba358-120">PARAMETERS</span></span>

### <span data-ttu-id="ba358-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ba358-121">-AsJob</span></span>
<span data-ttu-id="ba358-122">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ba358-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ba358-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba358-123">-DefaultProfile</span></span>
<span data-ttu-id="ba358-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba358-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba358-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ba358-125">-Force</span></span>
<span data-ttu-id="ba358-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba358-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ba358-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba358-127">-InputObject</span></span>
<span data-ttu-id="ba358-128">Obiekt wejściowy czasu przywracania puli SQL (czas tworzenia punktów), który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="ba358-128">SQL pool restore point creation time input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba358-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ba358-129">-Name</span></span>
<span data-ttu-id="ba358-130">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="ba358-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: SqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba358-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba358-131">-PassThru</span></span>
<span data-ttu-id="ba358-132">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="ba358-132">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="ba358-133">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="ba358-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="ba358-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba358-134">-ResourceGroupName</span></span>
<span data-ttu-id="ba358-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba358-135">Resource group name.</span></span>

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

### <span data-ttu-id="ba358-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba358-136">-ResourceId</span></span>
<span data-ttu-id="ba358-137">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="ba358-137">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="ba358-138">-RestorePointCreationDate</span><span class="sxs-lookup"><span data-stu-id="ba358-138">-RestorePointCreationDate</span></span>
<span data-ttu-id="ba358-139">Nazwa daty utworzenia punktu przywracania języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="ba358-139">Name of Synapse SQL Restore Point Creation Date .</span></span>

```yaml
Type: System.DateTime
Parameter Sets: DeleteByNameParameterSet, DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba358-140">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="ba358-140">-SqlPoolObject</span></span>
<span data-ttu-id="ba358-141">Obiekt wejściowy puli sql, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="ba358-141">Sql Pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: DeleteByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba358-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ba358-142">-WorkspaceName</span></span>
<span data-ttu-id="ba358-143">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="ba358-143">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="ba358-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba358-144">-Confirm</span></span>
<span data-ttu-id="ba358-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba358-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba358-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba358-146">-WhatIf</span></span>
<span data-ttu-id="ba358-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba358-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba358-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ba358-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba358-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba358-149">CommonParameters</span></span>
<span data-ttu-id="ba358-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba358-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba358-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba358-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba358-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba358-152">INPUTS</span></span>

### <span data-ttu-id="ba358-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ba358-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="ba358-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="ba358-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

### <span data-ttu-id="ba358-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span><span class="sxs-lookup"><span data-stu-id="ba358-155">Microsoft.Azure.Commands.Synapse.Models.PSRestorePoint</span></span>

### <span data-ttu-id="ba358-156">System.String</span><span class="sxs-lookup"><span data-stu-id="ba358-156">System.String</span></span>

## <span data-ttu-id="ba358-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba358-157">OUTPUTS</span></span>

### <span data-ttu-id="ba358-158">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ba358-158">System.Boolean</span></span>

## <span data-ttu-id="ba358-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba358-159">NOTES</span></span>

## <span data-ttu-id="ba358-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba358-160">RELATED LINKS</span></span>
