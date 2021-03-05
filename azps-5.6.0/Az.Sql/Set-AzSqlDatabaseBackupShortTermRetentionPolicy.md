---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: ccdcf55b61b57b54848f3310d7366bb76e0f6805
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994953"
---
# <span data-ttu-id="59907-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="59907-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="59907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59907-102">SYNOPSIS</span></span>
<span data-ttu-id="59907-103">Ustawia zasady przechowywania krótkich okresów kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="59907-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="59907-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59907-104">SYNTAX</span></span>

### <span data-ttu-id="59907-105">PolicyByResourceServerDatabaseSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="59907-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59907-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="59907-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59907-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="59907-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59907-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="59907-108">DESCRIPTION</span></span>
<span data-ttu-id="59907-109">Polecenie **cmdlet Set-AzSqlDatabaseBackupShortTermRetentionPolicy** pobiera do tej bazy danych zasady przechowywania krótkookresowe.</span><span class="sxs-lookup"><span data-stu-id="59907-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="59907-110">Zasady to okres przechowywania (w dniach) dla kopii zapasowych przywracania w momencie.</span><span class="sxs-lookup"><span data-stu-id="59907-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="59907-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59907-111">EXAMPLES</span></span>

### <span data-ttu-id="59907-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59907-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="59907-113">To polecenie ustawia zasady przechowywania krótkiego terminu dla bazy danych na 35 dni.</span><span class="sxs-lookup"><span data-stu-id="59907-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="59907-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59907-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="59907-115">To polecenie ustawia zasady przechowywania krótkich okresów dla bazy danych na 35 dni za pośrednictwem linii rurowych w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="59907-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="59907-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59907-116">PARAMETERS</span></span>

### <span data-ttu-id="59907-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="59907-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="59907-118">Obiekt bazy danych, dla których mają być pobierze się zasady.</span><span class="sxs-lookup"><span data-stu-id="59907-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="59907-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="59907-119">-DatabaseName</span></span>
<span data-ttu-id="59907-120">Nazwa bazy danych Azure SQL Database, która ma być używania.</span><span class="sxs-lookup"><span data-stu-id="59907-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="59907-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59907-121">-DefaultProfile</span></span>
<span data-ttu-id="59907-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59907-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59907-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59907-123">-ResourceGroupName</span></span>
<span data-ttu-id="59907-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59907-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="59907-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59907-125">-ResourceId</span></span>
<span data-ttu-id="59907-126">Identyfikator zasobu zasad przechowywania krótkich okresów.</span><span class="sxs-lookup"><span data-stu-id="59907-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="59907-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="59907-127">-RetentionDays</span></span>
<span data-ttu-id="59907-128">Ustawienie przechowywania kopii zapasowej w dniach.</span><span class="sxs-lookup"><span data-stu-id="59907-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="59907-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="59907-129">-ServerName</span></span>
<span data-ttu-id="59907-130">Nazwa serwera Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="59907-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="59907-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59907-131">-Confirm</span></span>
<span data-ttu-id="59907-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59907-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59907-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59907-133">-WhatIf</span></span>
<span data-ttu-id="59907-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59907-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59907-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="59907-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59907-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59907-136">CommonParameters</span></span>
<span data-ttu-id="59907-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59907-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59907-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59907-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59907-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59907-139">INPUTS</span></span>

### <span data-ttu-id="59907-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="59907-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="59907-141">System.String</span><span class="sxs-lookup"><span data-stu-id="59907-141">System.String</span></span>

## <span data-ttu-id="59907-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59907-142">OUTPUTS</span></span>

### <span data-ttu-id="59907-143">Microsoft.Azure.Commands.sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="59907-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="59907-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59907-144">NOTES</span></span>

## <span data-ttu-id="59907-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59907-145">RELATED LINKS</span></span>
