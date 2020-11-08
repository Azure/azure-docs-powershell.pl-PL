---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055264"
---
# <span data-ttu-id="00d50-101">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00d50-101">Get-AzureSqlDatabase</span></span>

## <span data-ttu-id="00d50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="00d50-102">SYNOPSIS</span></span>
<span data-ttu-id="00d50-103">Pobiera co najmniej jeden z baz danych.</span><span class="sxs-lookup"><span data-stu-id="00d50-103">Retrieves one or more databases.</span></span>

## <span data-ttu-id="00d50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="00d50-104">SYNTAX</span></span>

### <span data-ttu-id="00d50-105">ByConnectionContext (domyślny)</span><span class="sxs-lookup"><span data-stu-id="00d50-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="00d50-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="00d50-106">ByServerName</span></span>
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="00d50-107">Opis</span><span class="sxs-lookup"><span data-stu-id="00d50-107">DESCRIPTION</span></span>
<span data-ttu-id="00d50-108">Polecenie cmdlet **Get-AzureSqlDatabase** pobiera co najmniej jedno wystąpienie bazy danych SQL Azure z serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="00d50-108">The **Get-AzureSqlDatabase** cmdlet retrieves one or more instances of an Azure SQL Database from an Azure SQL Database server.</span></span>
<span data-ttu-id="00d50-109">Serwer można określić za pomocą kontekstu połączenia serwera bazy danych Azure SQL Server tworzonego przy użyciu polecenia cmdlet **New-AzureSqlDatabaseServerContext** .</span><span class="sxs-lookup"><span data-stu-id="00d50-109">You can specify the server with an Azure SQL Database server connection context that you create using the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span>
<span data-ttu-id="00d50-110">Jeśli określisz nazwę serwera bazy danych Azure SQL Server, polecenie cmdlet używa bieżących informacji o subskrypcji platformy Azure do uwierzytelnienia żądania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="00d50-110">Or, if you specify the Azure SQL Database server name, the cmdlet uses the current Azure subscription information to authenticate the request to access the server.</span></span>

<span data-ttu-id="00d50-111">Jeśli baza danych nie zostanie określona, polecenie cmdlet **Get-AzureSqlDatabase** zwraca wszystkie bazy danych z określonego serwera.</span><span class="sxs-lookup"><span data-stu-id="00d50-111">If you do not specify a database, the **Get-AzureSqlDatabase** cmdlet returns all databases from the specified server.</span></span>

<span data-ttu-id="00d50-112">Pobieranie restorableych baz danych:</span><span class="sxs-lookup"><span data-stu-id="00d50-112">Retrieving restorable dropped databases:</span></span>

<span data-ttu-id="00d50-113">Pobieranie restorableych baz danych przy użyciu parametru *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="00d50-113">Retrieve restorable dropped databases by using the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="00d50-114">Aby zwrócić wszystkie restorable porzucone bazy danych, użyj parametru *RestorableDropped* bez parametrów *DatabaseName* i *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="00d50-114">To return all restorable dropped databases use the *RestorableDropped* parameter without *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="00d50-115">Aby zwrócić określoną restorable porzucona baza danych, użyj parametru *RestorableDropped* z parametrami *DatabaseName* i *DatabaseDeletionDate* .</span><span class="sxs-lookup"><span data-stu-id="00d50-115">To return a specific restorable dropped database use the *RestorableDropped* parameter with the *DatabaseName* and *DatabaseDeletionDate* parameters.</span></span>
<span data-ttu-id="00d50-116">Podczas pobierania konkretnej restorable bazy danych przy użyciu parametru *DatabaseName* należy również uwzględnić parametr *DatabaseDeletionDate* , a określona wartość *DatabaseDeletionDate* musi uwzględniać czas w milisekundach zgodnych z odpowiednią bazą danych.</span><span class="sxs-lookup"><span data-stu-id="00d50-116">When retrieving a specific restorable dropped database by using the *DatabaseName* parameter you must also include the *DatabaseDeletionDate* parameter and the specified *DatabaseDeletionDate* value must include milliseconds to match the desired database.</span></span>

<span data-ttu-id="00d50-117">Polecenie cmdlet **Get-AzureSqlDatabase** zwraca wszystkie restorable porzucone na serwerze lub jedną określoną bazę danych, która pasuje zarówno do bazy danych *DatabaseName* , jak i *DatabaseDeletionDate*.</span><span class="sxs-lookup"><span data-stu-id="00d50-117">The **Get-AzureSqlDatabase** cmdlet returns either all restorable dropped databases on a server, or one specific database that matches both *DatabaseName* and *DatabaseDeletionDate*.</span></span>
<span data-ttu-id="00d50-118">Aby zwrócić restorable bazy danych, które spełniają inne kryteria, takie jak wszystkie restorable usunięte bazy danych o określonej nazwie, należy zwrócić wszystkie restorable usunięte bazy danych, a następnie filtrować wyniki na kliencie.</span><span class="sxs-lookup"><span data-stu-id="00d50-118">To return restorable dropped databases that satisfy different criteria, such as all restorable dropped databases of a specific name, you must return all restorable dropped databases, and then filter the results on the client.</span></span>

## <span data-ttu-id="00d50-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="00d50-119">EXAMPLES</span></span>

### <span data-ttu-id="00d50-120">Przykład 1: pobieranie wszystkich baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="00d50-120">Example 1: Retrieve all databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="00d50-121">To polecenie pobiera wszystkie bazy danych na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="00d50-121">This command retrieves all databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="00d50-122">Przykład 2: pobieranie wszystkich restorableych baz danych na serwerze</span><span class="sxs-lookup"><span data-stu-id="00d50-122">Example 2: Retrieve all restorable dropped databases on a server</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

<span data-ttu-id="00d50-123">To polecenie umożliwia pobranie wszystkich restorableych baz danych na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="00d50-123">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y.</span></span>

### <span data-ttu-id="00d50-124">Przykład 3: pobieranie bazy danych z serwera określonego w kontekście połączenia</span><span class="sxs-lookup"><span data-stu-id="00d50-124">Example 3: Retrieve a database from a server specified by a connection context</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

<span data-ttu-id="00d50-125">To polecenie pobiera bazę danych o nazwie Database01 z serwera określonego przez kontekst połączenia $Context.</span><span class="sxs-lookup"><span data-stu-id="00d50-125">This command retrieves database named Database01 from the server specified by the connection context $Context.</span></span>

### <span data-ttu-id="00d50-126">Przykład 4: przechowywanie obiektu bazy danych w zmiennej</span><span class="sxs-lookup"><span data-stu-id="00d50-126">Example 4: Store a database object in a variable</span></span>
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

<span data-ttu-id="00d50-127">To polecenie pobiera bazę danych o nazwie Database01 z serwera o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="00d50-127">This command retrieves database named Database01 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="00d50-128">Polecenie zapisuje obiekt bazy danych w zmiennej $Database 01.</span><span class="sxs-lookup"><span data-stu-id="00d50-128">The command stores the database object in the $Database01 variable.</span></span>

### <span data-ttu-id="00d50-129">Przykład 5: pobieranie restorable porzuconej bazy danych</span><span class="sxs-lookup"><span data-stu-id="00d50-129">Example 5: Retrieve a restorable dropped database</span></span>
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

<span data-ttu-id="00d50-130">To polecenie pobiera bazę danych restorable porzuconej o nazwie Database01, która została usunięta w 11/9/2012 z serwera o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="00d50-130">This command retrieves the restorable dropped database named Database01 that was deleted on 11/9/2012 from the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="00d50-131">To polecenie zapisuje wyniki w zmiennej $DroppedDB.</span><span class="sxs-lookup"><span data-stu-id="00d50-131">This command stores the results in the $DroppedDB variable.</span></span>

### <span data-ttu-id="00d50-132">Przykład 6: pobieranie wszystkich restorableych baz danych na serwerze i filtrowanie wyników</span><span class="sxs-lookup"><span data-stu-id="00d50-132">Example 6: Retrieve all restorable dropped databases on a server and filter the results</span></span>
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

<span data-ttu-id="00d50-133">To polecenie pobiera wszystkie restorable bazy danych z serwera o nazwie lpqd0zbr8y, a następnie filtruje wyniki tylko do baz danych o nazwie ContactDB.</span><span class="sxs-lookup"><span data-stu-id="00d50-133">This command retrieves all restorable dropped databases on the server named lpqd0zbr8y, and then filters the results to only the databases named ContactDB.</span></span>

## <span data-ttu-id="00d50-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="00d50-134">PARAMETERS</span></span>

### <span data-ttu-id="00d50-135">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="00d50-135">-ConnectionContext</span></span>
<span data-ttu-id="00d50-136">Określa kontekst połączenia serwera, z którego ma zostać pobrana baza danych.</span><span class="sxs-lookup"><span data-stu-id="00d50-136">Specifies the connection context of a server from which to retrieve a database.</span></span>

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00d50-137">-Database</span><span class="sxs-lookup"><span data-stu-id="00d50-137">-Database</span></span>
<span data-ttu-id="00d50-138">Określa obiekt reprezentujący bazę danych, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d50-138">Specifies an object that represents the database that this cmdlet retrieves.</span></span>

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00d50-139">-DatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="00d50-139">-DatabaseDeletionDate</span></span>
<span data-ttu-id="00d50-140">Określa datę i godzinę usunięcia.</span><span class="sxs-lookup"><span data-stu-id="00d50-140">Specifies the date and time of a deletion.</span></span>
<span data-ttu-id="00d50-141">Jeśli określisz parametr *RestorableDropped* , określ ten parametr, aby pobrać restorable porzuconej bazy danych na podstawie daty i godziny usunięcia.</span><span class="sxs-lookup"><span data-stu-id="00d50-141">If you specify the *RestorableDropped* parameter, specify this parameter to retrieve a restorable dropped database based on the deletion date and time.</span></span>

<span data-ttu-id="00d50-142">Parametr *DatabaseDeletionDate* musi uwzględniać czas w milisekundach, aby był zgodny z czasem odpowiedniej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="00d50-142">The *DatabaseDeletionDate* parameter must include milliseconds to match the time of the desired database.</span></span>
<span data-ttu-id="00d50-143">Określenie wartości bez milisekund powoduje, że nie można odnaleźć bazy danych.</span><span class="sxs-lookup"><span data-stu-id="00d50-143">Specifying a value without milliseconds results in the database not being found.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d50-144">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="00d50-144">-DatabaseName</span></span>
<span data-ttu-id="00d50-145">Określa nazwę bazy danych, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d50-145">Specifies the name of the database that this cmdlet retrieves.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00d50-146">-Profile</span><span class="sxs-lookup"><span data-stu-id="00d50-146">-Profile</span></span>
<span data-ttu-id="00d50-147">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d50-147">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="00d50-148">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="00d50-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="00d50-149">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="00d50-149">-RestorableDropped</span></span>
<span data-ttu-id="00d50-150">Wskazuje, że to polecenie cmdlet zwraca *RestorableDroppedDatabase* obiekty, a nie obiekty *bazy danych* .</span><span class="sxs-lookup"><span data-stu-id="00d50-150">Indicates that this cmdlet returns *RestorableDroppedDatabase* objects instead of *Database* objects.</span></span>
<span data-ttu-id="00d50-151">Parametru *DatabaseDeletionDate* można użyć w celu wybrania porzuconej restorable bazy danych.</span><span class="sxs-lookup"><span data-stu-id="00d50-151">You can use the *DatabaseDeletionDate* parameter to select a specific restorable dropped database.</span></span>

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

### <span data-ttu-id="00d50-152">-RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="00d50-152">-RestorableDroppedDatabase</span></span>
<span data-ttu-id="00d50-153">Określa obiekt reprezentujący restorable porzuconej bazy danych, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d50-153">Specifies an object that represents the restorable dropped database that this cmdlet retrieves.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00d50-154">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="00d50-154">-ServerName</span></span>
<span data-ttu-id="00d50-155">Określa nazwę serwera zawierającego bazę danych, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00d50-155">Specifies the name of the server that contains the database that this cmdlet retrieves.</span></span>
<span data-ttu-id="00d50-156">Polecenie cmdlet używa bieżącej subskrypcji platformy Azure do uzyskiwania dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="00d50-156">The cmdlet uses the current Azure subscription to access the server.</span></span>

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00d50-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00d50-157">CommonParameters</span></span>
<span data-ttu-id="00d50-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00d50-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00d50-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00d50-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00d50-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00d50-160">INPUTS</span></span>

### <span data-ttu-id="00d50-161">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="00d50-161">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="00d50-162">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="00d50-162">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

## <span data-ttu-id="00d50-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="00d50-163">OUTPUTS</span></span>

### <span data-ttu-id="00d50-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span><span class="sxs-lookup"><span data-stu-id="00d50-164">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\></span></span>
<span data-ttu-id="00d50-165">To polecenie cmdlet zwraca obiekt *bazy danych* , jeśli nie określisz parametru *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="00d50-165">This cmdlet returns a *Database* object if you do not specify the *RestorableDropped* parameter.</span></span>

### <span data-ttu-id="00d50-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span><span class="sxs-lookup"><span data-stu-id="00d50-166">IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\></span></span>
<span data-ttu-id="00d50-167">To polecenie cmdlet zwraca obiekt *RestorableDroppedDatabase* , jeśli określisz parametr *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="00d50-167">This cmdlet returns a *RestorableDroppedDatabase* object if you specify the *RestorableDropped* parameter.</span></span>

## <span data-ttu-id="00d50-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="00d50-168">NOTES</span></span>

## <span data-ttu-id="00d50-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00d50-169">RELATED LINKS</span></span>

[<span data-ttu-id="00d50-170">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="00d50-170">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="00d50-171">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="00d50-171">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="00d50-172">Nowe — AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00d50-172">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="00d50-173">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="00d50-173">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)

[<span data-ttu-id="00d50-174">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00d50-174">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="00d50-175">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="00d50-175">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


