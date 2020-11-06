---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabaseauditingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditingPolicy.md
ms.openlocfilehash: 9f551b5b334f6151b42faebf8b60d2939a0680d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542179"
---
# <span data-ttu-id="d0f7c-101">Set-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d0f7c-101">Set-AzureRmSqlDatabaseAuditingPolicy</span></span>

## <span data-ttu-id="d0f7c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0f7c-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f7c-103">Ustawia zasady inspekcji dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-103">Sets the auditing policy for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0f7c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0f7c-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditingPolicy [-AuditType <AuditType>] [-PassThru]
 [-AuditActionGroup <AuditActionGroups[]>] [-AuditAction <String[]>] [-EventType <String[]>]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>]
 [-TableIdentifier <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f7c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0f7c-105">DESCRIPTION</span></span>
<span data-ttu-id="d0f7c-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditingPolicy** powoduje zmianę zasad inspekcji bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-106">The **Set-AzureRmSqlDatabaseAuditingPolicy** cmdlet changes the auditing policy of an Azure SQL database.</span></span>
<span data-ttu-id="d0f7c-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="d0f7c-108">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>

<span data-ttu-id="d0f7c-109">Możesz również zdefiniować przechowywanie w tabeli Dziennik inspekcji, ustawiając wartość parametrów *RetentionInDays* i *TableIdentifier* , aby zdefiniować okres i materiał siewny dla nazw tabel dziennika inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-109">You can also define retention for the audit logs table by setting the value of the *RetentionInDays* and *TableIdentifier* parameters to define the period and the seed for the audit log table names.</span></span>
<span data-ttu-id="d0f7c-110">Określ parametr *EventType* definiujący typy zdarzeń do inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-110">Specify the *EventType* parameter to define which event types to audit.</span></span>

<span data-ttu-id="d0f7c-111">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="d0f7c-112">W przypadku inspekcji tabeli Jeśli baza danych korzystała z zasad serwera w celu prowadzenia inspekcji przed uruchomieniem tego polecenia cmdlet, inspekcja przestanie działać przy użyciu tych zasad.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-112">For Table Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, auditing stops using that policy.</span></span> <span data-ttu-id="d0f7c-113">W przypadku inspekcji obiektu BLOB, jeśli baza danych korzystała z zasad serwera w celu prowadzenia inspekcji przed uruchomieniem tego polecenia cmdlet, obie zasady inspekcji będą istnieć obok siebie.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-113">For Blob Auditing, if the database used the policy of its server for auditing before you ran this cmdlet, both auditing policies will exist side-by-side.</span></span>
<span data-ttu-id="d0f7c-114">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-114">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="d0f7c-115">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-115">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="d0f7c-116">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-116">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d0f7c-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0f7c-117">EXAMPLES</span></span>

### <span data-ttu-id="d0f7c-118">Przykład 1: Ustawianie zasad inspekcji bazy danych w celu korzystania z inspekcji tabeli</span><span class="sxs-lookup"><span data-stu-id="d0f7c-118">Example 1: Set the auditing policy of a database to use Table auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Table -StorageAccountName "Storage31"
```

<span data-ttu-id="d0f7c-119">To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01 w celu użycia konta magazynu o nazwie Storage31.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-119">This command sets the auditing policy of database named Database01 located on Server01 to use the storage account named Storage31.</span></span>

### <span data-ttu-id="d0f7c-120">Przykład 2: Ustawianie klucza konta magazynu istniejących zasad inspekcji bazy danych</span><span class="sxs-lookup"><span data-stu-id="d0f7c-120">Example 2: Set the storage account key of an existing auditing policy of a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -StorageAccountKey Secondary
```

<span data-ttu-id="d0f7c-121">To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01, aby nadal korzystać z tej samej nazwy konta magazynu, a następnie używać klucza pomocniczego.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-121">This command sets the auditing policy of database named Database01 located on Server01 to keep using the same storage account name but to now use the secondary key.</span></span>

### <span data-ttu-id="d0f7c-122">Przykład 3: Ustawianie zasad inspekcji bazy danych w celu używania określonego typu zdarzenia</span><span class="sxs-lookup"><span data-stu-id="d0f7c-122">Example 3: Set the auditing policy of a database to use a specific event type</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -EventType Login_Failure
```

### <span data-ttu-id="d0f7c-123">Przykład 4: Ustawianie zasad inspekcji bazy danych w celu używania inspekcji obiektów BLOB</span><span class="sxs-lookup"><span data-stu-id="d0f7c-123">Example 4: Set the auditing policy of a database to use Blob auditing</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -AuditAction "UPDATE ON database::[Database01] BY [public]"  -RetentionInDays 8
```

<span data-ttu-id="d0f7c-124">To polecenie ustawia zasady inspekcji bazy danych o nazwie Database01 znajdującej się na server01.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-124">This command sets the auditing policy of database named Database01 located on Server01.</span></span>
<span data-ttu-id="d0f7c-125">Zasady rejestrują typ zdarzenia Login_Failure.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-125">The policy logs the Login_Failure event type.</span></span>
<span data-ttu-id="d0f7c-126">Polecenie nie powoduje zmiany ustawień miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-126">The command does not change the storage settings.</span></span>

## <span data-ttu-id="d0f7c-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0f7c-127">PARAMETERS</span></span>

### <span data-ttu-id="d0f7c-128">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="d0f7c-128">-AuditAction</span></span>
<span data-ttu-id="d0f7c-129">Określ co najmniej jedno działanie inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-129">Specify one or more audit actions.</span></span>
<span data-ttu-id="d0f7c-130">Ten parametr dotyczy tylko inspekcji obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-130">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d0f7c-131">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="d0f7c-131">-AuditActionGroup</span></span>
<span data-ttu-id="d0f7c-132">Określanie jednej lub kilku grup akcji inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-132">Specify one or more audit action groups.</span></span>
<span data-ttu-id="d0f7c-133">Ten parametr dotyczy tylko inspekcji obiektu BLOB.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-133">This parameter is only applicable to Blob auditing.</span></span>

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

### <span data-ttu-id="d0f7c-134">-Audittype</span><span class="sxs-lookup"><span data-stu-id="d0f7c-134">-AuditType</span></span>
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

### <span data-ttu-id="d0f7c-135">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0f7c-135">-DatabaseName</span></span>
<span data-ttu-id="d0f7c-136">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-136">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="d0f7c-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f7c-137">-DefaultProfile</span></span>
<span data-ttu-id="d0f7c-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d0f7c-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0f7c-139">-EventType</span><span class="sxs-lookup"><span data-stu-id="d0f7c-139">-EventType</span></span>
<span data-ttu-id="d0f7c-140">Określa typy zdarzeń do inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-140">Specifies the event types to audit.</span></span>
<span data-ttu-id="d0f7c-141">Ten parametr dotyczy tylko inspekcji tabeli.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-141">This parameter is only applicable to Table auditing.</span></span>

<span data-ttu-id="d0f7c-142">Możesz określić kilka typów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-142">You can specify several event types.</span></span>
<span data-ttu-id="d0f7c-143">Możesz określić, czy wszystkie typy zdarzeń mają być poddawane inspekcji, czy żadne zdarzenia nie będą poddawane inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-143">You can specify All to audit all of the event types or None to specify that no events will be audited.</span></span>
<span data-ttu-id="d0f7c-144">W przypadku jednoczesnego określenia wszystkich lub brakujących poleceń nie można uruchomić polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-144">If you specify All or None at the same time, the cmdlet does not run.</span></span>

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

### <span data-ttu-id="d0f7c-145">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d0f7c-145">-PassThru</span></span>
<span data-ttu-id="d0f7c-146">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-146">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="d0f7c-147">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-147">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d0f7c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0f7c-148">-ResourceGroupName</span></span>
<span data-ttu-id="d0f7c-149">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-149">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d0f7c-150">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="d0f7c-150">-RetentionInDays</span></span>
<span data-ttu-id="d0f7c-151">Określa liczbę dni przechowywania w tabeli Dziennik inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-151">Specifies the number of retention days for the audit logs table.</span></span>
<span data-ttu-id="d0f7c-152">Wartość zero (0) oznacza, że tabela nie jest zachowywana.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-152">A value of zero (0) means that the table is not retained.</span></span>
<span data-ttu-id="d0f7c-153">Wartość domyślna to zero.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-153">The default value is zero.</span></span>
<span data-ttu-id="d0f7c-154">Jeśli określisz wartość większą niż zero, musisz określić wartość parametru *TableIdentifer* .</span><span class="sxs-lookup"><span data-stu-id="d0f7c-154">If you specify a value greater than zero, you must specify a value for the *TableIdentifer* parameter.</span></span>

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

### <span data-ttu-id="d0f7c-155">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="d0f7c-155">-ServerName</span></span>
<span data-ttu-id="d0f7c-156">Określa nazwę serwera, na którym jest przechowywana baza danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-156">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d0f7c-157">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d0f7c-157">-StorageAccountName</span></span>
<span data-ttu-id="d0f7c-158">Określa nazwę konta magazynu do inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-158">Specifies the name of the storage account for auditing the database.</span></span>
<span data-ttu-id="d0f7c-159">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-159">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="d0f7c-160">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-160">This parameter is not required.</span></span>
<span data-ttu-id="d0f7c-161">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-161">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy of the database.</span></span>
<span data-ttu-id="d0f7c-162">Jeśli zasady inspekcji bazy danych są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-162">If this is the first time a database auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="d0f7c-163">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="d0f7c-163">-StorageKeyType</span></span>
<span data-ttu-id="d0f7c-164">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-164">Specifies which of the storage access keys to use.</span></span>
<span data-ttu-id="d0f7c-165">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="d0f7c-165">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="d0f7c-166">Początkowe</span><span class="sxs-lookup"><span data-stu-id="d0f7c-166">Primary</span></span>
- <span data-ttu-id="d0f7c-167">Dodatkowej</span><span class="sxs-lookup"><span data-stu-id="d0f7c-167">Secondary</span></span>

<span data-ttu-id="d0f7c-168">Wartość domyślna to Primary (podstawowy).</span><span class="sxs-lookup"><span data-stu-id="d0f7c-168">The default value is Primary.</span></span>

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

### <span data-ttu-id="d0f7c-169">-TableIdentifier</span><span class="sxs-lookup"><span data-stu-id="d0f7c-169">-TableIdentifier</span></span>
<span data-ttu-id="d0f7c-170">Określa nazwę tabeli dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-170">Specifies the name of the audit logs table.</span></span>
<span data-ttu-id="d0f7c-171">Określ tę wartość, jeśli dla parametru *RetentionInDays* określono wartość większą niż zero.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-171">Specify this value if you specify a value greater than zero for the *RetentionInDays* parameter.</span></span>

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

### <span data-ttu-id="d0f7c-172">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0f7c-172">-Confirm</span></span>
<span data-ttu-id="d0f7c-173">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-173">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f7c-174">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f7c-174">-WhatIf</span></span>
<span data-ttu-id="d0f7c-175">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-175">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f7c-176">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-176">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f7c-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f7c-177">CommonParameters</span></span>
<span data-ttu-id="d0f7c-178">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f7c-179">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0f7c-179">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f7c-180">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0f7c-180">INPUTS</span></span>

### <span data-ttu-id="d0f7c-181">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0f7c-181">None</span></span>
<span data-ttu-id="d0f7c-182">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d0f7c-182">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d0f7c-183">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0f7c-183">OUTPUTS</span></span>

### <span data-ttu-id="d0f7c-184">Microsoft. Azure. Commands. SQL. Security. model. DatabaseAuditingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="d0f7c-184">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseAuditingPolicyModel</span></span>

## <span data-ttu-id="d0f7c-185">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0f7c-185">NOTES</span></span>

## <span data-ttu-id="d0f7c-186">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0f7c-186">RELATED LINKS</span></span>

[<span data-ttu-id="d0f7c-187">Get-AzureRmSqlDatabaseAuditingPolicy</span><span class="sxs-lookup"><span data-stu-id="d0f7c-187">Get-AzureRmSqlDatabaseAuditingPolicy</span></span>](./Get-AzureRmSqlDatabaseAuditingPolicy.md)

[<span data-ttu-id="d0f7c-188">Remove-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="d0f7c-188">Remove-AzureRmSqlDatabaseAuditing</span></span>](./Remove-AzureRmSqlDatabaseAuditing.md)

[<span data-ttu-id="d0f7c-189">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="d0f7c-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


