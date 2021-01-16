---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: ae09bb11b56bd6c5fa0add402ace850fe560b293
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383201"
---
# <span data-ttu-id="f61e2-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="f61e2-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="f61e2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f61e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f61e2-103">Zmienia ustawienia inspekcji obszaru roboczego analizy usługi Azure Synapse.</span><span class="sxs-lookup"><span data-stu-id="f61e2-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="f61e2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f61e2-104">SYNTAX</span></span>

### <span data-ttu-id="f61e2-105">SetByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f61e2-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f61e2-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f61e2-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f61e2-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f61e2-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f61e2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f61e2-108">DESCRIPTION</span></span>
<span data-ttu-id="f61e2-109">Polecenie cmdlet **Set-AzSynapseSqlAuditSetting** zmienia ustawienia inspekcji obszaru roboczego funkcji Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="f61e2-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="f61e2-110">Gdy magazyn obiektów BLOB jest miejscem docelowym dla dzienników inspekcji, określ parametr *StorageAccountResourceId* , aby określić konto magazynu dla dzienników inspekcji, a parametr *StorageKeyType* , aby zdefiniować klucze magazynowania.</span><span class="sxs-lookup"><span data-stu-id="f61e2-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="f61e2-111">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="f61e2-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="f61e2-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f61e2-112">EXAMPLES</span></span>

### <span data-ttu-id="f61e2-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f61e2-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="f61e2-114">Włączanie zasad inspekcji magazynu obiektów BLOB w obszarze roboczym funkcji Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f61e2-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f61e2-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f61e2-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="f61e2-116">Wyłącz zasady inspekcji magazynu obiektów BLOB w obszarze roboczym funkcji Azure Synapse analiza o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f61e2-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f61e2-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f61e2-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="f61e2-118">Włącz zasady inspekcji magazynu obiektów BLOB w obszarze roboczym funkcji Azure Synapse analiza o nazwie ContosoWorkspace z funkcją filtrowania zaawansowanego przy użyciu predykatu T-SQL.</span><span class="sxs-lookup"><span data-stu-id="f61e2-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="f61e2-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="f61e2-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="f61e2-120">Usuwanie ustawień filtrowania zaawansowanego z zasad inspekcji w obszarze roboczym funkcji Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="f61e2-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="f61e2-121">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="f61e2-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="f61e2-122">Wyłącz zasady inspekcji magazynu obiektów BLOB w obszarze roboczym funkcji Azure Synapse analiza o nazwie ContosoWorkspace za pośrednictwem rurociągu.</span><span class="sxs-lookup"><span data-stu-id="f61e2-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="f61e2-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f61e2-123">PARAMETERS</span></span>

### <span data-ttu-id="f61e2-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f61e2-124">-AsJob</span></span>
<span data-ttu-id="f61e2-125">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f61e2-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f61e2-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="f61e2-126">-AuditActionGroup</span></span>
<span data-ttu-id="f61e2-127">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="f61e2-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="f61e2-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f61e2-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="f61e2-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="f61e2-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="f61e2-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="f61e2-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="f61e2-131">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="f61e2-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="f61e2-132">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="f61e2-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="f61e2-133">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="f61e2-133">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="f61e2-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="f61e2-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="f61e2-135">Wskazuje, czy Magazyn obiektów BLOB jest miejscem docelowym dla rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="f61e2-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="f61e2-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f61e2-136">-DefaultProfile</span></span>
<span data-ttu-id="f61e2-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f61e2-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f61e2-138">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f61e2-138">-InputObject</span></span>
<span data-ttu-id="f61e2-139">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="f61e2-139">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f61e2-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f61e2-140">-PassThru</span></span>
<span data-ttu-id="f61e2-141">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="f61e2-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f61e2-142">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="f61e2-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f61e2-143">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="f61e2-143">-PredicateExpression</span></span>
<span data-ttu-id="f61e2-144">Predykat T-SQL (klauzula WHERE) służący do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="f61e2-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="f61e2-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f61e2-145">-ResourceGroupName</span></span>
<span data-ttu-id="f61e2-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f61e2-146">Resource group name.</span></span>

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

### <span data-ttu-id="f61e2-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f61e2-147">-ResourceId</span></span>
<span data-ttu-id="f61e2-148">Identyfikator zasobu obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f61e2-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="f61e2-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="f61e2-149">-RetentionInDays</span></span>
<span data-ttu-id="f61e2-150">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="f61e2-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="f61e2-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="f61e2-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="f61e2-152">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="f61e2-152">The storage account resource id</span></span>

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

### <span data-ttu-id="f61e2-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="f61e2-153">-StorageKeyType</span></span>
<span data-ttu-id="f61e2-154">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="f61e2-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="f61e2-155">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="f61e2-155">-WorkspaceName</span></span>
<span data-ttu-id="f61e2-156">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="f61e2-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f61e2-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f61e2-157">-Confirm</span></span>
<span data-ttu-id="f61e2-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f61e2-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f61e2-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f61e2-159">-WhatIf</span></span>
<span data-ttu-id="f61e2-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f61e2-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f61e2-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f61e2-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f61e2-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f61e2-162">CommonParameters</span></span>
<span data-ttu-id="f61e2-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f61e2-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f61e2-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f61e2-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f61e2-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f61e2-165">INPUTS</span></span>

### <span data-ttu-id="f61e2-166">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f61e2-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f61e2-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f61e2-167">OUTPUTS</span></span>

### <span data-ttu-id="f61e2-168">Microsoft. Azure. Commands. Synapse. models. WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="f61e2-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="f61e2-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f61e2-169">NOTES</span></span>

## <span data-ttu-id="f61e2-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f61e2-170">RELATED LINKS</span></span>
