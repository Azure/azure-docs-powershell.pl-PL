---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 94efd633a64bd1437206a00b83d86cf09fc56036
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708006"
---
# <span data-ttu-id="a4bb1-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="a4bb1-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="a4bb1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4bb1-102">SYNOPSIS</span></span>
<span data-ttu-id="a4bb1-103">Pobiera zasady przechowywania krótkoterminowych kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="a4bb1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4bb1-104">SYNTAX</span></span>

### <span data-ttu-id="a4bb1-105">PolicyByResourceServerDatabaseSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4bb1-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4bb1-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a4bb1-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4bb1-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a4bb1-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4bb1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4bb1-108">DESCRIPTION</span></span>
<span data-ttu-id="a4bb1-109">Polecenie cmdlet **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** pobiera krótkoterminowe zasady przechowywania zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="a4bb1-110">Zasada jest okresem przechowywania, w dniach, na potrzeby przywracania kopii zapasowych w czasie.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="a4bb1-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4bb1-111">EXAMPLES</span></span>

### <span data-ttu-id="a4bb1-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4bb1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="a4bb1-113">To polecenie pobiera krótkoterminowe zasady przechowywania dla database01.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="a4bb1-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4bb1-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="a4bb1-115">To polecenie pobiera krótkoterminowe zasady przechowywania dla database01 za pomocą połączeń rurowych w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="a4bb1-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4bb1-116">PARAMETERS</span></span>

### <span data-ttu-id="a4bb1-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="a4bb1-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="a4bb1-118">Obiekt bazy danych, dla którego mają zostać pozyskane zasady.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-118">The database object to get the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlDatabase

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb1-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a4bb1-119">-DatabaseName</span></span>
<span data-ttu-id="a4bb1-120">Nazwa bazy danych SQL Azure, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-120">The name of the Azure SQL Database to use.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4bb1-121">-DefaultProfile</span></span>
<span data-ttu-id="a4bb1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4bb1-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4bb1-123">-ResourceGroupName</span></span>
<span data-ttu-id="a4bb1-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb1-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a4bb1-125">-ResourceId</span></span>
<span data-ttu-id="a4bb1-126">Identyfikator zasobu zasad przechowywania w krótkim czasie.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-126">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb1-127">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a4bb1-127">-ServerName</span></span>
<span data-ttu-id="a4bb1-128">Nazwa programu Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-128">The name of the Azure SQL Server the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceServerDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4bb1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4bb1-129">CommonParameters</span></span>
<span data-ttu-id="a4bb1-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4bb1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4bb1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4bb1-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4bb1-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4bb1-132">INPUTS</span></span>

### <span data-ttu-id="a4bb1-133">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a4bb1-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="a4bb1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a4bb1-134">System.String</span></span>

## <span data-ttu-id="a4bb1-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4bb1-135">OUTPUTS</span></span>

### <span data-ttu-id="a4bb1-136">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a4bb1-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="a4bb1-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4bb1-137">NOTES</span></span>

## <span data-ttu-id="a4bb1-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4bb1-138">RELATED LINKS</span></span>
