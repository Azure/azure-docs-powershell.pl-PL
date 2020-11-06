---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditing.md
ms.openlocfilehash: 8480037bf4b756a03a40ad1c1dff01ab1d28ac69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548272"
---
# <span data-ttu-id="1c276-101">Set-AzureRmSqlServerAuditing</span><span class="sxs-lookup"><span data-stu-id="1c276-101">Set-AzureRmSqlServerAuditing</span></span>

## <span data-ttu-id="1c276-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c276-102">SYNOPSIS</span></span>
<span data-ttu-id="1c276-103">Zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c276-103">Changes the auditing settings of an Azure SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c276-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c276-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerAuditing -State <String> [-AuditActionGroup <AuditActionGroups[]>] [-PassThru]
 [-StorageAccountName <String>] [-StorageKeyType <String>] [-RetentionInDays <UInt32>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1c276-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c276-105">DESCRIPTION</span></span>
<span data-ttu-id="1c276-106">Polecenie cmdlet **Set-AzureRmSqlServerAuditing** zmienia ustawienia inspekcji programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1c276-106">The **Set-AzureRmSqlServerAuditing** cmdlet changes the auditing settings of an Azure SQL server.</span></span>
<span data-ttu-id="1c276-107">Aby użyć polecenia cmdlet, użyj parametrów *ResourceGroupName* oraz *nazwa_serwera* w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="1c276-107">To use the cmdlet, use the *ResourceGroupName* and *ServerName* parameters to identify the server.</span></span>
<span data-ttu-id="1c276-108">Określ parametr *StorageAccountName* , aby określić konto magazynu dla dzienników inspekcji i parametr *StorageKeyType* w celu zdefiniowania kluczy magazynowania.</span><span class="sxs-lookup"><span data-stu-id="1c276-108">Specify the *StorageAccountName* parameter to specify the storage account for the audit logs and the *StorageKeyType* parameter to define the storage keys.</span></span>
<span data-ttu-id="1c276-109">Użyj parametru *State* , aby włączyć/wyłączyć zasady.</span><span class="sxs-lookup"><span data-stu-id="1c276-109">Use the *State* parameter to enable/disable the policy.</span></span>

<span data-ttu-id="1c276-110">Możesz również zdefiniować przechowywanie dzienników inspekcji, ustawiając wartość parametru *RetentionInDays* w celu zdefiniowania okresu dla dzienników inspekcji.</span><span class="sxs-lookup"><span data-stu-id="1c276-110">You can also define retention for the audit logs by setting the value of the *RetentionInDays* parameter to define the period for the audit logs.</span></span>

<span data-ttu-id="1c276-111">Po pomyślnym uruchomieniu polecenia cmdlet Inspekcja baz danych SQL platformy Azure zdefiniowanych w określonym obszarze usługi Azure SQL Server jest włączona.</span><span class="sxs-lookup"><span data-stu-id="1c276-111">After the cmdlet runs successfully, auditing of the Azure SQL databases that are defined in the specified Azure SQL server is enabled.</span></span>
<span data-ttu-id="1c276-112">Jeśli użycie polecenia cmdlet powiedzie się i zostanie użyty parametr *PassThru* , funkcja zwraca obiekt opisujący bieżące zasady inspekcji obiektów BLOB oprócz identyfikatorów serwera.</span><span class="sxs-lookup"><span data-stu-id="1c276-112">If the cmdlet succeeds and you use the *PassThru* parameter, it returns an object describing the current blob auditing policy in addition to the server identifiers.</span></span>
<span data-ttu-id="1c276-113">Identyfikatory serwerów obejmują, ale nie są ograniczone do **ResourceGroupName** oraz **nazwa_serwera**.</span><span class="sxs-lookup"><span data-stu-id="1c276-113">Server identifiers include, but are not limited to, **ResourceGroupName** and **ServerName**.</span></span>

## <span data-ttu-id="1c276-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c276-114">EXAMPLES</span></span>

### <span data-ttu-id="1c276-115">Przykład 1. Włączanie zasad inspekcji serwera SQL w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="1c276-115">Example 1: Enable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Enabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountName "Storage22"
```

### <span data-ttu-id="1c276-116">Przykład 2: wyłączanie zasad inspekcji usługi SQL Server</span><span class="sxs-lookup"><span data-stu-id="1c276-116">Example 2: Disable the auditing policy of an Azure SQL server</span></span>
```
PS C:\>Set-AzureRmSqlServerAuditing -State Disabled -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

## <span data-ttu-id="1c276-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c276-117">PARAMETERS</span></span>

### <span data-ttu-id="1c276-118">-AuditActionGroup</span><span class="sxs-lookup"><span data-stu-id="1c276-118">-AuditActionGroup</span></span>
<span data-ttu-id="1c276-119">Zestaw grup akcji inspekcji</span><span class="sxs-lookup"><span data-stu-id="1c276-119">The set of the audit action groups</span></span>

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

### <span data-ttu-id="1c276-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c276-120">-PassThru</span></span>
<span data-ttu-id="1c276-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1c276-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1c276-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c276-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c276-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c276-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="1c276-124">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="1c276-124">-RetentionInDays</span></span>
<span data-ttu-id="1c276-125">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="1c276-125">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="1c276-126">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1c276-126">-ServerName</span></span>
<span data-ttu-id="1c276-127">Nazwa serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="1c276-127">SQL server name.</span></span>

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

### <span data-ttu-id="1c276-128">-State</span><span class="sxs-lookup"><span data-stu-id="1c276-128">-State</span></span>
<span data-ttu-id="1c276-129">Stan zasad inspekcji</span><span class="sxs-lookup"><span data-stu-id="1c276-129">The state of the auditing policy</span></span>

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

### <span data-ttu-id="1c276-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1c276-130">-StorageAccountName</span></span>
<span data-ttu-id="1c276-131">Nazwa konta magazynu</span><span class="sxs-lookup"><span data-stu-id="1c276-131">The name of the storage account</span></span>

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

### <span data-ttu-id="1c276-132">-StorageKeyType</span><span class="sxs-lookup"><span data-stu-id="1c276-132">-StorageKeyType</span></span>
<span data-ttu-id="1c276-133">Typ klucza magazynu</span><span class="sxs-lookup"><span data-stu-id="1c276-133">The type of the storage key</span></span>

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

### <span data-ttu-id="1c276-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c276-134">-Confirm</span></span>
<span data-ttu-id="1c276-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c276-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c276-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c276-136">-WhatIf</span></span>
<span data-ttu-id="1c276-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c276-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c276-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c276-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c276-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c276-139">-DefaultProfile</span></span>
<span data-ttu-id="1c276-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c276-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1c276-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c276-141">CommonParameters</span></span>
<span data-ttu-id="1c276-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c276-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c276-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c276-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c276-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c276-144">INPUTS</span></span>

## <span data-ttu-id="1c276-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c276-145">OUTPUTS</span></span>

### <span data-ttu-id="1c276-146">Microsoft. Azure. Commands. SQL. Security. model. ServerBlobAuditingSettingsModel</span><span class="sxs-lookup"><span data-stu-id="1c276-146">Microsoft.Azure.Commands.Sql.Security.Model.ServerBlobAuditingSettingsModel</span></span>

## <span data-ttu-id="1c276-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c276-147">NOTES</span></span>

## <span data-ttu-id="1c276-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c276-148">RELATED LINKS</span></span>

