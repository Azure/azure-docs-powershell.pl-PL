---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapsesqlpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseSqlPool.md
ms.openlocfilehash: 694b9811bf11454e232f1514b59b1b537e4720a5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223640"
---
# <span data-ttu-id="23965-101">New-AzSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="23965-101">New-AzSynapseSqlPool</span></span>

## <span data-ttu-id="23965-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23965-102">SYNOPSIS</span></span>
<span data-ttu-id="23965-103">Tworzy pulę SQL analizy Synapse.</span><span class="sxs-lookup"><span data-stu-id="23965-103">Creates a Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="23965-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23965-104">SYNTAX</span></span>

### <span data-ttu-id="23965-105">CreateByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="23965-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSynapseSqlPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -PerformanceLevel <String> [-Collation <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23965-106">CreateFromBackupIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-106">CreateFromBackupIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23965-107">CreateFromBackupIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-107">CreateFromBackupIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] -BackupResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23965-108">CreateFromBackupNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-108">CreateFromBackupNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23965-109">CreateFromBackupNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-109">CreateFromBackupNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>]
 [-Tag <Hashtable>] [-BackupResourceGroupName <String>] -BackupWorkspaceName <String>
 -BackupSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23965-110">CreateFromBackupInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-110">CreateFromBackupInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromBackup] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -BackupSqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23965-111">CreateFromRestorePointIdByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-111">CreateFromRestorePointIdByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23965-112">CreateFromRestorePointIdByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-112">CreateFromRestorePointIdByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> -SourceResourceId <String>
 [-RestorePoint <DateTime>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23965-113">CreateFromRestorePointNameByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-113">CreateFromRestorePointNameByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] -PerformanceLevel <String> [-SourceResourceGroupName <String>]
 -SourceWorkspaceName <String> -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23965-114">CreateFromRestorePointNameByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-114">CreateFromRestorePointNameByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] -WorkspaceObject <PSSynapseWorkspace> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-SourceResourceGroupName <String>] -SourceWorkspaceName <String>
 -SourceSqlPoolName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23965-115">CreateFromRestorePointInputObjectByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-115">CreateFromRestorePointInputObjectByNameParameterSet</span></span>
```
New-AzSynapseSqlPool [-FromRestorePoint] [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Version <Int32>] [-Tag <Hashtable>] [-PerformanceLevel <String>] -SourceSqlPoolObject <PSSynapseSqlPool>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23965-116">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23965-116">CreateByParentObjectParameterSet</span></span>
```
New-AzSynapseSqlPool -WorkspaceObject <PSSynapseWorkspace> -Name <String> [-Version <Int32>] [-Tag <Hashtable>]
 -PerformanceLevel <String> [-Collation <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23965-117">Opis</span><span class="sxs-lookup"><span data-stu-id="23965-117">DESCRIPTION</span></span>
<span data-ttu-id="23965-118">Polecenie cmdlet **New-AzSynapseSqlPool** tworzy pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="23965-118">The **New-AzSynapseSqlPool** cmdlet creates an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="23965-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23965-119">EXAMPLES</span></span>

### <span data-ttu-id="23965-120">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23965-120">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c
```

<span data-ttu-id="23965-121">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="23965-121">This command creates an Azure Synapse Analytics SQL pool.</span></span>

### <span data-ttu-id="23965-122">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="23965-122">Example 2</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupWorkspaceName ContosoWorkspace -BackupSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="23965-123">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, przywracając najnowszą kopię zapasową dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23965-123">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription.</span></span>

### <span data-ttu-id="23965-124">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="23965-124">Example 3</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromRestorePoint -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PerformanceLevel DW200c -SourceWorkspaceName ContosoWorkspace -SourceSqlPoolName ExistingContosoSqlPool
```

<span data-ttu-id="23965-125">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, wykorzystując punkt przywracania z dowolnej puli SQL w tej subskrypcji, aby odzyskać lub skopiować poprzedni stan.</span><span class="sxs-lookup"><span data-stu-id="23965-125">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

### <span data-ttu-id="23965-126">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="23965-126">Example 4</span></span>
```powershell
PS C:\> New-AzSynapseSqlPool -FromBackup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BackupResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/recoverableSqlPools/ExistingContosoSqlPool
```

<span data-ttu-id="23965-127">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, przywracając najnowszą kopię zapasową dowolnej puli SQL w tej subskrypcji z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="23965-127">This command creates an Azure Synapse Analytics SQL pool by restoring from the most recent backup of any SQL pool in this subscription with resource ID.</span></span>

### <span data-ttu-id="23965-128">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="23965-128">Example 5</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace
$ws |  New-AzSynapseSqlPool -FromRestorePoint -Name dwsql0554 -SourceResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/mandywtest/providers/Microsoft.Synapse/workspaces/ContosoWorkspace/sqlpools/ExistingContosoSqlPool -PerformanceLevel DW300c
```

<span data-ttu-id="23965-129">To polecenie tworzy pulę SQL usługi Azure Synapse Analytics, wykorzystując punkt przywracania z dowolnej puli SQL w tej subskrypcji w celu odzyskania lub skopiowania poprzedniego stanu z IDENTYFIKATORem zasobu.</span><span class="sxs-lookup"><span data-stu-id="23965-129">This command creates an Azure Synapse Analytics SQL pool by leveraging a restore point from any SQL pool in this subscription to recover or copy from a previous state with resource ID.</span></span>

## <span data-ttu-id="23965-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23965-130">PARAMETERS</span></span>

### <span data-ttu-id="23965-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23965-131">-AsJob</span></span>
<span data-ttu-id="23965-132">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="23965-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="23965-133">-BackupResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23965-133">-BackupResourceGroupName</span></span>
<span data-ttu-id="23965-134">Nazwa grupy zasobów, z której ma zostać utworzony obiekt puli SQL Bakcup.</span><span class="sxs-lookup"><span data-stu-id="23965-134">The resource group name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-135">-BackupResourceId</span><span class="sxs-lookup"><span data-stu-id="23965-135">-BackupResourceId</span></span>
<span data-ttu-id="23965-136">Identyfikator zasobu kopii zapasowej obiektu puli SQL do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="23965-136">The resource identifier of backup SQL pool object to restore from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-137">-BackupSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="23965-137">-BackupSqlPoolName</span></span>
<span data-ttu-id="23965-138">Nazwa Bakcup obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23965-138">The name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-139">-BackupSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="23965-139">-BackupSqlPoolObject</span></span>
<span data-ttu-id="23965-140">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="23965-140">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-141">-BackupWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23965-141">-BackupWorkspaceName</span></span>
<span data-ttu-id="23965-142">Nazwa obszaru roboczego Synapse Bakcup puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23965-142">The Synapse workspace name of bakcup SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet
Aliases: BackupServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-143">— Sortowanie</span><span class="sxs-lookup"><span data-stu-id="23965-143">-Collation</span></span>
<span data-ttu-id="23965-144">Sortowanie definiuje reguły, które sortują i porównują dane, i nie można ich zmieniać po utworzeniu puli SQL.</span><span class="sxs-lookup"><span data-stu-id="23965-144">Collation defines the rules that sort and compare data, and cannot be changed after SQL pool creation.</span></span>
<span data-ttu-id="23965-145">Domyślnym sortowaniem jest SQL_Latin1_General_CP1_CI_AS.</span><span class="sxs-lookup"><span data-stu-id="23965-145">The default collation is SQL_Latin1_General_CP1_CI_AS.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23965-146">-DefaultProfile</span></span>
<span data-ttu-id="23965-147">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="23965-147">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23965-148">-FromBackup</span><span class="sxs-lookup"><span data-stu-id="23965-148">-FromBackup</span></span>
<span data-ttu-id="23965-149">Wskazuje, że przywracana jest najnowsza kopia zapasowa dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23965-149">Indicates to restore from the most recent backup of any SQL pool in this subscription.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromBackupIdByNameParameterSet, CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromBackupInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-150">-FromRestorePoint</span><span class="sxs-lookup"><span data-stu-id="23965-150">-FromRestorePoint</span></span>
<span data-ttu-id="23965-151">Wskazuje, że do odzyskiwania lub kopiowania z poprzedniego stanu będzie można użyć punktu przywracania z dowolnej puli SQL w tej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="23965-151">Indicates to leverage a restore point from any SQL pool in this subscription to recover or copy from a previous state.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-152">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="23965-152">-Name</span></span>
<span data-ttu-id="23965-153">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="23965-153">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="23965-154">-PerformanceLevel</span><span class="sxs-lookup"><span data-stu-id="23965-154">-PerformanceLevel</span></span>
<span data-ttu-id="23965-155">Warstwa usług SQL i poziom wydajności, które mają zostać przypisane do puli SQL.</span><span class="sxs-lookup"><span data-stu-id="23965-155">The SQL Service tier and performance level to assign to the SQL pool.</span></span>
<span data-ttu-id="23965-156">Na przykład DW2000c.</span><span class="sxs-lookup"><span data-stu-id="23965-156">For example, DW2000c.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23965-157">-ResourceGroupName</span></span>
<span data-ttu-id="23965-158">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23965-158">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-159">-RestorePoint</span><span class="sxs-lookup"><span data-stu-id="23965-159">-RestorePoint</span></span>
<span data-ttu-id="23965-160">Migawka czasu do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="23965-160">Snapshot time to restore.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-161">-SourceResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23965-161">-SourceResourceGroupName</span></span>
<span data-ttu-id="23965-162">Nazwa grupy zasobów źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23965-162">The resource group name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-163">-SourceResourceId</span><span class="sxs-lookup"><span data-stu-id="23965-163">-SourceResourceId</span></span>
<span data-ttu-id="23965-164">Identyfikator zasobu źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23965-164">The resource identifier of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointIdByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-165">-SourceSqlPoolName</span><span class="sxs-lookup"><span data-stu-id="23965-165">-SourceSqlPoolName</span></span>
<span data-ttu-id="23965-166">Nazwa źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23965-166">The name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceDatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-167">-SourceSqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="23965-167">-SourceSqlPoolObject</span></span>
<span data-ttu-id="23965-168">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="23965-168">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-169">-SourceWorkspaceName</span><span class="sxs-lookup"><span data-stu-id="23965-169">-SourceWorkspaceName</span></span>
<span data-ttu-id="23965-170">Nazwa obszaru roboczego Synapse źródłowego obiektu puli SQL do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="23965-170">The Synapse workspace name of source SQL pool object to create from.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointNameByParentObjectParameterSet
Aliases: SourceServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="23965-171">-Tag</span></span>
<span data-ttu-id="23965-172">Ciąg znaków, który jest ciągiem znaczników skojarzonych z zasobem.</span><span class="sxs-lookup"><span data-stu-id="23965-172">A string,string dictionary of tags associated with the resource.</span></span>

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

### <span data-ttu-id="23965-173">-Version</span><span class="sxs-lookup"><span data-stu-id="23965-173">-Version</span></span>
<span data-ttu-id="23965-174">Wersja puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="23965-174">Version of Synapse SQL pool.</span></span> <span data-ttu-id="23965-175">Na przykład 2 lub 3.</span><span class="sxs-lookup"><span data-stu-id="23965-175">For example, 2 or 3.</span></span>

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

### <span data-ttu-id="23965-176">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="23965-176">-WorkspaceName</span></span>
<span data-ttu-id="23965-177">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="23965-177">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet, CreateFromBackupIdByNameParameterSet, CreateFromBackupNameByNameParameterSet, CreateFromBackupInputObjectByNameParameterSet, CreateFromRestorePointIdByNameParameterSet, CreateFromRestorePointNameByNameParameterSet, CreateFromRestorePointInputObjectByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23965-178">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="23965-178">-WorkspaceObject</span></span>
<span data-ttu-id="23965-179">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="23965-179">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: CreateFromBackupIdByParentObjectParameterSet, CreateFromBackupNameByParentObjectParameterSet, CreateFromRestorePointIdByParentObjectParameterSet, CreateFromRestorePointNameByParentObjectParameterSet, CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23965-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23965-180">-Confirm</span></span>
<span data-ttu-id="23965-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23965-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23965-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23965-182">-WhatIf</span></span>
<span data-ttu-id="23965-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23965-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23965-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23965-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23965-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23965-185">CommonParameters</span></span>
<span data-ttu-id="23965-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23965-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23965-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23965-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23965-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23965-188">INPUTS</span></span>

### <span data-ttu-id="23965-189">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="23965-189">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="23965-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23965-190">OUTPUTS</span></span>

### <span data-ttu-id="23965-191">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="23965-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="23965-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23965-192">NOTES</span></span>

## <span data-ttu-id="23965-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23965-193">RELATED LINKS</span></span>
