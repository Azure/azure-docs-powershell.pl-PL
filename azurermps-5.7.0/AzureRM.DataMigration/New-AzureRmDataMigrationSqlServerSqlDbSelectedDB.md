---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationsqlserversqldbselecteddb
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationSqlServerSqlDbSelectedDB.md
ms.openlocfilehash: 1be43b5d08011a71ec093df2f93c63dd04c6004d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544371"
---
# <span data-ttu-id="2c672-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span><span class="sxs-lookup"><span data-stu-id="2c672-101">New-AzureRmDataMigrationSqlServerSqlDbSelectedDB</span></span>

## <span data-ttu-id="2c672-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c672-102">SYNOPSIS</span></span>
<span data-ttu-id="2c672-103">Tworzy obiekt MigrateSqlServerSqlDbDatabaseInput, który zawiera informacje dotyczące źródłowej i docelowej bazy danych do migracji.</span><span class="sxs-lookup"><span data-stu-id="2c672-103">Creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c672-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c672-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationSqlServerSqlDbSelectedDB [-Id <String>] [-Name <String>] [-TargetDatabaseName <String>]
 [-MakeSourceDbReadOnly] [-TableMap <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="2c672-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2c672-105">DESCRIPTION</span></span>
<span data-ttu-id="2c672-106">Polecenie cmdlet New-AzureRmDataMigrationSqlServerSqlDbSelectedDB powoduje utworzenie obiektu MigrateSqlServerSqlDbDatabaseInput zawierającego informacje o źródłowej i docelowej bazie danych oraz mapowaniach tabeli do migracji.</span><span class="sxs-lookup"><span data-stu-id="2c672-106">The New-AzureRmDataMigrationSqlServerSqlDbSelectedDB cmdlet creates a MigrateSqlServerSqlDbDatabaseInput object that contains information about source and target databases, as well as the table mappings, for migration.</span></span> <span data-ttu-id="2c672-107">Tego polecenia cmdlet można użyć jako parametru za pomocą polecenia cmdlet New-AzureRmDataMigrationTask.</span><span class="sxs-lookup"><span data-stu-id="2c672-107">This cmdlet can be used as a parameter with the New-AzureRmDataMigrationTask cmdlet.</span></span>

## <span data-ttu-id="2c672-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c672-108">EXAMPLES</span></span>

### <span data-ttu-id="2c672-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2c672-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationSqlServerSqlDbSelectedDB  -Name AdventuerWorks2016 -TargetDatabaseName AdventureWorks2016
 -MakeSourceDbReadOnly -TableMap $tableMap
```

<span data-ttu-id="2c672-110">Powyższy przykład tworzy obiekt MigrateSqlServerSqlDbDatabaseInput do migrowania bazy danych **AdventureWorks2016** do bazy danych SQL Azure o tej samej nazwie.</span><span class="sxs-lookup"><span data-stu-id="2c672-110">The above example creates MigrateSqlServerSqlDbDatabaseInput object for migrating the **AdventureWorks2016** database to a SQL Azure database with the same name.</span></span>

## <span data-ttu-id="2c672-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c672-111">PARAMETERS</span></span>

### <span data-ttu-id="2c672-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c672-112">-Confirm</span></span>
<span data-ttu-id="2c672-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c672-113">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c672-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c672-114">-DefaultProfile</span></span>
<span data-ttu-id="2c672-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c672-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c672-116">-MakeSourceDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="2c672-116">-MakeSourceDbReadOnly</span></span>
<span data-ttu-id="2c672-117">Ustawianie bazy danych jako ReadOnly przed migracją</span><span class="sxs-lookup"><span data-stu-id="2c672-117">Set Database to readonly before migration</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c672-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c672-118">-Name</span></span>
<span data-ttu-id="2c672-119">Nazwa bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c672-119">The name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c672-120">-TableMap</span><span class="sxs-lookup"><span data-stu-id="2c672-120">-TableMap</span></span>
<span data-ttu-id="2c672-121">Mapowanie źródeł na tabele docelowe</span><span class="sxs-lookup"><span data-stu-id="2c672-121">mapping of source to target tables</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c672-122">-TargetDatabaseName</span><span class="sxs-lookup"><span data-stu-id="2c672-122">-TargetDatabaseName</span></span>
<span data-ttu-id="2c672-123">Nazwa docelowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c672-123">The name of the target Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="2c672-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c672-124">INPUTS</span></span>

### <span data-ttu-id="2c672-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="2c672-125">None</span></span>


## <span data-ttu-id="2c672-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c672-126">OUTPUTS</span></span>

### <span data-ttu-id="2c672-127">Microsoft. Azure. Management. datamigration. MODELES. MigrateSqlServerSqlDbDatabaseInput</span><span class="sxs-lookup"><span data-stu-id="2c672-127">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>


## <span data-ttu-id="2c672-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c672-128">NOTES</span></span>

## <span data-ttu-id="2c672-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c672-129">RELATED LINKS</span></span>


