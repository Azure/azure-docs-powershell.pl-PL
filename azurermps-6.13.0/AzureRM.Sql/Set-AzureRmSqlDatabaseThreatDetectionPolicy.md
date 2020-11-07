---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasethreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: fe8a76ed0851393462ba94937d2ab92914b503b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718257"
---
# <span data-ttu-id="25f50-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="25f50-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="25f50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25f50-102">SYNOPSIS</span></span>
<span data-ttu-id="25f50-103">Ustawia zasady wykrywania zagrożeń dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="25f50-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25f50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25f50-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25f50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25f50-105">DESCRIPTION</span></span>
<span data-ttu-id="25f50-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseThreatDetectionPolicy** ustawia zasady wykrywania zagrożeń w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="25f50-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="25f50-107">W celu włączenia wykrywania zagrożeń w bazie danych należy włączyć zasady inspekcji w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="25f50-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>
<span data-ttu-id="25f50-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.</span><span class="sxs-lookup"><span data-stu-id="25f50-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="25f50-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="25f50-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="25f50-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25f50-110">EXAMPLES</span></span>

### <span data-ttu-id="25f50-111">Przykład 1: Ustawianie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="25f50-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="25f50-112">To polecenie ustawia zasady wykrywania zagrożeń dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="25f50-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="25f50-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25f50-113">PARAMETERS</span></span>

### <span data-ttu-id="25f50-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25f50-114">-DatabaseName</span></span>
<span data-ttu-id="25f50-115">Określa nazwę bazy danych, w której ustawiono zasadę.</span><span class="sxs-lookup"><span data-stu-id="25f50-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="25f50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25f50-116">-DefaultProfile</span></span>
<span data-ttu-id="25f50-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25f50-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25f50-118">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="25f50-118">-EmailAdmins</span></span>
<span data-ttu-id="25f50-119">Określa, czy zasady wykrywania zagrożeń kontaktują się z administratorami za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="25f50-119">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="25f50-120">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="25f50-120">-ExcludedDetectionType</span></span>
<span data-ttu-id="25f50-121">Określa tablicę typów wykrywania, które należy wykluczyć z zasad.</span><span class="sxs-lookup"><span data-stu-id="25f50-121">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="25f50-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="25f50-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="25f50-123">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="25f50-123">Sql_Injection</span></span> 
- <span data-ttu-id="25f50-124">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="25f50-124">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="25f50-125">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="25f50-125">Access_Anomaly</span></span> 
- <span data-ttu-id="25f50-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="25f50-126">None</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]
Parameter Sets: (All)
Aliases:
Accepted values: Sql_Injection, Sql_Injection_Vulnerability, Access_Anomaly, None

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25f50-127">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="25f50-127">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="25f50-128">Określa rozdzielaną średnikami listę adresów e-mail, do których zasady wysyłają powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="25f50-128">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="25f50-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25f50-129">-PassThru</span></span>
<span data-ttu-id="25f50-130">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="25f50-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="25f50-131">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="25f50-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25f50-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25f50-132">-ResourceGroupName</span></span>
<span data-ttu-id="25f50-133">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="25f50-133">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="25f50-134">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="25f50-134">-RetentionInDays</span></span>
<span data-ttu-id="25f50-135">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="25f50-135">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="25f50-136">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="25f50-136">-ServerName</span></span>
<span data-ttu-id="25f50-137">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="25f50-137">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="25f50-138">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="25f50-138">-StorageAccountName</span></span>
<span data-ttu-id="25f50-139">Określa nazwę konta magazynu, które ma być używane.</span><span class="sxs-lookup"><span data-stu-id="25f50-139">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="25f50-140">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="25f50-140">Wildcards are not permitted.</span></span> <span data-ttu-id="25f50-141">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="25f50-141">This parameter is not required.</span></span> <span data-ttu-id="25f50-142">Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zasad wykrywania zagrożeń w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="25f50-142">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="25f50-143">Jeśli zasada wykrywania zagrożeń dla bazy danych jest zdefiniowana po raz pierwszy i ten parametr nie zostanie podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="25f50-143">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="25f50-144">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25f50-144">-Confirm</span></span>
<span data-ttu-id="25f50-145">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25f50-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25f50-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25f50-146">-WhatIf</span></span>
<span data-ttu-id="25f50-147">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25f50-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25f50-148">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25f50-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25f50-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25f50-149">CommonParameters</span></span>
<span data-ttu-id="25f50-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25f50-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25f50-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25f50-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25f50-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25f50-152">INPUTS</span></span>

### <span data-ttu-id="25f50-153">System. String</span><span class="sxs-lookup"><span data-stu-id="25f50-153">System.String</span></span>

### <span data-ttu-id="25f50-154">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="25f50-154">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="25f50-155">Microsoft. Azure. Commands. SQL. ThreatDetection. model. Detecttype []</span><span class="sxs-lookup"><span data-stu-id="25f50-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="25f50-156">System. Nullable ' 1 [[System. UInt32; mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="25f50-156">System.Nullable\`1[[System.UInt32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="25f50-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25f50-157">OUTPUTS</span></span>

### <span data-ttu-id="25f50-158">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="25f50-158">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="25f50-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25f50-159">NOTES</span></span>

## <span data-ttu-id="25f50-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25f50-160">RELATED LINKS</span></span>

[<span data-ttu-id="25f50-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="25f50-161">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="25f50-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="25f50-162">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="25f50-163">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="25f50-163">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


