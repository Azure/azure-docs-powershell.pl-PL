---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 07f6e9b01e3def2dfe7cc88602b9643344ff3c4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887058"
---
# <span data-ttu-id="19bab-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="19bab-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="19bab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19bab-102">SYNOPSIS</span></span>
<span data-ttu-id="19bab-103">Pobiera kopię zapasową bazy danych w postaci geograficznej.</span><span class="sxs-lookup"><span data-stu-id="19bab-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="19bab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19bab-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19bab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="19bab-105">DESCRIPTION</span></span>
<span data-ttu-id="19bab-106">Polecenie cmdlet **Get-AzSqlDatabaseGeoBackup** pobiera określoną geograficzną kopię zapasową bazy danych SQL lub wszystkie dostępne zapasowe kopie lustrzane na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="19bab-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="19bab-107">Kopia zapasowa miejsca geograficznego jest to zasób restorable, który używa plików danych z osobnej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="19bab-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="19bab-108">Za pomocą Geo-Restore możesz przywrócić kopię zapasową geograficznej w przypadku awarii regionalnej w celu odzyskania bazy danych do nowego regionu.</span><span class="sxs-lookup"><span data-stu-id="19bab-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="19bab-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="19bab-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="19bab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19bab-110">EXAMPLES</span></span>

### <span data-ttu-id="19bab-111">Przykład 1: pobieranie wszystkich rezerwowych kopii zapasowych na serwerze</span><span class="sxs-lookup"><span data-stu-id="19bab-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="19bab-112">To polecenie pobiera wszystkie dostępne zapasowe kopie lustrzane na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="19bab-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="19bab-113">Przykład 2: uzyskiwanie określonej geograficznie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="19bab-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="19bab-114">To polecenie uzyskuje kopię zapasową bazy danych w postaci Geo-rezerwowej o nazwie ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="19bab-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="19bab-115">Przykład 3: pobieranie wszystkich rezerwowych kopii zapasowych na serwerze przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="19bab-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="19bab-116">To polecenie pobiera wszystkie dostępne zapasowe kopie lustrzane na określonym serwerze, które zaczynają się od "contoso".</span><span class="sxs-lookup"><span data-stu-id="19bab-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="19bab-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19bab-117">PARAMETERS</span></span>

### <span data-ttu-id="19bab-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="19bab-118">-DatabaseName</span></span>
<span data-ttu-id="19bab-119">Określa nazwę bazy danych, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="19bab-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="19bab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19bab-120">-DefaultProfile</span></span>
<span data-ttu-id="19bab-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="19bab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19bab-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19bab-122">-ResourceGroupName</span></span>
<span data-ttu-id="19bab-123">Określa nazwę grupy zasobów, do której jest przypisany serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="19bab-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bab-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="19bab-124">-ServerName</span></span>
<span data-ttu-id="19bab-125">Określa nazwę serwera obsługującego kopię zapasową do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="19bab-125">Specifies the name of the server that hosts the backup to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19bab-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19bab-126">-Confirm</span></span>
<span data-ttu-id="19bab-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19bab-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bab-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19bab-128">-WhatIf</span></span>
<span data-ttu-id="19bab-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19bab-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19bab-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="19bab-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19bab-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19bab-131">CommonParameters</span></span>
<span data-ttu-id="19bab-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19bab-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19bab-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19bab-133">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19bab-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19bab-134">INPUTS</span></span>

### <span data-ttu-id="19bab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="19bab-135">System.String</span></span>

## <span data-ttu-id="19bab-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19bab-136">OUTPUTS</span></span>

### <span data-ttu-id="19bab-137">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="19bab-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="19bab-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19bab-138">NOTES</span></span>

## <span data-ttu-id="19bab-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19bab-139">RELATED LINKS</span></span>

[<span data-ttu-id="19bab-140">Omówienie: ciągłość usługi Cloud Business and odzyskiwanie danych po awarii bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="19bab-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="19bab-141">Odzyskiwanie bazy danych SQL Azure z awarii</span><span class="sxs-lookup"><span data-stu-id="19bab-141">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="19bab-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="19bab-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="19bab-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="19bab-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
