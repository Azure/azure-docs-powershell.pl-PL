---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: 2bae2753861f182943e4ced142f6a2b3ac84bb1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334561"
---
# <span data-ttu-id="32cf4-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="32cf4-101">Set-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="32cf4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="32cf4-103">Ustawia zasady przechowywania długoterminowych serwerów.</span><span class="sxs-lookup"><span data-stu-id="32cf4-103">Sets a server long term retention policy.</span></span>

## <span data-ttu-id="32cf4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32cf4-104">SYNTAX</span></span>

### <span data-ttu-id="32cf4-105">WeeklyRetentionRequired (domyślny)</span><span class="sxs-lookup"><span data-stu-id="32cf4-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy -WeeklyRetention <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32cf4-106">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="32cf4-106">RemovePolicy</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="32cf4-107">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="32cf4-107">MonthlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] -MonthlyRetention <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32cf4-108">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="32cf4-108">YearlyRetentionRequired</span></span>
```
Set-AzSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention <String>] [-MonthlyRetention <String>]
 -YearlyRetention <String> -WeekOfYear <Int32> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32cf4-109">Opis</span><span class="sxs-lookup"><span data-stu-id="32cf4-109">DESCRIPTION</span></span>
<span data-ttu-id="32cf4-110">Polecenie cmdlet **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** ustawia zasady przechowywania terminów długoterminowych zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="32cf4-110">The **Set-AzSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="32cf4-111">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="32cf4-111">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="32cf4-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32cf4-112">EXAMPLES</span></span>

### <span data-ttu-id="32cf4-113">Przykład 1: Ustawianie tygodniowego przechowywania bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="32cf4-113">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="32cf4-114">Spowoduje to ustawienie długoterminowych zasad przechowywania database01, aby zapisywać wszystkie tygodniowe pełne kopie zapasowe przez 2 tygodnie</span><span class="sxs-lookup"><span data-stu-id="32cf4-114">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="32cf4-115">Przykład 2: Ustawianie utrzymania miesięcznego bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="32cf4-115">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="32cf4-116">Spowoduje to ustawienie długoterminowych zasad przechowywania database01 w celu zapisania pierwszej pełnej kopii zapasowej każdego miesiąca przez 5 lat.</span><span class="sxs-lookup"><span data-stu-id="32cf4-116">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="32cf4-117">Przykład 3: Ustawianie rocznych warunków przechowywania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="32cf4-117">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="32cf4-118">Spowoduje to ustawienie długotrwałych zasad przechowywania database01 w celu zapisania pełnej kopii zapasowej wykonanej w dwudziestym 26 roku przez 10 lat.</span><span class="sxs-lookup"><span data-stu-id="32cf4-118">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="32cf4-119">Przykład 4: Ustawianie każdego zachowania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="32cf4-119">Example 4: Set each retention for the current version of long term retention policy</span></span>
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

<span data-ttu-id="32cf4-120">Spowoduje to ustawienie długotrwałych zasad przechowywania dla database01 w celu zapisania pełnej kopii zapasowej przez 14 dni, pierwsze pełne wykonywanie kopii zapasowych każdego miesiąca przez 24 tygodnie oraz wykonywanie pełnej kopii zapasowej w dwudziestym 26 roku przez 10 lat.</span><span class="sxs-lookup"><span data-stu-id="32cf4-120">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="32cf4-121">Przykład 5: usuwanie zasad przechowywania długich terminów</span><span class="sxs-lookup"><span data-stu-id="32cf4-121">Example 5: Remove the long term retention policy</span></span>
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

<span data-ttu-id="32cf4-122">Usuwa zasady database01, dzięki czemu nie są już zapisywane żadne długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="32cf4-122">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="32cf4-123">Nie będzie to miało wpływu na kopie zapasowe, które już zostały zrobione</span><span class="sxs-lookup"><span data-stu-id="32cf4-123">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="32cf4-124">Przykład 6: usuwanie zasad przechowywania długich terminów</span><span class="sxs-lookup"><span data-stu-id="32cf4-124">Example 6: Remove the long term retention policy</span></span>
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

<span data-ttu-id="32cf4-125">Jest to kolejny sposób na usunięcie zasad dla database01, dzięki czemu nie są już zapisywane żadne długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="32cf4-125">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="32cf4-126">Nie będzie to miało wpływu na kopie zapasowe, które już zostały zrobione</span><span class="sxs-lookup"><span data-stu-id="32cf4-126">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="32cf4-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32cf4-127">PARAMETERS</span></span>

### <span data-ttu-id="32cf4-128">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="32cf4-128">-DatabaseName</span></span>
<span data-ttu-id="32cf4-129">Nazwa bazy danych SQL Azure, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="32cf4-129">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="32cf4-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32cf4-130">-DefaultProfile</span></span>
<span data-ttu-id="32cf4-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32cf4-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32cf4-132">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="32cf4-132">-MonthlyRetention</span></span>
<span data-ttu-id="32cf4-133">Miesięczna retencja.</span><span class="sxs-lookup"><span data-stu-id="32cf4-133">The Monthly Retention.</span></span>
<span data-ttu-id="32cf4-134">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="32cf4-134">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="32cf4-135">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="32cf4-135">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="32cf4-136">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="32cf4-136">-RemovePolicy</span></span>
<span data-ttu-id="32cf4-137">Jeśli ta zasada jest podana, zasady dotyczące bazy danych zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="32cf4-137">If provided, the policy for the database will be removed.</span></span>

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

### <span data-ttu-id="32cf4-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32cf4-138">-ResourceGroupName</span></span>
<span data-ttu-id="32cf4-139">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="32cf4-139">The name of the resource group.</span></span>

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

### <span data-ttu-id="32cf4-140">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="32cf4-140">-ServerName</span></span>
<span data-ttu-id="32cf4-141">Nazwa programu Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="32cf4-141">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="32cf4-142">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="32cf4-142">-WeeklyRetention</span></span>
<span data-ttu-id="32cf4-143">Tygodniowe zatrzymanie.</span><span class="sxs-lookup"><span data-stu-id="32cf4-143">The Weekly Retention.</span></span>
<span data-ttu-id="32cf4-144">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="32cf4-144">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="32cf4-145">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="32cf4-145">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="32cf4-146">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="32cf4-146">-WeekOfYear</span></span>
<span data-ttu-id="32cf4-147">Tydzień roku, od 1 do 52, aby zaoszczędzić na rocznych zatrzymań.</span><span class="sxs-lookup"><span data-stu-id="32cf4-147">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

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

### <span data-ttu-id="32cf4-148">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="32cf4-148">-YearlyRetention</span></span>
<span data-ttu-id="32cf4-149">Roczny okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="32cf4-149">The Yearly Retention.</span></span>
<span data-ttu-id="32cf4-150">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="32cf4-150">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="32cf4-151">Istnieje co najmniej 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="32cf4-151">There is a minimum of 7 days and a maximum of 10 years.</span></span>

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

### <span data-ttu-id="32cf4-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32cf4-152">-Confirm</span></span>
<span data-ttu-id="32cf4-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32cf4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32cf4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32cf4-154">-WhatIf</span></span>
<span data-ttu-id="32cf4-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32cf4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32cf4-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="32cf4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32cf4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32cf4-157">CommonParameters</span></span>
<span data-ttu-id="32cf4-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32cf4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32cf4-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32cf4-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32cf4-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32cf4-160">INPUTS</span></span>

### <span data-ttu-id="32cf4-161">System. String</span><span class="sxs-lookup"><span data-stu-id="32cf4-161">System.String</span></span>

### <span data-ttu-id="32cf4-162">System. Int32</span><span class="sxs-lookup"><span data-stu-id="32cf4-162">System.Int32</span></span>

## <span data-ttu-id="32cf4-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32cf4-163">OUTPUTS</span></span>

### <span data-ttu-id="32cf4-164">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="32cf4-164">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="32cf4-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32cf4-165">NOTES</span></span>

## <span data-ttu-id="32cf4-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32cf4-166">RELATED LINKS</span></span>

[<span data-ttu-id="32cf4-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="32cf4-167">Get-AzSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="32cf4-168">Get-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="32cf4-168">Get-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="32cf4-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="32cf4-169">Remove-AzSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="32cf4-170">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="32cf4-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)