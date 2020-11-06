---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverauditing
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 2a81030cdf985ae338692e59d86da30cee50694f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544060"
---
# <span data-ttu-id="83f55-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="83f55-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="83f55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="83f55-102">SYNOPSIS</span></span>
<span data-ttu-id="83f55-103">Zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83f55-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83f55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="83f55-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="83f55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="83f55-105">DESCRIPTION</span></span>
<span data-ttu-id="83f55-106">Polecenie cmdlet **Set-AzureRmSqlServerAuditing** zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="83f55-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="83f55-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="83f55-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="83f55-108">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="83f55-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="83f55-109">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="83f55-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="83f55-110">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="83f55-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="83f55-111">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja baz danych SQL platformy Azure zdefiniowanych w określonym obszarze usługi Azure SQL Server jest włączona.</span><span class="sxs-lookup"><span data-stu-id="83f55-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="83f55-112">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektów BLOB oprócz identyfikatorów serwera.</span><span class="sxs-lookup"><span data-stu-id="83f55-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="83f55-113">Identyfikatory serwerów obejmują, ale nie są ograniczone do **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="83f55-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="83f55-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="83f55-114">EXAMPLES</span></span>

### <span data-ttu-id="83f55-115">Przykład 1. Włączanie zasad inspekcji serwera SQL w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="83f55-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="83f55-116">Przykład 2: wyłączanie zasad inspekcji usługi SQL Server</span><span class="sxs-lookup"><span data-stu-id="83f55-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="83f55-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="83f55-117">PARAMETERS</span></span>

### <span data-ttu-id="83f55-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="83f55-118">-AuditActionGroup</span></span>
<span data-ttu-id="83f55-119">Zalecany zestaw grup akcji, który ma być używany, jest następującą kombinacją — spowoduje to inspekcję wszystkich zapytań i procedur składowanych wykonywanych w bazie danych, a także udanych i nieudanych logowań:</span><span class="sxs-lookup"><span data-stu-id="83f55-119">The recommended set of action groups to use is the following combination - this will audit all the queries and stored procedures executed against the database, as well as successful and failed logins:</span></span>  
  
<span data-ttu-id="83f55-120">"BATCH_COMPLETED_GROUP",</span><span class="sxs-lookup"><span data-stu-id="83f55-120">"BATCH_COMPLETED_GROUP",</span></span>  
<span data-ttu-id="83f55-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span><span class="sxs-lookup"><span data-stu-id="83f55-121">"SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP",</span></span>  
<span data-ttu-id="83f55-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span><span class="sxs-lookup"><span data-stu-id="83f55-122">"FAILED_DATABASE_AUTHENTICATION_GROUP"</span></span>  

<span data-ttu-id="83f55-123">Ta powyższa kombinacja również jest skonfigurowanym ustawieniem domyślnym.</span><span class="sxs-lookup"><span data-stu-id="83f55-123">This above combination is also the set that is configured by default.</span></span> <span data-ttu-id="83f55-124">Te grupy obejmują wszystkie instrukcje SQL i procedury składowane wykonywane w odniesieniu do bazy danych i nie powinny być używane w połączeniu z innymi grupami, ponieważ spowoduje to powstanie zduplikowanych dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="83f55-124">These groups cover all SQL statements and stored procedures executed against the database, and should not be used in combination with other groups as this will result in duplicate audit logs.</span></span>
<span data-ttu-id="83f55-125">Aby uzyskać więcej informacji, zobacz https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups .</span><span class="sxs-lookup"><span data-stu-id="83f55-125">For more information, see https://docs.microsoft.com/en-us/sql/relational-databases/security/auditing/sql-server-audit-action-groups-and-actions#database-level-audit-action-groups.</span></span>

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

### <span data-ttu-id="83f55-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f55-126">-DefaultProfile</span></span>
<span data-ttu-id="83f55-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="83f55-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83f55-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83f55-128">-PassThru</span></span>
<span data-ttu-id="83f55-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="83f55-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="83f55-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f55-130">-ResourceGroupName</span></span>
<span data-ttu-id="83f55-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83f55-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="83f55-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="83f55-132">-RetentionInDays</span></span>
<span data-ttu-id="83f55-133">Liczba dni przechowywania dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="83f55-133">The number of retention days for the audit logs.</span></span>

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

### <span data-ttu-id="83f55-134">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="83f55-134">-ServerName</span></span>
<span data-ttu-id="83f55-135">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="83f55-135">SQL server name.</span></span>

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

### <span data-ttu-id="83f55-136">-State</span><span class="sxs-lookup"><span data-stu-id="83f55-136">-State</span></span>
<span data-ttu-id="83f55-137">Stan zasad.</span><span class="sxs-lookup"><span data-stu-id="83f55-137">The state of the policy.</span></span>

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

### <span data-ttu-id="83f55-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="83f55-138">-StorageAccountName</span></span>
<span data-ttu-id="83f55-139">Nazwa konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="83f55-139">The name of the storage account.</span></span> <span data-ttu-id="83f55-140">Znaki wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="83f55-140">Wildcard characters are not permitted.</span></span>  
<span data-ttu-id="83f55-141">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="83f55-141">This parameter is not required.</span></span>  
<span data-ttu-id="83f55-142">Jeśli ten parametr nie jest określony, polecenie cmdlet używa konta magazynu, które zostało zdefiniowane wcześniej jako część zasad inspekcji.</span><span class="sxs-lookup"><span data-stu-id="83f55-142">If you do not specify this parameter, the cmdlet uses the storage account that was defined previously as part of the auditing policy.</span></span>  
<span data-ttu-id="83f55-143">Jeśli zasady inspekcji są definiowane po raz pierwszy, a ten parametr nie jest określony, wykonanie polecenia cmdlet nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="83f55-143">If this is the first time an auditing policy is defined and you do not specify this parameter, the cmdlet fails.</span></span>

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

### <span data-ttu-id="83f55-144">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="83f55-144">-StorageKeyType</span></span>
<span data-ttu-id="83f55-145">Określa, który z kluczy dostępu do magazynowania ma być używany.</span><span class="sxs-lookup"><span data-stu-id="83f55-145">Specifies which of the storage access keys to use.</span></span>

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

### <span data-ttu-id="83f55-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83f55-146">-Confirm</span></span>
<span data-ttu-id="83f55-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83f55-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f55-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f55-148">-WhatIf</span></span>
<span data-ttu-id="83f55-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83f55-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="83f55-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="83f55-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f55-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f55-151">CommonParameters</span></span>
<span data-ttu-id="83f55-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83f55-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f55-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83f55-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f55-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83f55-154">INPUTS</span></span>

### <span data-ttu-id="83f55-155">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="83f55-155">None</span></span>
<span data-ttu-id="83f55-156">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="83f55-156">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="83f55-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="83f55-157">OUTPUTS</span></span>

### <span data-ttu-id="83f55-158">Microsoft. Azure. Commands. SQL. Security. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="83f55-158">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="83f55-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="83f55-159">NOTES</span></span>

## <span data-ttu-id="83f55-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83f55-160">RELATED LINKS</span></span>
