---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/new-azdatamigrationmongodbdatabasesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbDatabaseSetting.md
ms.openlocfilehash: cf034b01d0cc7bd707d65cb2ddd90e9567003861
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983146"
---
# <span data-ttu-id="1f7d4-101">New-AzDataMigrationMongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="1f7d4-101">New-AzDataMigrationMongoDbDatabaseSetting</span></span>

## <span data-ttu-id="1f7d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f7d4-102">SYNOPSIS</span></span>
<span data-ttu-id="1f7d4-103">Tworzy ustawienie bazy danych do migracji mongoDb</span><span class="sxs-lookup"><span data-stu-id="1f7d4-103">Creates database setting for migration for the mongoDb migration</span></span>

## <span data-ttu-id="1f7d4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1f7d4-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbDatabaseSetting  -Name <Name> [-RU <RU>] -CollectionSetting <Collections>
```

## <span data-ttu-id="1f7d4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1f7d4-105">DESCRIPTION</span></span>
<span data-ttu-id="1f7d4-106">Polecenie New-AzDataMigrationMongoDbDatabaseSetting cmdlet tworzy obiekt ustawień migracji określający zachowanie przepływności i usuwania.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-106">The New-AzDataMigrationMongoDbDatabaseSetting  cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="1f7d4-107">Wynik jest parą wartości klucza z nazwą kolekcji i wartością ustawienia, której można użyć w celu wywołania zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-107">The output is a key value pair with name of collection and value of the setting, which can be used in invoking the migration task.</span></span>

## <span data-ttu-id="1f7d4-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1f7d4-108">EXAMPLES</span></span>

### <span data-ttu-id="1f7d4-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1f7d4-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationMongoDbDatabaseSetting  -Name mycollection -RU 1000 -CollectionSetting @($coll1, $coll2)

Name Setting
---- -------
test Microsoft.Azure.Management.DataMigration.Models.MongoDbDatabaseSettings

```

## <span data-ttu-id="1f7d4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f7d4-110">PARAMETERS</span></span>

### <span data-ttu-id="1f7d4-111">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1f7d4-111">-Name</span></span>
<span data-ttu-id="1f7d4-112">Nazwa bazy danych</span><span class="sxs-lookup"><span data-stu-id="1f7d4-112">Name of the database</span></span>

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
### <span data-ttu-id="1f7d4-113">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="1f7d4-113">-TargetRequestUnit</span></span>
<span data-ttu-id="1f7d4-114">Dedykowana wartość jednostki żądania na poziomie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-114">The dedicated database level request unit value.</span></span> <span data-ttu-id="1f7d4-115">Jeśli nie jest ustawiona, ta kolekcja korzysta z udostępnionej bazy danych RU.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-115">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="1f7d4-116">— Kolekcje</span><span class="sxs-lookup"><span data-stu-id="1f7d4-116">-Collections</span></span>
<span data-ttu-id="1f7d4-117">Tablica obiektów ustawień kolekcji MongoDb zwracanych przez New-AzureRmDmsMongoDbDatabaseSetting połączenia.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-117">The array of MongoDb collection setting objects returned by New-AzureRmDmsMongoDbDatabaseSetting call.</span></span>

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

### <span data-ttu-id="1f7d4-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f7d4-118">CommonParameters</span></span>
<span data-ttu-id="1f7d4-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f7d4-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f7d4-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f7d4-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f7d4-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f7d4-121">INPUTS</span></span>

### <span data-ttu-id="1f7d4-122">Brak</span><span class="sxs-lookup"><span data-stu-id="1f7d4-122">None</span></span>

## <span data-ttu-id="1f7d4-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1f7d4-123">OUTPUTS</span></span>

### <span data-ttu-id="1f7d4-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span><span class="sxs-lookup"><span data-stu-id="1f7d4-124">Microsoft.Azure.Commands.DataMigration.Models.MongoDbDatabaseSetting</span></span>

## <span data-ttu-id="1f7d4-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1f7d4-125">NOTES</span></span>

## <span data-ttu-id="1f7d4-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1f7d4-126">RELATED LINKS</span></span>
