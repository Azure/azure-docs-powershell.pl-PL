---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: F7EF35E3-BC53-43D9-A71E-0B4316260A08
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseAuditing.md
ms.openlocfilehash: a6d09b573225efa5f8467e9ca02edb65a87ebe10
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544647"
---
# <span data-ttu-id="59043-101">Set-AzureRmSqlDatabaseAuditing</span><span class="sxs-lookup"><span data-stu-id="59043-101">Set-AzureRmSqlDatabaseAuditing</span></span>

## <span data-ttu-id="59043-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59043-102">SYNOPSIS</span></span>
<span data-ttu-id="59043-103">Zmienia ustawienia inspekcji bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="59043-103">Changes the auditing settings for an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59043-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59043-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseAuditing -State <String> [-PassThru] [-AuditActionGroup <AuditActionGroups[]>]
 [-AuditAction <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59043-105">Opis</span><span class="sxs-lookup"><span data-stu-id="59043-105">DESCRIPTION</span></span>
<span data-ttu-id="59043-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseAuditing** zmienia ustawienia inspekcji bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="59043-106">The **Set-AzureRmSqlDatabaseAuditing** cmdlet changes the auditing settings of an Azure SQL database.</span></span>
<span data-ttu-id="59043-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="59043-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="59043-108">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="59043-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="59043-109">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="59043-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="59043-110">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="59043-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="59043-111">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja bazy danych jest włączona.</span><span class="sxs-lookup"><span data-stu-id="59043-111">After the cmdlet runs successfully, auditing of the database is enabled.</span></span>
<span data-ttu-id="59043-112">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektu BLOB oprócz identyfikatorów bazy danych.</span><span class="sxs-lookup"><span data-stu-id="59043-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the database identifiers.</span></span>
<span data-ttu-id="59043-113">Identyfikatory bazy danych obejmują, ale nie są ograniczone do, **ResourceGroupName** , **nazwa_serwera** i **DatabaseName**.</span><span class="sxs-lookup"><span data-stu-id="59043-113">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

## <span data-ttu-id="59043-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59043-114">EXAMPLES</span></span>

### <span data-ttu-id="59043-115">Przykład 1. Włączanie zasad inspekcji bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="59043-115">Example 1: Enable the auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22" -DatabaseName "Database01"
```

### <span data-ttu-id="59043-116">Przykład 2: wyłączanie zasad inspekcji obiektu BLOB bazy danych Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="59043-116">Example 2: Disable the blob auditing policy of an Azure SQL database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

## <span data-ttu-id="59043-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59043-117">PARAMETERS</span></span>

### <span data-ttu-id="59043-118">-AuditAction</span><span class="sxs-lookup"><span data-stu-id="59043-118">-AuditAction</span></span>
<span data-ttu-id="59043-119">Zestaw akcji inspekcji</span><span class="sxs-lookup"><span data-stu-id="59043-119">The set of the audit actions</span></span>

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

### <span data-ttu-id="59043-120">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="59043-120">-AuditActionGroup</span></span>
<span data-ttu-id="59043-121">Zestaw grup akcji inspekcji</span><span class="sxs-lookup"><span data-stu-id="59043-121">The set of the audit action groups</span></span>

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

### <span data-ttu-id="59043-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59043-122">-DatabaseName</span></span>
<span data-ttu-id="59043-123">Nazwa bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="59043-123">SQL Database name.</span></span>

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

### <span data-ttu-id="59043-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59043-124">-PassThru</span></span>
<span data-ttu-id="59043-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="59043-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="59043-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59043-126">-ResourceGroupName</span></span>
<span data-ttu-id="59043-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59043-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="59043-128">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="59043-128">-RetentionInDays</span></span>
<span data-ttu-id="59043-129">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="59043-129">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="59043-130">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="59043-130">-ServerName</span></span>
<span data-ttu-id="59043-131">Nazwa serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="59043-131">SQL Database server name.</span></span>

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

### <span data-ttu-id="59043-132">-State</span><span class="sxs-lookup"><span data-stu-id="59043-132">-State</span></span>
<span data-ttu-id="59043-133">Stan zasad inspekcji</span><span class="sxs-lookup"><span data-stu-id="59043-133">The state of the auditing policy</span></span>

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

### <span data-ttu-id="59043-134">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="59043-134">-StorageAccountName</span></span>
<span data-ttu-id="59043-135">Nazwa konta magazynu</span><span class="sxs-lookup"><span data-stu-id="59043-135">The name of the storage account</span></span>

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

### <span data-ttu-id="59043-136">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="59043-136">-StorageKeyType</span></span>
<span data-ttu-id="59043-137">Typ klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="59043-137">The type of the storage key</span></span>

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

### <span data-ttu-id="59043-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59043-138">-Confirm</span></span>
<span data-ttu-id="59043-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59043-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59043-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59043-140">-WhatIf</span></span>
<span data-ttu-id="59043-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59043-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59043-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59043-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59043-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59043-143">-DefaultProfile</span></span>
<span data-ttu-id="59043-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59043-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="59043-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59043-145">CommonParameters</span></span>
<span data-ttu-id="59043-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59043-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59043-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59043-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59043-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59043-148">INPUTS</span></span>

## <span data-ttu-id="59043-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59043-149">OUTPUTS</span></span>

### <span data-ttu-id="59043-150">Microsoft. Azure. Commands. SQL. Security. model. DatabaseBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="59043-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="59043-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59043-151">NOTES</span></span>

## <span data-ttu-id="59043-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59043-152">RELATED LINKS</span></span>

