---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055369"
---
# <span data-ttu-id="a2753-101">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a2753-101">Stop-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="a2753-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2753-102">SYNOPSIS</span></span>
<span data-ttu-id="a2753-103">Przerywa ciągłą relację między kopiami.</span><span class="sxs-lookup"><span data-stu-id="a2753-103">Terminates a continuous copy relationship.</span></span>

## <span data-ttu-id="a2753-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2753-104">SYNTAX</span></span>

### <span data-ttu-id="a2753-105">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a2753-105">ByInputObject</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a2753-106">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="a2753-106">ByDatabase</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a2753-107">ByDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2753-107">ByDatabaseName</span></span>
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a2753-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a2753-108">DESCRIPTION</span></span>
<span data-ttu-id="a2753-109">Polecenie cmdlet **stop-AzureSqlDatabaseCopy** przerywa ciągłą relację kopiowania.</span><span class="sxs-lookup"><span data-stu-id="a2753-109">The **Stop-AzureSqlDatabaseCopy** cmdlet terminates a continuous copy relationship.</span></span>
<span data-ttu-id="a2753-110">To polecenie cmdlet zatrzymuje przepływ danych między źródłową bazą danych i pomocniczą lub docelową bazą danych, a następnie zmienia stan pomocniczej bazy danych na autonomiczną bazę danych online.</span><span class="sxs-lookup"><span data-stu-id="a2753-110">This cmdlet stops the data movement between the source database and secondary or target database, and then changes the state of the secondary database to be a stand-alone online database.</span></span>

<span data-ttu-id="a2753-111">Istnieją dwa sposoby kończenia nieciągłej relacji między kopiami, zakończenie lub planowane zakończenie oraz wymuszone zakończenie z możliwością utraty danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-111">There are two ways to end a continuous copy relationship, termination or planned termination and forced termination with possible data loss.</span></span>
<span data-ttu-id="a2753-112">Na serwerze obsługującym źródłową bazę danych możesz uruchomić to polecenie cmdlet w trybie kończenia lub wymuszonego zakończenia.</span><span class="sxs-lookup"><span data-stu-id="a2753-112">On the server that hosts the source database, you can run this cmdlet in termination or forced termination mode.</span></span>
<span data-ttu-id="a2753-113">Na serwerze obsługującym pomocniczą bazę danych należy użyć trybu wymuszonego kończenia.</span><span class="sxs-lookup"><span data-stu-id="a2753-113">On the server that hosts the secondary database, you must use forced termination mode.</span></span>

<span data-ttu-id="a2753-114">Planowane zakończenie nastąpi do momentu zablokowania wszystkich zatwierdzonych transakcji w źródłowej bazie danych w momencie uruchomienia polecenia cmdlet, które zostały zreplikowane do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-114">A planned termination waits until all committed transactions on the source database, at the time that you run the cmdlet, have been replicated to the secondary database.</span></span>
<span data-ttu-id="a2753-115">Wymuszone zakończenie nie odczeka na replikację transakcji zatwierdzonych i może spowodować utratę danych w pomocniczej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-115">Forced termination does not wait for replication of any outstanding committed transactions, and can cause possible data loss in the secondary database.</span></span>

<span data-ttu-id="a2753-116">Gdy stan replikacji jest OCZEKUJĄCy, tylko wymuszone zakończenie może pomyślnie zakończyć relację ciągłego kopiowania.</span><span class="sxs-lookup"><span data-stu-id="a2753-116">While replication status is PENDING, only forced termination can successfully end a continuous copy relationship.</span></span>
<span data-ttu-id="a2753-117">Jeśli stan replikacji jest OCZEKUJĄCy, zakończenie nie jest obsługiwane.</span><span class="sxs-lookup"><span data-stu-id="a2753-117">If the replication status is PENDING, termination that is not forced is not supported.</span></span>

## <span data-ttu-id="a2753-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2753-118">EXAMPLES</span></span>

### <span data-ttu-id="a2753-119">Przykład 1: kończenie ciągłej relacji kopii</span><span class="sxs-lookup"><span data-stu-id="a2753-119">Example 1: Terminate a continuous copy relationship</span></span>
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="a2753-120">To polecenie przerywa ciągłą relację między bazą danych o nazwanych zamówieniami na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="a2753-120">This command terminates the continuous copy relationship of database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="a2753-121">Serwer o nazwie bk0b8kf658 obsługuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-121">The server named bk0b8kf658 hosts the secondary database.</span></span>

### <span data-ttu-id="a2753-122">Przykład 2: Wymuszanie zamknięcia ciągłej relacji między kopiami</span><span class="sxs-lookup"><span data-stu-id="a2753-122">Example 2: Forcibly terminate a continuous copy relationship</span></span>
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

<span data-ttu-id="a2753-123">Pierwsze polecenie uzyskuje relację kopiowania bazy danych dla bazy danych o nazwie Orders na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="a2753-123">The first command gets the database copy relationship for the database named Orders on the server named lpqd0zbr8y.</span></span>

<span data-ttu-id="a2753-124">Drugie polecenie wymusza, że relacja ciągłej kopii z serwera obsługującego pomocniczą bazę danych jest przerywana.</span><span class="sxs-lookup"><span data-stu-id="a2753-124">The second command forcibly terminates a continuous copy relationship from the server that hosts the secondary database.</span></span>

## <span data-ttu-id="a2753-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2753-125">PARAMETERS</span></span>

### <span data-ttu-id="a2753-126">-Database</span><span class="sxs-lookup"><span data-stu-id="a2753-126">-Database</span></span>
<span data-ttu-id="a2753-127">Określa obiekt reprezentujący źródłową bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a2753-127">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="a2753-128">To polecenie cmdlet powoduje zakończenie ciągłej relacji kopii bazy danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a2753-128">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2753-129">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a2753-129">-DatabaseCopy</span></span>
<span data-ttu-id="a2753-130">Określa obiekt reprezentujący bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-130">Specifies an object that represents a database.</span></span>
<span data-ttu-id="a2753-131">To polecenie cmdlet powoduje zakończenie ciągłej relacji kopii bazy danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a2753-131">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>
<span data-ttu-id="a2753-132">Ten parametr akceptuje dane wejściowe potoku.</span><span class="sxs-lookup"><span data-stu-id="a2753-132">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="a2753-133">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2753-133">-DatabaseName</span></span>
<span data-ttu-id="a2753-134">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-134">Specifies the name of a database.</span></span>
<span data-ttu-id="a2753-135">To polecenie cmdlet powoduje zakończenie ciągłej relacji kopii bazy danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a2753-135">This cmdlet terminates the continuous copy relationship of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="a2753-136">-Force</span><span class="sxs-lookup"><span data-stu-id="a2753-136">-Force</span></span>
<span data-ttu-id="a2753-137">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a2753-137">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a2753-138">-ForcedTermination</span><span class="sxs-lookup"><span data-stu-id="a2753-138">-ForcedTermination</span></span>
<span data-ttu-id="a2753-139">Wskazuje, że to polecenie cmdlet powoduje wymuszone zakończenie działania relacji ciągłej kopii.</span><span class="sxs-lookup"><span data-stu-id="a2753-139">Indicates that this cmdlet causes forced termination of the continuous copy relationship.</span></span>
<span data-ttu-id="a2753-140">Wymuszone zakończenie może spowodować utratę danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-140">Forced termination may cause with data loss.</span></span>
<span data-ttu-id="a2753-141">Aby uruchomić to polecenie cmdlet na serwerze obsługującym docelową bazę danych, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a2753-141">To run this cmdlet on a server that hosts the target database, you must specify this parameter.</span></span>
<span data-ttu-id="a2753-142">Aby uruchomić to polecenie cmdlet na serwerze obsługującym źródłową bazę danych, jeśli pomocnicza baza danych jest niedostępna, należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="a2753-142">To run this cmdlet on a server that hosts the source database, if the secondary database is unavailable, you must specify this parameter.</span></span>

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

### <span data-ttu-id="a2753-143">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="a2753-143">-PartnerDatabase</span></span>
<span data-ttu-id="a2753-144">Określa nazwę pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-144">Specifies name of the secondary database.</span></span>
<span data-ttu-id="a2753-145">Jeśli określisz nazwę, musi ona odpowiadać nazwie źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-145">If you specify a name, it must match the name of the source database.</span></span>

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

### <span data-ttu-id="a2753-146">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="a2753-146">-PartnerServer</span></span>
<span data-ttu-id="a2753-147">Określa nazwę serwera obsługującego docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-147">Specifies the name of the server that hosts the target database.</span></span>

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

### <span data-ttu-id="a2753-148">-Profile</span><span class="sxs-lookup"><span data-stu-id="a2753-148">-Profile</span></span>
<span data-ttu-id="a2753-149">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2753-149">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a2753-150">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a2753-150">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a2753-151">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a2753-151">-ServerName</span></span>
<span data-ttu-id="a2753-152">Określa nazwę serwera, na którym znajduje się źródłowa baza danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-152">Specifies the name of the server on which the source database resides.</span></span>

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

### <span data-ttu-id="a2753-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a2753-153">-Confirm</span></span>
<span data-ttu-id="a2753-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2753-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2753-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2753-155">-WhatIf</span></span>
<span data-ttu-id="a2753-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a2753-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2753-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a2753-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2753-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2753-158">CommonParameters</span></span>
<span data-ttu-id="a2753-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2753-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2753-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2753-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2753-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2753-161">INPUTS</span></span>

### <span data-ttu-id="a2753-162">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a2753-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="a2753-163">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="a2753-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="a2753-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2753-164">OUTPUTS</span></span>

### <span data-ttu-id="a2753-165">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a2753-165">None</span></span>

## <span data-ttu-id="a2753-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2753-166">NOTES</span></span>
* <span data-ttu-id="a2753-167">Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="a2753-167">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="a2753-168">Aby zapoznać się z przykładem zastosowania uwierzytelniania opartego na certyfikatach w celu skonfigurowania bieżącego abonamentu, zobacz polecenie cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="a2753-168">For an example of how to use certificate-based authentication to set the current subscription, see the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
* <span data-ttu-id="a2753-169">Ograniczenia: na serwerze obsługującym pomocniczą bazę danych obsługiwana jest tylko wymuszona przerwa w pracy.</span><span class="sxs-lookup"><span data-stu-id="a2753-169">Restrictions: On the server that hosts the secondary database, only forced termination is supported.</span></span>
* <span data-ttu-id="a2753-170">Wpływ rozwiązania na poprzednią pomocniczą bazę danych: po zakończeniu pomocnicza baza danych stanie się niezależną bazą danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-170">Impact of termination on the former secondary database: After termination, the secondary database becomes an independent database.</span></span> <span data-ttu-id="a2753-171">Jeśli dopełnienie zostało już ukończone w pomocniczej bazie danych, po zakończeniu tej bazy danych jest otwarta, aby uzyskać pełen dostęp.</span><span class="sxs-lookup"><span data-stu-id="a2753-171">If seeding already completed on the secondary database, after termination this database is open for full access.</span></span> <span data-ttu-id="a2753-172">Jeśli źródłowa baza danych jest bazą danych do odczytu i zapisu, baza danych była bazą danych do odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="a2753-172">If the source database is a read-write database, the former secondary database becomes a read-write database, too.</span></span>

  <span data-ttu-id="a2753-173">Jeśli napełnianie jest obecnie w toku, wstępne umieszczanie jest przerywane, a pozostała pomocnicza baza danych nigdy nie staje się widoczna na serwerze obsługującym pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a2753-173">If seeding is currently in progress, seeding is aborted, and the former secondary database never becomes visible on the server that hosts the secondary database.</span></span>

* <span data-ttu-id="a2753-174">Źródłową bazę danych można ustawić w trybie tylko do odczytu.</span><span class="sxs-lookup"><span data-stu-id="a2753-174">You can set the source database to read-only mode.</span></span> <span data-ttu-id="a2753-175">Gwarantuje to, że źródłowe i pomocnicze bazy danych są synchronizowane po zakończeniu działania, i że podczas kończenia pracy nie są zatwierdzane żadne transakcje.</span><span class="sxs-lookup"><span data-stu-id="a2753-175">This guarantees that source and secondary databases are synchronized after termination, and makes sure that no transactions are committed during termination.</span></span> <span data-ttu-id="a2753-176">Po zakończeniu kończenia ustaw źródło z powrotem na tryb do odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="a2753-176">Once the termination finishes, set the source back to read-write mode.</span></span> <span data-ttu-id="a2753-177">Opcjonalnie możesz również ustawić poprzednią pomocniczą bazę danych w trybie do odczytu i zapisu.</span><span class="sxs-lookup"><span data-stu-id="a2753-177">Optionally, you can also set the former secondary database to read-write mode.</span></span>
* <span data-ttu-id="a2753-178">Monitorowanie: Aby sprawdzić stan operacji zarówno w źródle, jak i w miejscu docelowym relacji kopii ciągłej, użyj polecenia cmdlet **Get-AzureSqlDatabaseOperation** .</span><span class="sxs-lookup"><span data-stu-id="a2753-178">Monitoring: To verify the status of the operations at both the source and target of the continuous copy relationship, use the **Get-AzureSqlDatabaseOperation** cmdlet.</span></span>

## <span data-ttu-id="a2753-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2753-179">RELATED LINKS</span></span>

[<span data-ttu-id="a2753-180">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="a2753-180">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="a2753-181">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="a2753-181">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="a2753-182">Zatrzymywanie kopiowania bazy danych</span><span class="sxs-lookup"><span data-stu-id="a2753-182">Stop Database Copy</span></span>](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[<span data-ttu-id="a2753-183">Polecenia cmdlet usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="a2753-183">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="a2753-184">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a2753-184">Get-AzureSqlDatabaseCopy</span></span>](./Get-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="a2753-185">Start — AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="a2753-185">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)


