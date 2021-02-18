---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180898"
---
# <span data-ttu-id="c68ca-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="c68ca-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="c68ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c68ca-102">SYNOPSIS</span></span>
<span data-ttu-id="c68ca-103">Tworzy ustawienie kolekcji do migracji zgodnie z migracją mongoDb</span><span class="sxs-lookup"><span data-stu-id="c68ca-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="c68ca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c68ca-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="c68ca-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c68ca-105">DESCRIPTION</span></span>
<span data-ttu-id="c68ca-106">Polecenie New-AzDataMigrationMongoDbCollectionSetting cmdlet tworzy obiekt ustawień migracji określający zachowanie przepływności i usuwania.</span><span class="sxs-lookup"><span data-stu-id="c68ca-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="c68ca-107">Dane wyjściowe polecenia cmdlet to para wartości klucza z nazwą kolekcji i wartością ustawienia.</span><span class="sxs-lookup"><span data-stu-id="c68ca-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="c68ca-108">Dane wyjściowe są używane podczas składania ustawień poziomu bazy danych w celu migracji.</span><span class="sxs-lookup"><span data-stu-id="c68ca-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="c68ca-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c68ca-109">EXAMPLES</span></span>

### <span data-ttu-id="c68ca-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c68ca-110">Example 1</span></span>
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## <span data-ttu-id="c68ca-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c68ca-111">PARAMETERS</span></span>

### <span data-ttu-id="c68ca-112">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c68ca-112">-Name</span></span>
<span data-ttu-id="c68ca-113">Nazwa kolekcji</span><span class="sxs-lookup"><span data-stu-id="c68ca-113">Name of the collection</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68ca-114">-Skey</span><span class="sxs-lookup"><span data-stu-id="c68ca-114">-ShardKey</span></span>
<span data-ttu-id="c68ca-115">Rozdzielona przecinkami lista klawiszy skrótów.</span><span class="sxs-lookup"><span data-stu-id="c68ca-115">The comma separated list of the shard keys.</span></span> <span data-ttu-id="c68ca-116">W przypadku obiektu docelowego mongoDb możesz określić kolejność klucza sżdżu "Nazwa_klucza:Order", gdzie zamówienie ma wartość 1, -1 lub jest puste dla skrótu, na przykład "_id,email:-1".</span><span class="sxs-lookup"><span data-stu-id="c68ca-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c68ca-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="c68ca-117">-TargetRequestUnit</span></span>
<span data-ttu-id="c68ca-118">Wartość jednostki dedykowanego żądania kolekcji.</span><span class="sxs-lookup"><span data-stu-id="c68ca-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="c68ca-119">Jeśli nie jest ustawiona, ta kolekcja korzysta z udostępnionej bazy danych RU.</span><span class="sxs-lookup"><span data-stu-id="c68ca-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="c68ca-120">-CanDelete</span><span class="sxs-lookup"><span data-stu-id="c68ca-120">-CanDelete</span></span>
<span data-ttu-id="c68ca-121">Czy dane docelowe powinny zostać usunięte, jeśli przełącznik jest ustawiony, podczas migracji zostaną one wyczyszczone</span><span class="sxs-lookup"><span data-stu-id="c68ca-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### <span data-ttu-id="c68ca-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c68ca-122">CommonParameters</span></span>
<span data-ttu-id="c68ca-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c68ca-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c68ca-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c68ca-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c68ca-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c68ca-125">INPUTS</span></span>

### <span data-ttu-id="c68ca-126">Brak</span><span class="sxs-lookup"><span data-stu-id="c68ca-126">None</span></span>

## <span data-ttu-id="c68ca-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c68ca-127">OUTPUTS</span></span>

### <span data-ttu-id="c68ca-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="c68ca-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="c68ca-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c68ca-129">NOTES</span></span>

## <span data-ttu-id="c68ca-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c68ca-130">RELATED LINKS</span></span>
