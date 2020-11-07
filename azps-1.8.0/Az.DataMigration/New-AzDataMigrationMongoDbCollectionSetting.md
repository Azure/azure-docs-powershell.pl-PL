---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: aeb4c89ec4928118c5ebad05fe3c3602d88420ae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710001"
---
# <span data-ttu-id="b6351-101">New-AzDataMigrationMongoDbCollectionSetting</span><span class="sxs-lookup"><span data-stu-id="b6351-101">New-AzDataMigrationMongoDbCollectionSetting</span></span>

## <span data-ttu-id="b6351-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6351-102">SYNOPSIS</span></span>
<span data-ttu-id="b6351-103">Umożliwia utworzenie ustawienia kolekcji dla migracji zgodnie z migracją mongoDb.</span><span class="sxs-lookup"><span data-stu-id="b6351-103">Creates collection setting for migration according for the mongoDb migration</span></span>

## <span data-ttu-id="b6351-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6351-104">SYNTAX</span></span>

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## <span data-ttu-id="b6351-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b6351-105">DESCRIPTION</span></span>
<span data-ttu-id="b6351-106">Polecenie cmdlet New-AzDataMigrationMongoDbCollectionSetting tworzy obiekt ustawienia migracji, który określa przepływność i zachowanie usuwania.</span><span class="sxs-lookup"><span data-stu-id="b6351-106">The New-AzDataMigrationMongoDbCollectionSetting cmdlet creates the migration setting object that specifies the throughput and delete behavior.</span></span>
<span data-ttu-id="b6351-107">Dane wyjściowe polecenie cmdlet to para wartości klucza z nazwą kolekcji oraz wartością ustawienia.</span><span class="sxs-lookup"><span data-stu-id="b6351-107">The output the cmdlet is key value pair with name of the collection, and value of the setting.</span></span> <span data-ttu-id="b6351-108">Wyniki są używane w asemblerze ustawień poziomu bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="b6351-108">The output is used in assembling the database level settings for migration.</span></span>

## <span data-ttu-id="b6351-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6351-109">EXAMPLES</span></span>

### <span data-ttu-id="b6351-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6351-110">Example 1</span></span>
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

## <span data-ttu-id="b6351-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6351-111">PARAMETERS</span></span>

### <span data-ttu-id="b6351-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6351-112">-Name</span></span>
<span data-ttu-id="b6351-113">Nazwa kolekcji</span><span class="sxs-lookup"><span data-stu-id="b6351-113">Name of the collection</span></span>

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

### <span data-ttu-id="b6351-114">-ShardKey</span><span class="sxs-lookup"><span data-stu-id="b6351-114">-ShardKey</span></span>
<span data-ttu-id="b6351-115">Rozdzielana przecinkami lista kluczy Shard.</span><span class="sxs-lookup"><span data-stu-id="b6351-115">The comma seperated list of the shard keys.</span></span> <span data-ttu-id="b6351-116">W przypadku elementu docelowego mongoDb można określić kolejność kluczy Shard "ShardKeyName: Order", gdzie LP jest 1,-1 lub pusta w celu utworzenia skrótu, na przykład "_id, poczta e-mail:-1".</span><span class="sxs-lookup"><span data-stu-id="b6351-116">For mongoDb target, you can specify shard key order of "ShardKeyName:Order", where order is 1, -1 or empty for hashed, for example "_id,email:-1".</span></span>

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

### <span data-ttu-id="b6351-117">-TargetRequestUnit</span><span class="sxs-lookup"><span data-stu-id="b6351-117">-TargetRequestUnit</span></span>
<span data-ttu-id="b6351-118">Dedykowana wartość jednostki żądania kolekcji.</span><span class="sxs-lookup"><span data-stu-id="b6351-118">The dedicated collection request unit value.</span></span> <span data-ttu-id="b6351-119">Jeśli ta funkcja nie jest ustawiona, kolekcja używa współużytkowanej bazy danych RU.</span><span class="sxs-lookup"><span data-stu-id="b6351-119">If not set, that collection uses shared database RU.</span></span>

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

### <span data-ttu-id="b6351-120">-Usuń</span><span class="sxs-lookup"><span data-stu-id="b6351-120">-CanDelete</span></span>
<span data-ttu-id="b6351-121">Czy chcesz, aby dane docelowe były usuwane, jeśli przełącznik jest ustawiony, zostanie oczyszczony po migracji.</span><span class="sxs-lookup"><span data-stu-id="b6351-121">Whether the target data is supposed to be deleted, if the switch is set, it will be cleaned up at migration</span></span>

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


### <span data-ttu-id="b6351-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6351-122">CommonParameters</span></span>
<span data-ttu-id="b6351-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6351-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6351-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6351-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6351-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6351-125">INPUTS</span></span>

### <span data-ttu-id="b6351-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b6351-126">None</span></span>

## <span data-ttu-id="b6351-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6351-127">OUTPUTS</span></span>

### <span data-ttu-id="b6351-128">Microsoft. Azure. Commands. datamigration. MODELES. MongoDbCollectionSetting></span><span class="sxs-lookup"><span data-stu-id="b6351-128">Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting></span></span>

## <span data-ttu-id="b6351-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6351-129">NOTES</span></span>

## <span data-ttu-id="b6351-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6351-130">RELATED LINKS</span></span>