---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 457FD595-D5E1-45C4-9DB8-C3C6C30A0E94
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseThreatDetectionPolicy.md
ms.openlocfilehash: 746a9a9908865047d5b904b5b47b71ca9c30fbd3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542819"
---
# <span data-ttu-id="e8354-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8354-101">Set-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>

## <span data-ttu-id="e8354-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8354-102">SYNOPSIS</span></span>
<span data-ttu-id="e8354-103">Ustawia zasady wykrywania zagrożeń dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e8354-103">Sets a threat detection policy on a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8354-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8354-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <DetectionType[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8354-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8354-105">DESCRIPTION</span></span>
<span data-ttu-id="e8354-106">Polecenie cmdlet **Set-AzureRmSqlDatabaseThreatDetectionPolicy** ustawia zasady wykrywania zagrożeń w bazie danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="e8354-106">The **Set-AzureRmSqlDatabaseThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL database.</span></span>
<span data-ttu-id="e8354-107">W celu włączenia wykrywania zagrożeń w bazie danych należy włączyć zasady inspekcji w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e8354-107">In order to enable threat detection on a database an auditing policy must be enabled on that database.</span></span>

<span data-ttu-id="e8354-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* , *nazwa_serwera* i *DatabaseName* , które identyfikują bazę danych.</span><span class="sxs-lookup"><span data-stu-id="e8354-108">To use this cmdlet, specify the *ResourceGroupName* , *ServerName* and *DatabaseName* parameters to identify the database.</span></span>

<span data-ttu-id="e8354-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="e8354-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e8354-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8354-110">EXAMPLES</span></span>

### <span data-ttu-id="e8354-111">Przykład 1: Ustawianie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="e8354-111">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -DatabaseName "Database01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability", "SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="e8354-112">To polecenie ustawia zasady wykrywania zagrożeń dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="e8354-112">This command sets the threat detection policy for a database named Database01 on the server named Server01.</span></span>

## <span data-ttu-id="e8354-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8354-113">PARAMETERS</span></span>

### <span data-ttu-id="e8354-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e8354-114">-DatabaseName</span></span>
<span data-ttu-id="e8354-115">Określa nazwę bazy danych, w której ustawiono zasadę.</span><span class="sxs-lookup"><span data-stu-id="e8354-115">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="e8354-116">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="e8354-116">-EmailAdmins</span></span>
<span data-ttu-id="e8354-117">Określa, czy zasady wykrywania zagrożeń kontaktują się z administratorami za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="e8354-117">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="e8354-118">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="e8354-118">-ExcludedDetectionType</span></span>
<span data-ttu-id="e8354-119">Określa tablicę typów wykrywania, które należy wykluczyć z zasad.</span><span class="sxs-lookup"><span data-stu-id="e8354-119">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="e8354-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e8354-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e8354-121">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="e8354-121">Sql_Injection</span></span> 
- <span data-ttu-id="e8354-122">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="e8354-122">Sql_Injection_Vulnerability</span></span> 
- <span data-ttu-id="e8354-123">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="e8354-123">Access_Anomaly</span></span> 
- <span data-ttu-id="e8354-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8354-124">None</span></span>

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

### <span data-ttu-id="e8354-125">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="e8354-125">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="e8354-126">Określa rozdzielaną średnikami listę adresów e-mail, do których zasady wysyłają powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="e8354-126">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="e8354-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8354-127">-PassThru</span></span>
<span data-ttu-id="e8354-128">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="e8354-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e8354-129">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="e8354-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e8354-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8354-130">-ResourceGroupName</span></span>
<span data-ttu-id="e8354-131">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="e8354-131">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e8354-132">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e8354-132">-RetentionInDays</span></span>
<span data-ttu-id="e8354-133">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="e8354-133">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="e8354-134">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e8354-134">-ServerName</span></span>
<span data-ttu-id="e8354-135">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="e8354-135">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="e8354-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e8354-136">-StorageAccountName</span></span>
<span data-ttu-id="e8354-137">Określa nazwę konta magazynu, które ma być używane.</span><span class="sxs-lookup"><span data-stu-id="e8354-137">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="e8354-138">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="e8354-138">Wildcards are not permitted.</span></span> <span data-ttu-id="e8354-139">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8354-139">This parameter is not required.</span></span> <span data-ttu-id="e8354-140">Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zasad wykrywania zagrożeń w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="e8354-140">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="e8354-141">Jeśli zasada wykrywania zagrożeń dla bazy danych jest zdefiniowana po raz pierwszy i ten parametr nie zostanie podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="e8354-141">If this is the first time a database threat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="e8354-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8354-142">-Confirm</span></span>
<span data-ttu-id="e8354-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8354-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8354-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8354-144">-WhatIf</span></span>
<span data-ttu-id="e8354-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8354-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8354-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8354-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8354-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8354-147">-DefaultProfile</span></span>
<span data-ttu-id="e8354-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8354-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8354-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8354-149">CommonParameters</span></span>
<span data-ttu-id="e8354-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8354-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8354-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8354-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8354-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8354-152">INPUTS</span></span>

###  
<span data-ttu-id="e8354-153">Nie możesz popotokować danych wejściowych tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8354-153">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="e8354-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8354-154">OUTPUTS</span></span>

### <span data-ttu-id="e8354-155">Microsoft. Azure. Commands. SQL. ThreatDetection. model. DatabaseThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="e8354-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DatabaseThreatDetectionPolicyModel</span></span>
<span data-ttu-id="e8354-156">To polecenie cmdlet zwraca obiekt **model. DatabaseThreatDetectionPolicyModel** .</span><span class="sxs-lookup"><span data-stu-id="e8354-156">This cmdlet returns a **Model.DatabaseThreatDetectionPolicyModel** object.</span></span>

## <span data-ttu-id="e8354-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8354-157">NOTES</span></span>

## <span data-ttu-id="e8354-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8354-158">RELATED LINKS</span></span>

[<span data-ttu-id="e8354-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8354-159">Get-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Get-AzureRmSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="e8354-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="e8354-160">Remove-AzureRmSqlDatabaseThreatDetectionPolicy</span></span>](./Remove-AzureRmSqlDatabaseThreatDetectionPolicy.md)

[<span data-ttu-id="e8354-161">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="e8354-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


