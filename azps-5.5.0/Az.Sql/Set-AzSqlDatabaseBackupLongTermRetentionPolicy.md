---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188011"
---
# <span data-ttu-id="2dd80-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2dd80-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="2dd80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dd80-102">SYNOPSIS</span></span>
<span data-ttu-id="2dd80-103">Ustawia zasady przechowywania długoterminowego serwera.</span><span class="sxs-lookup"><span data-stu-id="2dd80-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="2dd80-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2dd80-104">SYNTAX</span></span>

### <span data-ttu-id="2dd80-105">WeeklyRetentionRequired (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2dd80-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd80-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="2dd80-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2dd80-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="2dd80-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2dd80-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="2dd80-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2dd80-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2dd80-109">DESCRIPTION</span></span>
<span data-ttu-id="2dd80-110">Polecenie cmdlet **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** ustawia dla tej bazy danych zasady przechowywania przez długi czas.</span><span class="sxs-lookup"><span data-stu-id="2dd80-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="2dd80-111">Zasady są zasobem kopii zapasowej azure używanym do definiowania zasad przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="2dd80-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="2dd80-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2dd80-112">EXAMPLES</span></span>

### <span data-ttu-id="2dd80-113">Przykład 1. Ustawianie tygodniowego przechowywania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="2dd80-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="2dd80-114">Dzięki temu zasady przechowywania przez długi czas w bazie danych01 są zachowywane co tydzień z pełną kopią zapasową przez 2 tygodnie.</span><span class="sxs-lookup"><span data-stu-id="2dd80-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="2dd80-115">Przykład 2. Ustawianie miesięcznego okresu przechowywania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="2dd80-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="2dd80-116">W ten sposób są ustawiane zasady przechowywania danych przez długi czas w bazie danych01 w celu zapisywania pierwszej pełnej kopii zapasowej każdego miesiąca przez 5 lat.</span><span class="sxs-lookup"><span data-stu-id="2dd80-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="2dd80-117">Przykład 3. Ustawianie przechowywania co rok dla bieżącej wersji zasad przechowywania długoterminowych</span><span class="sxs-lookup"><span data-stu-id="2dd80-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="2dd80-118">W ten sposób są ustawiane zasady przechowywania danych przez długi czas w bazie danych 01 w celu zapisania pełnej kopii zapasowej wykonanej w 26. tygodniu roku przez 10 lat.</span><span class="sxs-lookup"><span data-stu-id="2dd80-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="2dd80-119">Przykład 4. Ustawianie każdego przechowywania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="2dd80-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
Location                               :
```

<span data-ttu-id="2dd80-120">Dzięki temu zasady przechowywania przez długi czas w bazie danych01 są zachowywane przez 14 dni, pierwsza pełna kopia zapasowa każdego miesiąca przez 24 tygodnie i pełna kopia zapasowa 10 lat z 26. tygodnia roku.</span><span class="sxs-lookup"><span data-stu-id="2dd80-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="2dd80-121">Przykład 5. Usuwanie długoterminowych zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="2dd80-121">Example 5: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="2dd80-122">Usuwa zasady dla bazy danych 01, aby nie zapisywały już żadnych długoterminowych kopii zapasowych przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2dd80-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="2dd80-123">Nie ma to wpływu na kopie zapasowe, które zostały już wykonane</span><span class="sxs-lookup"><span data-stu-id="2dd80-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="2dd80-124">Przykład 6. Usuwanie długoterminowych zasad przechowywania</span><span class="sxs-lookup"><span data-stu-id="2dd80-124">Example 6: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
Location                               :
```

<span data-ttu-id="2dd80-125">Jest to inny sposób usuwania zasad dla bazy danych 01, aby nie zapisywały już żadnych długoterminowych kopii zapasowych przechowywania.</span><span class="sxs-lookup"><span data-stu-id="2dd80-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="2dd80-126">Nie ma to wpływu na kopie zapasowe, które zostały już wykonane</span><span class="sxs-lookup"><span data-stu-id="2dd80-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="2dd80-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2dd80-127">PARAMETERS</span></span>

### <span data-ttu-id="2dd80-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2dd80-128">-DatabaseName</span></span>
<span data-ttu-id="2dd80-129">Nazwa bazy danych Azure SQL Database, która ma być używania.</span><span class="sxs-lookup"><span data-stu-id="2dd80-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="2dd80-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dd80-130">-DefaultProfile</span></span>
<span data-ttu-id="2dd80-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2dd80-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2dd80-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="2dd80-132">-MonthlyRetention</span></span>
<span data-ttu-id="2dd80-133">Miesięczne przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="2dd80-133">The Monthly Retention.</span></span>
<span data-ttu-id="2dd80-134">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.</span><span class="sxs-lookup"><span data-stu-id="2dd80-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2dd80-135">Maksymalna długość wynosi 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="2dd80-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd80-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="2dd80-136">-RemovePolicy</span></span>
<span data-ttu-id="2dd80-137">Jeśli zostanie to podane, zasady bazy danych zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="2dd80-137">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2dd80-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dd80-138">-ResourceGroupName</span></span>
<span data-ttu-id="2dd80-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2dd80-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="2dd80-140">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2dd80-140">-ServerName</span></span>
<span data-ttu-id="2dd80-141">Nazwa serwera Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="2dd80-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="2dd80-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="2dd80-142">-WeeklyRetention</span></span>
<span data-ttu-id="2dd80-143">Tygodniowe przechowywanie.</span><span class="sxs-lookup"><span data-stu-id="2dd80-143">The Weekly Retention.</span></span>
<span data-ttu-id="2dd80-144">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.</span><span class="sxs-lookup"><span data-stu-id="2dd80-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2dd80-145">Maksymalna długość wynosi 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="2dd80-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd80-146">- WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="2dd80-146">-WeekOfYear</span></span>
<span data-ttu-id="2dd80-147">Tydzień roku, od 1 do 52, aby zapisać na przechowywanie co rok.</span><span class="sxs-lookup"><span data-stu-id="2dd80-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd80-148">- YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="2dd80-148">-YearlyRetention</span></span>
<span data-ttu-id="2dd80-149">Przechowywanie co rok.</span><span class="sxs-lookup"><span data-stu-id="2dd80-149">The Yearly Retention.</span></span>
<span data-ttu-id="2dd80-150">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, jednostkami będą dni.</span><span class="sxs-lookup"><span data-stu-id="2dd80-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="2dd80-151">Maksymalna długość wynosi 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="2dd80-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: System.String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dd80-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2dd80-152">-Confirm</span></span>
<span data-ttu-id="2dd80-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2dd80-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dd80-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dd80-154">-WhatIf</span></span>
<span data-ttu-id="2dd80-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2dd80-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2dd80-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2dd80-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dd80-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dd80-157">CommonParameters</span></span>
<span data-ttu-id="2dd80-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2dd80-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dd80-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2dd80-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dd80-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd80-160">INPUTS</span></span>

### <span data-ttu-id="2dd80-161">System.String</span><span class="sxs-lookup"><span data-stu-id="2dd80-161">System.String</span></span>

### <span data-ttu-id="2dd80-162">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2dd80-162">System.Int32</span></span>

## <span data-ttu-id="2dd80-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2dd80-163">OUTPUTS</span></span>

### <span data-ttu-id="2dd80-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2dd80-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="2dd80-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2dd80-165">NOTES</span></span>

## <span data-ttu-id="2dd80-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2dd80-166">RELATED LINKS</span></span>

[<span data-ttu-id="2dd80-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2dd80-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="2dd80-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2dd80-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2dd80-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="2dd80-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="2dd80-170">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2dd80-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)