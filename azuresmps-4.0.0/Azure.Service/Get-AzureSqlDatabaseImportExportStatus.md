---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 4661C479-6E3B-425D-B9D2-B36D7A83130C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c55ebd22337a8078f3ae495b3901317f4201e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055260"
---
# <span data-ttu-id="475c9-101">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="475c9-101">Get-AzureSqlDatabaseImportExportStatus</span></span>

## <span data-ttu-id="475c9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="475c9-102">SYNOPSIS</span></span>
<span data-ttu-id="475c9-103">Pobiera stan żądania importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="475c9-103">Gets the status of an import or export request.</span></span>

## <span data-ttu-id="475c9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="475c9-104">SYNTAX</span></span>

### <span data-ttu-id="475c9-105">ByConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="475c9-105">ByConnectionInfo</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Username <String> -Password <String> -ServerName <String>
 -RequestId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="475c9-106">ByRequestObject</span><span class="sxs-lookup"><span data-stu-id="475c9-106">ByRequestObject</span></span>
```
Get-AzureSqlDatabaseImportExportStatus -Request <ImportExportRequest> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="475c9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="475c9-107">DESCRIPTION</span></span>
<span data-ttu-id="475c9-108">Polecenie cmdlet **Get-AzureSqlDatabaseImportExportStatus** Pobiera stan żądania importu lub eksportu.</span><span class="sxs-lookup"><span data-stu-id="475c9-108">The **Get-AzureSqlDatabaseImportExportStatus** cmdlet gets the status of an import or export request.</span></span>
<span data-ttu-id="475c9-109">Polecenie cmdlet Start-AzureSqlDatabaseImport lub Start-AzureSqlDatabaseExport inicjuje żądania.</span><span class="sxs-lookup"><span data-stu-id="475c9-109">The Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet initiates requests.</span></span>
<span data-ttu-id="475c9-110">Obiekt request można określić przy użyciu parametru *Request* lub można go zidentyfikować przy użyciu parametru *IdentyfikatorŻądania* oraz parametrów *username* , *Password* i *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="475c9-110">You can specify the request object by using the *Request* parameter, or you can identify the request by using the *RequestId* parameter and the *Username* , *Password* , and *ServerName* parameters.</span></span>

## <span data-ttu-id="475c9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="475c9-111">EXAMPLES</span></span>

### <span data-ttu-id="475c9-112">Przykład 1: uzyskiwanie statusu żądania eksportu</span><span class="sxs-lookup"><span data-stu-id="475c9-112">Example 1: Get the status of an export request</span></span>
```
PS C:\> $ExportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
PS C:\> Get-AzureSqlDatabaseImportExportStatus -Request $ExportRequest
```

<span data-ttu-id="475c9-113">Pierwsze polecenie tworzy żądanie eksportu, a następnie zapisuje je w zmiennej $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="475c9-113">The first command creates an export request, and then stores it in the $ExportRequest variable.</span></span>

<span data-ttu-id="475c9-114">Drugie polecenie uzyskuje stan żądania eksportu przechowywanego w $ExportRequest.</span><span class="sxs-lookup"><span data-stu-id="475c9-114">The second command gets the status of the export request stored in $ExportRequest.</span></span>

## <span data-ttu-id="475c9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="475c9-115">PARAMETERS</span></span>

### <span data-ttu-id="475c9-116">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="475c9-116">-Password</span></span>
<span data-ttu-id="475c9-117">Określa hasło wymagane do nawiązania połączenia z serwerem bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="475c9-117">Specifies the password that is required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="475c9-118">Jeśli określono parametr *numer_id_żądania* , należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="475c9-118">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475c9-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="475c9-119">-Profile</span></span>
<span data-ttu-id="475c9-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="475c9-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="475c9-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="475c9-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="475c9-122">-Request</span><span class="sxs-lookup"><span data-stu-id="475c9-122">-Request</span></span>
<span data-ttu-id="475c9-123">Określa obiekt **ImportExportRequest** .</span><span class="sxs-lookup"><span data-stu-id="475c9-123">Specifies an **ImportExportRequest** object.</span></span>
<span data-ttu-id="475c9-124">Aby uzyskać obiekt request importu lub eksportu, użyj polecenia cmdlet Start-AzureSqlDatabaseImport lub Start-AzureSqlDatabaseExport.</span><span class="sxs-lookup"><span data-stu-id="475c9-124">To obtain an import or export request object, use the Start-AzureSqlDatabaseImport or Start-AzureSqlDatabaseExport cmdlet.</span></span>

```yaml
Type: ImportExportRequest
Parameter Sets: ByRequestObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475c9-125">-IdentyfikatorŻądania</span><span class="sxs-lookup"><span data-stu-id="475c9-125">-RequestId</span></span>
<span data-ttu-id="475c9-126">Określa identyfikator GUID operacji importu lub eksportu, dla którego to polecenie cmdlet pobiera stan.</span><span class="sxs-lookup"><span data-stu-id="475c9-126">Specifies the GUID of the import or export operation for which this cmdlet gets status.</span></span>
<span data-ttu-id="475c9-127">W przypadku określenia tego parametru należy określić parametry *username* , *Password* i *nazwa_serwera* .</span><span class="sxs-lookup"><span data-stu-id="475c9-127">If you specify this parameter, you must specify the *UserName* , *Password* , and *ServerName* parameters.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475c9-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="475c9-128">-ServerName</span></span>
<span data-ttu-id="475c9-129">Określa nazwę serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="475c9-129">Specifies the name of the Azure SQL Database server.</span></span>
<span data-ttu-id="475c9-130">Jeśli określono parametr *numer_id_żądania* , należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="475c9-130">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475c9-131">-Username</span><span class="sxs-lookup"><span data-stu-id="475c9-131">-Username</span></span>
<span data-ttu-id="475c9-132">Określa nazwę użytkownika wymaganą do nawiązania połączenia z serwerem bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="475c9-132">Specifies the user name required to connect to the Azure SQL Database server.</span></span>
<span data-ttu-id="475c9-133">Jeśli określono parametr *numer_id_żądania* , należy określić ten parametr.</span><span class="sxs-lookup"><span data-stu-id="475c9-133">You must specify this parameter if you specified the *RequestId* parameter.</span></span>

```yaml
Type: String
Parameter Sets: ByConnectionInfo
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="475c9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="475c9-134">CommonParameters</span></span>
<span data-ttu-id="475c9-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="475c9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="475c9-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="475c9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="475c9-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="475c9-137">INPUTS</span></span>

## <span data-ttu-id="475c9-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="475c9-138">OUTPUTS</span></span>

### <span data-ttu-id="475c9-139">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. ImportExport. StatusInfo</span><span class="sxs-lookup"><span data-stu-id="475c9-139">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExport.StatusInfo</span></span>

## <span data-ttu-id="475c9-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="475c9-140">NOTES</span></span>

## <span data-ttu-id="475c9-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="475c9-141">RELATED LINKS</span></span>

[<span data-ttu-id="475c9-142">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="475c9-142">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="475c9-143">Uzyskiwanie statusu bazy danych importowania eksportu</span><span class="sxs-lookup"><span data-stu-id="475c9-143">Get Import Export Database Status</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781289.aspx)

[<span data-ttu-id="475c9-144">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="475c9-144">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="475c9-145">Start — AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="475c9-145">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)

[<span data-ttu-id="475c9-146">Start — AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="475c9-146">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


