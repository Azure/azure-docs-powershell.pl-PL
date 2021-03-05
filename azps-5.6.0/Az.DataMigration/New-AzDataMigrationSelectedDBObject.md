---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: c6e417ade1e411eaaa0b86f8f69ac6c17f228e91
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998047"
---
# <span data-ttu-id="e99f6-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="e99f6-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="e99f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e99f6-102">SYNOPSIS</span></span>
<span data-ttu-id="e99f6-103">Tworzy obiekt wejściowy bazy danych zawierający informacje o źródłowych i docelowych bazach danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="e99f6-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="e99f6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e99f6-104">SYNTAX</span></span>

### <span data-ttu-id="e99f6-105">MigrateSqlServerSqlDb (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e99f6-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e99f6-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="e99f6-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e99f6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e99f6-107">DESCRIPTION</span></span>
<span data-ttu-id="e99f6-108">Polecenie New-AzDataMigrationSelectedDB cmdlet tworzy do migracji obiekt informacyjny bazy danych zawierający informacje o źródłowej i docelowej bazie danych, a także mapowania tabel.</span><span class="sxs-lookup"><span data-stu-id="e99f6-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="e99f6-109">To polecenie cmdlet może być używane jako parametr z New-AzDataMigrationTask cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e99f6-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="e99f6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e99f6-110">EXAMPLES</span></span>

### <span data-ttu-id="e99f6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e99f6-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="e99f6-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e99f6-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="e99f6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e99f6-113">PARAMETERS</span></span>

### <span data-ttu-id="e99f6-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="e99f6-114">-BackupFileShare</span></span>
<span data-ttu-id="e99f6-115">Udział plików, w którym należy wrócić do kopii zapasowej plików bazy danych na serwerze źródłowym dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e99f6-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="e99f6-116">To ustawienie umożliwia zastępowanie informacji o udostępnianiu plików dla każdej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e99f6-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="e99f6-117">Użyj w pełni kwalifikowanej nazwy domeny dla serwera.</span><span class="sxs-lookup"><span data-stu-id="e99f6-117">Use fully qualified domain name for the server.</span></span>

```yaml
Type: Microsoft.Azure.Management.DataMigration.Models.FileShare
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e99f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e99f6-118">-DefaultProfile</span></span>
<span data-ttu-id="e99f6-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e99f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e99f6-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="e99f6-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="e99f6-121">Ustawianie odczytu bazy danych przed migracją</span><span class="sxs-lookup"><span data-stu-id="e99f6-121">Set Database to readonly before migration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99f6-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="e99f6-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="e99f6-123">Ustaw typ migracji programu SQL Server na migrację bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e99f6-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99f6-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="e99f6-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="e99f6-125">Ustaw typ migracji programu SQL Server na migrację MI bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="e99f6-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MigrateSqlServerSqlDbMi
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99f6-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e99f6-126">-SourceDatabaseName</span></span>
<span data-ttu-id="e99f6-127">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e99f6-127">The name of the source database.</span></span>

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

### <span data-ttu-id="e99f6-128">- TableMap</span><span class="sxs-lookup"><span data-stu-id="e99f6-128">-TableMap</span></span>
<span data-ttu-id="e99f6-129">mapowanie tabel źródłowych na docelowe</span><span class="sxs-lookup"><span data-stu-id="e99f6-129">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: MigrateSqlServerSqlDb
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e99f6-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="e99f6-130">-TargetDatabaseName</span></span>
<span data-ttu-id="e99f6-131">Nazwa docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e99f6-131">The name of the target database.</span></span>

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

### <span data-ttu-id="e99f6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e99f6-132">CommonParameters</span></span>
<span data-ttu-id="e99f6-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e99f6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e99f6-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e99f6-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e99f6-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e99f6-135">INPUTS</span></span>

### <span data-ttu-id="e99f6-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span><span class="sxs-lookup"><span data-stu-id="e99f6-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="e99f6-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e99f6-137">OUTPUTS</span></span>

### <span data-ttu-id="e99f6-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="e99f6-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="e99f6-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e99f6-139">NOTES</span></span>

## <span data-ttu-id="e99f6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e99f6-140">RELATED LINKS</span></span>
