---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198570"
---
# <span data-ttu-id="ae4b6-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="ae4b6-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="ae4b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae4b6-102">SYNOPSIS</span></span>
<span data-ttu-id="ae4b6-103">Otrzymuje zasady przechowywania kopii zapasowej przez krótki okres.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="ae4b6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ae4b6-104">SYNTAX</span></span>

### <span data-ttu-id="ae4b6-105">PolicyByResourceInstanceDatabaseSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ae4b6-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae4b6-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ae4b6-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae4b6-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ae4b6-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae4b6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ae4b6-108">DESCRIPTION</span></span>
<span data-ttu-id="ae4b6-109">Polecenie **cmdlet Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** pobiera zasady przechowywania krótkookresowe zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="ae4b6-110">Zasady to okres przechowywania (w dniach) dla kopii zapasowych przywracania w momencie.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="ae4b6-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ae4b6-111">EXAMPLES</span></span>

### <span data-ttu-id="ae4b6-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ae4b6-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="ae4b6-113">To polecenie pobiera zasady przechowywania krótkiego terminu dla bazy danych01.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="ae4b6-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ae4b6-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="ae4b6-115">To polecenie pobiera zasady przechowywania krótkiego terminu dla bazy danych01 za pośrednictwem linii rurowych w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="ae4b6-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ae4b6-116">Example 3</span></span>
```powershell
PS C:\> Get-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 7

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 7
```

<span data-ttu-id="ae4b6-117">To polecenie pobiera zasady przechowywania krótkiego terminu dla wszystkich usuniętych baz danych o nazwie database01 za pośrednictwem linii rurowych w usuniętym obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="ae4b6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae4b6-118">PARAMETERS</span></span>

### <span data-ttu-id="ae4b6-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae4b6-119">-DatabaseName</span></span>
<span data-ttu-id="ae4b6-120">Nazwa bazy danych Azure SQL Instance Database, dla których mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae4b6-121">-DefaultProfile</span></span>
<span data-ttu-id="ae4b6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae4b6-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="ae4b6-123">-DeletionDate</span></span>
<span data-ttu-id="ae4b6-124">Data usunięcia bazy danych Azure SQL Instance Database do pobierania kopii zapasowych z dokładnością milisekundy (np. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="ae4b6-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4b6-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae4b6-125">-InputObject</span></span>
<span data-ttu-id="ae4b6-126">Obiekt bazy danych na żywo lub usunięty w celu uzyskania/ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-126">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae4b6-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="ae4b6-127">-InstanceName</span></span>
<span data-ttu-id="ae4b6-128">Nazwa wystąpienia zarządzanego przez usługę Azure SQL, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae4b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="ae4b6-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceInstanceDatabaseSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae4b6-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae4b6-131">-ResourceId</span></span>
<span data-ttu-id="ae4b6-132">Identyfikator zasobu zasad przechowywania krótkich okresów.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="ae4b6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae4b6-133">CommonParameters</span></span>
<span data-ttu-id="ae4b6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae4b6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae4b6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae4b6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae4b6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae4b6-136">INPUTS</span></span>

### <span data-ttu-id="ae4b6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="ae4b6-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="ae4b6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ae4b6-138">System.String</span></span>

## <span data-ttu-id="ae4b6-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae4b6-139">OUTPUTS</span></span>

### <span data-ttu-id="ae4b6-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="ae4b6-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="ae4b6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ae4b6-141">NOTES</span></span>

## <span data-ttu-id="ae4b6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae4b6-142">RELATED LINKS</span></span>
