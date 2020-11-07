---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: ee54928b1f32c726bc2847eace77e6ccbe48c4d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544059"
---
# <span data-ttu-id="e301e-101">Set-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e301e-101">Set-AzureRmSqlServerAuditingPolicy</span></span>

## <span data-ttu-id="e301e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e301e-102">SYNOPSIS</span></span>
<span data-ttu-id="e301e-103">Zmienia zasady inspekcji serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e301e-103">Changes the auditing policy of a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e301e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e301e-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e301e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e301e-105">DESCRIPTION</span></span>
<span data-ttu-id="e301e-106">Polecenie cmdlet **Set-AzureRmSqlServerAuditingPolicy** zmienia zasady inspekcji serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e301e-106">The **Set-AzureRmSqlServerAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL Database server.</span></span>
<span data-ttu-id="e301e-107">Określ parametry *ResourceGroupName* i *nazwa_serwera* identyfikujące serwer, parametr *StorageAccountName* umożliwiający określenie konta magazynu dla dzienników inspekcji oraz parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania do użycia.</span><span class="sxs-lookup"><span data-stu-id="e301e-107">Specify the *ResourceGroupName* and *ServerName* parameters to identify the server, the *StorageAccountName* parameter to specify the storage account for the audit logs, and the *StorageKeyType* parameter to define the storage keys to use.</span></span>

<span data-ttu-id="e301e-108">Możesz również zdefiniować przechowywanie w tabeli Dziennik inspekcji, ustawiając wartość parametrów *RetentionInDays* i *TableIdentifier* , aby zdefiniować okres i materiał siewny dla nazw tabel dziennika inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-108">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="e301e-109">Określ parametr *EventType* definiujący typy zdarzeń do inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-109">Specify the *EventType* parameter to define which event types to audit.</span></span>
<span data-ttu-id="e301e-110">Po uruchomieniu tego polecenia cmdlet Inspekcja baz danych korzystających z zasad tego serwera jest włączona.</span><span class="sxs-lookup"><span data-stu-id="e301e-110">After you run this cmdlet, auditing of the databases that use the policy of this server is enabled.</span></span>
<span data-ttu-id="e301e-111">Jeśli polecenie cmdlet powiedzie się i określisz parametr *PassThru* , polecenie cmdlet zwróci obiekt opisujący bieżące zasady inspekcji i identyfikatory serwera.</span><span class="sxs-lookup"><span data-stu-id="e301e-111">If the cmdlet succeeds and you specify the *PassThru* parameter, the cmdlet returns an object that describes the current auditing policy, and the server identifiers.</span></span>
<span data-ttu-id="e301e-112">Identyfikatory serwera obejmują **ResourceGroupName** i **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="e301e-112">Server identifiers include **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="e301e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e301e-113">EXAMPLES</span></span>

### <span data-ttu-id="e301e-114">Przykład 1: Ustawianie zasad inspekcji programu Azure SQL Server używanie inspekcji tabeli</span><span class="sxs-lookup"><span data-stu-id="e301e-114">Example 1: Set the auditing policy of an Azure SQL server use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

<span data-ttu-id="e301e-115">To polecenie ustawia zasady inspekcji serwera o nazwie Server01, aby korzystać z konta magazynu o nazwie Storage22.</span><span class="sxs-lookup"><span data-stu-id="e301e-115">This command sets the auditing policy of the server named Server01 to use a storage account named Storage22.</span></span>

### <span data-ttu-id="e301e-116">Przykład 2: Ustawianie klucza konta magazynu istniejących zasad inspekcji dla programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="e301e-116">Example 2: Set the storage account key of an existing auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

<span data-ttu-id="e301e-117">To polecenie ustawia zasady inspekcji serwera o nazwie Server01, aby używać klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="e301e-117">This command sets the auditing policy of the server named Server01 to use the secondary key.</span></span>
<span data-ttu-id="e301e-118">Polecenie nie powoduje zmiany nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="e301e-118">The command does not modify the storage account name.</span></span>

### <span data-ttu-id="e301e-119">Przykład 3: Ustawianie zasad inspekcji programu Azure SQL Server w celu używania określonego typu zdarzenia</span><span class="sxs-lookup"><span data-stu-id="e301e-119">Example 3: Set the auditing policy of an Azure SQL server to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### <span data-ttu-id="e301e-120">Przykład 4: Ustawianie zasad inspekcji bazy danych w celu używania inspekcji obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="e301e-120">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

<span data-ttu-id="e301e-121">To polecenie ustawia zasady inspekcji serwera o nazwie Server01, aby korzystały z typu zdarzenia Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="e301e-121">This command sets the auditing policy of the server named Server01 to use the Login_Failure event type.</span></span>
<span data-ttu-id="e301e-122">To polecenie nie modyfikuje żadnego innego ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e301e-122">This command does not modify any other setting.</span></span>

## <span data-ttu-id="e301e-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e301e-123">PARAMETERS</span></span>

### <span data-ttu-id="e301e-124">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="e301e-124">-AuditActionGroup</span></span>
<span data-ttu-id="e301e-125">Określanie jednej lub kilku grup akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-125">Specify one or more audit action groups.</span></span> <span data-ttu-id="e301e-126">Ten parametr dotyczy tylko inspekcji obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="e301e-126">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="e301e-127">-Audittype</span><span class="sxs-lookup"><span data-stu-id="e301e-127">-AuditType</span></span>
<span data-ttu-id="e301e-128">Określ typ inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-128">Specify the audit type.</span></span> <span data-ttu-id="e301e-129">Dzienniki inspekcji można zapisywać w magazynie tabel lub w magazynie obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="e301e-129">Audit logs can be written to Table storage or Blob storage.</span></span> <span data-ttu-id="e301e-130">Inspekcja obiektów BLOB zapewnia wyższą wydajność i obsługuje inspekcję na poziomie obiektów.</span><span class="sxs-lookup"><span data-stu-id="e301e-130">Blob auditing provides higher performance and supports object-level auditing.</span></span>

```yaml
Type: AuditType
Parameter Sets: (All)
Aliases:
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e301e-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e301e-131">-DefaultProfile</span></span>
<span data-ttu-id="e301e-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e301e-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e301e-133">-EventType</span><span class="sxs-lookup"><span data-stu-id="e301e-133">-EventType</span></span>
<span data-ttu-id="e301e-134">Określa typy zdarzeń do inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-134">Specifies the event types to audit.</span></span>
<span data-ttu-id="e301e-135">Ten parametr dotyczy tylko inspekcji tabeli.</span><span class="sxs-lookup"><span data-stu-id="e301e-135">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="e301e-136">Możesz określić kilka typów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e301e-136">You can specify several event types.</span></span>
<span data-ttu-id="e301e-137">Możesz określić, czy wszystkie typy zdarzeń mają być poddawane inspekcji, czy żadne zdarzenia nie będą poddawane inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-137">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="e301e-138">Jeśli jednocześnie określisz wszystkie lub nie, polecenie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e301e-138">If you specify All or None at the same time, the command fails.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e301e-139">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e301e-139">-PassThru</span></span>
<span data-ttu-id="e301e-140">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e301e-140">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e301e-141">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e301e-141">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e301e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e301e-142">-ResourceGroupName</span></span>
<span data-ttu-id="e301e-143">Określa nazwę grupy zasobów zawierającej bazę danych.</span><span class="sxs-lookup"><span data-stu-id="e301e-143">Specifies the name of the resource group that contains the database.</span></span>

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

### <span data-ttu-id="e301e-144">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e301e-144">-RetentionInDays</span></span>
<span data-ttu-id="e301e-145">Określa liczbę dni przechowywania w tabeli Dziennik inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-145">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="e301e-146">Wartość zero (0) oznacza, że tabela nie jest zachowywana.</span><span class="sxs-lookup"><span data-stu-id="e301e-146">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="e301e-147">jest to ustawienie domyślne.</span><span class="sxs-lookup"><span data-stu-id="e301e-147">this is the default.</span></span>
<span data-ttu-id="e301e-148">W przypadku określenia wartości większej niż zero należy również określić wartość parametru *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="e301e-148">If you specify a value greater than zero, you must also specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="e301e-149">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e301e-149">-ServerName</span></span>
<span data-ttu-id="e301e-150">Określa nazwę serwera, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="e301e-150">Specifies the name of the server that contains the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e301e-151">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e301e-151">-StorageAccountName</span></span>
<span data-ttu-id="e301e-152">Określa nazwę konta magazynu do inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e301e-152">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="e301e-153">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="e301e-153">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="e301e-154">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e301e-154">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="e301e-155">Jeśli zasady inspekcji bazy danych są definiowane po raz pierwszy i nie określono tego parametru, polecenie nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e301e-155">If this is the first time a database auditing policy is defined and you do not specify this parameter, the command fails.</span></span>

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

### <span data-ttu-id="e301e-156">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="e301e-156">-StorageKeyType</span></span>
<span data-ttu-id="e301e-157">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e301e-157">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="e301e-158">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e301e-158">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e301e-159">Początkowe</span><span class="sxs-lookup"><span data-stu-id="e301e-159">Primary</span></span>
- <span data-ttu-id="e301e-160">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="e301e-160">Secondary</span></span>

<span data-ttu-id="e301e-161">Wartość domyślna to Primary (podstawowy).</span><span class="sxs-lookup"><span data-stu-id="e301e-161">The default value is Primary.</span></span>

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

### <span data-ttu-id="e301e-162">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="e301e-162">-TableIdentifier</span></span>
<span data-ttu-id="e301e-163">Określa nazwę tabeli dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="e301e-163">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="e301e-164">Określ tę wartość, jeśli dla parametru *RetentionInDays* określono wartość większą niż zero.</span><span class="sxs-lookup"><span data-stu-id="e301e-164">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="e301e-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e301e-165">-Confirm</span></span>
<span data-ttu-id="e301e-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e301e-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e301e-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e301e-167">-WhatIf</span></span>
<span data-ttu-id="e301e-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e301e-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e301e-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e301e-169">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e301e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e301e-170">CommonParameters</span></span>
<span data-ttu-id="e301e-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e301e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e301e-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e301e-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e301e-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e301e-173">INPUTS</span></span>

### <span data-ttu-id="e301e-174">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e301e-174">None</span></span>
<span data-ttu-id="e301e-175">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e301e-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e301e-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e301e-176">OUTPUTS</span></span>

### <span data-ttu-id="e301e-177">Microsoft. Azure. Commands. SQL. Security. model. ServerAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e301e-177">Microsoft.Azure.Commands.Sql.Security.Model.ServerAuditingPolicyModel</span></span>

## <span data-ttu-id="e301e-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e301e-178">NOTES</span></span>

## <span data-ttu-id="e301e-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e301e-179">RELATED LINKS</span></span>

[<span data-ttu-id="e301e-180">Get-AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e301e-180">Get-AzureRmSqlServerAuditingPolicy</span></span>](./Get-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="e301e-181">Użyj — AzureRmSqlServerAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="e301e-181">Use-AzureRmSqlServerAuditingPolicy</span></span>](./Use-AzureRmSqlServerAuditingPolicy.md)

[<span data-ttu-id="e301e-182">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e301e-182">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

