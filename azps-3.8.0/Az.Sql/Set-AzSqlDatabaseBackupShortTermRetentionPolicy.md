---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasebackupshorttermretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseBackupShortTermRetentionPolicy.md
ms.openlocfilehash: d605262a76d27295761ce54d59d092a490da5abc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049925"
---
# <span data-ttu-id="96c5f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="96c5f-101">Set-AzSqlDatabaseBackupShortTermRetentionPolicy</span></span>

## <span data-ttu-id="96c5f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96c5f-102">SYNOPSIS</span></span>
<span data-ttu-id="96c5f-103">Ustawia zasady przechowywania krótkoterminowej kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="96c5f-103">Sets a backup short term retention policy.</span></span>

## <span data-ttu-id="96c5f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96c5f-104">SYNTAX</span></span>

### <span data-ttu-id="96c5f-105">PolicyByResourceServerDatabaseSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96c5f-105">PolicyByResourceServerDatabaseSet (Default)</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> [-ResourceGroupName] <String>
 [-ServerName] <String> [-DatabaseName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c5f-106">PolicyByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="96c5f-106">PolicyByInputObjectSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32>
 -AzureSqlDatabaseObject <AzureSqlDatabaseModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96c5f-107">PolicyByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="96c5f-107">PolicyByResourceIdSet</span></span>
```
Set-AzSqlDatabaseBackupShortTermRetentionPolicy [-RetentionDays] <Int32> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96c5f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="96c5f-108">DESCRIPTION</span></span>
<span data-ttu-id="96c5f-109">Polecenie cmdlet **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** pobiera zasady przechowywania krótkoterminowego zarejestrowane w tej bazie danych.</span><span class="sxs-lookup"><span data-stu-id="96c5f-109">The **Set-AzSqlDatabaseBackupShortTermRetentionPolicy** cmdlet gets the short term retention policy registered to this database.</span></span>
<span data-ttu-id="96c5f-110">Zasada jest okresem przechowywania, w dniach, na potrzeby przywracania kopii zapasowych w czasie.</span><span class="sxs-lookup"><span data-stu-id="96c5f-110">The policy is the retention period, in days, for point-in-time restore backups.</span></span>

## <span data-ttu-id="96c5f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96c5f-111">EXAMPLES</span></span>

### <span data-ttu-id="96c5f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96c5f-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSqlDatabaseBackupShortTermRetentionPolicy -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="96c5f-113">To polecenie ustawia krótkoterminowe zasady przechowywania dla database01 do 35 dni.</span><span class="sxs-lookup"><span data-stu-id="96c5f-113">This command sets the short term retention policy for database01 to 35 days.</span></span>

### <span data-ttu-id="96c5f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="96c5f-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourcegroup01 -ServerName server01 -DatabaseName database01 | Set-AzSqlDatabaseBackupShortTermRetentionPolicy -RetentionDays 35
 ResourceGroupName ServerName  DatabaseName RetentionDays
----------------- ----------  ------------ -------------
resourcegroup01   server01    database01   35
```

<span data-ttu-id="96c5f-115">To polecenie ustawia krótkoterminowe zasady przechowywania dla database01 do 35 dni przez potok w obiekcie bazy danych.</span><span class="sxs-lookup"><span data-stu-id="96c5f-115">This command sets the short term retention policy for database01 to 35 days via piping in a database object.</span></span>

## <span data-ttu-id="96c5f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96c5f-116">PARAMETERS</span></span>

### <span data-ttu-id="96c5f-117">-AzureSqlDatabaseObject</span><span class="sxs-lookup"><span data-stu-id="96c5f-117">-AzureSqlDatabaseObject</span></span>
<span data-ttu-id="96c5f-118">Obiekt bazy danych, dla którego mają zostać pozyskane zasady.</span><span class="sxs-lookup"><span data-stu-id="96c5f-118">The database object to get the policy for.</span></span>

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

### <span data-ttu-id="96c5f-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96c5f-119">-DatabaseName</span></span>
<span data-ttu-id="96c5f-120">Nazwa bazy danych SQL Azure, która ma zostać użyta.</span><span class="sxs-lookup"><span data-stu-id="96c5f-120">The name of the Azure SQL Database to use.</span></span>

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

### <span data-ttu-id="96c5f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96c5f-121">-DefaultProfile</span></span>
<span data-ttu-id="96c5f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96c5f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96c5f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96c5f-123">-ResourceGroupName</span></span>
<span data-ttu-id="96c5f-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96c5f-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="96c5f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96c5f-125">-ResourceId</span></span>
<span data-ttu-id="96c5f-126">Identyfikator zasobu zasad przechowywania w krótkim czasie.</span><span class="sxs-lookup"><span data-stu-id="96c5f-126">The short term retention policy resource Id.</span></span>

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

### <span data-ttu-id="96c5f-127">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="96c5f-127">-RetentionDays</span></span>
<span data-ttu-id="96c5f-128">Ustawienie przechowywania kopii zapasowej w dniach.</span><span class="sxs-lookup"><span data-stu-id="96c5f-128">The backup retention setting, in days.</span></span>

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

### <span data-ttu-id="96c5f-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="96c5f-129">-ServerName</span></span>
<span data-ttu-id="96c5f-130">Nazwa programu Azure SQL Server, w którym znajduje się baza danych.</span><span class="sxs-lookup"><span data-stu-id="96c5f-130">The name of the Azure SQL Server the database is in.</span></span>

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

### <span data-ttu-id="96c5f-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="96c5f-131">-Confirm</span></span>
<span data-ttu-id="96c5f-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96c5f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96c5f-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96c5f-133">-WhatIf</span></span>
<span data-ttu-id="96c5f-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96c5f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96c5f-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="96c5f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96c5f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96c5f-136">CommonParameters</span></span>
<span data-ttu-id="96c5f-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96c5f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96c5f-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96c5f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96c5f-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96c5f-139">INPUTS</span></span>

### <span data-ttu-id="96c5f-140">Microsoft. Azure. Commands. SQL. Database. model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="96c5f-140">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

### <span data-ttu-id="96c5f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="96c5f-141">System.String</span></span>

## <span data-ttu-id="96c5f-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96c5f-142">OUTPUTS</span></span>

### <span data-ttu-id="96c5f-143">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="96c5f-143">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseBackupShortTermRetentionPolicyModel</span></span>

## <span data-ttu-id="96c5f-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96c5f-144">NOTES</span></span>

## <span data-ttu-id="96c5f-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96c5f-145">RELATED LINKS</span></span>
