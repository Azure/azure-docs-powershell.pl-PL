---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195562"
---
# <span data-ttu-id="d8513-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="d8513-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="d8513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8513-102">SYNOPSIS</span></span>
<span data-ttu-id="d8513-103">Zmienia ustawienia inspekcji dla puli języka SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d8513-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="d8513-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8513-104">SYNTAX</span></span>

### <span data-ttu-id="d8513-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8513-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8513-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8513-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8513-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8513-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8513-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8513-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8513-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8513-109">DESCRIPTION</span></span>
<span data-ttu-id="d8513-110">Polecenie **cmdlet Set-AzSynapseSqlPoolAuditSetting** zmienia ustawienia inspekcji puli SQL Synapse Analytics platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d8513-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="d8513-111">Gdy magazyn obiektów blob jest miejscem docelowym dzienników inspekcji, określ parametr *StorageAccountResourceId* w celu określenia konta magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8513-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="d8513-112">Można również zdefiniować przechowywanie dla dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d8513-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="d8513-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8513-113">EXAMPLES</span></span>

### <span data-ttu-id="d8513-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8513-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="d8513-115">Włącz zasady inspekcji magazynu obiektów blob puli SQL Usługi Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="d8513-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="d8513-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d8513-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="d8513-117">Wyłącz zasady inspekcji magazynu obiektów blob puli SQL Usługi Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="d8513-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="d8513-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d8513-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="d8513-119">Włącz zasady inspekcji magazynu obiektów blob puli SQL Usługi Azure Synapse Analytics o nazwie ContosoSqlPool za pomocą filtrowania zaawansowanego przy użyciu predykatu T-SQL.</span><span class="sxs-lookup"><span data-stu-id="d8513-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="d8513-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="d8513-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="d8513-121">Usuń zaawansowane ustawienie filtrowania z zasad inspekcji puli SQL Usługi Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="d8513-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="d8513-122">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="d8513-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="d8513-123">Wyłącz zasady inspekcji magazynu obiektów blob puli SQL Usługi Azure Synapse Analytics o nazwie ContosoSqlPool za pośrednictwem potoku.</span><span class="sxs-lookup"><span data-stu-id="d8513-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="d8513-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8513-124">PARAMETERS</span></span>

### <span data-ttu-id="d8513-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d8513-125">-AsJob</span></span>
<span data-ttu-id="d8513-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="d8513-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8513-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="d8513-127">-AuditAction</span></span>
<span data-ttu-id="d8513-128">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d8513-128">The set of audit actions.</span></span>

<span data-ttu-id="d8513-129">Obsługiwane akcje do inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="d8513-129">The supported actions to audit are:</span></span>

<span data-ttu-id="d8513-130">SELECT</span><span class="sxs-lookup"><span data-stu-id="d8513-130">SELECT</span></span>

<span data-ttu-id="d8513-131">UPDATE</span><span class="sxs-lookup"><span data-stu-id="d8513-131">UPDATE</span></span>

<span data-ttu-id="d8513-132">INSERT</span><span class="sxs-lookup"><span data-stu-id="d8513-132">INSERT</span></span>

<span data-ttu-id="d8513-133">DELETE</span><span class="sxs-lookup"><span data-stu-id="d8513-133">DELETE</span></span>

<span data-ttu-id="d8513-134">EXECUTE</span><span class="sxs-lookup"><span data-stu-id="d8513-134">EXECUTE</span></span>

<span data-ttu-id="d8513-135">RECEIVE</span><span class="sxs-lookup"><span data-stu-id="d8513-135">RECEIVE</span></span>

<span data-ttu-id="d8513-136">REFERENCES</span><span class="sxs-lookup"><span data-stu-id="d8513-136">REFERENCES</span></span>

<span data-ttu-id="d8513-137">Ogólnym formularzem definiującym akcję, która ma być poddana inspekcji, jest:</span><span class="sxs-lookup"><span data-stu-id="d8513-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="d8513-138">\[action \] ON object BY \[ \] \[ principal\]</span><span class="sxs-lookup"><span data-stu-id="d8513-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="d8513-139">Obiekt w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok, procedura składowana, albo do całej bazy \[ \] danych lub schematu.</span><span class="sxs-lookup"><span data-stu-id="d8513-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="d8513-140">W innych przypadkach używane są odpowiednio formularze DATABASE:: \[ dbname \] i SCHEMA:: \[ \] schemaname.</span><span class="sxs-lookup"><span data-stu-id="d8513-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="d8513-141">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="d8513-141">For example:</span></span>

<span data-ttu-id="d8513-142">SELECT on dbo.myTable by public</span><span class="sxs-lookup"><span data-stu-id="d8513-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="d8513-143">Select on DATABASE::myDatabase by public</span><span class="sxs-lookup"><span data-stu-id="d8513-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="d8513-144">SELECT on SCHEMA::mySchema by public</span><span class="sxs-lookup"><span data-stu-id="d8513-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="d8513-145">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="d8513-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d8513-146">-AuditActionGroup</span></span>
<span data-ttu-id="d8513-147">Zalecany zestaw grup akcji do użycia to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur przechowywanych wykonywanych w bazie danych, a także pomyślnego i nieudanych logowania:</span><span class="sxs-lookup"><span data-stu-id="d8513-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="d8513-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d8513-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="d8513-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="d8513-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="d8513-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="d8513-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="d8513-151">Ta kombinacja jest również skonfigurowanym domyślnie zestawem.</span><span class="sxs-lookup"><span data-stu-id="d8513-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="d8513-152">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w bazie danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to zduplikowane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d8513-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="d8513-153">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="d8513-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.AuditActionGroup[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="d8513-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="d8513-155">Wskazuje, czy magazyn obiektów blob jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d8513-155">Indicates whether blob storage is a destination for audit records.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8513-156">-DefaultProfile</span></span>
<span data-ttu-id="d8513-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8513-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8513-158">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8513-158">-InputObject</span></span>
<span data-ttu-id="d8513-159">Obiekt wejściowy puli SQL, który zwykle przechodził przez potok.</span><span class="sxs-lookup"><span data-stu-id="d8513-159">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-160">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8513-160">-Name</span></span>
<span data-ttu-id="d8513-161">Nazwa puli języka SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8513-161">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet, SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8513-162">-PassThru</span></span>
<span data-ttu-id="d8513-163">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="d8513-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="d8513-164">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="d8513-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="d8513-165">-PreddicateExpression</span><span class="sxs-lookup"><span data-stu-id="d8513-165">-PredicateExpression</span></span>
<span data-ttu-id="d8513-166">Predykat T-SQL (klauzula WHERE) używany do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d8513-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="d8513-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8513-167">-ResourceGroupName</span></span>
<span data-ttu-id="d8513-168">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8513-168">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8513-169">-ResourceId</span></span>
<span data-ttu-id="d8513-170">Identyfikator zasobu synapse SQL Pool.</span><span class="sxs-lookup"><span data-stu-id="d8513-170">Resource identifier of Synapse SQL Pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d8513-171">-RetentionInDays</span></span>
<span data-ttu-id="d8513-172">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d8513-172">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d8513-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="d8513-174">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="d8513-174">The storage account resource id</span></span>

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

### <span data-ttu-id="d8513-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d8513-175">-StorageKeyType</span></span>
<span data-ttu-id="d8513-176">Określa, których kluczy dostępu do magazynu należy użyć.</span><span class="sxs-lookup"><span data-stu-id="d8513-176">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-177">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d8513-177">-WorkspaceName</span></span>
<span data-ttu-id="d8513-178">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="d8513-178">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-179">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d8513-179">-WorkspaceObject</span></span>
<span data-ttu-id="d8513-180">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="d8513-180">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d8513-181">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8513-181">-Confirm</span></span>
<span data-ttu-id="d8513-182">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8513-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8513-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8513-183">-WhatIf</span></span>
<span data-ttu-id="d8513-184">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8513-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8513-185">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8513-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8513-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8513-186">CommonParameters</span></span>
<span data-ttu-id="d8513-187">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8513-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8513-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8513-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8513-189">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8513-189">INPUTS</span></span>

### <span data-ttu-id="d8513-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="d8513-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="d8513-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="d8513-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="d8513-192">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8513-192">OUTPUTS</span></span>

### <span data-ttu-id="d8513-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="d8513-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="d8513-194">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8513-194">NOTES</span></span>

## <span data-ttu-id="d8513-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8513-195">RELATED LINKS</span></span>
