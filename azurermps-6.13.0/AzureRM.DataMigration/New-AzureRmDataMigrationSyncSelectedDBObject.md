---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: fc400c9eeb64acfa081d5a60a5e65089f415817b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718609"
---
# <span data-ttu-id="fec43-101">New-AzureRmDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="fec43-101">New-AzureRmDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="fec43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fec43-102">SYNOPSIS</span></span>
<span data-ttu-id="fec43-103">Umożliwia utworzenie obiektu informacyjnego bazy danych określonego dla scenariusza synchronizacji, który ma być wykorzystywany do wykonania zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="fec43-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fec43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fec43-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String>
 -TableMap <Hashtable> [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>]
 [-TargetSetting <Hashtable>] -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fec43-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fec43-105">DESCRIPTION</span></span>

<span data-ttu-id="fec43-106">Polecenie cmdlet New-AzureRmDataMigrationSyncSelectedDB powoduje utworzenie obiektu informacyjnego bazy danych określonego dla scenariusza synchronizacji zawierającego informacje o źródłowych i docelowych bazach danych.</span><span class="sxs-lookup"><span data-stu-id="fec43-106">The New-AzureRmDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="fec43-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fec43-107">EXAMPLES</span></span>

### <span data-ttu-id="fec43-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fec43-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzureRmDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="fec43-109">W tym przykładzie przedstawiono tworzenie obiektu metadanych bazy danych z opisem migrowania ustawień $DatabaseName do bazy danych $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="fec43-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="fec43-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fec43-110">PARAMETERS</span></span>

### <span data-ttu-id="fec43-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec43-111">-DefaultProfile</span></span>
<span data-ttu-id="fec43-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fec43-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="fec43-113">-MigrationSetting</span></span>
<span data-ttu-id="fec43-114">Ustawienia migracji, które dostrajają zachowanie migracji</span><span class="sxs-lookup"><span data-stu-id="fec43-114">Migration settings which tune the migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="fec43-115">-SchemaName</span></span>
<span data-ttu-id="fec43-116">Nazwa schematu do migrowania</span><span class="sxs-lookup"><span data-stu-id="fec43-116">Schema name to be migrated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fec43-117">-SourceDatabaseName</span></span>
<span data-ttu-id="fec43-118">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="fec43-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="fec43-119">-SourceSetting</span></span>
<span data-ttu-id="fec43-120">Ustawienia źródła umożliwiające strojenie zachowania źródłowego punktu końcowego migracji</span><span class="sxs-lookup"><span data-stu-id="fec43-120">Source settings to tune source endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-121">-TableMap</span><span class="sxs-lookup"><span data-stu-id="fec43-121">-TableMap</span></span>
<span data-ttu-id="fec43-122">Mapowanie źródeł na tabele docelowe</span><span class="sxs-lookup"><span data-stu-id="fec43-122">Mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="fec43-123">-TargetDatabaseName</span></span>
<span data-ttu-id="fec43-124">Nazwa docelowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="fec43-124">The name of the target database</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-125">-TargetSetting</span><span class="sxs-lookup"><span data-stu-id="fec43-125">-TargetSetting</span></span>
<span data-ttu-id="fec43-126">Ustawienia elementu docelowego umożliwiającego strojenie zachowania docelowej migracji punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="fec43-126">Target settings to tune target endpoint migration behavior</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec43-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec43-127">CommonParameters</span></span>
<span data-ttu-id="fec43-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fec43-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec43-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fec43-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec43-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fec43-130">INPUTS</span></span>

### <span data-ttu-id="fec43-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fec43-131">None</span></span>

## <span data-ttu-id="fec43-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fec43-132">OUTPUTS</span></span>

### <span data-ttu-id="fec43-133">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="fec43-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="fec43-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fec43-134">NOTES</span></span>

## <span data-ttu-id="fec43-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fec43-135">RELATED LINKS</span></span>