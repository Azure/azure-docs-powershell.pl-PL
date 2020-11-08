---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054392"
---
# <span data-ttu-id="e583d-101">Start-AzureSqlDatabaseRestore</span><span class="sxs-lookup"><span data-stu-id="e583d-101">Start-AzureSqlDatabaseRestore</span></span>

## <span data-ttu-id="e583d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e583d-102">SYNOPSIS</span></span>
<span data-ttu-id="e583d-103">Umożliwia wykonanie punktu przywracania bazy danych w czasie.</span><span class="sxs-lookup"><span data-stu-id="e583d-103">Performs a point in time restore of a database.</span></span>

## <span data-ttu-id="e583d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e583d-104">SYNTAX</span></span>

### <span data-ttu-id="e583d-105">BySourceDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e583d-105">BySourceDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e583d-106">BySourceRestorableDroppedDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="e583d-106">BySourceRestorableDroppedDatabaseObject</span></span>
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e583d-107">BySourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e583d-107">BySourceDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e583d-108">BySourceRestorableDroppedDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e583d-108">BySourceRestorableDroppedDatabaseName</span></span>
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e583d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="e583d-109">DESCRIPTION</span></span>
<span data-ttu-id="e583d-110">Polecenie cmdlet **Start-AzureSqlDatabaseRestore** wykonuje operację przywracania czasu dla podstawowej, standardowej lub Premium bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-110">The **Start-AzureSqlDatabaseRestore** cmdlet performs a point in time restore of a Basic, Standard or Premium database.</span></span>
<span data-ttu-id="e583d-111">Baza danych SQL Azure zachowuje podstawowe kopie zapasowe baz danych — 7 dni, standard przez 14 dni i Premium dla 35 dni.</span><span class="sxs-lookup"><span data-stu-id="e583d-111">Azure SQL Database retains Basic database backups 7 days, Standard for 14 days, and Premium for 35 days.</span></span>
<span data-ttu-id="e583d-112">Operacja restore powoduje utworzenie nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-112">The restore operation creates a new database.</span></span>
<span data-ttu-id="e583d-113">Jeśli źródłowa baza danych nie zostanie usunięta, parametr *SourceDatabaseName* i *TargetDatabaseName* musi mieć różne wartości.</span><span class="sxs-lookup"><span data-stu-id="e583d-113">If the source database is not deleted, the *SourceDatabaseName* and *TargetDatabaseName* parameter must have different values.</span></span>

<span data-ttu-id="e583d-114">Baza danych SQL Azure nie obsługuje obecnie przywracania serwera.</span><span class="sxs-lookup"><span data-stu-id="e583d-114">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="e583d-115">Nazwy serwerów źródłowych i docelowych muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="e583d-115">The source and target server names must be the same.</span></span>

## <span data-ttu-id="e583d-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e583d-116">EXAMPLES</span></span>

### <span data-ttu-id="e583d-117">Przykład 1: Przywracanie bazy danych określonej jako obiekt w momencie</span><span class="sxs-lookup"><span data-stu-id="e583d-117">Example 1: Restore a database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="e583d-118">Pierwsze polecenie pobiera obiekt bazy danych dla bazy danych o nazwie Database17 na serwerze o nazwie Server01, a następnie zapisuje go w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="e583d-118">The first command gets a database object for the database named Database17 on the server named Server01, and then stores it in the $Database variable.</span></span>

<span data-ttu-id="e583d-119">Drugie polecenie przywraca bazę danych do określonego momentu w określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="e583d-119">The second command restores the database to a specific point in time.</span></span>
<span data-ttu-id="e583d-120">Polecenie określa nazwę nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-120">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="e583d-121">Przykład 2: Przywracanie bazy danych określonej według nazwy do punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="e583d-121">Example 2: Restore a database specified by name to a point in time</span></span>
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

<span data-ttu-id="e583d-122">To polecenie przywraca bazę danych o nazwie Database17 do określonego momentu w określonej chwili.</span><span class="sxs-lookup"><span data-stu-id="e583d-122">This command restores the database named Database17 to a specific point in time.</span></span>
<span data-ttu-id="e583d-123">Polecenie określa nazwę nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-123">The command specifies at name for the new database.</span></span>

### <span data-ttu-id="e583d-124">Przykład 3: Przywracanie porzuconej bazy danych określonej jako obiekt do punktu w czasie</span><span class="sxs-lookup"><span data-stu-id="e583d-124">Example 3: Restore a dropped database specified as an object to a point in time</span></span>
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

<span data-ttu-id="e583d-125">Pierwsze polecenie pobiera obiekt bazy danych dla bazy danych o nazwie Database01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="e583d-125">The first command gets a database object for the database named Database01 on the server named Server01.</span></span>
<span data-ttu-id="e583d-126">Polecenie określa parametr *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="e583d-126">The command specifies the *RestorableDropped* parameter.</span></span>
<span data-ttu-id="e583d-127">Z tego powodu polecenie cmdlet pobiera restorable porzucona baza danych o określonym punkcie przywracania.</span><span class="sxs-lookup"><span data-stu-id="e583d-127">Therefore, the cmdlet gets restorable dropped database the specified restore point.</span></span>
<span data-ttu-id="e583d-128">Polecenie zapisuje ten obiekt bazy danych w zmiennej $Database.</span><span class="sxs-lookup"><span data-stu-id="e583d-128">The command stores that database object in the $Database variable.</span></span>

<span data-ttu-id="e583d-129">Drugie polecenie przywraca porzucona bazę danych określoną przez $Database.</span><span class="sxs-lookup"><span data-stu-id="e583d-129">The second command restores the dropped database specified by $Database.</span></span>
<span data-ttu-id="e583d-130">Polecenie określa nazwę nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-130">The command specifies at name for the new database.</span></span>

## <span data-ttu-id="e583d-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e583d-131">PARAMETERS</span></span>

### <span data-ttu-id="e583d-132">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="e583d-132">-PointInTime</span></span>
<span data-ttu-id="e583d-133">Określa punkt przywracania, do którego ma zostać przywrócona baza danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-133">Specifies the restore point to which to restore the database.</span></span>
<span data-ttu-id="e583d-134">Gdy operacja przywracania zakończy się, baza danych zostanie przywrócona do stanu, w którym znajduje się na dacie i godzinie określającej ten parametr.</span><span class="sxs-lookup"><span data-stu-id="e583d-134">When the restore operation finishes, the database is restored to the state it was at the date and time that this parameter specifies.</span></span>
<span data-ttu-id="e583d-135">Domyślnie dla bazy danych na żywo, która jest obecnie ustawiona jako bieżąca godzina, a w przypadku porzuconej bazy danych, to polecenie cmdlet używa godziny porzucenia bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-135">By default, for a live database this set to the current time, and for a dropped database, this cmdlet uses the time when the database was dropped.</span></span>

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

### <span data-ttu-id="e583d-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="e583d-136">-Profile</span></span>
<span data-ttu-id="e583d-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e583d-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e583d-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e583d-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e583d-139">-RestorableDropped</span><span class="sxs-lookup"><span data-stu-id="e583d-139">-RestorableDropped</span></span>
<span data-ttu-id="e583d-140">Wskazuje, że to polecenie cmdlet przywraca restorable porzuconej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-140">Indicates that this cmdlet restores a restorable dropped database.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-141">-SourceDatabase</span><span class="sxs-lookup"><span data-stu-id="e583d-141">-SourceDatabase</span></span>
<span data-ttu-id="e583d-142">Określa nazwę bazy danych, która jest przywracana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e583d-142">Specifies the name of the database that this cmdlet restores.</span></span>

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-143">-SourceDatabaseDeletionDate</span><span class="sxs-lookup"><span data-stu-id="e583d-143">-SourceDatabaseDeletionDate</span></span>
<span data-ttu-id="e583d-144">Określa datę i godzinę usunięcia bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-144">Specifies the date and time when the database was deleted.</span></span>
<span data-ttu-id="e583d-145">Należy uwzględnić czas w milisekundach podczas określania czasu, który będzie odpowiadał rzeczywistemu czasowi usunięcia bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-145">You must include milliseconds when you specify the time to match the actual database deletion time.</span></span>

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-146">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e583d-146">-SourceDatabaseName</span></span>
<span data-ttu-id="e583d-147">Określa nazwę bazy danych na żywo, która jest przywracana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e583d-147">Specifies the name of the live database that this cmdlet restores.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-148">-SourceRestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e583d-148">-SourceRestorableDroppedDatabase</span></span>
<span data-ttu-id="e583d-149">Określa obiekt reprezentujący restorable porzuconej bazy danych, która jest przywracana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e583d-149">Specifies an object that represents the restorable dropped database that this cmdlet restores.</span></span>
<span data-ttu-id="e583d-150">Aby uzyskać obiekt **RestorableDroppedDatabase** , użyj polecenia cmdlet Get-AzureSqlDatabase, a następnie określ parametr *RestorableDropped* .</span><span class="sxs-lookup"><span data-stu-id="e583d-150">To obtain a **RestorableDroppedDatabase** object, use the Get-AzureSqlDatabase cmdlet, and specify the *RestorableDropped* parameter.</span></span>

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-151">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="e583d-151">-SourceServerName</span></span>
<span data-ttu-id="e583d-152">Określa nazwę serwera, na którym jest uruchomiona źródłowa baza danych, lub w której uruchomiono źródłową bazę danych przed jej usunięciem.</span><span class="sxs-lookup"><span data-stu-id="e583d-152">Specifies the name of the server on which the source database is live and running, or on which the source database ran before it was deleted.</span></span>

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-153">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e583d-153">-TargetDatabaseName</span></span>
<span data-ttu-id="e583d-154">Określa nazwę nowej bazy danych, którą ma utworzyć operacja przywracania.</span><span class="sxs-lookup"><span data-stu-id="e583d-154">Specifies the name of the new database that the restore operation creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e583d-155">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="e583d-155">-TargetServerName</span></span>
<span data-ttu-id="e583d-156">Określa nazwę serwera, na którym jest przywracana baza danych.</span><span class="sxs-lookup"><span data-stu-id="e583d-156">Specifies the name of the server to which this cmdlet restores the database.</span></span>

<span data-ttu-id="e583d-157">Baza danych SQL Azure nie obsługuje obecnie przywracania serwera.</span><span class="sxs-lookup"><span data-stu-id="e583d-157">Azure SQL Database does not currently support cross server restore.</span></span>
<span data-ttu-id="e583d-158">Nazwy serwerów źródłowych i docelowych muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="e583d-158">The source and target server names must be the same.</span></span>

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

### <span data-ttu-id="e583d-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e583d-159">CommonParameters</span></span>
<span data-ttu-id="e583d-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e583d-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e583d-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e583d-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e583d-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e583d-162">INPUTS</span></span>

### <span data-ttu-id="e583d-163">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. RestorableDroppedDatabase</span><span class="sxs-lookup"><span data-stu-id="e583d-163">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase</span></span>

### <span data-ttu-id="e583d-164">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="e583d-164">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="e583d-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e583d-165">OUTPUTS</span></span>

### <span data-ttu-id="e583d-166">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. RestoreDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="e583d-166">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestoreDatabaseOperation</span></span>

## <span data-ttu-id="e583d-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e583d-167">NOTES</span></span>
* <span data-ttu-id="e583d-168">Aby uruchomić to polecenie cmdlet, należy użyć uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="e583d-168">You must use certificate based authentication to run this cmdlet.</span></span> <span data-ttu-id="e583d-169">Uruchom następujące polecenia na komputerze, na którym Uruchom to polecenie cmdlet:</span><span class="sxs-lookup"><span data-stu-id="e583d-169">Run the following commands on the computer where run this cmdlet:</span></span> 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## <span data-ttu-id="e583d-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e583d-170">RELATED LINKS</span></span>

[<span data-ttu-id="e583d-171">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="e583d-171">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="e583d-172">Żądanie utworzenia bazy danych</span><span class="sxs-lookup"><span data-stu-id="e583d-172">Create Database Restore Request</span></span>](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[<span data-ttu-id="e583d-173">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e583d-173">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="e583d-174">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e583d-174">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)


