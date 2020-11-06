---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: 5eedeea96f7c1c2491e7388734b51977cb0dd1c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542180"
---
# <span data-ttu-id="86c60-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="86c60-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="86c60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86c60-102">SYNOPSIS</span></span>
<span data-ttu-id="86c60-103">Zmienia ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="86c60-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="86c60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86c60-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86c60-105">Opis</span><span class="sxs-lookup"><span data-stu-id="86c60-105">DESCRIPTION</span></span>
<span data-ttu-id="86c60-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditing** zmienia ustawienia inspekcji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="86c60-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="86c60-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="86c60-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="86c60-108">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="86c60-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="86c60-109">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="86c60-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="86c60-110">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="86c60-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="86c60-111">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="86c60-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="86c60-112">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektu BLOB oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="86c60-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="86c60-113">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="86c60-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="86c60-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86c60-114">EXAMPLES</span></span>

### <span data-ttu-id="86c60-115">Przykład 1. Włączanie zasad inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="86c60-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="86c60-116">Przykład 2: wyłączanie zasad inspekcji obiektu BLOB bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="86c60-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="86c60-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86c60-117">PARAMETERS</span></span>

### <span data-ttu-id="86c60-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="86c60-118">-AuditAction</span></span>
<span data-ttu-id="86c60-119">Zestaw akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="86c60-119">The set of audit actions.</span></span>  
<span data-ttu-id="86c60-120">Obsługiwane działania podlegające inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="86c60-120">The supported actions to audit are:</span></span>  
<span data-ttu-id="86c60-121">ZAZNACZYSZ</span><span class="sxs-lookup"><span data-stu-id="86c60-121">SELECT</span></span>  
<span data-ttu-id="86c60-122">AKTUALIZOWANE</span><span class="sxs-lookup"><span data-stu-id="86c60-122">UPDATE</span></span>  
<span data-ttu-id="86c60-123">STAW</span><span class="sxs-lookup"><span data-stu-id="86c60-123">INSERT</span></span>  
<span data-ttu-id="86c60-124">USUWAĆ</span><span class="sxs-lookup"><span data-stu-id="86c60-124">DELETE</span></span>  
<span data-ttu-id="86c60-125">URUCHOMIĆ</span><span class="sxs-lookup"><span data-stu-id="86c60-125">EXECUTE</span></span>  
<span data-ttu-id="86c60-126">OTRZYMA</span><span class="sxs-lookup"><span data-stu-id="86c60-126">RECEIVE</span></span>  
<span data-ttu-id="86c60-127">MATERIAŁY</span><span class="sxs-lookup"><span data-stu-id="86c60-127">REFERENCES</span></span>  

<span data-ttu-id="86c60-128">Formularz ogólne definiujący akcję do przeprowadzenia inspekcji to:</span><span class="sxs-lookup"><span data-stu-id="86c60-128">The general form for defining an action to be audited is:</span></span>

<span data-ttu-id="86c60-129">Action NA [obiekt] według [podmiot zabezpieczeń]</span><span class="sxs-lookup"><span data-stu-id="86c60-129">[action] ON [object] BY [principal]</span></span>

<span data-ttu-id="86c60-130">Należy pamiętać, że [obiekt] w powyższym formacie może odwoływać się do obiektu, takiego jak tabela, widok lub procedura składowana albo cała baza danych lub schemat.</span><span class="sxs-lookup"><span data-stu-id="86c60-130">Note that [object] in the above format can refer to an object like a table, view, or stored procedure, or an entire database or schema.</span></span> <span data-ttu-id="86c60-131">W tych przypadkach baza danych formularze: [dbname] i schemat:: [SchemaName] są używane odpowiednio.</span><span class="sxs-lookup"><span data-stu-id="86c60-131">For the latter cases, the forms DATABASE::[dbname] and SCHEMA::[schemaname] are used, respectively.</span></span>

<span data-ttu-id="86c60-132">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="86c60-132">For example:</span></span>  
<span data-ttu-id="86c60-133">Wybierz pozycję na dbo. myTable według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="86c60-133">SELECT on dbo.myTable by public</span></span>  
<span data-ttu-id="86c60-134">Wybierz w bazie danych:: Moja baza danych przez publiczną</span><span class="sxs-lookup"><span data-stu-id="86c60-134">SELECT on DATABASE::myDatabase by public</span></span>  
<span data-ttu-id="86c60-135">Wybierz pozycję w SCHEMAcie:: moje schematy według opinii publicznej</span><span class="sxs-lookup"><span data-stu-id="86c60-135">SELECT on SCHEMA::mySchema by public</span></span>  

<span data-ttu-id="86c60-136">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions .</span><span class="sxs-lookup"><span data-stu-id="86c60-136">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-actions.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-137">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="86c60-137">-AuditActionGroup</span></span>
<span data-ttu-id="86c60-138">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="86c60-138">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="86c60-139">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="86c60-139">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="86c60-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="86c60-140">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="86c60-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="86c60-141">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="86c60-142">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="86c60-142">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="86c60-143">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="86c60-143">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="86c60-144">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="86c60-144">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

```yaml
Type: AuditActionGroups[]
Parameter Sets: (All)
Aliases:
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, AUDIT_CHANGE_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-145">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="86c60-145">-DatabaseName</span></span>
<span data-ttu-id="86c60-146">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="86c60-146">SQL Database name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86c60-147">-DefaultProfile</span></span>
<span data-ttu-id="86c60-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86c60-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86c60-149">-PassThru</span></span>
<span data-ttu-id="86c60-150">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="86c60-150">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86c60-151">-ResourceGroupName</span></span>
<span data-ttu-id="86c60-152">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86c60-152">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-153">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="86c60-153">-RetentionInDays</span></span>
<span data-ttu-id="86c60-154">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="86c60-154">The number of retention days for the audit logs.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-155">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="86c60-155">-ServerName</span></span>
<span data-ttu-id="86c60-156">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="86c60-156">SQL Database server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-157">-State</span><span class="sxs-lookup"><span data-stu-id="86c60-157">-State</span></span>
<span data-ttu-id="86c60-158">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="86c60-158">The state of the policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-159">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="86c60-159">-StorageAccountName</span></span>
<span data-ttu-id="86c60-160">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="86c60-160">The name of the storage account.</span></span> <span data-ttu-id="86c60-161">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="86c60-161">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="86c60-162">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="86c60-162">This parameter is not required.</span></span>  
<span data-ttu-id="86c60-163">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="86c60-163">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="86c60-164">Jeśli zasady inspekcji są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="86c60-164">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-165">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="86c60-165">-StorageKeyType</span></span>
<span data-ttu-id="86c60-166">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="86c60-166">Specifies which of the storage access keys to use.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-167">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86c60-167">-Confirm</span></span>
<span data-ttu-id="86c60-168">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c60-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86c60-169">-WhatIf</span></span>
<span data-ttu-id="86c60-170">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86c60-170">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86c60-171">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86c60-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86c60-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86c60-172">CommonParameters</span></span>
<span data-ttu-id="86c60-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86c60-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86c60-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86c60-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86c60-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86c60-175">INPUTS</span></span>

### <span data-ttu-id="86c60-176">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="86c60-176">None</span></span>
<span data-ttu-id="86c60-177">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="86c60-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="86c60-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86c60-178">OUTPUTS</span></span>

### <span data-ttu-id="86c60-179">Microsoft. Azure. Commands. SQL. Security. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="86c60-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="86c60-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86c60-180">NOTES</span></span>

## <span data-ttu-id="86c60-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86c60-181">RELATED LINKS</span></span>
