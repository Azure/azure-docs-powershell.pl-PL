---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 3666fd9c790f5445f83c3a068e7423b64a172c5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053244"
---
# <span data-ttu-id="22df3-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="22df3-101">Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="22df3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22df3-102">SYNOPSIS</span></span>
<span data-ttu-id="22df3-103">Pobiera zasady przechowywania krótkoterminowych kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="22df3-103">Gets a backup short term retention policy.</span></span>

## <span data-ttu-id="22df3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22df3-104">SYNTAX</span></span>

### <span data-ttu-id="22df3-105">PolicyByResourceInstanceDatabaseSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22df3-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22df3-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="22df3-106">PolicyByInputObjectSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -InputObject <AzureSqlManagedDatabaseBaseModel>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22df3-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="22df3-107">PolicyByResourceIdSet</span></span>
```
Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22df3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="22df3-108">DESCRIPTION</span></span>
<span data-ttu-id="22df3-109">Polecenie cmdlet **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** pobiera krótkoterminowe zasady przechowywania zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="22df3-109">The **Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="22df3-110">Zasada jest okresem przechowywania, w dniach, na potrzeby przywracania kopii zapasowych w czasie.</span><span class="sxs-lookup"><span data-stu-id="22df3-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="22df3-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22df3-111">EXAMPLES</span></span>

### <span data-ttu-id="22df3-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22df3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="22df3-113">To polecenie pobiera krótkoterminowe zasady przechowywania dla database01.</span><span class="sxs-lookup"><span data-stu-id="22df3-113">This command gets the short term retention policy for database01.</span></span>

### <span data-ttu-id="22df3-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="22df3-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName instance01 -DatabaseName database01 | Get-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 7
```

<span data-ttu-id="22df3-115">To polecenie pobiera krótkoterminowe zasady przechowywania dla database01 za pomocą połączeń rurowych w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="22df3-115">This command gets the short term retention policy for database01 via piping in a database object.</span></span>

### <span data-ttu-id="22df3-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="22df3-116">Example 3</span></span>
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

<span data-ttu-id="22df3-117">To polecenie pobiera krótkoterminowe zasady przechowywania dla wszystkich usuniętych baz danych o nazwie database01 za pomocą połączeń rurowych w usuniętym obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="22df3-117">This command gets the short term retention policy for all deleted databases named database01 via piping in a deleted database object.</span></span>

## <span data-ttu-id="22df3-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22df3-118">PARAMETERS</span></span>

### <span data-ttu-id="22df3-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22df3-119">-DatabaseName</span></span>
<span data-ttu-id="22df3-120">Nazwa bazy danych wystąpienia SQL Azure, do której mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="22df3-120">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="22df3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22df3-121">-DefaultProfile</span></span>
<span data-ttu-id="22df3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22df3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22df3-123">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="22df3-123">-DeletionDate</span></span>
<span data-ttu-id="22df3-124">Data usunięcia bazy danych wystąpienia SQL Azure w celu pobrania kopii zapasowych z dokładnością do milisekund (na przykład 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="22df3-124">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="22df3-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="22df3-125">-InputObject</span></span>
<span data-ttu-id="22df3-126">Obiekt na żywo lub usunięty, aby uzyskać/ustawić zasady.</span><span class="sxs-lookup"><span data-stu-id="22df3-126">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="22df3-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="22df3-127">-InstanceName</span></span>
<span data-ttu-id="22df3-128">Nazwa wystąpienia zarządzanego w usłudze Azure SQL, w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="22df3-128">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="22df3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22df3-129">-ResourceGroupName</span></span>
<span data-ttu-id="22df3-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22df3-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="22df3-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22df3-131">-ResourceId</span></span>
<span data-ttu-id="22df3-132">Identyfikator zasobu zasad przechowywania w krótkim czasie.</span><span class="sxs-lookup"><span data-stu-id="22df3-132">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="22df3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22df3-133">CommonParameters</span></span>
<span data-ttu-id="22df3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22df3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22df3-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22df3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22df3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22df3-136">INPUTS</span></span>

### <span data-ttu-id="22df3-137">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="22df3-137">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="22df3-138">System. String</span><span class="sxs-lookup"><span data-stu-id="22df3-138">System.String</span></span>

## <span data-ttu-id="22df3-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22df3-139">OUTPUTS</span></span>

### <span data-ttu-id="22df3-140">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="22df3-140">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="22df3-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22df3-141">NOTES</span></span>

## <span data-ttu-id="22df3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22df3-142">RELATED LINKS</span></span>
