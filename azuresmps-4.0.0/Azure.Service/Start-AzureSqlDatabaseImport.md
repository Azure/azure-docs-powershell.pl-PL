---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5EE936CA-DD9A-4BC6-B835-E22AE633B46D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bc7c8f39f1bdbd35cfffeb59b3b4f184f30845e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054393"
---
# <span data-ttu-id="dd4c0-101">Start-AzureSqlDatabaseImport</span><span class="sxs-lookup"><span data-stu-id="dd4c0-101">Start-AzureSqlDatabaseImport</span></span>

## <span data-ttu-id="dd4c0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd4c0-102">SYNOPSIS</span></span>
<span data-ttu-id="dd4c0-103">Rozpoczyna operację importowania z magazynu obiektów BLOB do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-103">Starts an import operation from blob storage to an Azure SQL Database.</span></span>

## <span data-ttu-id="dd4c0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd4c0-104">SYNTAX</span></span>

### <span data-ttu-id="dd4c0-105">ByContainerObject</span><span class="sxs-lookup"><span data-stu-id="dd4c0-105">ByContainerObject</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContainer <AzureStorageContainer> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dd4c0-106">ByContainerName</span><span class="sxs-lookup"><span data-stu-id="dd4c0-106">ByContainerName</span></span>
```
Start-AzureSqlDatabaseImport -SqlConnectionContext <ISqlServerConnectionInformation>
 -StorageContext <IStorageContext> -StorageContainerName <String> -DatabaseName <String> -BlobName <String>
 [-Edition <DatabaseEdition>] [-DatabaseMaxSize <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dd4c0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dd4c0-107">DESCRIPTION</span></span>
<span data-ttu-id="dd4c0-108">Polecenie cmdlet **Start-AzureSqlDatabaseImport** rozpoczyna operację importowania z magazynu obiektów blob platformy Azure do bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-108">The **Start-AzureSqlDatabaseImport** cmdlet starts an import operation from Azure Blob storage to an Azure SQL Database.</span></span>
<span data-ttu-id="dd4c0-109">Jeśli baza danych nie istnieje, to polecenie cmdlet tworzy je przy użyciu określonych wartości rozmiaru i wersji.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-109">If the database does not exist, this cmdlet creates it by using the size and edition values that you specify.</span></span>
<span data-ttu-id="dd4c0-110">Operacja wymaga kontekstu połączenia serwera bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-110">The operation requires a database server connection context.</span></span>
<span data-ttu-id="dd4c0-111">Użyj polecenia cmdlet Get-AzureSqlDatabaseImportExportStatus, aby uzyskać stan operacji importowania.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-111">Use the Get-AzureSqlDatabaseImportExportStatus cmdlet to get the status of the import operation.</span></span>

## <span data-ttu-id="dd4c0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd4c0-112">EXAMPLES</span></span>

### <span data-ttu-id="dd4c0-113">Przykład 1: Importowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="dd4c0-113">Example 1: Import a database</span></span>
```
PS C:\>$Credential = Get-Credential
PS C:\> $SqlContext = New-AzureSqlDatabaseServerContext -ServerName $ServerName -Credentials $Credential
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName $StorageName -StorageAccountKey $StorageKey
PS C:\> $Container = Get-AzureStorageContainer -Name $ContainerName -Context $StorageContext
PS C:\> $ImportRequest = Start-AzureSqlDatabaseImport -SqlConnectionContext $SqlContext -StorageContainer $Container -DatabaseName $DatabaseName -BlobName $BlobName
```

<span data-ttu-id="dd4c0-114">W tym przykładzie zainicjowano proces importowania z przestrzeni dyskowej BLOB w zmiennej $BlobName w bazie danych SQL Azure o nazwie DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-114">This example initiates an import process from the Blob storage in the $BlobName variable into the Azure SQL Database named DatabaseName.</span></span>

## <span data-ttu-id="dd4c0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd4c0-115">PARAMETERS</span></span>

### <span data-ttu-id="dd4c0-116">-Obiekt blobname</span><span class="sxs-lookup"><span data-stu-id="dd4c0-116">-BlobName</span></span>
<span data-ttu-id="dd4c0-117">Określa nazwę magazynu obiektów blob platformy Azure, na podstawie którego ten aplet polecenia zaimportuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-117">Specifies the name of the Azure Blob storage from which this cmdlet imports the database.</span></span>

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

### <span data-ttu-id="dd4c0-118">-DatabaseMaxSize</span><span class="sxs-lookup"><span data-stu-id="dd4c0-118">-DatabaseMaxSize</span></span>
<span data-ttu-id="dd4c0-119">Określa maksymalny rozmiar bazy danych (w gigabajtach).</span><span class="sxs-lookup"><span data-stu-id="dd4c0-119">Specifies the maximum size, in gigabytes, for the database.</span></span>
<span data-ttu-id="dd4c0-120">Jeśli baza danych nie istnieje, to polecenie cmdlet utworzy je na podstawie tego maksymalnego rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-120">If the database does not exist, this cmdlet creates it based on this maximum size.</span></span>
<span data-ttu-id="dd4c0-121">Dopuszczalne wartości różnią się w zależności od wersji.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-121">The acceptable values differ based on edition.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4c0-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="dd4c0-122">-DatabaseName</span></span>
<span data-ttu-id="dd4c0-123">Określa nazwę bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-123">Specifies a name for the database.</span></span>
<span data-ttu-id="dd4c0-124">Jeśli baza danych nie istnieje, to polecenie cmdlet tworzy je i przypisuje nazwę, jaką ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-124">If the database does not exist, this cmdlet creates it, and assigns the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="dd4c0-125">-Edition</span><span class="sxs-lookup"><span data-stu-id="dd4c0-125">-Edition</span></span>
<span data-ttu-id="dd4c0-126">Określa wersję bazy danych.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-126">Specifies the edition of the database.</span></span>
<span data-ttu-id="dd4c0-127">Jeśli baza danych nie istnieje, to polecenie cmdlet tworzy je jako tę wersję.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-127">If the database does not exist, this cmdlet creates it as this edition.</span></span>
<span data-ttu-id="dd4c0-128">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="dd4c0-128">Valid values are:</span></span> 

- <span data-ttu-id="dd4c0-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dd4c0-129">None</span></span>
- <span data-ttu-id="dd4c0-130">Siecią</span><span class="sxs-lookup"><span data-stu-id="dd4c0-130">Web</span></span> 
- <span data-ttu-id="dd4c0-131">Biznesu</span><span class="sxs-lookup"><span data-stu-id="dd4c0-131">Business</span></span> 
- <span data-ttu-id="dd4c0-132">Podstawowym</span><span class="sxs-lookup"><span data-stu-id="dd4c0-132">Basic</span></span>
- <span data-ttu-id="dd4c0-133">Standard</span><span class="sxs-lookup"><span data-stu-id="dd4c0-133">Standard</span></span>
- <span data-ttu-id="dd4c0-134">Ubezpieczeni</span><span class="sxs-lookup"><span data-stu-id="dd4c0-134">Premium</span></span>

<span data-ttu-id="dd4c0-135">Domyślnie jest to sieć Web.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-135">The default is Web.</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd4c0-136">-Profile</span><span class="sxs-lookup"><span data-stu-id="dd4c0-136">-Profile</span></span>
<span data-ttu-id="dd4c0-137">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dd4c0-138">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dd4c0-139">-SqlConnectionContext</span><span class="sxs-lookup"><span data-stu-id="dd4c0-139">-SqlConnectionContext</span></span>
<span data-ttu-id="dd4c0-140">Określa kontekst połączenia serwera, który zawiera bazę danych.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-140">Specifies the connection context of a server that contains the database.</span></span>

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

### <span data-ttu-id="dd4c0-141">-StorageContainer</span><span class="sxs-lookup"><span data-stu-id="dd4c0-141">-StorageContainer</span></span>
<span data-ttu-id="dd4c0-142">Określa kontener magazynu zawierający obiekt BLOB, z którego to polecenie cmdlet importuje bazę danych.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-142">Specifies the storage container that contains the Blob from which this cmdlet imports a database.</span></span>

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

### <span data-ttu-id="dd4c0-143">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="dd4c0-143">-StorageContainerName</span></span>
<span data-ttu-id="dd4c0-144">Określa nazwę kontenera magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-144">Specifies the name of the Blob storage container.</span></span>

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

### <span data-ttu-id="dd4c0-145">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dd4c0-145">-StorageContext</span></span>
<span data-ttu-id="dd4c0-146">Określa kontekst kontenera magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-146">Specifies the context of the Blob storage container.</span></span>

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

### <span data-ttu-id="dd4c0-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd4c0-147">CommonParameters</span></span>
<span data-ttu-id="dd4c0-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd4c0-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd4c0-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd4c0-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd4c0-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd4c0-150">INPUTS</span></span>

## <span data-ttu-id="dd4c0-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd4c0-151">OUTPUTS</span></span>

### <span data-ttu-id="dd4c0-152">Microsoft. platformy windowsazure. Commands. SQLDatabase. Services. ImportExportRequest</span><span class="sxs-lookup"><span data-stu-id="dd4c0-152">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.ImportExportRequest</span></span>

## <span data-ttu-id="dd4c0-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd4c0-153">NOTES</span></span>

## <span data-ttu-id="dd4c0-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd4c0-154">RELATED LINKS</span></span>

[<span data-ttu-id="dd4c0-155">Baza danych SQL Azure</span><span class="sxs-lookup"><span data-stu-id="dd4c0-155">Azure SQL Database</span></span>](https://azure.microsoft.com/en-us/services/sql-database/)

[<span data-ttu-id="dd4c0-156">Importowanie bazy danych</span><span class="sxs-lookup"><span data-stu-id="dd4c0-156">Import Database</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn781284.aspx)

[<span data-ttu-id="dd4c0-157">Operacje dotyczące baz danych platformy Azure SQL</span><span class="sxs-lookup"><span data-stu-id="dd4c0-157">Operations for Azure SQL Databases</span></span>](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[<span data-ttu-id="dd4c0-158">Get-AzureSqlDatabaseImportExportStatus</span><span class="sxs-lookup"><span data-stu-id="dd4c0-158">Get-AzureSqlDatabaseImportExportStatus</span></span>](./Get-AzureSqlDatabaseImportExportStatus.md)

[<span data-ttu-id="dd4c0-159">Start — AzureSqlDatabaseExport</span><span class="sxs-lookup"><span data-stu-id="dd4c0-159">Start-AzureSqlDatabaseExport</span></span>](./Start-AzureSqlDatabaseExport.md)


