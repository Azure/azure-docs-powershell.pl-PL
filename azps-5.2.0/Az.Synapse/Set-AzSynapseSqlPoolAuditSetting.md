---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolAuditSetting.md
ms.openlocfilehash: 91691741fd7b26d8f33880dee252501c626a4bc6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335614"
---
# <span data-ttu-id="642ad-101">Set-AzSynapseSqlPoolAuditSetting</span><span class="sxs-lookup"><span data-stu-id="642ad-101">Set-AzSynapseSqlPoolAuditSetting</span></span>

## <span data-ttu-id="642ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="642ad-102">SYNOPSIS</span></span>
<span data-ttu-id="642ad-103">Zmienia ustawienia inspekcji puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="642ad-103">Changes the auditing settings for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="642ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="642ad-104">SYNTAX</span></span>

### <span data-ttu-id="642ad-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="642ad-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642ad-106">SetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="642ad-106">SetByParentObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-AuditActionGroup <AuditActionGroup[]>] [-AuditAction <String[]>] [-PredicateExpression <String>]
 [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642ad-107">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="642ad-107">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -InputObject <PSSynapseSqlPool> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="642ad-108">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="642ad-108">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlPoolAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-AuditAction <String[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="642ad-109">Opis</span><span class="sxs-lookup"><span data-stu-id="642ad-109">DESCRIPTION</span></span>
<span data-ttu-id="642ad-110">Polecenie cmdlet **Set-AzSynapseSqlPoolAuditSetting** zmienia ustawienia inspekcji puli SQL usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="642ad-110">The **Set-AzSynapseSqlPoolAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics SQL pool.</span></span>
<span data-ttu-id="642ad-111">Gdy magazyn obiektów BLOB jest miejscem docelowym dla dzienników inspekcji, określ parametr *StorageAccountResourceId* , aby określić konto magazynu dla dzienników inspekcji, a parametr *StorageKeyType* , aby zdefiniować klucze magazynowania.</span><span class="sxs-lookup"><span data-stu-id="642ad-111">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="642ad-112">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="642ad-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="642ad-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="642ad-113">EXAMPLES</span></span>

### <span data-ttu-id="642ad-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="642ad-114">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="642ad-115">Włącz zasady inspekcji magazynu obiektów BLOB puli SQL usługi Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="642ad-115">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="642ad-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="642ad-116">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Disabled
```

<span data-ttu-id="642ad-117">Wyłącz zasady inspekcji magazynu obiektów BLOB puli SQL usługi Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="642ad-117">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="642ad-118">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="642ad-118">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="642ad-119">Włącz zasady inspekcji magazynu obiektów BLOB dla puli usługi Azure Synapse Analytics SQL o nazwie ContosoSqlPool z funkcją filtrowania zaawansowanego przy użyciu predykatu T-SQL.</span><span class="sxs-lookup"><span data-stu-id="642ad-119">Enable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="642ad-120">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="642ad-120">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolAuditSetting -WorkspaceName ContosoWorkspace -Name ContosoSqlPool -PredicateExpression ""
```

<span data-ttu-id="642ad-121">Usuń ustawienie filtrowania zaawansowanego z zasad inspekcji puli SQL usługi Azure Synapse Analytics o nazwie ContosoSqlPool.</span><span class="sxs-lookup"><span data-stu-id="642ad-121">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool.</span></span>

### <span data-ttu-id="642ad-122">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="642ad-122">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="642ad-123">Wyłącz zasady inspekcji magazynu obiektów BLOB puli SQL usługi Azure Synapse Analytics o nazwie ContosoSqlPool za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="642ad-123">Disable the blob storage auditing policy of an Azure Synapse Analytics SQL pool named ContosoSqlPool through pipeline.</span></span>

## <span data-ttu-id="642ad-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="642ad-124">PARAMETERS</span></span>

### <span data-ttu-id="642ad-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="642ad-125">-AsJob</span></span>
<span data-ttu-id="642ad-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="642ad-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="642ad-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="642ad-127">-AuditAction</span></span>
<span data-ttu-id="642ad-128">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="642ad-128">The set of audit actions.</span></span>

<span data-ttu-id="642ad-129">Obsługiwane działania podlegające inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="642ad-129">The supported actions to audit are:</span></span>

<span data-ttu-id="642ad-130">ZAZNACZYSZ</span><span class="sxs-lookup"><span data-stu-id="642ad-130">SELECT</span></span>

<span data-ttu-id="642ad-131">AKTUALIZOWANE</span><span class="sxs-lookup"><span data-stu-id="642ad-131">UPDATE</span></span>

<span data-ttu-id="642ad-132">STAW</span><span class="sxs-lookup"><span data-stu-id="642ad-132">INSERT</span></span>

<span data-ttu-id="642ad-133">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="642ad-133">DELETE</span></span>

<span data-ttu-id="642ad-134">URUCHOMIĆ</span><span class="sxs-lookup"><span data-stu-id="642ad-134">EXECUTE</span></span>

<span data-ttu-id="642ad-135">OTRZYMA</span><span class="sxs-lookup"><span data-stu-id="642ad-135">RECEIVE</span></span>

<span data-ttu-id="642ad-136">MATERIAŁY</span><span class="sxs-lookup"><span data-stu-id="642ad-136">REFERENCES</span></span>

<span data-ttu-id="642ad-137">Formularz ogólne definiujący akcję do przeprowadzenia inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="642ad-137">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="642ad-138">\[Akcja \] na \[ obiekcie \] według \[ podmiotu zabezpieczeń\]</span><span class="sxs-lookup"><span data-stu-id="642ad-138">\[action\] ON \[object\] BY \[principal\]</span></span>

<span data-ttu-id="642ad-139">Należy zwrócić uwagę, że \[ obiekt \] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana albo cała baza danych lub schemat.</span><span class="sxs-lookup"><span data-stu-id="642ad-139">Note that \[object\] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span>
<span data-ttu-id="642ad-140">W przypadku tych ostatnich przypadków baza danych formularze:: \[ dbname \] and Schema: \[ \] są używane odpowiednio: SchemaName.</span><span class="sxs-lookup"><span data-stu-id="642ad-140">For the latter cases, the forms DATABASE::\[dbname\] and SCHEMA::\[schemaname\] are used, respectively.</span></span>

<span data-ttu-id="642ad-141">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="642ad-141">For example:</span></span>

<span data-ttu-id="642ad-142">Wybierz pozycję na dbo. myTable według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="642ad-142">SELECT on dbo.myTable by public</span></span>

<span data-ttu-id="642ad-143">Wybierz w bazie danych:: Moja baza danych przez publiczną</span><span class="sxs-lookup"><span data-stu-id="642ad-143">SELECT on DATABASE::myDatabase by public</span></span>

<span data-ttu-id="642ad-144">Wybierz pozycję w SCHEMAcie:: moje schematy według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="642ad-144">SELECT on SCHEMA::mySchema by public</span></span>

<span data-ttu-id="642ad-145">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="642ad-145">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

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

### <span data-ttu-id="642ad-146">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="642ad-146">-AuditActionGroup</span></span>
<span data-ttu-id="642ad-147">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="642ad-147">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="642ad-148">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="642ad-148">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="642ad-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="642ad-149">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="642ad-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="642ad-150">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="642ad-151">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="642ad-151">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="642ad-152">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="642ad-152">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="642ad-153">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="642ad-153">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="642ad-154">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="642ad-154">-BlobStorageTargetState</span></span>
<span data-ttu-id="642ad-155">Wskazuje, czy Magazyn obiektów BLOB jest miejscem docelowym dla rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="642ad-155">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="642ad-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="642ad-156">-DefaultProfile</span></span>
<span data-ttu-id="642ad-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="642ad-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="642ad-158">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="642ad-158">-InputObject</span></span>
<span data-ttu-id="642ad-159">Obiekt wejściowy zestawu SQL, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="642ad-159">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="642ad-160">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="642ad-160">-Name</span></span>
<span data-ttu-id="642ad-161">Nazwa puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="642ad-161">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="642ad-162">-PassThru</span><span class="sxs-lookup"><span data-stu-id="642ad-162">-PassThru</span></span>
<span data-ttu-id="642ad-163">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="642ad-163">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="642ad-164">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="642ad-164">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="642ad-165">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="642ad-165">-PredicateExpression</span></span>
<span data-ttu-id="642ad-166">Predykat T-SQL (klauzula WHERE) służący do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="642ad-166">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="642ad-167">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="642ad-167">-ResourceGroupName</span></span>
<span data-ttu-id="642ad-168">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="642ad-168">Resource group name.</span></span>

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

### <span data-ttu-id="642ad-169">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="642ad-169">-ResourceId</span></span>
<span data-ttu-id="642ad-170">Identyfikator zasobu puli SQL Synapse.</span><span class="sxs-lookup"><span data-stu-id="642ad-170">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="642ad-171">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="642ad-171">-RetentionInDays</span></span>
<span data-ttu-id="642ad-172">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="642ad-172">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="642ad-173">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="642ad-173">-StorageAccountResourceId</span></span>
<span data-ttu-id="642ad-174">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="642ad-174">The storage account resource id</span></span>

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

### <span data-ttu-id="642ad-175">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="642ad-175">-StorageKeyType</span></span>
<span data-ttu-id="642ad-176">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="642ad-176">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="642ad-177">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="642ad-177">-WorkspaceName</span></span>
<span data-ttu-id="642ad-178">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="642ad-178">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="642ad-179">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="642ad-179">-WorkspaceObject</span></span>
<span data-ttu-id="642ad-180">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="642ad-180">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="642ad-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="642ad-181">-Confirm</span></span>
<span data-ttu-id="642ad-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="642ad-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="642ad-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="642ad-183">-WhatIf</span></span>
<span data-ttu-id="642ad-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="642ad-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="642ad-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="642ad-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="642ad-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="642ad-186">CommonParameters</span></span>
<span data-ttu-id="642ad-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="642ad-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="642ad-188">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="642ad-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="642ad-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="642ad-189">INPUTS</span></span>

### <span data-ttu-id="642ad-190">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="642ad-190">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="642ad-191">Microsoft. Azure. Commands. Synapse. models. PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="642ad-191">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="642ad-192">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="642ad-192">OUTPUTS</span></span>

### <span data-ttu-id="642ad-193">Microsoft. Azure. Commands. Synapse. models. SqlPoolAuditModel</span><span class="sxs-lookup"><span data-stu-id="642ad-193">Microsoft.Azure.Commands.Synapse.Models.SqlPoolAuditModel</span></span>

## <span data-ttu-id="642ad-194">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="642ad-194">NOTES</span></span>

## <span data-ttu-id="642ad-195">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="642ad-195">RELATED LINKS</span></span>
