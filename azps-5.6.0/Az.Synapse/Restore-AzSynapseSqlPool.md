---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 3a9620a6b5fa68fc2d4e5baf647d8dc720d787a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995856"
---
# <span data-ttu-id="11b83-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11b83-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="11b83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b83-102">SYNOPSIS</span></span>
<span data-ttu-id="11b83-103">Przywraca pulę języka SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="11b83-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="11b83-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="11b83-104">SYNTAX</span></span>

### <span data-ttu-id="11b83-105">RestoreFromBackupIdByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="11b83-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11b83-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b83-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="11b83-107">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b83-107">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11b83-108">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="11b83-108">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 -PerformanceLevel <String> -ResourceId <String> -RestorePoint <DateTime> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11b83-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="11b83-109">DESCRIPTION</span></span>
<span data-ttu-id="11b83-110">Polecenie **cmdlet Restore-AzSynapseSqlPool** przywraca pulę sql usługi Azure Synapse Analytics z kopii zapasowej lub punktu przywracania dowolnej puli SQL.</span><span class="sxs-lookup"><span data-stu-id="11b83-110">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="11b83-111">Przywrócona pula sql jest tworzona jako nowa pula SQL.</span><span class="sxs-lookup"><span data-stu-id="11b83-111">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="11b83-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="11b83-112">EXAMPLES</span></span>

### <span data-ttu-id="11b83-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="11b83-113">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="11b83-114">To polecenie tworzy pulę sql usługi Azure Synapse Analytics, przywracając z najnowszej kopii zapasowej dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="11b83-114">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="11b83-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="11b83-115">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="11b83-116">To polecenie tworzy pulę sql analizy Azure Synapse Analytics, wykorzystując punkt przywracania z dowolnej puli sql w tej subskrypcji w celu odzyskania lub skopiowania z poprzedniego stanu.</span><span class="sxs-lookup"><span data-stu-id="11b83-116">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="11b83-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="11b83-117">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="11b83-118">To polecenie tworzy pulę sql analizy Azure Synapse Analytics, przywracając z najnowszej kopii zapasowej dowolną pulę SQL w tej subskrypcji przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="11b83-118">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="11b83-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="11b83-119">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="11b83-120">To polecenie tworzy pulę sql usługi Azure Synapse Analytics, wykorzystując punkt przywracania z dowolnej puli sql w tej subskrypcji w celu odzyskania lub skopiowania z poprzedniego stanu z identyfikatorem zasobu.</span><span class="sxs-lookup"><span data-stu-id="11b83-120">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="11b83-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11b83-121">PARAMETERS</span></span>

### <span data-ttu-id="11b83-122">— AsJob</span><span class="sxs-lookup"><span data-stu-id="11b83-122">-AsJob</span></span>
<span data-ttu-id="11b83-123">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="11b83-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="11b83-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b83-124">-DefaultProfile</span></span>
<span data-ttu-id="11b83-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="11b83-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11b83-126">— FromBackup</span><span class="sxs-lookup"><span data-stu-id="11b83-126">-FromBackup</span></span>
<span data-ttu-id="11b83-127">Oznacza, że należy przywrócić najnowszą kopię zapasową dowolnej puli języka SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="11b83-127">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-128">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="11b83-128">-FromRestorePoint</span></span>
<span data-ttu-id="11b83-129">Wskazuje, że aby odzyskać lub skopiować dane z poprzedniego stanu, skorzystaj z punktu przywracania z dowolnej puli sql w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="11b83-129">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-130">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="11b83-130">-Name</span></span>
<span data-ttu-id="11b83-131">Nazwa puli sql Synapse.</span><span class="sxs-lookup"><span data-stu-id="11b83-131">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetSqlPoolName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-132">- PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="11b83-132">-PerformanceLevel</span></span>
<span data-ttu-id="11b83-133">Warstwa i poziom wydajności usługi SQL, które można przypisać do puli sql.</span><span class="sxs-lookup"><span data-stu-id="11b83-133">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="11b83-134">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="11b83-134">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11b83-135">-ResourceGroupName</span></span>
<span data-ttu-id="11b83-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="11b83-136">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11b83-137">-ResourceId</span></span>
<span data-ttu-id="11b83-138">Identyfikator zasobu bazy danych do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="11b83-138">The resource ID of the database to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-139">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="11b83-139">-RestorePoint</span></span>
<span data-ttu-id="11b83-140">Czas migawki, który należy przywrócić.</span><span class="sxs-lookup"><span data-stu-id="11b83-140">Snapshot time to restore.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases: PointInTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="11b83-141">-WorkspaceName</span></span>
<span data-ttu-id="11b83-142">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="11b83-142">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-143">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="11b83-143">-WorkspaceObject</span></span>
<span data-ttu-id="11b83-144">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="11b83-144">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11b83-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11b83-145">-Confirm</span></span>
<span data-ttu-id="11b83-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="11b83-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11b83-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11b83-147">-WhatIf</span></span>
<span data-ttu-id="11b83-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11b83-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11b83-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="11b83-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11b83-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b83-150">CommonParameters</span></span>
<span data-ttu-id="11b83-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11b83-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b83-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11b83-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b83-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11b83-153">INPUTS</span></span>

### <span data-ttu-id="11b83-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="11b83-154">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="11b83-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11b83-155">OUTPUTS</span></span>

### <span data-ttu-id="11b83-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="11b83-156">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="11b83-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="11b83-157">NOTES</span></span>

## <span data-ttu-id="11b83-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11b83-158">RELATED LINKS</span></span>
