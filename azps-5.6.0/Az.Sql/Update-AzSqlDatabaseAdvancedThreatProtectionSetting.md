---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 9677f45e772cbcb48190f5792df97e96051180c4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992272"
---
# <span data-ttu-id="200e2-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="200e2-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="200e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="200e2-102">SYNOPSIS</span></span>
<span data-ttu-id="200e2-103">Ustawia zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="200e2-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="200e2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="200e2-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="200e2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="200e2-105">DESCRIPTION</span></span>
<span data-ttu-id="200e2-106">Polecenie cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="200e2-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="200e2-107">Aby włączyć zaawansowaną ochronę przed zagrożeniami w bazie danych, ustawienia inspekcji muszą być włączone w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="200e2-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="200e2-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName,* *ServerName* i *DatabaseName* w celu zidentyfikowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="200e2-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="200e2-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="200e2-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="200e2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="200e2-110">EXAMPLES</span></span>

### <span data-ttu-id="200e2-111">Przykład 1. Ustawianie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="200e2-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="200e2-112">To polecenie określa zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych o nazwie Database01 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="200e2-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="200e2-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="200e2-113">PARAMETERS</span></span>

### <span data-ttu-id="200e2-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="200e2-114">-DatabaseName</span></span>
<span data-ttu-id="200e2-115">Określa nazwę bazy danych, w której są ustawione ustawienia.</span><span class="sxs-lookup"><span data-stu-id="200e2-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="200e2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="200e2-116">-DefaultProfile</span></span>
<span data-ttu-id="200e2-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="200e2-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="200e2-118">- EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="200e2-118">-EmailAdmins</span></span>
<span data-ttu-id="200e2-119">Określa, czy administratorzy zaawansowanych ustawień ochrony przed zagrożeniami kontaktowali się przy użyciu poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="200e2-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="200e2-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="200e2-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="200e2-121">Określa tablicę typów wykrywania, które mają być wykluczone z ustawień.</span><span class="sxs-lookup"><span data-stu-id="200e2-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="200e2-122">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="200e2-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="200e2-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="200e2-123">Sql_Injection</span></span> 
- <span data-ttu-id="200e2-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="200e2-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="200e2-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="200e2-125">Access_Anomaly</span></span> 
- <span data-ttu-id="200e2-126">Brak</span><span class="sxs-lookup"><span data-stu-id="200e2-126">None</span></span>

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

### <span data-ttu-id="200e2-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="200e2-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="200e2-128">Określa rozdzielaną średnikami listę adresów e-mail, do których ustawienia wysyłają alerty.</span><span class="sxs-lookup"><span data-stu-id="200e2-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="200e2-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="200e2-129">-PassThru</span></span>
<span data-ttu-id="200e2-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="200e2-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="200e2-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="200e2-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="200e2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="200e2-132">-ResourceGroupName</span></span>
<span data-ttu-id="200e2-133">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="200e2-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="200e2-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="200e2-134">-RetentionInDays</span></span>
<span data-ttu-id="200e2-135">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="200e2-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="200e2-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="200e2-136">-ServerName</span></span>
<span data-ttu-id="200e2-137">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="200e2-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="200e2-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="200e2-138">-StorageAccountName</span></span>
<span data-ttu-id="200e2-139">Określa nazwę używanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="200e2-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="200e2-140">Symbole wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="200e2-140">Wildcards are not permitted.</span></span> <span data-ttu-id="200e2-141">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="200e2-141">This parameter is not required.</span></span> <span data-ttu-id="200e2-142">Jeśli ten parametr nie zostanie podany, polecenie cmdlet będzie używać konta magazynu zdefiniowanego wcześniej jako część zaawansowanych ustawień ochrony przed zagrożeniami w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="200e2-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="200e2-143">Jeśli po raz pierwszy zdefiniowano zaawansowane ustawienia ochrony przed zagrożeniami bazy danych, a ten parametr nie jest podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="200e2-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="200e2-144">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="200e2-144">-Confirm</span></span>
<span data-ttu-id="200e2-145">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="200e2-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="200e2-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="200e2-146">-WhatIf</span></span>
<span data-ttu-id="200e2-147">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="200e2-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="200e2-148">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="200e2-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="200e2-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="200e2-149">CommonParameters</span></span>
<span data-ttu-id="200e2-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="200e2-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="200e2-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="200e2-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="200e2-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="200e2-152">INPUTS</span></span>

### <span data-ttu-id="200e2-153">System.String</span><span class="sxs-lookup"><span data-stu-id="200e2-153">System.String</span></span>

### <span data-ttu-id="200e2-154">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="200e2-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="200e2-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="200e2-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="200e2-156">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="200e2-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="200e2-157">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="200e2-157">OUTPUTS</span></span>

### <span data-ttu-id="200e2-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="200e2-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="200e2-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="200e2-159">NOTES</span></span>

## <span data-ttu-id="200e2-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="200e2-160">RELATED LINKS</span></span>

[<span data-ttu-id="200e2-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="200e2-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="200e2-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="200e2-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="200e2-163">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="200e2-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


