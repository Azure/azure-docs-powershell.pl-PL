---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseGeoBackup.md
ms.openlocfilehash: 0ca3a6c467ab5fd7dd681164d88686a6360394ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176979"
---
# <span data-ttu-id="6a320-101">Get-AzSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="6a320-101">Get-AzSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="6a320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a320-102">SYNOPSIS</span></span>
<span data-ttu-id="6a320-103">Pobiera nadmiarową geograficznie kopię zapasową bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a320-103">Gets a geo-redundant backup of a database.</span></span>

## <span data-ttu-id="6a320-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6a320-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a320-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6a320-105">DESCRIPTION</span></span>
<span data-ttu-id="6a320-106">Polecenie **cmdlet Get-AzSqlDatabaseGeoBackup** pobiera określoną geograficznie nadmiarową kopię zapasową bazy danych SQL lub wszystkie dostępne geograficznie nadmiarowe kopie zapasowe na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="6a320-106">The **Get-AzSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="6a320-107">Geograficznie nadmiarowa kopia zapasowa to zasób, który można przywrócić, używając plików danych z oddzielnej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="6a320-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="6a320-108">Za pomocą programu Geo-Restore można przywrócić geograficznie nadmiarową kopię zapasową w przypadku 30-65-65-65-855 000 w celu odzyskania bazy danych w nowym regionie.</span><span class="sxs-lookup"><span data-stu-id="6a320-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="6a320-109">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="6a320-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6a320-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6a320-110">EXAMPLES</span></span>

### <span data-ttu-id="6a320-111">Przykład 1. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych na serwerze</span><span class="sxs-lookup"><span data-stu-id="6a320-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="6a320-112">To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="6a320-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="6a320-113">Przykład 2. Uzyskiwanie określonej nadmiarowej geograficznej kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="6a320-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="6a320-114">To polecenie pobiera geograficznie nadmiarową kopię zapasową bazy danych o nazwie ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="6a320-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

### <span data-ttu-id="6a320-115">Przykład 3. Uzyskiwanie wszystkich nadmiarowych geograficznie kopii zapasowych na serwerze przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="6a320-115">Example 3: Get all geo-redundant backups on a server using filtering</span></span>
```
PS C:\>Get-AzSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "Contoso*"
```

<span data-ttu-id="6a320-116">To polecenie pobiera wszystkie dostępne geograficznie nadmiarowe kopie zapasowe na określonym serwerze, których nazwa rozpoczyna się od "Contoso".</span><span class="sxs-lookup"><span data-stu-id="6a320-116">This command gets all available geo-redundant backups on a specified server that start with "Contoso".</span></span>

## <span data-ttu-id="6a320-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6a320-117">PARAMETERS</span></span>

### <span data-ttu-id="6a320-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6a320-118">-DatabaseName</span></span>
<span data-ttu-id="6a320-119">Określa nazwę bazy danych do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="6a320-119">Specifies the name of the database to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a320-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a320-120">-DefaultProfile</span></span>
<span data-ttu-id="6a320-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6a320-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a320-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a320-122">-ResourceGroupName</span></span>
<span data-ttu-id="6a320-123">Określa nazwę grupy zasobów, do której jest przypisany serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="6a320-123">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="6a320-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6a320-124">-ServerName</span></span>
<span data-ttu-id="6a320-125">Określa nazwę serwera hostatora kopii zapasowej do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="6a320-125">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="6a320-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a320-126">-Confirm</span></span>
<span data-ttu-id="6a320-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6a320-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a320-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a320-128">-WhatIf</span></span>
<span data-ttu-id="6a320-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a320-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a320-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6a320-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a320-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a320-131">CommonParameters</span></span>
<span data-ttu-id="6a320-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a320-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a320-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6a320-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a320-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a320-134">INPUTS</span></span>

### <span data-ttu-id="6a320-135">System.String</span><span class="sxs-lookup"><span data-stu-id="6a320-135">System.String</span></span>

## <span data-ttu-id="6a320-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6a320-136">OUTPUTS</span></span>

### <span data-ttu-id="6a320-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="6a320-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="6a320-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6a320-138">NOTES</span></span>

## <span data-ttu-id="6a320-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a320-139">RELATED LINKS</span></span>

[<span data-ttu-id="6a320-140">Omówienie: zapewnianie ciągłości działania i odzyskiwanie baz danych w chmurze za pomocą usługi SQL Database</span><span class="sxs-lookup"><span data-stu-id="6a320-140">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](http://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="6a320-141">Odzyskiwanie bazy danych Azure SQL Database po 30-55 dniach</span><span class="sxs-lookup"><span data-stu-id="6a320-141">Recover an Azure SQL Database from an outage</span></span>](http://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="6a320-142">Restore-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="6a320-142">Restore-AzSqlDatabase</span></span>](./Restore-AzSqlDatabase.md)

[<span data-ttu-id="6a320-143">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="6a320-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
