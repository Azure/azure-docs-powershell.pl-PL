---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332053"
---
# <span data-ttu-id="802f7-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="802f7-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="802f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="802f7-102">SYNOPSIS</span></span>
<span data-ttu-id="802f7-103">Ustawia zasady przechowywania krótkoterminowej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="802f7-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="802f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="802f7-104">SYNTAX</span></span>

### <span data-ttu-id="802f7-105">PolicyByResourceInstanceDatabaseSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="802f7-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="802f7-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="802f7-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="802f7-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="802f7-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="802f7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="802f7-108">DESCRIPTION</span></span>
<span data-ttu-id="802f7-109">Polecenie cmdlet **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** pobiera zasady przechowywania krótkoterminowego zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="802f7-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="802f7-110">Zasada jest okresem przechowywania, w dniach, na potrzeby przywracania kopii zapasowych w czasie.</span><span class="sxs-lookup"><span data-stu-id="802f7-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="802f7-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="802f7-111">EXAMPLES</span></span>

### <span data-ttu-id="802f7-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="802f7-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="802f7-113">To polecenie ustawia krótkoterminowe zasady przechowywania dla database01 do 35 dni.</span><span class="sxs-lookup"><span data-stu-id="802f7-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="802f7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="802f7-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="802f7-115">To polecenie ustawia krótkoterminowe zasady przechowywania dla database01 do 35 dni przez potok w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="802f7-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="802f7-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="802f7-116">Example 3</span></span>
```powershell
PS C:\> Set-AzSqlDeletedInstanceDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -InstanceName "ContosoServer" -DatabaseName "DB1" | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 8
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-03 12:00:17 AM
RetentionDays     : 8

ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      : 2019-03-02 11:00:16 PM
RetentionDays     : 8
```

<span data-ttu-id="802f7-117">To polecenie ustawia krótkoterminowe zasady przechowywania dla wszystkich usuniętych baz danych o nazwie DB1 za pomocą połączeń rurowych w usuniętym obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="802f7-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="802f7-118">Uwaga w usuniętych bazach danych można tylko skrócić okres przechowywania.</span><span class="sxs-lookup"><span data-stu-id="802f7-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="802f7-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="802f7-119">PARAMETERS</span></span>

### <span data-ttu-id="802f7-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="802f7-120">-DatabaseName</span></span>
<span data-ttu-id="802f7-121">Nazwa bazy danych wystąpienia SQL Azure, do której mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="802f7-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="802f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="802f7-122">-DefaultProfile</span></span>
<span data-ttu-id="802f7-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="802f7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="802f7-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="802f7-124">-DeletionDate</span></span>
<span data-ttu-id="802f7-125">Data usunięcia bazy danych wystąpienia SQL Azure w celu pobrania kopii zapasowych z dokładnością do milisekund (na przykład 2016-02-23T00:21:22.847 Z)</span><span class="sxs-lookup"><span data-stu-id="802f7-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="802f7-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="802f7-126">-InputObject</span></span>
<span data-ttu-id="802f7-127">Obiekt na żywo lub usunięty, aby uzyskać/ustawić zasady.</span><span class="sxs-lookup"><span data-stu-id="802f7-127">The live or deleted database object to get/set the policy for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel
Parameter Sets: PolicyByInputObjectSet
Aliases: AzureSqlInstanceDatabase, AzureInstanceDatabaseObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="802f7-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="802f7-128">-InstanceName</span></span>
<span data-ttu-id="802f7-129">Nazwa wystąpienia zarządzanego w usłudze Azure SQL, w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="802f7-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="802f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="802f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="802f7-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="802f7-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="802f7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="802f7-132">-ResourceId</span></span>
<span data-ttu-id="802f7-133">Identyfikator zasobu zasad przechowywania w krótkim czasie.</span><span class="sxs-lookup"><span data-stu-id="802f7-133">The short term retention policy resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="802f7-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="802f7-134">-RetentionDays</span></span>
<span data-ttu-id="802f7-135">Dni przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="802f7-135">Days of backup retention.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802f7-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="802f7-136">-Confirm</span></span>
<span data-ttu-id="802f7-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="802f7-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802f7-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="802f7-138">-WhatIf</span></span>
<span data-ttu-id="802f7-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="802f7-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="802f7-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="802f7-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="802f7-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="802f7-141">CommonParameters</span></span>
<span data-ttu-id="802f7-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="802f7-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="802f7-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="802f7-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="802f7-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="802f7-144">INPUTS</span></span>

### <span data-ttu-id="802f7-145">Microsoft. Azure. Commands. SQL. ManagedDatabase. model. AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="802f7-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="802f7-146">System. String</span><span class="sxs-lookup"><span data-stu-id="802f7-146">System.String</span></span>

## <span data-ttu-id="802f7-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="802f7-147">OUTPUTS</span></span>

### <span data-ttu-id="802f7-148">Microsoft. Azure. Commands. SQL. ManagedDatabaseBackup. model. AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="802f7-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="802f7-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="802f7-149">NOTES</span></span>

## <span data-ttu-id="802f7-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="802f7-150">RELATED LINKS</span></span>
