---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055259"
---
# <span data-ttu-id="f482d-101">Get-AzureSqlDatabaseOperation</span><span class="sxs-lookup"><span data-stu-id="f482d-101">Get-AzureSqlDatabaseOperation</span></span>

## <span data-ttu-id="f482d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f482d-102">SYNOPSIS</span></span>
<span data-ttu-id="f482d-103">Pobiera stan operacji bazy danych na serwerze Azure.</span><span class="sxs-lookup"><span data-stu-id="f482d-103">Gets the status of database operations on an Azure server.</span></span>

## <span data-ttu-id="f482d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f482d-104">SYNTAX</span></span>

### <span data-ttu-id="f482d-105">ByConnectionContext (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f482d-105">ByConnectionContext (Default)</span></span>
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="f482d-106">ByServerName</span><span class="sxs-lookup"><span data-stu-id="f482d-106">ByServerName</span></span>
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f482d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f482d-107">DESCRIPTION</span></span>
<span data-ttu-id="f482d-108">Polecenie cmdlet **Get-AzureSqlDatabaseOperation** Pobiera stan operacji bazy danych na określonym serwerze Azure.</span><span class="sxs-lookup"><span data-stu-id="f482d-108">The **Get-AzureSqlDatabaseOperation** cmdlet gets the status of database operations on the specified Azure server.</span></span>
<span data-ttu-id="f482d-109">Jeśli określisz tylko parametr *nazwa_serwera* lub *ConnectionContext* , polecenie cmdlet pobiera wszystkie operacje bazy danych dla serwera.</span><span class="sxs-lookup"><span data-stu-id="f482d-109">If you specify only the *ServerName* or *ConnectionContext* parameter, the cmdlet gets all the database operations for the server.</span></span>
<span data-ttu-id="f482d-110">Jeśli określisz również bazę danych przy użyciu parametru *Database* lub *DatabaseName* , to polecenie cmdlet pobiera wszystkie operacje dla określonej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f482d-110">If you also specify a database by using the *Database* or *DatabaseName* parameter, this cmdlet gets all the operations for the specified database.</span></span>
<span data-ttu-id="f482d-111">Jeśli określisz identyfikator GUID operacji i *nazwa_serwera* lub *ConnectionContext* , polecenie cmdlet pobiera pojedynczą operację bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f482d-111">If you specify an operation GUID, and *ServerName* or *ConnectionContext* , the cmdlet gets a single database operation.</span></span>

## <span data-ttu-id="f482d-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f482d-112">EXAMPLES</span></span>

### <span data-ttu-id="f482d-113">Przykład 1: uzyskiwanie stanu wszystkich operacji bazy danych dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="f482d-113">Example 1: Get the status of all database operations for a database</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

<span data-ttu-id="f482d-114">To polecenie uzyskuje stan wszystkich operacji bazy danych w bazie danych o nazwie Database17 na serwerze, który $Context określał kontekst połączenia.</span><span class="sxs-lookup"><span data-stu-id="f482d-114">This command gets the status of all database operations on the database named Database17 on the server that the connection context $Context specifies.</span></span>

### <span data-ttu-id="f482d-115">Przykład 2: uzyskiwanie stanu wszystkich operacji bazy danych dla serwera</span><span class="sxs-lookup"><span data-stu-id="f482d-115">Example 2: Get the status of all database operations for a server</span></span>
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

<span data-ttu-id="f482d-116">To polecenie pobiera stan wszystkich operacji bazy danych na serwerze, który $Context określał kontekst połączenia.</span><span class="sxs-lookup"><span data-stu-id="f482d-116">This command gets the status of all database operations on the server that the connection context $Context specifies.</span></span>

## <span data-ttu-id="f482d-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f482d-117">PARAMETERS</span></span>

### <span data-ttu-id="f482d-118">-ConnectionContext</span><span class="sxs-lookup"><span data-stu-id="f482d-118">-ConnectionContext</span></span>
<span data-ttu-id="f482d-119">Określa kontekst połączenia serwera.</span><span class="sxs-lookup"><span data-stu-id="f482d-119">Specifies the connection context of a server.</span></span>

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

### <span data-ttu-id="f482d-120">-Database</span><span class="sxs-lookup"><span data-stu-id="f482d-120">-Database</span></span>
<span data-ttu-id="f482d-121">Określa obiekt reprezentujący bazę danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f482d-121">Specifies an object that represents an Azure SQL Database.</span></span>
<span data-ttu-id="f482d-122">W przypadku określenia tego parametru należy określić parametr *servername* lub parametr *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="f482d-122">If you specify this parameter, you must specify the *ServerName* parameter or *ConnectionContext* parameter.</span></span>

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

### <span data-ttu-id="f482d-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f482d-123">-DatabaseName</span></span>
<span data-ttu-id="f482d-124">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f482d-124">Specifies the name of a database.</span></span>
<span data-ttu-id="f482d-125">W przypadku określenia tego parametru należy określić parametr *servername* lub parametr *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="f482d-125">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f482d-126">-OperationGuid</span><span class="sxs-lookup"><span data-stu-id="f482d-126">-OperationGuid</span></span>
<span data-ttu-id="f482d-127">Określa identyfikator operacji reprezentujący określoną operację bazy danych, dla której to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="f482d-127">Specifies the operation ID that represents a specific database operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="f482d-128">Identyfikatory operacji można uzyskać, żądając wszystkich operacji bazy danych usługi Azure SQL Server lub serwera.</span><span class="sxs-lookup"><span data-stu-id="f482d-128">You can obtain operation IDs by requesting all the database operations for a Azure SQL Database or server.</span></span>
<span data-ttu-id="f482d-129">W przypadku określenia tego parametru należy określić parametr *servername* lub parametr *ConnectionContext* .</span><span class="sxs-lookup"><span data-stu-id="f482d-129">If you specify this parameter, you must specify the *ServerName* parameter or the *ConnectionContext* parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f482d-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="f482d-130">-Profile</span></span>
<span data-ttu-id="f482d-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f482d-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f482d-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="f482d-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f482d-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f482d-133">-ServerName</span></span>
<span data-ttu-id="f482d-134">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="f482d-134">Specifies the name of a server.</span></span>

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

### <span data-ttu-id="f482d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f482d-135">CommonParameters</span></span>
<span data-ttu-id="f482d-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f482d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f482d-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f482d-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f482d-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f482d-138">INPUTS</span></span>

### <span data-ttu-id="f482d-139">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database</span><span class="sxs-lookup"><span data-stu-id="f482d-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

### <span data-ttu-id="f482d-140">Microsoft. platformy windowsazure. Commands. SQLDatabase. model. SqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f482d-140">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext</span></span>

### <span data-ttu-id="f482d-141">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f482d-141">System.Guid</span></span>

## <span data-ttu-id="f482d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f482d-142">OUTPUTS</span></span>

### <span data-ttu-id="f482d-143">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponseList []</span><span class="sxs-lookup"><span data-stu-id="f482d-143">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponseList[]</span></span>
<span data-ttu-id="f482d-144">To polecenie cmdlet zwraca tablicę obiektów **DatabaseOperationResponseList** , jeśli zostanie wyświetlonych wiele operacji.</span><span class="sxs-lookup"><span data-stu-id="f482d-144">This cmdlet returns an array of **DatabaseOperationResponseList** objects if you get multiple operations.</span></span>

### <span data-ttu-id="f482d-145">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. Server. Database. DatabaseOperationResponse</span><span class="sxs-lookup"><span data-stu-id="f482d-145">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database.DatabaseOperationResponse</span></span>

## <span data-ttu-id="f482d-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f482d-146">NOTES</span></span>

## <span data-ttu-id="f482d-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f482d-147">RELATED LINKS</span></span>

[<span data-ttu-id="f482d-148">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="f482d-148">Azure SQL Database</span></span>](https://msdn.microsoft.com/library/ee336279.aspx)

[<span data-ttu-id="f482d-149">Stan operacji bazy danych</span><span class="sxs-lookup"><span data-stu-id="f482d-149">Database Operation Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[<span data-ttu-id="f482d-150">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="f482d-150">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="f482d-151">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f482d-151">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="f482d-152">Nowe — AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="f482d-152">New-AzureSqlDatabaseServerContext</span></span>](./New-AzureSqlDatabaseServerContext.md)


