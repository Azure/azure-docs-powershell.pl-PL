---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationSelectedDBObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSelectedDBObject.md
ms.openlocfilehash: d8303dadef33944addf63323e57727ef85acce6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716580"
---
# <span data-ttu-id="8cfc3-101">New-AzureRmDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="8cfc3-101">New-AzureRmDataMigrationSelectedDBObject</span></span>

## <span data-ttu-id="8cfc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cfc3-102">SYNOPSIS</span></span>
<span data-ttu-id="8cfc3-103">Tworzy obiekt wejściowy bazy danych, który zawiera informacje dotyczące źródłowej i docelowej bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-103">Creates a database input object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cfc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cfc3-104">SYNTAX</span></span>

### <span data-ttu-id="8cfc3-105">MigrateSqlServerSqlDb (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cfc3-105">MigrateSqlServerSqlDb (Default)</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDb] [-MakeSourceDbReadOnly]
 [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cfc3-106">MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="8cfc3-106">MigrateSqlServerSqlDbMi</span></span>
```
New-AzureRmDataMigrationSelectedDBObject -SourceDatabaseName <String> -TargetDatabaseName <String>
 [-MigrateSqlServerSqlDbMi] [-BackupFileShare <FileShare>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8cfc3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8cfc3-107">DESCRIPTION</span></span>
<span data-ttu-id="8cfc3-108">Polecenie cmdlet New-AzureRmDataMigrationSelectedDB powoduje utworzenie obiektu informacji o bazie danych zawierającego informacje o źródłowej i docelowej bazie danych oraz mapowaniach tabeli do migracji.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-108">The New-AzureRmDataMigrationSelectedDB cmdlet creates a database info object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="8cfc3-109">Tego polecenia cmdlet można użyć jako parametru za pomocą polecenia cmdlet New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-109">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="8cfc3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cfc3-110">EXAMPLES</span></span>

### <span data-ttu-id="8cfc3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8cfc3-111">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDb -Name "HR" -TargetDatabaseName "HR_PSTEST" -TableMap $tableMap

Name TargetDatabaseName MakeSourceDbReadOnly TableMap
---- ------------------ -------------------- --------
HR   HR_PSTEST                         False {[HR.COUNTRIES, HR.COUNTRIES]}
```


### <span data-ttu-id="8cfc3-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8cfc3-112">Example 2</span></span>
```
PS C:\> New-AzureRmDataMigrationSelectedDB -MigrateSqlServerSqlDbMi -Name "HR" -TargetDatabaseName "HR_PSTEST" -BackupFileShare $backupFileShare

Name RestoreDatabaseName BackupFileShare
---- ------------------- ---------------
HR   HRTest              Microsoft.Azure.Management.DataMigration.Models.FileShare
```


## <span data-ttu-id="8cfc3-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cfc3-113">PARAMETERS</span></span>

### <span data-ttu-id="8cfc3-114">-BackupFileShare</span><span class="sxs-lookup"><span data-stu-id="8cfc3-114">-BackupFileShare</span></span>
<span data-ttu-id="8cfc3-115">Udostępnianie plików, w którym należy wykonać kopię zapasową plików bazy danych serwera źródłowego dla tej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-115">File share where the source server database files for this database should be backed up.</span></span>
<span data-ttu-id="8cfc3-116">To ustawienie umożliwia zastąpienie informacji o udziałach plików każdej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-116">Use this setting to override file share information for each database.</span></span>
<span data-ttu-id="8cfc3-117">Użyj w pełni kwalifikowanej nazwy domeny dla serwera.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-117">Use fully qualified domain name for the server.</span></span>

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

### <span data-ttu-id="8cfc3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cfc3-118">-DefaultProfile</span></span>
<span data-ttu-id="8cfc3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cfc3-120">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="8cfc3-120">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="8cfc3-121">Ustawianie bazy danych jako ReadOnly przed migracją</span><span class="sxs-lookup"><span data-stu-id="8cfc3-121">Set Database to readonly before migration</span></span>

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

### <span data-ttu-id="8cfc3-122">-MigrateSqlServerSqlDb</span><span class="sxs-lookup"><span data-stu-id="8cfc3-122">-MigrateSqlServerSqlDb</span></span>
<span data-ttu-id="8cfc3-123">Ustaw typ migracji na program SQL Server na migrację SQL DB.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-123">Set migration type to SQL Server to SQL DB Migration.</span></span>

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

### <span data-ttu-id="8cfc3-124">-MigrateSqlServerSqlDbMi</span><span class="sxs-lookup"><span data-stu-id="8cfc3-124">-MigrateSqlServerSqlDbMi</span></span>
<span data-ttu-id="8cfc3-125">Ustaw typ migracji na program SQL Server na migrację SQL DB MI.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-125">Set migration type to SQL Server to SQL DB MI Migration.</span></span>

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

### <span data-ttu-id="8cfc3-126">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8cfc3-126">-SourceDatabaseName</span></span>
<span data-ttu-id="8cfc3-127">Nazwa źródłowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-127">The name of the source database.</span></span>

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

### <span data-ttu-id="8cfc3-128">-TableMap</span><span class="sxs-lookup"><span data-stu-id="8cfc3-128">-TableMap</span></span>
<span data-ttu-id="8cfc3-129">Mapowanie źródeł na tabele docelowe</span><span class="sxs-lookup"><span data-stu-id="8cfc3-129">mapping of source to target tables</span></span>

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

### <span data-ttu-id="8cfc3-130">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="8cfc3-130">-TargetDatabaseName</span></span>
<span data-ttu-id="8cfc3-131">Nazwa docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-131">The name of the target database.</span></span>

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

### <span data-ttu-id="8cfc3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cfc3-132">CommonParameters</span></span>
<span data-ttu-id="8cfc3-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cfc3-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cfc3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cfc3-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cfc3-135">INPUTS</span></span>

### <span data-ttu-id="8cfc3-136">Microsoft. Azure. Management. datamigration. model.</span><span class="sxs-lookup"><span data-stu-id="8cfc3-136">Microsoft.Azure.Management.DataMigration.Models.FileShare</span></span>

## <span data-ttu-id="8cfc3-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cfc3-137">OUTPUTS</span></span>

### <span data-ttu-id="8cfc3-138">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="8cfc3-138">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="8cfc3-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cfc3-139">NOTES</span></span>

## <span data-ttu-id="8cfc3-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cfc3-140">RELATED LINKS</span></span>
