---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 3005E411-9466-4602-8E07-F4EF8804AB2A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22bff485bf49e0ec5f482e1325af661862583605
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054718"
---
# <span data-ttu-id="4f89b-101">Start-AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="4f89b-101">Start-AzureSqlDatabaseExport</span></span>

## <span data-ttu-id="4f89b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f89b-102">SYNOPSIS</span></span>
<span data-ttu-id="4f89b-103">Rozpoczyna operację eksportowania z bazy danych SQL Azure do magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f89b-103">Starts an export operation from an Azure SQL Database to Blob storage.</span></span>

## <span data-ttu-id="4f89b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f89b-104">SYNTAX</span></span>

### <span data-ttu-id="4f89b-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="4f89b-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="4f89b-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="4f89b-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseExport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4f89b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4f89b-107">DESCRIPTION</span></span>
<span data-ttu-id="4f89b-108">Polecenie cmdlet **Start-AzureSqlDatabaseExport** rozpoczyna operację eksportowania z bazy danych SQL Azure do magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f89b-108">The **Start-AzureSqlDatabaseExport** cmdlet starts an export operation from an Azure SQL Database to Blob storage.</span></span>
<span data-ttu-id="4f89b-109">Operacja wymaga kontekstu połączenia serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="4f89b-109">The operation requires a database server connection context.</span></span>
<span data-ttu-id="4f89b-110">Użyj polecenia cmdlet Get-AzureSqlDatabaseImportExportStatus, aby uzyskać stan operacji eksportowania.</span><span class="sxs-lookup"><span data-stu-id="4f89b-110">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the export operation.</span></span>

## <span data-ttu-id="4f89b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f89b-111">EXAMPLES</span></span>

### <span data-ttu-id="4f89b-112">Przykład 1. Eksportowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="4f89b-112">Example 1: Export a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credential $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $exportRequest = Start-AzureSqlDatabaseExport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="4f89b-113">W tym przykładzie zainicjowano proces eksportowania z bazy danych SQL Azure zawierającej nazwę przechowywaną w zmiennej $DatabaseName do magazynu obiektów BLOB przechowywanego w zmiennej $BlobName.</span><span class="sxs-lookup"><span data-stu-id="4f89b-113">This example initiates an export process from the Azure SQL Database that has the name stored in the $DatabaseName variable to the Blob storage stored in the $BlobName variable.</span></span>

## <span data-ttu-id="4f89b-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f89b-114">PARAMETERS</span></span>

### <span data-ttu-id="4f89b-115">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="4f89b-115">-BlobName</span></span>
<span data-ttu-id="4f89b-116">Określa nazwę magazynu obiektów blob platformy Azure, w którym polecenie cmdlet eksportuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="4f89b-116">Specifies the name of the Azure Blob storage into which this cmdlet exports the database.</span></span>

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

### <span data-ttu-id="4f89b-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4f89b-117">-DatabaseName</span></span>
<span data-ttu-id="4f89b-118">Określa nazwę bazy danych, z której to polecenie cmdlet eksportuje dane.</span><span class="sxs-lookup"><span data-stu-id="4f89b-118">Specifies the name of the database from which this cmdlet exports data.</span></span>

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

### <span data-ttu-id="4f89b-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="4f89b-119">-Profile</span></span>
<span data-ttu-id="4f89b-120">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f89b-120">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4f89b-121">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="4f89b-121">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="4f89b-122">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="4f89b-122">-SqlConnectionContext</span></span>
<span data-ttu-id="4f89b-123">Określa kontekst połączenia serwera, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="4f89b-123">Specifies the connection context of a server that contains the database.</span></span>

```yaml
Type: ISqlServerConnectionInformation
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f89b-124">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="4f89b-124">-StorageContainer</span></span>
<span data-ttu-id="4f89b-125">Określa kontener magazynu zawierający obiekt BLOB, do którego jest eksportowany Program Database.</span><span class="sxs-lookup"><span data-stu-id="4f89b-125">Specifies the storage container that contains the Blob into which this cmdlet export a database.</span></span>

```yaml
Type: AzureStorageContainer
Parameter Sets: ByContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f89b-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="4f89b-126">-StorageContainerName</span></span>
<span data-ttu-id="4f89b-127">Określa nazwę kontenera magazynu zawierającego obiekt BLOB, do którego jest eksportowany baza danych przy użyciu tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4f89b-127">Specifies the name of the storage container that contains the Blob into which this cmdlet exports a database.</span></span>

```yaml
Type: String
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f89b-128">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="4f89b-128">-StorageContext</span></span>
<span data-ttu-id="4f89b-129">Określa kontekst kontenera magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="4f89b-129">Specifies the context of the Blob storage container.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ByContainerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f89b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f89b-130">CommonParameters</span></span>
<span data-ttu-id="4f89b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f89b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f89b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f89b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f89b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f89b-133">INPUTS</span></span>

## <span data-ttu-id="4f89b-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f89b-134">OUTPUTS</span></span>

### <span data-ttu-id="4f89b-135">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="4f89b-135">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="4f89b-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f89b-136">NOTES</span></span>

## <span data-ttu-id="4f89b-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f89b-137">RELATED LINKS</span></span>

[<span data-ttu-id="4f89b-138">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="4f89b-138">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="4f89b-139">Eksportowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="4f89b-139">Export Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781282.aspx)

[<span data-ttu-id="4f89b-140">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="4f89b-140">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="4f89b-141">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="4f89b-141">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="4f89b-142">Start — AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="4f89b-142">Start-AzureSqlDatabaseImport</span></span>](./Start-AzureSqlDatabaseImport.md)


