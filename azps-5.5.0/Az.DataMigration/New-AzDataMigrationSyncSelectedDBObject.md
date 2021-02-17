---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSyncSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSyncSelectedDBObject.md
ms.openlocfilehash: d045e25c754dc852bed127b4361d3d7eb584022b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180874"
---
# <span data-ttu-id="f66ee-101">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="f66ee-101">New-AzDataMigrationSyncSelectedDBObject</span></span>

## <span data-ttu-id="f66ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f66ee-102">SYNOPSIS</span></span>
<span data-ttu-id="f66ee-103">Tworzy obiekt informacyjny bazy danych specyficzny dla scenariusza synchronizacji, który ma być używany do zadania migracji.</span><span class="sxs-lookup"><span data-stu-id="f66ee-103">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

## <span data-ttu-id="f66ee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f66ee-104">SYNTAX</span></span>

```
New-AzDataMigrationSyncSelectedDBObject -TargetDatabaseName <String> -SchemaName <String> -TableMap <Hashtable>
 [-MigrationSetting <Hashtable>] [-SourceSetting <Hashtable>] [-TargetSetting <Hashtable>]
 -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f66ee-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f66ee-105">DESCRIPTION</span></span>

<span data-ttu-id="f66ee-106">Polecenie New-AzDataMigrationSyncSelectedDB cmdlet tworzy obiekt informacyjny bazy danych specyficzny dla scenariusza synchronizacji, który zawiera informacje o źródłowej i docelowej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="f66ee-106">The New-AzDataMigrationSyncSelectedDB cmdlet creates a database info object specific to the sync scenario which contains information about source and target databases.</span></span>

## <span data-ttu-id="f66ee-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f66ee-107">EXAMPLES</span></span>

### <span data-ttu-id="f66ee-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f66ee-108">Example 1</span></span>
```
PS C:\> $tableMap = New-Object 'system.collections.hashtable'
    $tableMap.Add("dbo.TestTable1", "dbo.TestTable1")
    $tableMap.Add("dbo.TestTable2","dbo.TestTable2")

    $selectedDbs = New-AzDmsSyncSelectedDBObject 
        -TargetDatabaseName DatabaseName `
        -SchemaName dbo `
        -TableMap $tableMap `
        -SourceDatabaseName DatabaseName
```

<span data-ttu-id="f66ee-109">W tym przykładzie jest tworzyny obiekt metadanych bazy danych opisujący ustawienia migrowania $DatabaseName do $DatabaseName.</span><span class="sxs-lookup"><span data-stu-id="f66ee-109">This example creates a database metadata object describing the migrating settings for $DatabaseName to database $DatabaseName.</span></span>  

## <span data-ttu-id="f66ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f66ee-110">PARAMETERS</span></span>

### <span data-ttu-id="f66ee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f66ee-111">-DefaultProfile</span></span>
<span data-ttu-id="f66ee-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f66ee-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66ee-113">-MigrationSetting</span><span class="sxs-lookup"><span data-stu-id="f66ee-113">-MigrationSetting</span></span>
<span data-ttu-id="f66ee-114">Ustawienia migracji, które dostrajają zachowanie migracji</span><span class="sxs-lookup"><span data-stu-id="f66ee-114">Migration settings which tune the migration behavior</span></span>

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

### <span data-ttu-id="f66ee-115">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f66ee-115">-SchemaName</span></span>
<span data-ttu-id="f66ee-116">Nazwa schematu do zmigrowania</span><span class="sxs-lookup"><span data-stu-id="f66ee-116">Schema name to be migrated</span></span>

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

### <span data-ttu-id="f66ee-117">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f66ee-117">-SourceDatabaseName</span></span>
<span data-ttu-id="f66ee-118">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f66ee-118">The name of the source database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f66ee-119">-SourceSetting</span><span class="sxs-lookup"><span data-stu-id="f66ee-119">-SourceSetting</span></span>
<span data-ttu-id="f66ee-120">Ustawienia źródła w celu dostosowania zachowania migracji punktu końcowego źródła</span><span class="sxs-lookup"><span data-stu-id="f66ee-120">Source settings to tune source endpoint migration behavior</span></span>

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

### <span data-ttu-id="f66ee-121">- TableMap</span><span class="sxs-lookup"><span data-stu-id="f66ee-121">-TableMap</span></span>
<span data-ttu-id="f66ee-122">Mapowanie tabel źródłowych na docelowe</span><span class="sxs-lookup"><span data-stu-id="f66ee-122">Mapping of source to target tables</span></span>

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

### <span data-ttu-id="f66ee-123">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f66ee-123">-TargetDatabaseName</span></span>
<span data-ttu-id="f66ee-124">Nazwa docelowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="f66ee-124">The name of the target database</span></span>

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

### <span data-ttu-id="f66ee-125">- TargetSetting</span><span class="sxs-lookup"><span data-stu-id="f66ee-125">-TargetSetting</span></span>
<span data-ttu-id="f66ee-126">Ustawienia docelowe w celu dostosowania zachowania migracji punktu końcowego</span><span class="sxs-lookup"><span data-stu-id="f66ee-126">Target settings to tune target endpoint migration behavior</span></span>

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

### <span data-ttu-id="f66ee-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f66ee-127">CommonParameters</span></span>
<span data-ttu-id="f66ee-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f66ee-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f66ee-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f66ee-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f66ee-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f66ee-130">INPUTS</span></span>

### <span data-ttu-id="f66ee-131">Brak</span><span class="sxs-lookup"><span data-stu-id="f66ee-131">None</span></span>

## <span data-ttu-id="f66ee-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f66ee-132">OUTPUTS</span></span>

### <span data-ttu-id="f66ee-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span><span class="sxs-lookup"><span data-stu-id="f66ee-133">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbSyncTaskInput</span></span>

## <span data-ttu-id="f66ee-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f66ee-134">NOTES</span></span>

## <span data-ttu-id="f66ee-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f66ee-135">RELATED LINKS</span></span>
