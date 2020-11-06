---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasebackuplongtermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md
ms.openlocfilehash: c5450ea3ffdcc8c76fa88c8721902b8f8ae77794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542167"
---
# <span data-ttu-id="54c9d-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54c9d-101">Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>

## <span data-ttu-id="54c9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54c9d-102">SYNOPSIS</span></span>
<span data-ttu-id="54c9d-103">Ustawia zasady przechowywania długoterminowych serwerów.</span><span class="sxs-lookup"><span data-stu-id="54c9d-103">Sets a server long term retention policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="54c9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54c9d-104">SYNTAX</span></span>

### <span data-ttu-id="54c9d-105">WeeklyRetentionRequired (domyślny)</span><span class="sxs-lookup"><span data-stu-id="54c9d-105">WeeklyRetentionRequired (Default)</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-WeeklyRetention] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c9d-106">Dziedziczone</span><span class="sxs-lookup"><span data-stu-id="54c9d-106">Legacy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -State <String> -ResourceId <String> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c9d-107">RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="54c9d-107">RemovePolicy</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [-RemovePolicy] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c9d-108">MonthlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="54c9d-108">MonthlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>] [-MonthlyRetention] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54c9d-109">YearlyRetentionRequired</span><span class="sxs-lookup"><span data-stu-id="54c9d-109">YearlyRetentionRequired</span></span>
```
Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy [[-WeeklyRetention] <String>]
 [[-MonthlyRetention] <String>] [-YearlyRetention] <String> [-WeekOfYear] <Int32> [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c9d-110">Opis</span><span class="sxs-lookup"><span data-stu-id="54c9d-110">DESCRIPTION</span></span>
<span data-ttu-id="54c9d-111">Polecenie cmdlet **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** ustawia zasady przechowywania terminów długoterminowych zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="54c9d-111">The **Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy** cmdlet sets the long term retention policy registered to this database.</span></span>
<span data-ttu-id="54c9d-112">Zasady to zasób kopii zapasowej platformy Azure służący do definiowania zasad magazynu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="54c9d-112">The policy is an Azure Backup resource used to define backup storage policy.</span></span>

## <span data-ttu-id="54c9d-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54c9d-113">EXAMPLES</span></span>

### <span data-ttu-id="54c9d-114">Przykład 1: Ustawianie tygodniowego przechowywania bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="54c9d-114">Example 1: Set the weekly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P2W


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P2W
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="54c9d-115">Spowoduje to ustawienie długoterminowych zasad przechowywania database01, aby zapisywać wszystkie tygodniowe pełne kopie zapasowe przez 2 tygodnie</span><span class="sxs-lookup"><span data-stu-id="54c9d-115">This sets the long term retention policy of database01 to save every weekly full backup for 2 weeks</span></span>

### <span data-ttu-id="54c9d-116">Przykład 2: Ustawianie utrzymania miesięcznego bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="54c9d-116">Example 2: Set the monthly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -MonthlyRetention P5Y


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : P5Y
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="54c9d-117">Spowoduje to ustawienie długoterminowych zasad przechowywania database01 w celu zapisania pierwszej pełnej kopii zapasowej każdego miesiąca przez 5 lat.</span><span class="sxs-lookup"><span data-stu-id="54c9d-117">This sets the long term retention policy of database01 to save the first full backup of each month for 5 years</span></span>

### <span data-ttu-id="54c9d-118">Przykład 3: Ustawianie rocznych warunków przechowywania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="54c9d-118">Example 3: Set the yearly retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="54c9d-119">Spowoduje to ustawienie długotrwałych zasad przechowywania database01 w celu zapisania pełnej kopii zapasowej wykonanej w dwudziestym 26 roku przez 10 lat.</span><span class="sxs-lookup"><span data-stu-id="54c9d-119">This sets the long term retention policy of database01 to save the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="54c9d-120">Przykład 4: Ustawianie każdego zachowania dla bieżącej wersji zasad przechowywania długoterminowego</span><span class="sxs-lookup"><span data-stu-id="54c9d-120">Example 4: Set each retention for the current version of long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention 14 -MonthlyRetention P24W -YearlyRetention P10Y -WeekOfYear 26


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : P14D
MonthlyRetention                       : P24W
YearlyRetention                        : P10Y
WeekOfYear                             : 26
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="54c9d-121">Spowoduje to ustawienie długotrwałych zasad przechowywania dla database01 w celu zapisania pełnej kopii zapasowej przez 14 dni, pierwsze pełne wykonywanie kopii zapasowych każdego miesiąca przez 24 tygodnie oraz wykonywanie pełnej kopii zapasowej w dwudziestym 26 roku przez 10 lat.</span><span class="sxs-lookup"><span data-stu-id="54c9d-121">This sets the long term retention policy of database01 to save each full backup for 14 days, the first full backup of each month for 24 weeks, and the full backup taken on the 26th week of the year for 10 years</span></span>

### <span data-ttu-id="54c9d-122">Przykład 4: usuwanie zasad przechowywania długich terminów</span><span class="sxs-lookup"><span data-stu-id="54c9d-122">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RemovePolicy


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="54c9d-123">Usuwa zasady database01, dzięki czemu nie są już zapisywane żadne długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="54c9d-123">Removes the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="54c9d-124">Nie będzie to miało wpływu na kopie zapasowe, które już zostały zrobione</span><span class="sxs-lookup"><span data-stu-id="54c9d-124">This will not affect backups that have already been taken</span></span>

### <span data-ttu-id="54c9d-125">Przykład 4: usuwanie zasad przechowywania długich terminów</span><span class="sxs-lookup"><span data-stu-id="54c9d-125">Example 4: Remove the long term retention policy</span></span>
```powershell
PS C:\> Set-AzureRmSqlDatabaseBackupLongTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -WeeklyRetention P0D


ResourceGroupName                      : resourcegroup01
ServerName                             : server01
DatabaseName                           : database01
WeeklyRetention                        : PT0S
MonthlyRetention                       : PT0S
YearlyRetention                        : PT0S
WeekOfYear                             : 0
State                                  :
RecoveryServicesBackupPolicyResourceId :
Location                               :
```

<span data-ttu-id="54c9d-126">Jest to kolejny sposób na usunięcie zasad dla database01, dzięki czemu nie są już zapisywane żadne długoterminowe kopie zapasowe przechowywania.</span><span class="sxs-lookup"><span data-stu-id="54c9d-126">This is another way of removing the policy for database01 so it no longer saves any long term retention backups.</span></span>
<span data-ttu-id="54c9d-127">Nie będzie to miało wpływu na kopie zapasowe, które już zostały zrobione</span><span class="sxs-lookup"><span data-stu-id="54c9d-127">This will not affect backups that have already been taken</span></span>

## <span data-ttu-id="54c9d-128">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54c9d-128">PARAMETERS</span></span>

### <span data-ttu-id="54c9d-129">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="54c9d-129">-DatabaseName</span></span>
<span data-ttu-id="54c9d-130">Nazwa bazy danych SQL Azure, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="54c9d-130">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="54c9d-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c9d-131">-DefaultProfile</span></span>
<span data-ttu-id="54c9d-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="54c9d-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="54c9d-133">-MonthlyRetention</span><span class="sxs-lookup"><span data-stu-id="54c9d-133">-MonthlyRetention</span></span>
<span data-ttu-id="54c9d-134">Miesięczna retencja.</span><span class="sxs-lookup"><span data-stu-id="54c9d-134">The Monthly Retention.</span></span>
<span data-ttu-id="54c9d-135">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="54c9d-135">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="54c9d-136">Istnieje minumum 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="54c9d-136">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-137">-RemovePolicy</span><span class="sxs-lookup"><span data-stu-id="54c9d-137">-RemovePolicy</span></span>
<span data-ttu-id="54c9d-138">Jeśli ta zasada jest podana, zasady dotyczące bazy danych zostaną usunięte.</span><span class="sxs-lookup"><span data-stu-id="54c9d-138">If provided, the policy for the database will be removed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemovePolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c9d-139">-ResourceGroupName</span></span>
<span data-ttu-id="54c9d-140">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="54c9d-140">The name of the resource group.</span></span>

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

### <span data-ttu-id="54c9d-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c9d-141">-ResourceId</span></span>
<span data-ttu-id="54c9d-142">Identyfikator zasobu kopii zapasowej zasad przechowywania długich terminów.</span><span class="sxs-lookup"><span data-stu-id="54c9d-142">The Resource ID of the backup long term retention policy.</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-143">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="54c9d-143">-ServerName</span></span>
<span data-ttu-id="54c9d-144">Nazwa programu Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="54c9d-144">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="54c9d-145">-State</span><span class="sxs-lookup"><span data-stu-id="54c9d-145">-State</span></span>
<span data-ttu-id="54c9d-146">Stan zasad tworzenia kopii zapasowej długoterminowej przechowywania, "włączony" lub "Disabled"</span><span class="sxs-lookup"><span data-stu-id="54c9d-146">The state of the long term retention backup policy, 'Enabled' or 'Disabled'</span></span>

```yaml
Type: String
Parameter Sets: Legacy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-147">-WeeklyRetention</span><span class="sxs-lookup"><span data-stu-id="54c9d-147">-WeeklyRetention</span></span>
<span data-ttu-id="54c9d-148">Tygodniowe zatrzymanie.</span><span class="sxs-lookup"><span data-stu-id="54c9d-148">The Weekly Retention.</span></span>
<span data-ttu-id="54c9d-149">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="54c9d-149">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="54c9d-150">Istnieje minumum 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="54c9d-150">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: WeeklyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: MonthlyRetentionRequired, YearlyRetentionRequired
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-151">-WeekOfYear</span><span class="sxs-lookup"><span data-stu-id="54c9d-151">-WeekOfYear</span></span>
<span data-ttu-id="54c9d-152">Tydzień roku, od 1 do 52, aby zaoszczędzić na rocznych zatrzymań.</span><span class="sxs-lookup"><span data-stu-id="54c9d-152">The Week of Year, 1 to 52, to save for the Yearly Retention.</span></span>

```yaml
Type: Int32
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-153">-YearlyRetention</span><span class="sxs-lookup"><span data-stu-id="54c9d-153">-YearlyRetention</span></span>
<span data-ttu-id="54c9d-154">Roczny okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="54c9d-154">The Yearly Retention.</span></span>
<span data-ttu-id="54c9d-155">Jeśli zamiast ciągu ISO 8601 zostanie przekazana tylko liczba, dni zostaną przyjmowane jako jednostki.</span><span class="sxs-lookup"><span data-stu-id="54c9d-155">If just a number is passed instead of an ISO 8601 string, days will be assumed as the units.</span></span>
<span data-ttu-id="54c9d-156">Istnieje minumum 7 dni i maksymalnie 10 lat.</span><span class="sxs-lookup"><span data-stu-id="54c9d-156">There is a minumum of 7 days and a maximum of 10 years.</span></span>

```yaml
Type: String
Parameter Sets: YearlyRetentionRequired
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c9d-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="54c9d-157">-Confirm</span></span>
<span data-ttu-id="54c9d-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c9d-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54c9d-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c9d-159">-WhatIf</span></span>
<span data-ttu-id="54c9d-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c9d-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c9d-161">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="54c9d-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54c9d-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c9d-162">CommonParameters</span></span>
<span data-ttu-id="54c9d-163">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c9d-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="54c9d-164">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54c9d-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c9d-165">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54c9d-165">INPUTS</span></span>

### <span data-ttu-id="54c9d-166">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="54c9d-166">None</span></span>
<span data-ttu-id="54c9d-167">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="54c9d-167">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="54c9d-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54c9d-168">OUTPUTS</span></span>

### <span data-ttu-id="54c9d-169">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="54c9d-169">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupLongTermRetentionPolicyModel</span></span>

## <span data-ttu-id="54c9d-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54c9d-170">NOTES</span></span>

## <span data-ttu-id="54c9d-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54c9d-171">RELATED LINKS</span></span>

[<span data-ttu-id="54c9d-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="54c9d-172">Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy</span></span>](./Get-AzureRmSqlDatabaseBackupLongTermRetentionPolicy.md)

[<span data-ttu-id="54c9d-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="54c9d-173">Get-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Get-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="54c9d-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span><span class="sxs-lookup"><span data-stu-id="54c9d-174">Remove-AzureRmSqlDatabaseLongTermRetentionBackup</span></span>](./Remove-AzureRmSqlDatabaseLongTermRetentionBackup.md)

[<span data-ttu-id="54c9d-175">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="54c9d-175">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
