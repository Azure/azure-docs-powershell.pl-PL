---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 80887d1c3cfc91c9eba23f686deac071660cf852
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550168"
---
# <span data-ttu-id="3e21a-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="3e21a-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="3e21a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e21a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e21a-103">Zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e21a-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e21a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e21a-104">SYNTAX</span></span>

### <span data-ttu-id="3e21a-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3e21a-105">DefaultParameterSet (Default)</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-PredicateExpression <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e21a-106">StorageAccountSubscriptionIdSet</span><span class="sxs-lookup"><span data-stu-id="3e21a-106">StorageAccountSubscriptionIdSet</span></span>
```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 -StorageAccountName <String> [-StorageAccountSubscriptionId <Guid>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-PredicateExpression <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3e21a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3e21a-107">DESCRIPTION</span></span>
<span data-ttu-id="3e21a-108">Polecenie cmdlet **Set-AzureRmSqlServerAuditing** zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3e21a-108">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="3e21a-109">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="3e21a-109">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="3e21a-110">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3e21a-110">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="3e21a-111">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="3e21a-111">Use the *State* parameter to enable/disable the policy.</span></span>
<span data-ttu-id="3e21a-112">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-112">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>
<span data-ttu-id="3e21a-113">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja baz danych SQL platformy Azure zdefiniowanych w określonym obszarze usługi Azure SQL Server jest włączona.</span><span class="sxs-lookup"><span data-stu-id="3e21a-113">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="3e21a-114">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektów BLOB oprócz identyfikatorów serwera.</span><span class="sxs-lookup"><span data-stu-id="3e21a-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="3e21a-115">Identyfikatory serwerów obejmują, ale nie są ograniczone do **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="3e21a-115">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="3e21a-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e21a-116">EXAMPLES</span></span>

### <span data-ttu-id="3e21a-117">Przykład 1. Włączanie zasad inspekcji serwera SQL w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="3e21a-117">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="3e21a-118">Przykład 2: wyłączanie zasad inspekcji usługi SQL Server</span><span class="sxs-lookup"><span data-stu-id="3e21a-118">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

### <span data-ttu-id="3e21a-119">Przykład 3: Włączanie zasad inspekcji programu Azure SQL Server przy użyciu konta magazynu z innej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3e21a-119">Example 3: Enable the auditing policy of an Azure SQL server using a storage account from a different subscription</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -StorageAccountSubscriptionId "7fe3301d-31d3-4668-af5e-211a890ba6e3"
```

### <span data-ttu-id="3e21a-120">Przykład 4: Włączanie rozszerzonych zasad inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="3e21a-120">Example 4: Enable the extended auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression "statement <> 'select 1'"
```

### <span data-ttu-id="3e21a-121">Przykład 5: usuwanie zasad inspekcji rozszerzonej bazy danych usługi Azure SQL i Ustawianie zasad inspekcji zamiast tej funkcji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-121">Example 5: Remove the extended auditing policy of an Azure SQL database, and set an auditing policy instead of it.</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01" -PredicateExpression ""
```

## <span data-ttu-id="3e21a-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e21a-122">PARAMETERS</span></span>

### <span data-ttu-id="3e21a-123">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="3e21a-123">-AuditActionGroup</span></span>
<span data-ttu-id="3e21a-124">Zalecany zestaw grup akcji, który ma być używany, to następująca kombinacja — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" Ta powyższa kombinacja jest również skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="3e21a-124">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins: "BATCH_COMPLETED_GROUP", "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="3e21a-125">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-125">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span> <span data-ttu-id="3e21a-126">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="3e21a-126">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e21a-127">-DefaultProfile</span></span>
<span data-ttu-id="3e21a-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e21a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3e21a-129">-PassThru</span></span>
<span data-ttu-id="3e21a-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="3e21a-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-131">-PredicateExpression</span><span class="sxs-lookup"><span data-stu-id="3e21a-131">-PredicateExpression</span></span>
<span data-ttu-id="3e21a-132">Instrukcja klauzuli WHERE użytej do filtrowania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-132">The statement of the Where Clause used to filter audit logs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e21a-133">-ResourceGroupName</span></span>
<span data-ttu-id="3e21a-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e21a-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-135">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3e21a-135">-RetentionInDays</span></span>
<span data-ttu-id="3e21a-136">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-136">The number of retention days for the audit logs.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-137">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="3e21a-137">-ServerName</span></span>
<span data-ttu-id="3e21a-138">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="3e21a-138">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-139">-State</span><span class="sxs-lookup"><span data-stu-id="3e21a-139">-State</span></span>
<span data-ttu-id="3e21a-140">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="3e21a-140">The state of the policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-141">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e21a-141">-StorageAccountName</span></span>
<span data-ttu-id="3e21a-142">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3e21a-142">The name of the storage account.</span></span> <span data-ttu-id="3e21a-143">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="3e21a-143">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="3e21a-144">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3e21a-144">This parameter is not required.</span></span>
<span data-ttu-id="3e21a-145">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="3e21a-145">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>
<span data-ttu-id="3e21a-146">Jeśli zasady inspekcji są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="3e21a-146">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-147">-StorageAccountSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3e21a-147">-StorageAccountSubscriptionId</span></span>
<span data-ttu-id="3e21a-148">Określa identyfikator subskrypcji konta magazynu</span><span class="sxs-lookup"><span data-stu-id="3e21a-148">Specifies storage account subscription id</span></span>

```yaml
Type: System.Guid
Parameter Sets: StorageAccountSubscriptionIdSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-149">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="3e21a-149">-StorageKeyType</span></span>
<span data-ttu-id="3e21a-150">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="3e21a-150">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e21a-151">-Confirm</span></span>
<span data-ttu-id="3e21a-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e21a-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e21a-153">-WhatIf</span></span>
<span data-ttu-id="3e21a-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e21a-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3e21a-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e21a-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e21a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e21a-156">CommonParameters</span></span>
<span data-ttu-id="3e21a-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e21a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e21a-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e21a-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e21a-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e21a-159">INPUTS</span></span>

## <span data-ttu-id="3e21a-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e21a-160">OUTPUTS</span></span>

## <span data-ttu-id="3e21a-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e21a-161">NOTES</span></span>

## <span data-ttu-id="3e21a-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e21a-162">RELATED LINKS</span></span>
