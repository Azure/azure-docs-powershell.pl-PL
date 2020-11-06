---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 256AA6F4-D856-4713-A0AC-0DA1A145AA5C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasegeobackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDatabaseGeoBackup.md
ms.openlocfilehash: f22730e39a1b53cfea8181163dd770c67dc598a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543384"
---
# <span data-ttu-id="09afe-101">Get-AzureRmSqlDatabaseGeoBackup</span><span class="sxs-lookup"><span data-stu-id="09afe-101">Get-AzureRmSqlDatabaseGeoBackup</span></span>

## <span data-ttu-id="09afe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09afe-102">SYNOPSIS</span></span>
<span data-ttu-id="09afe-103">Pobiera kopię zapasową bazy danych w postaci geograficznej.</span><span class="sxs-lookup"><span data-stu-id="09afe-103">Gets a geo-redundant backup of a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09afe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09afe-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackup [-ServerName] <String> [[-DatabaseName] <String>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09afe-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09afe-105">DESCRIPTION</span></span>
<span data-ttu-id="09afe-106">Polecenie cmdlet **Get-AzureRMSqlDatabaseGeoBackup** pobiera określoną geograficzną kopię zapasową bazy danych SQL lub wszystkie dostępne zapasowe kopie lustrzane na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="09afe-106">The **Get-AzureRMSqlDatabaseGeoBackup** cmdlet gets a specified geo-redundant backup of a SQL database or all available geo-redundant backups on a specified server.</span></span>
<span data-ttu-id="09afe-107">Kopia zapasowa miejsca geograficznego jest to zasób restorable, który używa plików danych z osobnej lokalizacji geograficznej.</span><span class="sxs-lookup"><span data-stu-id="09afe-107">A geo-redundant backup is a restorable resource using data files from a separate geographic location.</span></span>
<span data-ttu-id="09afe-108">Za pomocą Geo-Restore możesz przywrócić kopię zapasową geograficznej w przypadku awarii regionalnej w celu odzyskania bazy danych do nowego regionu.</span><span class="sxs-lookup"><span data-stu-id="09afe-108">You can use Geo-Restore to restore a geo-redundant backup in the event of a regional outage to recover your database to a new region.</span></span>
<span data-ttu-id="09afe-109">To polecenie cmdlet jest również obsługiwane przez usługę bazy danych SQL Server undatabase na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="09afe-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="09afe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09afe-110">EXAMPLES</span></span>

### <span data-ttu-id="09afe-111">Przykład 1: pobieranie wszystkich rezerwowych kopii zapasowych na serwerze</span><span class="sxs-lookup"><span data-stu-id="09afe-111">Example 1: Get all geo-redundant backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="09afe-112">To polecenie pobiera wszystkie dostępne zapasowe kopie lustrzane na określonym serwerze.</span><span class="sxs-lookup"><span data-stu-id="09afe-112">This command gets all available geo-redundant backups on a specified server.</span></span>

### <span data-ttu-id="09afe-113">Przykład 2: uzyskiwanie określonej geograficznie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="09afe-113">Example 2: Get a specified geo-redundant backup</span></span>
```
PS C:\>Get-AzureRMSqlDatabaseGeoBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="09afe-114">To polecenie uzyskuje kopię zapasową bazy danych w postaci Geo-rezerwowej o nazwie ContosoDatabase.</span><span class="sxs-lookup"><span data-stu-id="09afe-114">This command gets the database geo-redundant backup named ContosoDatabase.</span></span>

## <span data-ttu-id="09afe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09afe-115">PARAMETERS</span></span>

### <span data-ttu-id="09afe-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="09afe-116">-DatabaseName</span></span>
<span data-ttu-id="09afe-117">Określa nazwę bazy danych, którą należy pobrać.</span><span class="sxs-lookup"><span data-stu-id="09afe-117">Specifies the name of the database to get.</span></span>

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

### <span data-ttu-id="09afe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09afe-118">-DefaultProfile</span></span>
<span data-ttu-id="09afe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="09afe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09afe-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09afe-120">-ResourceGroupName</span></span>
<span data-ttu-id="09afe-121">Określa nazwę grupy zasobów, do której jest przypisany serwer bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="09afe-121">Specifies the name of the resource group to which the SQL database server is assigned.</span></span>

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

### <span data-ttu-id="09afe-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="09afe-122">-ServerName</span></span>
<span data-ttu-id="09afe-123">Określa nazwę serwera obsługującego kopię zapasową do przywrócenia.</span><span class="sxs-lookup"><span data-stu-id="09afe-123">Specifies the name of the server that hosts the backup to restore.</span></span>

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

### <span data-ttu-id="09afe-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09afe-124">-Confirm</span></span>
<span data-ttu-id="09afe-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09afe-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09afe-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09afe-126">-WhatIf</span></span>
<span data-ttu-id="09afe-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09afe-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09afe-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09afe-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09afe-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09afe-129">CommonParameters</span></span>
<span data-ttu-id="09afe-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09afe-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09afe-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09afe-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09afe-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09afe-132">INPUTS</span></span>

### <span data-ttu-id="09afe-133">System. String</span><span class="sxs-lookup"><span data-stu-id="09afe-133">System.String</span></span>

## <span data-ttu-id="09afe-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09afe-134">OUTPUTS</span></span>

### <span data-ttu-id="09afe-135">Microsoft. Azure. Commands. SQL. Backup. model. AzureSqlDatabaseGeoBackupModel</span><span class="sxs-lookup"><span data-stu-id="09afe-135">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDatabaseGeoBackupModel</span></span>

## <span data-ttu-id="09afe-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09afe-136">NOTES</span></span>

## <span data-ttu-id="09afe-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09afe-137">RELATED LINKS</span></span>

[<span data-ttu-id="09afe-138">Omówienie: ciągłość usługi Cloud Business and odzyskiwanie danych po awarii bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="09afe-138">Overview: Cloud business continuity and database disaster recovery with SQL Database</span></span>](https://go.microsoft.com/fwlink/?LinkId=746881)

[<span data-ttu-id="09afe-139">Odzyskiwanie bazy danych SQL Azure z awarii</span><span class="sxs-lookup"><span data-stu-id="09afe-139">Recover an Azure SQL Database from an outage</span></span>](https://go.microsoft.com/fwlink/?LinkId=746882)

[<span data-ttu-id="09afe-140">Restore-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="09afe-140">Restore-AzureRmSqlDatabase</span></span>](./Restore-AzureRmSqlDatabase.md)

[<span data-ttu-id="09afe-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="09afe-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
