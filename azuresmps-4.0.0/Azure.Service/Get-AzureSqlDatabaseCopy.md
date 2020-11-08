---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055261"
---
# <span data-ttu-id="fbf48-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbf48-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="fbf48-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fbf48-102">SYNOPSIS</span></span>
<span data-ttu-id="fbf48-103">Sprawdza stan relacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="fbf48-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="fbf48-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fbf48-104">SYNTAX</span></span>

### <span data-ttu-id="fbf48-105">ByServerNameOnly (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fbf48-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="fbf48-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbf48-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="fbf48-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="fbf48-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="fbf48-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fbf48-108">DESCRIPTION</span></span>
<span data-ttu-id="fbf48-109">Polecenie cmdlet **Get-AzureSqlDatabaseCopy** sprawdza stan jednej lub większej liczby aktywnych relacji między kopiami.</span><span class="sxs-lookup"><span data-stu-id="fbf48-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="fbf48-110">Uruchom to polecenie cmdlet po uruchomieniu Start-AzureSqlDatabaseCopy lub Stop-AzureSqlDatabaseCopy polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbf48-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="fbf48-111">Możesz sprawdzić określoną relację kopiowania, wszystkie relacje kopiowania lub przefiltrowaną listę relacji kopiowania, takich jak wszystkie kopie na określonym serwerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="fbf48-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="fbf48-112">To polecenie cmdlet można uruchomić na serwerze obsługującym źródłową lub docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fbf48-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="fbf48-113">To polecenie cmdlet jest synchroniczne.</span><span class="sxs-lookup"><span data-stu-id="fbf48-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="fbf48-114">Polecenie cmdlet blokuje konsolę programu Azure PowerShell do momentu, gdy zwróci ona obiekt status.</span><span class="sxs-lookup"><span data-stu-id="fbf48-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="fbf48-115">Parametry *PartnerServer* i *PartnerDatabase* są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="fbf48-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="fbf48-116">Jeśli nie określisz żadnego z parametrów, to polecenie cmdlet zwróci tabelę wyników.</span><span class="sxs-lookup"><span data-stu-id="fbf48-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="fbf48-117">Aby wyświetlić stan tylko określonej bazy danych, należy określić oba parametry.</span><span class="sxs-lookup"><span data-stu-id="fbf48-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="fbf48-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fbf48-118">EXAMPLES</span></span>

### <span data-ttu-id="fbf48-119">Przykład 1. Pobieranie stanu kopii bazy danych</span><span class="sxs-lookup"><span data-stu-id="fbf48-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="fbf48-120">To polecenie uzyskuje stan bazy danych nazwane zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="fbf48-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="fbf48-121">Parametr *PartnerServer* ogranicza to polecenie do serwera bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="fbf48-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="fbf48-122">Przykład 2: pobieranie stanu wszystkich kopii w serverGet stan wszystkich kopii na serwerze</span><span class="sxs-lookup"><span data-stu-id="fbf48-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="fbf48-123">To polecenie uzyskuje stan wszystkich aktywnych kopii na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="fbf48-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="fbf48-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fbf48-124">PARAMETERS</span></span>

### <span data-ttu-id="fbf48-125">-Database</span><span class="sxs-lookup"><span data-stu-id="fbf48-125">-Database</span></span>
<span data-ttu-id="fbf48-126">Określa obiekt reprezentujący źródłową bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="fbf48-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="fbf48-127">To polecenie cmdlet pobiera stan kopii bazy danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fbf48-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="fbf48-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbf48-128">-DatabaseCopy</span></span>
<span data-ttu-id="fbf48-129">Określa obiekt reprezentujący bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fbf48-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="fbf48-130">To polecenie cmdlet pobiera stan kopii bazy danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fbf48-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="fbf48-131">Ten parametr akceptuje dane wejściowe potoku.</span><span class="sxs-lookup"><span data-stu-id="fbf48-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="fbf48-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbf48-132">-DatabaseName</span></span>
<span data-ttu-id="fbf48-133">Określa nazwę źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fbf48-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="fbf48-134">To polecenie cmdlet umożliwia pobieranie statusu kopii bazy danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="fbf48-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf48-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="fbf48-135">-PartnerDatabase</span></span>
<span data-ttu-id="fbf48-136">Określa nazwę pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fbf48-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="fbf48-137">Jeśli nie można odnaleźć tej bazy danych w dynamicznym widoku zarządzania sys.dm_database_copies, to polecenie cmdlet zwróci pusty obiekt status.</span><span class="sxs-lookup"><span data-stu-id="fbf48-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf48-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="fbf48-138">-PartnerServer</span></span>
<span data-ttu-id="fbf48-139">Określa nazwę serwera obsługującego docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="fbf48-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="fbf48-140">Jeśli nie odnaleziono tego serwera w dynamicznym widoku zarządzania sys.dm_database_copies, to polecenie cmdlet zwróci pusty obiekt status.</span><span class="sxs-lookup"><span data-stu-id="fbf48-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbf48-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="fbf48-141">-Profile</span></span>
<span data-ttu-id="fbf48-142">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fbf48-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="fbf48-143">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="fbf48-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="fbf48-144">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="fbf48-144">-ServerName</span></span>
<span data-ttu-id="fbf48-145">Określa nazwę serwera, na którym znajduje się kopia bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fbf48-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="fbf48-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbf48-146">CommonParameters</span></span>
<span data-ttu-id="fbf48-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbf48-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbf48-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbf48-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbf48-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbf48-149">INPUTS</span></span>

### <span data-ttu-id="fbf48-150">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbf48-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="fbf48-151">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="fbf48-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="fbf48-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fbf48-152">OUTPUTS</span></span>

### <span data-ttu-id="fbf48-153">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbf48-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="fbf48-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fbf48-154">NOTES</span></span>
* <span data-ttu-id="fbf48-155">Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="fbf48-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="fbf48-156">Aby zapoznać się z przykładem używania uwierzytelniania opartego na certyfikatach do ustawiania bieżącej subskrypcji, zobacz polecenie cmdlet New-AzureSqlDatabaseServerContext.</span><span class="sxs-lookup"><span data-stu-id="fbf48-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="fbf48-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbf48-157">RELATED LINKS</span></span>

[<span data-ttu-id="fbf48-158">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="fbf48-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="fbf48-159">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="fbf48-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="fbf48-160">Polecenia cmdlet usługi Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="fbf48-160">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="fbf48-161">Start — AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbf48-161">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="fbf48-162">Zatrzymaj — AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="fbf48-162">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


