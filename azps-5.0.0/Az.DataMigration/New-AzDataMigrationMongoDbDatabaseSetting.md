---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305395"
---
# <span data-ttu-id="396bc-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="396bc-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="396bc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="396bc-102">SYNOPSIS</span></span>
<span data-ttu-id="396bc-103">Tworzenie ustawienia bazy danych do migracji dla migracji mongoDb</span><span class="sxs-lookup"><span data-stu-id="396bc-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="396bc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="396bc-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="396bc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="396bc-105">DESCRIPTION</span></span>
<span data-ttu-id="396bc-106">Polecenie cmdlet New-AzDataMigrationMongoDbDatabaseSetting tworzy obiekt ustawienia migracji, który określa przepływność i zachowanie usuwania.</span><span class="sxs-lookup"><span data-stu-id="396bc-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="396bc-107">Wartość wyjściowa to para kluczowa z nazwą kolekcji i wartością ustawienia, która może być używana podczas wywoływania zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="396bc-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="396bc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="396bc-108">EXAMPLES</span></span>

### <span data-ttu-id="396bc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="396bc-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="396bc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="396bc-110">PARAMETERS</span></span>

### <span data-ttu-id="396bc-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="396bc-111">-Name</span></span>
<span data-ttu-id="396bc-112">Nazwa bazy danych</span><span class="sxs-lookup"><span data-stu-id="396bc-112">Name of the database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="396bc-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="396bc-113">-TargetRequestUnit</span></span>
<span data-ttu-id="396bc-114">Dedykowana wartość jednostki żądania na poziomie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="396bc-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="396bc-115">Jeśli ta funkcja nie jest ustawiona, kolekcja używa współużytkowanej bazy danych RU.</span><span class="sxs-lookup"><span data-stu-id="396bc-115">If not set, that collection uses shared database RU.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396bc-116">-Kolekcje</span><span class="sxs-lookup"><span data-stu-id="396bc-116">-Collections</span></span>
<span data-ttu-id="396bc-117">Tablica obiektów ustawień kolekcji MongoDb zwróconych przez New-AzureRmDmsMongoDbDatabaseSetting rozmowę.</span><span class="sxs-lookup"><span data-stu-id="396bc-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

```yaml
Type: System.Collections.Generic.KeyValuePair<string, MongoDbCollectionSettings>[]
Parameter Sets: (All)
Aliases: colls

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="396bc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="396bc-118">CommonParameters</span></span>
<span data-ttu-id="396bc-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="396bc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="396bc-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="396bc-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="396bc-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="396bc-121">INPUTS</span></span>

### <span data-ttu-id="396bc-122">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="396bc-122">None</span></span>

## <span data-ttu-id="396bc-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="396bc-123">OUTPUTS</span></span>

### <span data-ttu-id="396bc-124">Microsoft. Azure. Commands. datamigration. models. MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="396bc-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="396bc-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="396bc-125">NOTES</span></span>

## <span data-ttu-id="396bc-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="396bc-126">RELATED LINKS</span></span>
