---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlDatabaseAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlDatabaseAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 1bd5906ac4736fc2aace122070edfebe1e59fe3f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332914"
---
# <span data-ttu-id="29fe7-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="29fe7-101">Update-AzSqlDatabaseAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="29fe7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29fe7-102">SYNOPSIS</span></span>
<span data-ttu-id="29fe7-103">Ustawia zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="29fe7-103">Sets a advanced threat protection settings on a database.</span></span>

## <span data-ttu-id="29fe7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29fe7-104">SYNTAX</span></span>

```
Update-AzSqlDatabaseAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29fe7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="29fe7-105">DESCRIPTION</span></span>
<span data-ttu-id="29fe7-106">Polecenie cmdlet **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="29fe7-106">The **Update-AzSqlDatabaseAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL database.</span></span>
<span data-ttu-id="29fe7-107">Aby włączyć zaawansowaną ochronę przed zagrożeniami w bazie danych, muszą być włączone ustawienia inspekcji w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="29fe7-107">In order to enable advanced threat protection on a database an auditing settings must be enabled on that database.</span></span>
<span data-ttu-id="29fe7-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName*, *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.</span><span class="sxs-lookup"><span data-stu-id="29fe7-108">To use this cmdlet, specify the *ResourceGroupName*, *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="29fe7-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="29fe7-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="29fe7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29fe7-110">EXAMPLES</span></span>

### <span data-ttu-id="29fe7-111">Przykład 1: Ustawianie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="29fe7-111">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlDatabaseAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="29fe7-112">To polecenie ustawia zaawansowane ustawienia ochrony przed zagrożeniami dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="29fe7-112">This command sets the advanced threat protection settings for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="29fe7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29fe7-113">PARAMETERS</span></span>

### <span data-ttu-id="29fe7-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="29fe7-114">-DatabaseName</span></span>
<span data-ttu-id="29fe7-115">Określa nazwę bazy danych, w której ustawiono ustawienia.</span><span class="sxs-lookup"><span data-stu-id="29fe7-115">Specifies the name of the database where the settings is set.</span></span>

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

### <span data-ttu-id="29fe7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29fe7-116">-DefaultProfile</span></span>
<span data-ttu-id="29fe7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="29fe7-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="29fe7-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="29fe7-118">-EmailAdmins</span></span>
<span data-ttu-id="29fe7-119">Określa, czy ustawienia zaawansowanego ochrony przed zagrożeniami mają kontakt z administratorami za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="29fe7-119">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="29fe7-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="29fe7-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="29fe7-121">Określa tablicę typów wykrywania, które należy wykluczyć z ustawień.</span><span class="sxs-lookup"><span data-stu-id="29fe7-121">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="29fe7-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="29fe7-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="29fe7-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="29fe7-123">Sql_Injection</span></span> 
- <span data-ttu-id="29fe7-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="29fe7-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="29fe7-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="29fe7-125">Access_Anomaly</span></span> 
- <span data-ttu-id="29fe7-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="29fe7-126">None</span></span>

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

### <span data-ttu-id="29fe7-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="29fe7-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="29fe7-128">Określa rozdzielaną średnikami listę adresów e-mail, do których mają być wysyłane powiadomienia o ustawieniach.</span><span class="sxs-lookup"><span data-stu-id="29fe7-128">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="29fe7-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="29fe7-129">-PassThru</span></span>
<span data-ttu-id="29fe7-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="29fe7-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="29fe7-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="29fe7-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="29fe7-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29fe7-132">-ResourceGroupName</span></span>
<span data-ttu-id="29fe7-133">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="29fe7-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="29fe7-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="29fe7-134">-RetentionInDays</span></span>
<span data-ttu-id="29fe7-135">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="29fe7-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="29fe7-136">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="29fe7-136">-ServerName</span></span>
<span data-ttu-id="29fe7-137">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="29fe7-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="29fe7-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="29fe7-138">-StorageAccountName</span></span>
<span data-ttu-id="29fe7-139">Określa nazwę konta magazynu, które ma być używane.</span><span class="sxs-lookup"><span data-stu-id="29fe7-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="29fe7-140">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="29fe7-140">Wildcards are not permitted.</span></span> <span data-ttu-id="29fe7-141">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="29fe7-141">This parameter is not required.</span></span> <span data-ttu-id="29fe7-142">Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zaawansowanego ustawienia ochrony przed zagrożeniami w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="29fe7-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="29fe7-143">Jeśli jest to pierwsza definicja zaawansowanego ustawienia ochrony przed zagrożeniami dla bazy danych i nie zostanie podany ten parametr, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="29fe7-143">If this is the first time a database advanced threat protection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="29fe7-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="29fe7-144">-Confirm</span></span>
<span data-ttu-id="29fe7-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29fe7-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29fe7-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29fe7-146">-WhatIf</span></span>
<span data-ttu-id="29fe7-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="29fe7-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29fe7-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="29fe7-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29fe7-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29fe7-149">CommonParameters</span></span>
<span data-ttu-id="29fe7-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29fe7-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29fe7-151">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29fe7-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29fe7-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29fe7-152">INPUTS</span></span>

### <span data-ttu-id="29fe7-153">System. String</span><span class="sxs-lookup"><span data-stu-id="29fe7-153">System.String</span></span>

### <span data-ttu-id="29fe7-154">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29fe7-154">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="29fe7-155">Microsoft. Azure. Commands. SQL. ThreatDetection. model. Detecttype []</span><span class="sxs-lookup"><span data-stu-id="29fe7-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="29fe7-156">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="29fe7-156">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="29fe7-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29fe7-157">OUTPUTS</span></span>

### <span data-ttu-id="29fe7-158">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="29fe7-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="29fe7-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29fe7-159">NOTES</span></span>

## <span data-ttu-id="29fe7-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29fe7-160">RELATED LINKS</span></span>

[<span data-ttu-id="29fe7-161">Get-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="29fe7-161">Get-AzSqlDatabaseThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="29fe7-162">Remove-AzSqlDatabaseThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="29fe7-162">Remove-AzSqlDatabaseThreatDetectionsettings</span></span>](./Remove-AzSqlDatabaseThreatDetectionsettings.md)

[<span data-ttu-id="29fe7-163">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="29fe7-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


