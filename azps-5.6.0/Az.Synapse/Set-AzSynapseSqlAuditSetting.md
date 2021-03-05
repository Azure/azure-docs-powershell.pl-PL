---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/set-azsynapsesqlauditsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlAuditSetting.md
ms.openlocfilehash: 15d553800aa51bdf4752902dadd8d5b15fcdf2f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992125"
---
# <span data-ttu-id="cbeb1-101">Set-AzSynapseSqlAuditSetting</span><span class="sxs-lookup"><span data-stu-id="cbeb1-101">Set-AzSynapseSqlAuditSetting</span></span>

## <span data-ttu-id="cbeb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbeb1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbeb1-103">Zmienia ustawienia inspekcji w obszarze roboczym analizy Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-103">Changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>

## <span data-ttu-id="cbeb1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cbeb1-104">SYNTAX</span></span>

### <span data-ttu-id="cbeb1-105">SetByNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="cbeb1-105">SetByNameParameterSet (Default)</span></span>
```
Set-AzSynapseSqlAuditSetting [-ResourceGroupName <String>] -WorkspaceName <String>
 [-AuditActionGroup <AuditActionGroup[]>] [-PredicateExpression <String>] [-BlobStorageTargetState <String>]
 [-StorageAccountResourceId <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbeb1-106">SetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbeb1-106">SetByInputObjectParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -InputObject <PSSynapseWorkspace> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbeb1-107">SetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cbeb1-107">SetByResourceIdParameterSet</span></span>
```
Set-AzSynapseSqlAuditSetting -ResourceId <String> [-AuditActionGroup <AuditActionGroup[]>]
 [-PredicateExpression <String>] [-BlobStorageTargetState <String>] [-StorageAccountResourceId <String>]
 [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbeb1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cbeb1-108">DESCRIPTION</span></span>
<span data-ttu-id="cbeb1-109">Polecenie **cmdlet Set-AzSynapseSqlAuditSetting** zmienia ustawienia inspekcji obszaru roboczego usługi Azure Synapse Analytics.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-109">The **Set-AzSynapseSqlAuditSetting** cmdlet changes the auditing settings of an Azure Synapse Analytics Workspace.</span></span>
<span data-ttu-id="cbeb1-110">Gdy magazyn obiektów blob jest miejscem docelowym dzienników inspekcji, określ parametr *StorageAccountResourceId* w celu określenia konta magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynu.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-110">When blob storage is a destination for audit logs, specify the *StorageAccountResourceId* parameter to determine the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span> <span data-ttu-id="cbeb1-111">Można również zdefiniować przechowywanie dla dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-111">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

## <span data-ttu-id="cbeb1-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cbeb1-112">EXAMPLES</span></span>

### <span data-ttu-id="cbeb1-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cbeb1-113">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary
```

<span data-ttu-id="cbeb1-114">Włącz zasady inspekcji magazynu obiektów blob w obszarze roboczym analizy Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-114">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cbeb1-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cbeb1-115">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Disabled
```

<span data-ttu-id="cbeb1-116">Wyłącz zasady inspekcji magazynu obiektów blob w obszarze roboczym analizy Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-116">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cbeb1-117">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="cbeb1-117">Example 3</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -BlobStorageTargetState Enabled -StorageAccountResourceId "/subscriptions/7fe3301d-31d3-4668-af5e-211a890ba6e3/resourceGroups/resourcegroup01/providers/Microsoft.Storage/storageAccounts/mystorage" -StorageKeyType Primary -PredicateExpression "statement <> 'select 1'"
```

<span data-ttu-id="cbeb1-118">Włącz zasady inspekcji magazynu obiektów blob w obszarze roboczym analizy Azure Synapse Analytics o nazwie ContosoWorkspace z zaawansowanym filtrowaniem przy użyciu predykatu T-SQL.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-118">Enable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace with advanced filtering using a T-SQL predicate.</span></span>

### <span data-ttu-id="cbeb1-119">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="cbeb1-119">Example 4</span></span>
```powershell
PS C:\> Set-AzSynapseSqlAuditSetting -WorkspaceName ContosoWorkspace -PredicateExpression ""
```

<span data-ttu-id="cbeb1-120">Usuń zaawansowane ustawienie filtrowania z zasad inspekcji obszaru roboczego usługi Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-120">Remove the advanced filtering setting from the auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="cbeb1-121">Przykład 5</span><span class="sxs-lookup"><span data-stu-id="cbeb1-121">Example 5</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Set-AzSynapseSqlAuditSetting -BlobStorageTargetState Disabled
```

<span data-ttu-id="cbeb1-122">Wyłącz zasady inspekcji magazynu obiektów blob w potoku obszaru roboczego analizy Azure Synapse Analytics o nazwie ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-122">Disable the blob storage auditing policy of an Azure Synapse Analytics Workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="cbeb1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cbeb1-123">PARAMETERS</span></span>

### <span data-ttu-id="cbeb1-124">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cbeb1-124">-AsJob</span></span>
<span data-ttu-id="cbeb1-125">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cbeb1-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cbeb1-126">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="cbeb1-126">-AuditActionGroup</span></span>
<span data-ttu-id="cbeb1-127">Zalecany zestaw grup akcji do użycia to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur przechowywanych wykonywanych w bazie danych, a także pomyślnych i nieudanych logowania:</span><span class="sxs-lookup"><span data-stu-id="cbeb1-127">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>



<span data-ttu-id="cbeb1-128">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="cbeb1-128">"BATCH_COMPLETED_GROUP",</span></span>

<span data-ttu-id="cbeb1-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="cbeb1-129">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>

<span data-ttu-id="cbeb1-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="cbeb1-130">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>

<span data-ttu-id="cbeb1-131">Ta kombinacja jest również skonfigurowanym domyślnie zestawem.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-131">This above combination is also the set that is configured by default.</span></span>
<span data-ttu-id="cbeb1-132">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w bazie danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to zduplikowane dzienniki inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-132">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>

<span data-ttu-id="cbeb1-133">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="cbeb1-133">For more information, see https://docs.microsoft.com/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="cbeb1-134">-BlobStorageTargetState</span><span class="sxs-lookup"><span data-stu-id="cbeb1-134">-BlobStorageTargetState</span></span>
<span data-ttu-id="cbeb1-135">Wskazuje, czy magazyn obiektów blob jest miejscem docelowym rekordów inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-135">Indicates whether blob storage is a destination for audit records.</span></span>

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

### <span data-ttu-id="cbeb1-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbeb1-136">-DefaultProfile</span></span>
<span data-ttu-id="cbeb1-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbeb1-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cbeb1-138">-InputObject</span></span>
<span data-ttu-id="cbeb1-139">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-139">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="cbeb1-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbeb1-140">-PassThru</span></span>
<span data-ttu-id="cbeb1-141">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-141">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="cbeb1-142">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-142">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="cbeb1-143">-PreddicateExpression</span><span class="sxs-lookup"><span data-stu-id="cbeb1-143">-PredicateExpression</span></span>
<span data-ttu-id="cbeb1-144">Predykat T-SQL (klauzula WHERE) używany do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-144">The T-SQL predicate (WHERE clause) used to filter audit logs.</span></span>

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

### <span data-ttu-id="cbeb1-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbeb1-145">-ResourceGroupName</span></span>
<span data-ttu-id="cbeb1-146">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-146">Resource group name.</span></span>

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

### <span data-ttu-id="cbeb1-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cbeb1-147">-ResourceId</span></span>
<span data-ttu-id="cbeb1-148">Identyfikator zasobu obszaru roboczego programu Synapse.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-148">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="cbeb1-149">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="cbeb1-149">-RetentionInDays</span></span>
<span data-ttu-id="cbeb1-150">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-150">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="cbeb1-151">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="cbeb1-151">-StorageAccountResourceId</span></span>
<span data-ttu-id="cbeb1-152">Identyfikator zasobu konta magazynu</span><span class="sxs-lookup"><span data-stu-id="cbeb1-152">The storage account resource id</span></span>

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

### <span data-ttu-id="cbeb1-153">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="cbeb1-153">-StorageKeyType</span></span>
<span data-ttu-id="cbeb1-154">Określa, których kluczy dostępu do magazynu należy użyć.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-154">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="cbeb1-155">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="cbeb1-155">-WorkspaceName</span></span>
<span data-ttu-id="cbeb1-156">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-156">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="cbeb1-157">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cbeb1-157">-Confirm</span></span>
<span data-ttu-id="cbeb1-158">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cbeb1-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbeb1-159">-WhatIf</span></span>
<span data-ttu-id="cbeb1-160">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbeb1-161">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cbeb1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbeb1-162">CommonParameters</span></span>
<span data-ttu-id="cbeb1-163">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbeb1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbeb1-164">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cbeb1-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbeb1-165">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbeb1-165">INPUTS</span></span>

### <span data-ttu-id="cbeb1-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="cbeb1-166">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="cbeb1-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbeb1-167">OUTPUTS</span></span>

### <span data-ttu-id="cbeb1-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span><span class="sxs-lookup"><span data-stu-id="cbeb1-168">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAuditModel</span></span>

## <span data-ttu-id="cbeb1-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cbeb1-169">NOTES</span></span>

## <span data-ttu-id="cbeb1-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbeb1-170">RELATED LINKS</span></span>
