---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405622"
---
# <span data-ttu-id="7eeaf-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7eeaf-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="7eeaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7eeaf-102">SYNOPSIS</span></span>
<span data-ttu-id="7eeaf-103">Kończy relację kopiowania ciągłego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="7eeaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7eeaf-104">SYNTAX</span></span>

### <span data-ttu-id="7eeaf-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7eeaf-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7eeaf-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="7eeaf-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7eeaf-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="7eeaf-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7eeaf-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="7eeaf-108">DESCRIPTION</span></span>
<span data-ttu-id="7eeaf-109">Polecenie **cmdlet Stop-AzureSqlDatabaseCopy** kończy relację kopiowania ciągłego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="7eeaf-110">To polecenie cmdlet zatrzymuje ruch danych między źródłową bazą danych a pomocniczą lub docelową bazą danych, a następnie zmienia stan pomocniczej bazy danych na autonomiczną bazę danych online.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="7eeaf-111">Istnieją dwa sposoby zakończenia ciągłej relacji kopiowania, zakończenia lub planowanego zakończenia oraz rozwiązania wymuszonego z możliwością utraty danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="7eeaf-112">Na serwerze hostowym źródłową bazę danych możesz uruchomić to polecenie cmdlet w trybie zakończenia lub zakończenia wymuszonego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="7eeaf-113">Na serwerze hostowym pomocniczą bazę danych należy użyć trybu zakończenia wymuszonego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="7eeaf-114">Planowane zakończenie czeka, aż wszystkie zatwierdzone transakcje w źródłowej bazie danych (w momencie uruchamiania polecenia cmdlet) będą replikowane do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="7eeaf-115">Zakończenie wymuszone nie czeka na replikację wszystkich zaległych transakcji zatwierdzonej i może spowodować utratę danych w pomocniczej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="7eeaf-116">Gdy stan replikacji to OCZEKUJE, tylko wymuszone zakończenie może pomyślnie zakończyć relację kopiowania ciągłego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="7eeaf-117">Jeśli stan replikacji to OCZEKUJE, zakończenie, które nie jest wymuszone, nie jest obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="7eeaf-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7eeaf-118">EXAMPLES</span></span>

### <span data-ttu-id="7eeaf-119">Przykład 1. Zakończenie relacji kopiowania ciągłego</span><span class="sxs-lookup"><span data-stu-id="7eeaf-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="7eeaf-120">To polecenie kończy relację kopiowania ciągłego bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="7eeaf-121">Serwer o nazwie bk0b8kf658 hostuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="7eeaf-122">Przykład 2. Forcibly terminate a continuous copy relationship</span><span class="sxs-lookup"><span data-stu-id="7eeaf-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="7eeaf-123">Pierwsze polecenie pobiera relację kopiowania bazy danych dla bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="7eeaf-124">Drugie polecenie na stałe kończy relację kopiowania ciągłego z serwera hostowego pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="7eeaf-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7eeaf-125">PARAMETERS</span></span>

### <span data-ttu-id="7eeaf-126">— Baza danych</span><span class="sxs-lookup"><span data-stu-id="7eeaf-126">-Database</span></span>
<span data-ttu-id="7eeaf-127">Określa obiekt reprezentujący źródłową bazę danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="7eeaf-128">To polecenie cmdlet powoduje zakończenie relacji kopii ciągłej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7eeaf-129">-DatabaseCopy</span></span>
<span data-ttu-id="7eeaf-130">Określa obiekt reprezentujący bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="7eeaf-131">To polecenie cmdlet powoduje zakończenie relacji kopii ciągłej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="7eeaf-132">Ten parametr akceptuje dane wejściowe potoku.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-132">This parameter accepts pipeline input.</span></span>

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7eeaf-133">-DatabaseName</span></span>
<span data-ttu-id="7eeaf-134">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-134">Specifies the name of a database.</span></span>
<span data-ttu-id="7eeaf-135">To polecenie cmdlet powoduje zakończenie relacji kopii ciągłej bazy danych, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-136">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="7eeaf-136">-Force</span></span>
<span data-ttu-id="7eeaf-137">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7eeaf-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="7eeaf-138">-ForcedTermination</span></span>
<span data-ttu-id="7eeaf-139">Wskazuje, że to polecenie cmdlet powoduje wymuszone zakończenie relacji kopiowania ciągłego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="7eeaf-140">Wymuszone rozwiązanie umowy może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="7eeaf-141">Aby uruchomić to polecenie cmdlet na serwerze hostowym docelową bazę danych, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="7eeaf-142">Aby uruchomić to polecenie cmdlet na serwerze hostowym źródłową bazę danych, jeśli pomocnicza baza danych jest niedostępna, musisz określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="7eeaf-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="7eeaf-143">-PartnerDatabase</span></span>
<span data-ttu-id="7eeaf-144">Określa nazwę pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="7eeaf-145">Określenie nazwy musi być zgodne z nazwą źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-145">If you specify a name, it must match the name of the source database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="7eeaf-146">-PartnerServer</span></span>
<span data-ttu-id="7eeaf-147">Określa nazwę serwera hostowego docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-147">Specifies the name of the server that hosts the target database.</span></span>

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-148">— Profil</span><span class="sxs-lookup"><span data-stu-id="7eeaf-148">-Profile</span></span>
<span data-ttu-id="7eeaf-149">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7eeaf-150">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-151">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7eeaf-151">-ServerName</span></span>
<span data-ttu-id="7eeaf-152">Określa nazwę serwera, na którym znajduje się źródłowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-152">Specifies the name of the server on which the source database resides.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7eeaf-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7eeaf-153">-Confirm</span></span>
<span data-ttu-id="7eeaf-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7eeaf-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7eeaf-155">-WhatIf</span></span>
<span data-ttu-id="7eeaf-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7eeaf-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7eeaf-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eeaf-158">CommonParameters</span></span>
<span data-ttu-id="7eeaf-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eeaf-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eeaf-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eeaf-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eeaf-161">INPUTS</span></span>

### <span data-ttu-id="7eeaf-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7eeaf-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="7eeaf-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="7eeaf-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="7eeaf-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7eeaf-164">OUTPUTS</span></span>

### <span data-ttu-id="7eeaf-165">Brak</span><span class="sxs-lookup"><span data-stu-id="7eeaf-165">None</span></span>

## <span data-ttu-id="7eeaf-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7eeaf-166">NOTES</span></span>
* <span data-ttu-id="7eeaf-167">Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="7eeaf-168">Aby uzyskać przykład sposobu używania uwierzytelniania opartego na certyfikatach w celu ustawienia bieżącej subskrypcji, zobacz polecenie cmdlet **New-AzureSqlDatabaseServerContext.**</span><span class="sxs-lookup"><span data-stu-id="7eeaf-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="7eeaf-169">Ograniczenia: Na serwerze hostowym pomocniczą bazę danych obsługiwane jest tylko rozwiązanie wymuszone.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="7eeaf-170">Wpływ zakończenia na poprzednią pomocniczą bazę danych: Po zakończeniu pomocnicza baza danych staje się niezależną bazą danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="7eeaf-171">Jeśli baza danych została już ukończona w pomocniczej bazie danych, po zakończeniu tej bazy danych będzie ona otwarta do pełnego dostępu.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="7eeaf-172">Jeśli źródłową bazą danych jest baza danych do odczytu i zapisu, poprzednia pomocnicza baza danych również staje się bazą danych do odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="7eeaf-173">Jeśli trwa iniekcjowanie, oznacza to, że iniekcjowanie zostanie przerwane, a poprzednia pomocnicza baza danych nigdy nie będzie widoczna na serwerze hostowym pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="7eeaf-174">Źródłową bazę danych można ustawić jako tryb tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="7eeaf-175">Gwarantuje to synchronizowanie źródłowych i pomocniczych baz danych po zakończeniu oraz zapewnia, że podczas zakończenia nie są zatwierdzone żadne transakcje.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="7eeaf-176">Po zakończeniu zakończenia ustaw dla źródła powrót do trybu odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="7eeaf-177">Opcjonalnie możesz również ustawić dla poprzedniej pomocniczej bazy danych tryb odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="7eeaf-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="7eeaf-178">Monitorowanie: Aby sprawdzić stan operacji na poziomie źródłowym i docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation.**</span><span class="sxs-lookup"><span data-stu-id="7eeaf-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="7eeaf-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7eeaf-179">RELATED LINKS</span></span>

[<span data-ttu-id="7eeaf-180">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="7eeaf-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="7eeaf-181">Operacje na platformie Azure SQL Databases</span><span class="sxs-lookup"><span data-stu-id="7eeaf-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="7eeaf-182">Zatrzymywanie kopiowania bazy danych</span><span class="sxs-lookup"><span data-stu-id="7eeaf-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[<span data-ttu-id="7eeaf-183">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7eeaf-183">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="7eeaf-184">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="7eeaf-184">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


