---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlinstancedatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: 93c4c5c1fa269414b80001f9fd24f1a79c5ed4de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176739"
---
# <span data-ttu-id="85ace-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="85ace-101">Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="85ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ace-102">SYNOPSIS</span></span>
<span data-ttu-id="85ace-103">Ustawia zasady przechowywania krótkich okresów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="85ace-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="85ace-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="85ace-104">SYNTAX</span></span>

### <span data-ttu-id="85ace-105">PolicyByResourceInstanceDatabaseSet (Domyślny)</span><span class="sxs-lookup"><span data-stu-id="85ace-105">PolicyByResourceInstanceDatabaseSet (Default)</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-DeletionDate <DateTime>] [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85ace-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="85ace-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-InputObject] <AzureSqlManagedDatabaseBaseModel>
 [-RetentionDays] <Int32> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85ace-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="85ace-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy [-ResourceId] <String> [-RetentionDays] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ace-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="85ace-108">DESCRIPTION</span></span>
<span data-ttu-id="85ace-109">Polecenie cmdlet **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** pobiera do tej bazy danych zasady przechowywania krótkookresowe.</span><span class="sxs-lookup"><span data-stu-id="85ace-109">The **Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="85ace-110">Zasady to okres przechowywania (w dniach) dla okresów przywracania kopii zapasowych z czasem.</span><span class="sxs-lookup"><span data-stu-id="85ace-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="85ace-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="85ace-111">EXAMPLES</span></span>

### <span data-ttu-id="85ace-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="85ace-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="85ace-113">To polecenie ustawia zasady przechowywania krótkiego terminu dla bazy danych na 35 dni.</span><span class="sxs-lookup"><span data-stu-id="85ace-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="85ace-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="85ace-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourcegroup01 -InstanceName server01 -DatabaseName database01 | Set-AzSqlInstanceDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
ResourceGroupName : resourcegroup01
InstanceName      : instance01
DatabaseName      : database01
DeletionDate      :
RetentionDays     : 35
```

<span data-ttu-id="85ace-115">To polecenie ustawia zasady przechowywania krótkich okresów dla bazy danych na 35 dni za pośrednictwem linii rurowych w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="85ace-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

### <span data-ttu-id="85ace-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="85ace-116">Example 3</span></span>
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

<span data-ttu-id="85ace-117">To polecenie ustawia zasady przechowywania krótkiego terminu dla wszystkich usuniętych baz danych o nazwie DB1 za pośrednictwem linii rurowych w usuniętym obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="85ace-117">This command sets the short term retention policy for all deleted databases named DB1 via piping in a deleted database object.</span></span> <span data-ttu-id="85ace-118">Zwróć uwagę, że okres przechowywania można skrócić tylko w przypadku usuniętych baz danych.</span><span class="sxs-lookup"><span data-stu-id="85ace-118">Note you can only reduce retention period on deleted databases.</span></span>

## <span data-ttu-id="85ace-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85ace-119">PARAMETERS</span></span>

### <span data-ttu-id="85ace-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="85ace-120">-DatabaseName</span></span>
<span data-ttu-id="85ace-121">Nazwa bazy danych Azure SQL Instance Database, dla których mają być pobierane kopie zapasowe.</span><span class="sxs-lookup"><span data-stu-id="85ace-121">The name of the Azure SQL Instance Database to retrieve backups for.</span></span>

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

### <span data-ttu-id="85ace-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ace-122">-DefaultProfile</span></span>
<span data-ttu-id="85ace-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="85ace-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ace-124">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="85ace-124">-DeletionDate</span></span>
<span data-ttu-id="85ace-125">Data usunięcia bazy danych Azure SQL Instance Database do pobierania kopii zapasowych z dokładnością milisekundy (np. 2016-02-23T00:21:22.847Z)</span><span class="sxs-lookup"><span data-stu-id="85ace-125">The deletion date of the Azure SQL Instance Database to retrieve backups for, with millisecond precision (e.g. 2016-02-23T00:21:22.847Z)</span></span>

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

### <span data-ttu-id="85ace-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ace-126">-InputObject</span></span>
<span data-ttu-id="85ace-127">Obiekt bazy danych na żywo lub usunięty w celu uzyskania/ustawienia zasad.</span><span class="sxs-lookup"><span data-stu-id="85ace-127">The live or deleted database object to get/set the policy for.</span></span>

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

### <span data-ttu-id="85ace-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="85ace-128">-InstanceName</span></span>
<span data-ttu-id="85ace-129">Nazwa wystąpienia zarządzanego przez usługę Azure SQL, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="85ace-129">The name of the Azure SQL Managed Instance the database is in.</span></span>

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

### <span data-ttu-id="85ace-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ace-130">-ResourceGroupName</span></span>
<span data-ttu-id="85ace-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="85ace-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="85ace-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85ace-132">-ResourceId</span></span>
<span data-ttu-id="85ace-133">Identyfikator zasobu zasad przechowywania krótkich okresów.</span><span class="sxs-lookup"><span data-stu-id="85ace-133">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="85ace-134">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="85ace-134">-RetentionDays</span></span>
<span data-ttu-id="85ace-135">Dni przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="85ace-135">Days of backup retention.</span></span>

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

### <span data-ttu-id="85ace-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="85ace-136">-Confirm</span></span>
<span data-ttu-id="85ace-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="85ace-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ace-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85ace-138">-WhatIf</span></span>
<span data-ttu-id="85ace-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85ace-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85ace-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="85ace-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ace-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ace-141">CommonParameters</span></span>
<span data-ttu-id="85ace-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85ace-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ace-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85ace-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ace-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="85ace-144">INPUTS</span></span>

### <span data-ttu-id="85ace-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span><span class="sxs-lookup"><span data-stu-id="85ace-145">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseBaseModel</span></span>

### <span data-ttu-id="85ace-146">System.String</span><span class="sxs-lookup"><span data-stu-id="85ace-146">System.String</span></span>

## <span data-ttu-id="85ace-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="85ace-147">OUTPUTS</span></span>

### <span data-ttu-id="85ace-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="85ace-148">Microsoft.Azure.Commands.Sql.ManagedDatabaseBackup.Model.AzureSqlManagedDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="85ace-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="85ace-149">NOTES</span></span>

## <span data-ttu-id="85ace-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="85ace-150">RELATED LINKS</span></span>
