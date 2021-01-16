---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/restore-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Restore-AzSynapseSqlPool.md
ms.openlocfilehash: 7fbc6cedf039cca33d0a30b39a21f9cdcb350b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333790"
---
# <span data-ttu-id="163a2-101">Restore-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="163a2-101">Restore-AzSynapseSqlPool</span></span>

## <span data-ttu-id="163a2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="163a2-102">SYNOPSIS</span></span>
<span data-ttu-id="163a2-103">Przywraca pulę SQL Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="163a2-103">Restores a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="163a2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="163a2-104">SYNTAX</span></span>

### <span data-ttu-id="163a2-105">RestoreFromBackupIdByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="163a2-105">RestoreFromBackupIdByNameParameterSet (Default)</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163a2-106">RestoreFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-106">RestoreFromBackupIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="163a2-107">RestoreFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-107">RestoreFromBackupNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="163a2-108">RestoreFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-108">RestoreFromBackupNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Tag <Hashtable>]
 [-BackupResourceGroupName <String>] -BackupWorkspaceName <String> -BackupSqlPoolName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163a2-109">RestoreFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-109">RestoreFromBackupInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163a2-110">RestoreFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-110">RestoreFromRestorePointIdByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="163a2-111">RestoreFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-111">RestoreFromRestorePointIdByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String> [-RestorePoint <DateTime>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163a2-112">RestoreFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-112">RestoreFromRestorePointNameByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="163a2-113">RestoreFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-113">RestoreFromRestorePointNameByParentObjectParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="163a2-114">RestoreFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="163a2-114">RestoreFromRestorePointInputObjectByNameParameterSet</span></span>
```
Restore-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="163a2-115">Opis</span><span class="sxs-lookup"><span data-stu-id="163a2-115">DESCRIPTION</span></span>
<span data-ttu-id="163a2-116">Polecenie cmdlet **Restore-AzSynapseSqlPool** przywraca pulę SQL usługi Azure Synapse Analytics z kopii zapasowej lub punktu przywracania dowolnej puli SQL.</span><span class="sxs-lookup"><span data-stu-id="163a2-116">The **Restore-AzSynapseSqlPool** cmdlet restores an Azure Synapse Analytics SQL pool from a backup or a restore point of any SQL pool.</span></span>
<span data-ttu-id="163a2-117">Przywrócona Pula SQL została utworzona jako nowa pula SQL.</span><span class="sxs-lookup"><span data-stu-id="163a2-117">The restored SQL pool is created as a new SQL pool.</span></span>

## <span data-ttu-id="163a2-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="163a2-118">EXAMPLES</span></span>

### <span data-ttu-id="163a2-119">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="163a2-119">Example 1</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="163a2-120">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, przywracając najnowszą kopię zapasową dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="163a2-120">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="163a2-121">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="163a2-121">Example 2</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="163a2-122">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, wykorzystując punkt przywracania z dowolnej puli SQL w tej subskrypcji, aby odzyskać lub skopiować poprzedni stan.</span><span class="sxs-lookup"><span data-stu-id="163a2-122">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="163a2-123">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="163a2-123">Example 3</span></span>
```powershell
PS C:\> Restore-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="163a2-124">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, przywracając najnowszą kopię zapasową dowolnej puli SQL w tej subskrypcji z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="163a2-124">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="163a2-125">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="163a2-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws | Restore-AzSynapseSqlPool -FromRestorePoint -Name ContosoSqlPool -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="163a2-126">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, wykorzystując punkt przywracania z dowolnej puli SQL w tej subskrypcji w celu odzyskania lub skopiowania poprzedniego stanu z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="163a2-126">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="163a2-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="163a2-127">PARAMETERS</span></span>

### <span data-ttu-id="163a2-128">-AsJob</span><span class="sxs-lookup"><span data-stu-id="163a2-128">-AsJob</span></span>
<span data-ttu-id="163a2-129">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="163a2-129">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="163a2-130">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163a2-130">-BackupResourceGroupName</span></span>
<span data-ttu-id="163a2-131">Nazwa grupy zasobów, z której ma zostać utworzony obiekt puli SQL Bakcup.</span><span class="sxs-lookup"><span data-stu-id="163a2-131">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-132">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="163a2-132">-BackupResourceId</span></span>
<span data-ttu-id="163a2-133">Identyfikator zasobu kopii zapasowej obiektu puli SQL do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-133">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-134">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="163a2-134">-BackupSqlPoolName</span></span>
<span data-ttu-id="163a2-135">Nazwa Bakcup obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-135">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-136">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="163a2-136">-BackupSqlPoolObject</span></span>
<span data-ttu-id="163a2-137">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="163a2-137">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-138">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="163a2-138">-BackupWorkspaceName</span></span>
<span data-ttu-id="163a2-139">Nazwa obszaru roboczego Synapse Bakcup puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-139">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="163a2-140">-DefaultProfile</span></span>
<span data-ttu-id="163a2-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="163a2-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="163a2-142">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="163a2-142">-FromBackup</span></span>
<span data-ttu-id="163a2-143">Wskazuje, że przywracana jest najnowsza kopia zapasowa dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="163a2-143">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-144">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="163a2-144">-FromRestorePoint</span></span>
<span data-ttu-id="163a2-145">Wskazuje, że do odzyskiwania lub kopiowania z poprzedniego stanu będzie można użyć punktu przywracania z dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="163a2-145">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="163a2-146">-Name</span></span>
<span data-ttu-id="163a2-147">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="163a2-147">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="163a2-148">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="163a2-148">-PerformanceLevel</span></span>
<span data-ttu-id="163a2-149">Warstwa usług SQL i poziom wydajności, które mają zostać przypisane do puli SQL.</span><span class="sxs-lookup"><span data-stu-id="163a2-149">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="163a2-150">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="163a2-150">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163a2-151">-ResourceGroupName</span></span>
<span data-ttu-id="163a2-152">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="163a2-152">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-153">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="163a2-153">-RestorePoint</span></span>
<span data-ttu-id="163a2-154">Migawka czasu do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-154">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-155">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="163a2-155">-SourceResourceGroupName</span></span>
<span data-ttu-id="163a2-156">Nazwa grupy zasobów źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-156">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-157">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="163a2-157">-SourceResourceId</span></span>
<span data-ttu-id="163a2-158">Identyfikator zasobu źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-158">The resource identifier of source SQL pool object to create from.</span></span>

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

### <span data-ttu-id="163a2-159">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="163a2-159">-SourceSqlPoolName</span></span>
<span data-ttu-id="163a2-160">Nazwa źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-160">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-161">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="163a2-161">-SourceSqlPoolObject</span></span>
<span data-ttu-id="163a2-162">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="163a2-162">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-163">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="163a2-163">-SourceWorkspaceName</span></span>
<span data-ttu-id="163a2-164">Nazwa obszaru roboczego Synapse źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="163a2-164">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="163a2-165">-Tag</span></span>
<span data-ttu-id="163a2-166">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="163a2-166">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="163a2-167">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="163a2-167">-WorkspaceName</span></span>
<span data-ttu-id="163a2-168">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="163a2-168">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreFromBackupIdByNameParameterSet, RestoreFromBackupNameByNameParameterSet, RestoreFromBackupInputObjectByNameParameterSet, RestoreFromRestorePointIdByNameParameterSet, RestoreFromRestorePointNameByNameParameterSet, RestoreFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-169">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="163a2-169">-WorkspaceObject</span></span>
<span data-ttu-id="163a2-170">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="163a2-170">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RestoreFromBackupIdByParentObjectParameterSet, RestoreFromBackupNameByParentObjectParameterSet, RestoreFromRestorePointIdByParentObjectParameterSet, RestoreFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="163a2-171">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="163a2-171">-Confirm</span></span>
<span data-ttu-id="163a2-172">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="163a2-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="163a2-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="163a2-173">-WhatIf</span></span>
<span data-ttu-id="163a2-174">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="163a2-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="163a2-175">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="163a2-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="163a2-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="163a2-176">CommonParameters</span></span>
<span data-ttu-id="163a2-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="163a2-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="163a2-178">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="163a2-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="163a2-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="163a2-179">INPUTS</span></span>

### <span data-ttu-id="163a2-180">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="163a2-180">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="163a2-181">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="163a2-181">OUTPUTS</span></span>

### <span data-ttu-id="163a2-182">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="163a2-182">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="163a2-183">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="163a2-183">NOTES</span></span>

## <span data-ttu-id="163a2-184">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="163a2-184">RELATED LINKS</span></span>
