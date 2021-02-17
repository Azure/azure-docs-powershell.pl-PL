---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: 9ae50501306dfa1a76fa4966113ac2e9b681f6c5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196546"
---
# <span data-ttu-id="eadd3-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="eadd3-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="eadd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eadd3-102">SYNOPSIS</span></span>
<span data-ttu-id="eadd3-103">Tworzy ustawienie bazy danych do migracji mongoDb</span><span class="sxs-lookup"><span data-stu-id="eadd3-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="eadd3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="eadd3-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="eadd3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="eadd3-105">DESCRIPTION</span></span>
<span data-ttu-id="eadd3-106">Polecenie New-AzDataMigrationMongoDbDatabaseSetting cmdlet tworzy obiekt ustawień migracji określający zachowanie przepływności i usuwania.</span><span class="sxs-lookup"><span data-stu-id="eadd3-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="eadd3-107">Dane wyjściowe to para wartości klucza z nazwą kolekcji i wartością ustawienia, której można użyć w celu wywołania zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="eadd3-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="eadd3-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="eadd3-108">EXAMPLES</span></span>

### <span data-ttu-id="eadd3-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eadd3-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="eadd3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eadd3-110">PARAMETERS</span></span>

### <span data-ttu-id="eadd3-111">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="eadd3-111">-Name</span></span>
<span data-ttu-id="eadd3-112">Nazwa bazy danych</span><span class="sxs-lookup"><span data-stu-id="eadd3-112">Name of the database</span></span>

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
### <span data-ttu-id="eadd3-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="eadd3-113">-TargetRequestUnit</span></span>
<span data-ttu-id="eadd3-114">Dedykowana wartość jednostki żądania na poziomie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="eadd3-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="eadd3-115">Jeśli nie jest ustawiona, ta kolekcja korzysta z udostępnionej bazy danych RU.</span><span class="sxs-lookup"><span data-stu-id="eadd3-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="eadd3-116">— Kolekcje</span><span class="sxs-lookup"><span data-stu-id="eadd3-116">-Collections</span></span>
<span data-ttu-id="eadd3-117">Tablica obiektów ustawień kolekcji MongoDb zwracanych przez New-AzureRmDmsMongoDbDatabaseSetting połączenia.</span><span class="sxs-lookup"><span data-stu-id="eadd3-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="eadd3-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eadd3-118">CommonParameters</span></span>
<span data-ttu-id="eadd3-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eadd3-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eadd3-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eadd3-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eadd3-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eadd3-121">INPUTS</span></span>

### <span data-ttu-id="eadd3-122">Brak</span><span class="sxs-lookup"><span data-stu-id="eadd3-122">None</span></span>

## <span data-ttu-id="eadd3-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="eadd3-123">OUTPUTS</span></span>

### <span data-ttu-id="eadd3-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="eadd3-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="eadd3-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="eadd3-125">NOTES</span></span>

## <span data-ttu-id="eadd3-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eadd3-126">RELATED LINKS</span></span>
