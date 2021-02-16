---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402426"
---
# <span data-ttu-id="764df-101">Get-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="764df-101">Get-AzureSqlDatabaseCopy</span></span>

## <span data-ttu-id="764df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="764df-102">SYNOPSIS</span></span>
<span data-ttu-id="764df-103">Sprawdza stan relacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="764df-103">Checks the status of copy relationships.</span></span>

## <span data-ttu-id="764df-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="764df-104">SYNTAX</span></span>

### <span data-ttu-id="764df-105">ByServerNameOnly (Default)</span><span class="sxs-lookup"><span data-stu-id="764df-105">ByServerNameOnly (Default)</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="764df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="764df-106">ByInputObject</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="764df-107">ByDatabase</span><span class="sxs-lookup"><span data-stu-id="764df-107">ByDatabase</span></span>
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="764df-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="764df-108">DESCRIPTION</span></span>
<span data-ttu-id="764df-109">Polecenie **cmdlet Get-AzureSqlDatabaseCopy** sprawdza stan co najmniej jednej aktywnej relacji kopiowania.</span><span class="sxs-lookup"><span data-stu-id="764df-109">The **Get-AzureSqlDatabaseCopy** cmdlet checks the status of one or more active copy relationships.</span></span>
<span data-ttu-id="764df-110">Uruchom to polecenie cmdlet po uruchomieniu Start-AzureSqlDatabaseCopy lub Stop-AzureSqlDatabaseCopy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="764df-110">Run this cmdlet after you run the Start-AzureSqlDatabaseCopy or Stop-AzureSqlDatabaseCopy cmdlet.</span></span>
<span data-ttu-id="764df-111">Możesz sprawdzić konkretną relację kopiowania, wszystkie relacje kopiowania lub filtrowaną listę relacji kopiowania, na przykład wszystkie kopie na określonym serwerze docelowym.</span><span class="sxs-lookup"><span data-stu-id="764df-111">You can check a specific copy relationship, all copy relationships, or a filtered list of copy relationships, such as all copies on a specific target server.</span></span>
<span data-ttu-id="764df-112">To polecenie cmdlet można uruchomić na serwerze hostowym źródłową lub docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="764df-112">You can run this cmdlet on the server that hosts the source or target database.</span></span>

<span data-ttu-id="764df-113">To polecenie cmdlet jest synchroniczne.</span><span class="sxs-lookup"><span data-stu-id="764df-113">This cmdlet is synchronous.</span></span>
<span data-ttu-id="764df-114">Polecenie cmdlet blokuje konsolę programu Azure PowerShell do momentu, aż zwróci obiekt stanu.</span><span class="sxs-lookup"><span data-stu-id="764df-114">The cmdlet blocks the Azure PowerShell console until it returns a status object.</span></span>

<span data-ttu-id="764df-115">Parametry *partnerServer i* *PartnerDatabase* są opcjonalne.</span><span class="sxs-lookup"><span data-stu-id="764df-115">The *PartnerServer* and *PartnerDatabase* parameters are optional.</span></span>
<span data-ttu-id="764df-116">Jeśli nie określisz ani jednego z parametrów, to polecenie cmdlet zwróci tabelę wyników.</span><span class="sxs-lookup"><span data-stu-id="764df-116">If you do not specify either parameter, this cmdlet returns a table of results.</span></span>
<span data-ttu-id="764df-117">Aby wyświetlić stan tylko dla konkretnej bazy danych, określ oba parametry.</span><span class="sxs-lookup"><span data-stu-id="764df-117">To see the status for only a particular database, specify both parameters.</span></span>

## <span data-ttu-id="764df-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="764df-118">EXAMPLES</span></span>

### <span data-ttu-id="764df-119">Przykład 1. Uzyskiwanie stanu kopii bazy danych</span><span class="sxs-lookup"><span data-stu-id="764df-119">Example 1: Get the copy status of a database</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

<span data-ttu-id="764df-120">To polecenie pobiera stan bazy danych o nazwie Zamówienia na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="764df-120">This command gets the status of the database named Orders on the server named lpqd0zbr8y.</span></span>
<span data-ttu-id="764df-121">Parametr *PartnerServer* ogranicza to polecenie do serwera bk0b8kf658.</span><span class="sxs-lookup"><span data-stu-id="764df-121">The *PartnerServer* parameter restricts this command to the bk0b8kf658 server.</span></span>

### <span data-ttu-id="764df-122">Przykład 2. Uzyskiwanie stanu wszystkich kopii na serwerzeUzyskanie stanu wszystkich kopii na serwerze</span><span class="sxs-lookup"><span data-stu-id="764df-122">Example 2: Get the status of all copies on a serverGet the status of all copies on a server</span></span>
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

<span data-ttu-id="764df-123">To polecenie pobiera stan wszystkich aktywnych kopii na serwerze o nazwie lpqd0zbr8y.</span><span class="sxs-lookup"><span data-stu-id="764df-123">This command gets the status of all active copies on the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="764df-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="764df-124">PARAMETERS</span></span>

### <span data-ttu-id="764df-125">— Baza danych</span><span class="sxs-lookup"><span data-stu-id="764df-125">-Database</span></span>
<span data-ttu-id="764df-126">Określa obiekt reprezentujący źródłową bazę danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="764df-126">Specifies an object that represents the source Azure SQL Database.</span></span>
<span data-ttu-id="764df-127">To polecenie cmdlet pobiera stan kopii bazy danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="764df-127">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="764df-128">-DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="764df-128">-DatabaseCopy</span></span>
<span data-ttu-id="764df-129">Określa obiekt reprezentujący bazę danych.</span><span class="sxs-lookup"><span data-stu-id="764df-129">Specifies an object that represents a database.</span></span>
<span data-ttu-id="764df-130">To polecenie cmdlet pobiera stan kopii bazy danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="764df-130">This cmdlet gets the copy status of the database that this parameter specifies.</span></span>
<span data-ttu-id="764df-131">Ten parametr akceptuje dane wejściowe potoku.</span><span class="sxs-lookup"><span data-stu-id="764df-131">This parameter accepts pipeline input.</span></span>

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

### <span data-ttu-id="764df-132">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="764df-132">-DatabaseName</span></span>
<span data-ttu-id="764df-133">Określa nazwę źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="764df-133">Specifies the name of the source database.</span></span>
<span data-ttu-id="764df-134">To polecenie cmdlet pobiera stan kopii bazy danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="764df-134">This cmdlet gets that copy status of the database that this parameter specifies.</span></span>

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

### <span data-ttu-id="764df-135">-PartnerDatabase</span><span class="sxs-lookup"><span data-stu-id="764df-135">-PartnerDatabase</span></span>
<span data-ttu-id="764df-136">Określa nazwę pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="764df-136">Specifies name of the secondary database.</span></span>
<span data-ttu-id="764df-137">Jeśli ta baza danych nie zostanie znaleziona w sys.dm_database_copies zarządzania dynamicznego, to polecenie cmdlet zwraca pusty obiekt stanu.</span><span class="sxs-lookup"><span data-stu-id="764df-137">If this database is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="764df-138">-PartnerServer</span><span class="sxs-lookup"><span data-stu-id="764df-138">-PartnerServer</span></span>
<span data-ttu-id="764df-139">Określa nazwę serwera hostowego docelową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="764df-139">Specifies the name of the server that hosts the target database.</span></span>
<span data-ttu-id="764df-140">Jeśli ten serwer nie zostanie znaleziony w sys.dm_database_copies zarządzania dynamicznego, to polecenie cmdlet zwraca pusty obiekt stanu.</span><span class="sxs-lookup"><span data-stu-id="764df-140">If this server is not found in the sys.dm_database_copies dynamic management view, this cmdlet returns an empty status object.</span></span>

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

### <span data-ttu-id="764df-141">— Profil</span><span class="sxs-lookup"><span data-stu-id="764df-141">-Profile</span></span>
<span data-ttu-id="764df-142">Określa profil platformy Azure, z którego będzie odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="764df-142">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="764df-143">Jeśli nie określisz profilu, to polecenie cmdlet zostanie odczytane z lokalnego profilu domyślnego.</span><span class="sxs-lookup"><span data-stu-id="764df-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="764df-144">-ServerName</span><span class="sxs-lookup"><span data-stu-id="764df-144">-ServerName</span></span>
<span data-ttu-id="764df-145">Określa nazwę serwera, na którym znajduje się kopia bazy danych.</span><span class="sxs-lookup"><span data-stu-id="764df-145">Specifies the name of the server on which the database copy resides.</span></span>

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

### <span data-ttu-id="764df-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="764df-146">CommonParameters</span></span>
<span data-ttu-id="764df-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="764df-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="764df-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="764df-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="764df-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="764df-149">INPUTS</span></span>

### <span data-ttu-id="764df-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="764df-150">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

### <span data-ttu-id="764df-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span><span class="sxs-lookup"><span data-stu-id="764df-151">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database</span></span>

## <span data-ttu-id="764df-152">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="764df-152">OUTPUTS</span></span>

### <span data-ttu-id="764df-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="764df-153">Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy</span></span>

## <span data-ttu-id="764df-154">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="764df-154">NOTES</span></span>
* <span data-ttu-id="764df-155">Uwierzytelnianie: to polecenie cmdlet wymaga uwierzytelniania opartego na certyfikatach.</span><span class="sxs-lookup"><span data-stu-id="764df-155">Authentication: This cmdlet requires certificate-based authentication.</span></span> <span data-ttu-id="764df-156">Aby uzyskać przykład sposobu używania uwierzytelniania opartego na certyfikatach w celu ustawienia bieżącej subskrypcji, zobacz New-AzureSqlDatabaseServerContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="764df-156">For an example of how to use certificate-based authentication to set the current subscription, see the New-AzureSqlDatabaseServerContext cmdlet.</span></span>

## <span data-ttu-id="764df-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="764df-157">RELATED LINKS</span></span>

[<span data-ttu-id="764df-158">Azure SQL Database</span><span class="sxs-lookup"><span data-stu-id="764df-158">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="764df-159">Operacje na platformie Azure SQL Databases</span><span class="sxs-lookup"><span data-stu-id="764df-159">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[<span data-ttu-id="764df-160">Start-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="764df-160">Start-AzureSqlDatabaseCopy</span></span>](./Start-AzureSqlDatabaseCopy.md)

[<span data-ttu-id="764df-161">Stop-AzureSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="764df-161">Stop-AzureSqlDatabaseCopy</span></span>](./Stop-AzureSqlDatabaseCopy.md)


