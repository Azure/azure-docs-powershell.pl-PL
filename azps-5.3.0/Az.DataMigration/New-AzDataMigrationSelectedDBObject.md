---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377652"
---
# <span data-ttu-id="a2ecd-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="a2ecd-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="a2ecd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ecd-103">Tworzy obiekt wejściowy bazy danych, który zawiera informacje dotyczące źródłowej i docelowej bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="a2ecd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2ecd-104">SYNTAX</span></span>

### <span data-ttu-id="a2ecd-105">MigrateSqlServerSqlDb (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a2ecd-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2ecd-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="a2ecd-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2ecd-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a2ecd-107">DESCRIPTION</span></span>
<span data-ttu-id="a2ecd-108">Polecenie cmdlet New-AzDataMigrationSelectedDB powoduje utworzenie obiektu informacji o bazie danych zawierającego informacje o źródłowej i docelowej bazie danych oraz mapowaniach tabeli do migracji.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="a2ecd-109">Tego polecenia cmdlet można użyć jako parametru za pomocą polecenia cmdlet New-AzDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="a2ecd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2ecd-110">EXAMPLES</span></span>

### <span data-ttu-id="a2ecd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a2ecd-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="a2ecd-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a2ecd-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="a2ecd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2ecd-113">PARAMETERS</span></span>

### <span data-ttu-id="a2ecd-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="a2ecd-114">-BackupFileShare</span></span>
<span data-ttu-id="a2ecd-115">Udostępnianie plików, w którym należy wykonać kopię zapasową plików bazy danych serwera źródłowego dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="a2ecd-116">To ustawienie umożliwia zastąpienie informacji o udziałach plików każdej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="a2ecd-117">Użyj w pełni kwalifikowanej nazwy domeny dla serwera.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="a2ecd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ecd-118">-DefaultProfile</span></span>
<span data-ttu-id="a2ecd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2ecd-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="a2ecd-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="a2ecd-121">Ustawianie bazy danych jako ReadOnly przed migracją</span><span class="sxs-lookup"><span data-stu-id="a2ecd-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="a2ecd-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="a2ecd-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="a2ecd-123">Ustaw typ migracji na program SQL Server na migrację SQL DB.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="a2ecd-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="a2ecd-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="a2ecd-125">Ustaw typ migracji na program SQL Server na migrację SQL DB MI.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="a2ecd-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2ecd-126">-SourceDatabaseName</span></span>
<span data-ttu-id="a2ecd-127">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-127">The name of the source database.</span></span>

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

### <span data-ttu-id="a2ecd-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="a2ecd-128">-TableMap</span></span>
<span data-ttu-id="a2ecd-129">Mapowanie źródeł na tabele docelowe</span><span class="sxs-lookup"><span data-stu-id="a2ecd-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="a2ecd-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="a2ecd-130">-TargetDatabaseName</span></span>
<span data-ttu-id="a2ecd-131">Nazwa docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-131">The name of the target database.</span></span>

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

### <span data-ttu-id="a2ecd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ecd-132">CommonParameters</span></span>
<span data-ttu-id="a2ecd-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ecd-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ecd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ecd-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2ecd-135">INPUTS</span></span>

### <span data-ttu-id="a2ecd-136">Microsoft. Azure. Management. datamigration. model.</span><span class="sxs-lookup"><span data-stu-id="a2ecd-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="a2ecd-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2ecd-137">OUTPUTS</span></span>

### <span data-ttu-id="a2ecd-138">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="a2ecd-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="a2ecd-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2ecd-139">NOTES</span></span>

## <span data-ttu-id="a2ecd-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2ecd-140">RELATED LINKS</span></span>
