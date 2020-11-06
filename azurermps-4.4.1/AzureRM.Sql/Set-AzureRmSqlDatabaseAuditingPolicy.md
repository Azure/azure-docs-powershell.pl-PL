---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 99fb9bf57f056a869310de2fe27d00a72ce5d8c3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527197"
---
# <span data-ttu-id="c4d82-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4d82-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="c4d82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c4d82-102">SYNOPSIS</span></span>
<span data-ttu-id="c4d82-103">Ustawia zasady inspekcji dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4d82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c4d82-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4d82-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c4d82-105">DESCRIPTION</span></span>
<span data-ttu-id="c4d82-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditingPolicy** powoduje zmianę zasad inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="c4d82-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="c4d82-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="c4d82-108">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c4d82-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="c4d82-109">Możesz również zdefiniować przechowywanie w tabeli Dziennik inspekcji, ustawiając wartość parametrów *RetentionInDays* i *TableIdentifier* , aby zdefiniować okres i materiał siewny dla nazw tabel dziennika inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="c4d82-110">Określ parametr *EventType* definiujący typy zdarzeń do inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="c4d82-111">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="c4d82-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="c4d82-112">Jeśli baza danych korzystała z zasad serwera w celu prowadzenia inspekcji przed uruchomieniem tego polecenia cmdlet, inspekcja przestanie działać przy użyciu tych zasad.</span><span class="sxs-lookup"><span data-stu-id="c4d82-112">If the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span>
<span data-ttu-id="c4d82-113">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-113">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="c4d82-114">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="c4d82-114">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="c4d82-115">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d82-115">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="c4d82-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c4d82-116">EXAMPLES</span></span>

### <span data-ttu-id="c4d82-117">Przykład 1: Ustawianie zasad inspekcji bazy danych w celu korzystania z inspekcji tabeli</span><span class="sxs-lookup"><span data-stu-id="c4d82-117">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="c4d82-118">To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01 w celu użycia konta magazynu o nazwie Storage31.</span><span class="sxs-lookup"><span data-stu-id="c4d82-118">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="c4d82-119">Przykład 2: Ustawianie klucza konta magazynu istniejących zasad inspekcji bazy danych</span><span class="sxs-lookup"><span data-stu-id="c4d82-119">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="c4d82-120">To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01, aby nadal korzystać z tej samej nazwy konta magazynu, a następnie używać klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="c4d82-120">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="c4d82-121">Przykład 3: Ustawianie zasad inspekcji bazy danych w celu używania określonego typu zdarzenia</span><span class="sxs-lookup"><span data-stu-id="c4d82-121">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="c4d82-122">Przykład 4: Ustawianie zasad inspekcji bazy danych w celu używania inspekcji obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="c4d82-122">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="c4d82-123">To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01.</span><span class="sxs-lookup"><span data-stu-id="c4d82-123">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="c4d82-124">Zasady rejestrują typ zdarzenia Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="c4d82-124">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="c4d82-125">Polecenie nie powoduje zmiany ustawień miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c4d82-125">The command does not change the storage settings.</span></span>

## <span data-ttu-id="c4d82-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c4d82-126">PARAMETERS</span></span>

### <span data-ttu-id="c4d82-127">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="c4d82-127">-AuditAction</span></span>
<span data-ttu-id="c4d82-128">Określ co najmniej jedno działanie inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-128">Specify one or more audit actions.</span></span>
<span data-ttu-id="c4d82-129">Ten parametr dotyczy tylko inspekcji obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c4d82-129">This parameter is only applicable to Blob auditing.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d82-130">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="c4d82-130">-AuditActionGroup</span></span>
<span data-ttu-id="c4d82-131">Określanie jednej lub kilku grup akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-131">Specify one or more audit action groups.</span></span>
<span data-ttu-id="c4d82-132">Ten parametr dotyczy tylko inspekcji obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="c4d82-132">This parameter is only applicable to Blob auditing.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d82-133">-Audittype</span><span class="sxs-lookup"><span data-stu-id="c4d82-133">-AuditType</span></span>
```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d82-134">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c4d82-134">-DatabaseName</span></span>
<span data-ttu-id="c4d82-135">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-135">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d82-136">-EventType</span><span class="sxs-lookup"><span data-stu-id="c4d82-136">-EventType</span></span>
<span data-ttu-id="c4d82-137">Określa typy zdarzeń do inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-137">Specifies the event types to audit.</span></span>
<span data-ttu-id="c4d82-138">Ten parametr dotyczy tylko inspekcji tabeli.</span><span class="sxs-lookup"><span data-stu-id="c4d82-138">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="c4d82-139">Możesz określić kilka typów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c4d82-139">You can specify several event types.</span></span>
<span data-ttu-id="c4d82-140">Możesz określić, czy wszystkie typy zdarzeń mają być poddawane inspekcji, czy żadne zdarzenia nie będą poddawane inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-140">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="c4d82-141">W przypadku jednoczesnego określenia wszystkich lub brakujących poleceń nie można uruchomić polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d82-141">If you specify All or None at the same time, the cmdlet does not run.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4d82-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4d82-142">-PassThru</span></span>
<span data-ttu-id="c4d82-143">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="c4d82-143">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c4d82-144">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c4d82-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4d82-145">-ResourceGroupName</span></span>
<span data-ttu-id="c4d82-146">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-146">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="c4d82-147">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c4d82-147">-RetentionInDays</span></span>
<span data-ttu-id="c4d82-148">Określa liczbę dni przechowywania w tabeli Dziennik inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-148">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="c4d82-149">Wartość zero (0) oznacza, że tabela nie jest zachowywana.</span><span class="sxs-lookup"><span data-stu-id="c4d82-149">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="c4d82-150">Wartość domyślna to zero.</span><span class="sxs-lookup"><span data-stu-id="c4d82-150">The default value is zero.</span></span>
<span data-ttu-id="c4d82-151">Jeśli określisz wartość większą niż zero, musisz określić wartość parametru *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="c4d82-151">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="c4d82-152">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c4d82-152">-ServerName</span></span>
<span data-ttu-id="c4d82-153">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-153">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="c4d82-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c4d82-154">-StorageAccountName</span></span>
<span data-ttu-id="c4d82-155">Określa nazwę konta magazynu do inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-155">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="c4d82-156">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="c4d82-156">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="c4d82-157">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c4d82-157">This parameter is not required.</span></span>
<span data-ttu-id="c4d82-158">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="c4d82-158">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="c4d82-159">Jeśli zasady inspekcji bazy danych są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="c4d82-159">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="c4d82-160">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="c4d82-160">-StorageKeyType</span></span>
<span data-ttu-id="c4d82-161">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c4d82-161">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="c4d82-162">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c4d82-162">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c4d82-163">Początkowe</span><span class="sxs-lookup"><span data-stu-id="c4d82-163">Primary</span></span>
- <span data-ttu-id="c4d82-164">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="c4d82-164">Secondary</span></span>

<span data-ttu-id="c4d82-165">Wartość domyślna to Primary (podstawowy).</span><span class="sxs-lookup"><span data-stu-id="c4d82-165">The default value is Primary.</span></span>

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

### <span data-ttu-id="c4d82-166">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="c4d82-166">-TableIdentifier</span></span>
<span data-ttu-id="c4d82-167">Określa nazwę tabeli dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="c4d82-167">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="c4d82-168">Określ tę wartość, jeśli dla parametru *RetentionInDays* określono wartość większą niż zero.</span><span class="sxs-lookup"><span data-stu-id="c4d82-168">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="c4d82-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c4d82-169">-Confirm</span></span>
<span data-ttu-id="c4d82-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d82-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4d82-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4d82-171">-WhatIf</span></span>
<span data-ttu-id="c4d82-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4d82-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4d82-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c4d82-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4d82-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4d82-174">-DefaultProfile</span></span>
<span data-ttu-id="c4d82-175">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c4d82-175">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c4d82-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4d82-176">CommonParameters</span></span>
<span data-ttu-id="c4d82-177">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4d82-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4d82-178">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4d82-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4d82-179">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c4d82-179">INPUTS</span></span>

## <span data-ttu-id="c4d82-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c4d82-180">OUTPUTS</span></span>

### <span data-ttu-id="c4d82-181">Microsoft. Azure. Commands. SQL. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="c4d82-181">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="c4d82-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c4d82-182">NOTES</span></span>

## <span data-ttu-id="c4d82-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c4d82-183">RELATED LINKS</span></span>

[<span data-ttu-id="c4d82-184">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="c4d82-184">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="c4d82-185">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="c4d82-185">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="c4d82-186">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c4d82-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


