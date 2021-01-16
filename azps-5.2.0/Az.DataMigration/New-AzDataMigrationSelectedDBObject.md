---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationSelectedDBObject.md
ms.openlocfilehash: 0e4557f44d3219b55edc0bd31464033e9000c772
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350413"
---
# <span data-ttu-id="1fb61-101">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="1fb61-101">New-AzDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="1fb61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fb61-102">SYNOPSIS</span></span>
<span data-ttu-id="1fb61-103">Tworzy obiekt wejściowy bazy danych, który zawiera informacje dotyczące źródłowej i docelowej bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="1fb61-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

## <span data-ttu-id="1fb61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fb61-104">SYNTAX</span></span>

### <span data-ttu-id="1fb61-105">MigrateSqlServerSqlDb (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1fb61-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1fb61-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="1fb61-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1fb61-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1fb61-107">DESCRIPTION</span></span>
<span data-ttu-id="1fb61-108">Polecenie cmdlet New-AzDataMigrationSelectedDB powoduje utworzenie obiektu informacji o bazie danych zawierającego informacje o źródłowej i docelowej bazie danych oraz mapowaniach tabeli do migracji.</span><span class="sxs-lookup"><span data-stu-id="1fb61-108">The New-AzDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="1fb61-109">Tego polecenia cmdlet można użyć jako parametru za pomocą polecenia cmdlet New-AzDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="1fb61-109">This cmdlet can be used as a parameter with the New-AzDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="1fb61-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fb61-110">EXAMPLES</span></span>

### <span data-ttu-id="1fb61-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1fb61-111">Example 1</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```

### <span data-ttu-id="1fb61-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1fb61-112">Example 2</span></span>
```
PS C:\> New-AzDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```

## <span data-ttu-id="1fb61-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fb61-113">PARAMETERS</span></span>

### <span data-ttu-id="1fb61-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="1fb61-114">-BackupFileShare</span></span>
<span data-ttu-id="1fb61-115">Udostępnianie plików, w którym należy wykonać kopię zapasową plików bazy danych serwera źródłowego dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1fb61-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="1fb61-116">To ustawienie umożliwia zastąpienie informacji o udziałach plików każdej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="1fb61-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="1fb61-117">Użyj w pełni kwalifikowanej nazwy domeny dla serwera.</span><span class="sxs-lookup"><span data-stu-id="1fb61-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="1fb61-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fb61-118">-DefaultProfile</span></span>
<span data-ttu-id="1fb61-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1fb61-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fb61-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="1fb61-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="1fb61-121">Ustawianie bazy danych jako ReadOnly przed migracją</span><span class="sxs-lookup"><span data-stu-id="1fb61-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="1fb61-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="1fb61-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="1fb61-123">Ustaw typ migracji na program SQL Server na migrację SQL DB.</span><span class="sxs-lookup"><span data-stu-id="1fb61-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="1fb61-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="1fb61-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="1fb61-125">Ustaw typ migracji na program SQL Server na migrację SQL DB MI.</span><span class="sxs-lookup"><span data-stu-id="1fb61-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="1fb61-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fb61-126">-SourceDatabaseName</span></span>
<span data-ttu-id="1fb61-127">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1fb61-127">The name of the source database.</span></span>

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

### <span data-ttu-id="1fb61-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="1fb61-128">-TableMap</span></span>
<span data-ttu-id="1fb61-129">Mapowanie źródeł na tabele docelowe</span><span class="sxs-lookup"><span data-stu-id="1fb61-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="1fb61-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="1fb61-130">-TargetDatabaseName</span></span>
<span data-ttu-id="1fb61-131">Nazwa docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1fb61-131">The name of the target database.</span></span>

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

### <span data-ttu-id="1fb61-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fb61-132">CommonParameters</span></span>
<span data-ttu-id="1fb61-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fb61-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fb61-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fb61-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fb61-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fb61-135">INPUTS</span></span>

### <span data-ttu-id="1fb61-136">Microsoft. Azure. Management. datamigration. model.</span><span class="sxs-lookup"><span data-stu-id="1fb61-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="1fb61-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fb61-137">OUTPUTS</span></span>

### <span data-ttu-id="1fb61-138">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="1fb61-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="1fb61-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fb61-139">NOTES</span></span>

## <span data-ttu-id="1fb61-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fb61-140">RELATED LINKS</span></span>
