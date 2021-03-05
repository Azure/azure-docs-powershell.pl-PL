---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 4cb97982ed3649502bcf11ce471cef0231ae3058
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967505"
---
# <span data-ttu-id="f8c94-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="f8c94-101">Get-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="f8c94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c94-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c94-103">Pobiera zasady przechowywania kopii zapasowej krótkiego okresu.</span><span class="sxs-lookup"><span data-stu-id="f8c94-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="f8c94-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f8c94-104">SYNTAX</span></span>

### <span data-ttu-id="f8c94-105">PolicyByResourceServerDatabaseSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f8c94-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c94-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f8c94-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -AzureSqlDatabaseObject <AzureSqlDatabaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f8c94-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f8c94-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8c94-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f8c94-108">DESCRIPTION</span></span>
<span data-ttu-id="f8c94-109">Polecenie **cmdlet Get-AzSqlDatabaseBackupShortTermRetentionPolicy** pobiera do tej bazy danych zasady przechowywania krótkookresowe.</span><span class="sxs-lookup"><span data-stu-id="f8c94-109">The **Get-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="f8c94-110">Zasady to okres przechowywania (w dniach) dla kopii zapasowych przywracania w momencie.</span><span class="sxs-lookup"><span data-stu-id="f8c94-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="f8c94-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f8c94-111">EXAMPLES</span></span>

### <span data-ttu-id="f8c94-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f8c94-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="f8c94-113">To polecenie pobiera zasady przechowywania dotyczące krótkich okresów dla bazy danych01.</span><span class="sxs-lookup"><span data-stu-id="f8c94-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="f8c94-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f8c94-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Get-AzSqlDatabaseBackupShortTermRetentionPolicy

ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="f8c94-115">To polecenie pobiera zasady przechowywania krótkiego terminu dla bazy danych01 za pośrednictwem linii rurowych w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f8c94-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

## <span data-ttu-id="f8c94-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8c94-116">PARAMETERS</span></span>

### <span data-ttu-id="f8c94-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="f8c94-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="f8c94-118">Obiekt bazy danych, dla których mają być pobierze się zasady.</span><span class="sxs-lookup"><span data-stu-id="f8c94-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="f8c94-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8c94-119">-DatabaseName</span></span>
<span data-ttu-id="f8c94-120">Nazwa bazy danych Azure SQL Database, która ma być używania.</span><span class="sxs-lookup"><span data-stu-id="f8c94-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="f8c94-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c94-121">-DefaultProfile</span></span>
<span data-ttu-id="f8c94-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f8c94-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c94-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c94-123">-ResourceGroupName</span></span>
<span data-ttu-id="f8c94-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f8c94-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="f8c94-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8c94-125">-ResourceId</span></span>
<span data-ttu-id="f8c94-126">Identyfikator zasobu zasad przechowywania krótkich okresów.</span><span class="sxs-lookup"><span data-stu-id="f8c94-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="f8c94-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8c94-127">-ServerName</span></span>
<span data-ttu-id="f8c94-128">Nazwa serwera Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="f8c94-128">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="f8c94-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c94-129">CommonParameters</span></span>
<span data-ttu-id="f8c94-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8c94-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c94-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8c94-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c94-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8c94-132">INPUTS</span></span>

### <span data-ttu-id="f8c94-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="f8c94-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="f8c94-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f8c94-134">System.String</span></span>

## <span data-ttu-id="f8c94-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f8c94-135">OUTPUTS</span></span>

### <span data-ttu-id="f8c94-136">Microsoft.Azure.Commands.sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f8c94-136">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="f8c94-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f8c94-137">NOTES</span></span>

## <span data-ttu-id="f8c94-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f8c94-138">RELATED LINKS</span></span>
