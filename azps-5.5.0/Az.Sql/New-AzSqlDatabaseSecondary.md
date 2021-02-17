---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178419"
---
# <span data-ttu-id="f3fe6-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f3fe6-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="f3fe6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3fe6-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fe6-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="f3fe6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f3fe6-104">SYNTAX</span></span>

### <span data-ttu-id="f3fe6-105">DtuBasedDatabase (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f3fe6-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f3fe6-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="f3fe6-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3fe6-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f3fe6-107">DESCRIPTION</span></span>
<span data-ttu-id="f3fe6-108">Polecenie cmdlet **New-AzSqlDatabaseSecondary** zastępuje Start-AzSqlDatabaseCopy cmdlet podczas konfigurowania replikacji geograficznej dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="f3fe6-109">Zwraca obiekt linku replikacji geograficznej z podstawowej do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="f3fe6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f3fe6-110">EXAMPLES</span></span>

### <span data-ttu-id="f3fe6-111">Przykład 1. Ustanawianie aktywnych Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="f3fe6-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="f3fe6-112">Przykład 2. Ustanawianie Geo-Replication i określanie nazwy bazy danych partnera, która ma być inna niż nazwa źródłowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="f3fe6-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="f3fe6-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3fe6-113">PARAMETERS</span></span>

### <span data-ttu-id="f3fe6-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="f3fe6-114">-AllowConnections</span></span>
<span data-ttu-id="f3fe6-115">Określa wartość przeczytaną pomocniczej bazy danych Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="f3fe6-116">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="f3fe6-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f3fe6-117">Nie</span><span class="sxs-lookup"><span data-stu-id="f3fe6-117">No</span></span>
- <span data-ttu-id="f3fe6-118">Wszystkie</span><span class="sxs-lookup"><span data-stu-id="f3fe6-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f3fe6-119">-AsJob</span></span>
<span data-ttu-id="f3fe6-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f3fe6-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="f3fe6-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="f3fe6-122">Nadmiarowość magazynu kopii zapasowej używana do przechowywania kopii zapasowych dla bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="f3fe6-123">Dostępne są następujące opcje: Lokalny, Strefa i Geo.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-124">-DatabaseName</span></span>
<span data-ttu-id="f3fe6-125">Określa nazwę bazy danych, która ma pełnić nazwę podstawową.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-125">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fe6-126">-DefaultProfile</span></span>
<span data-ttu-id="f3fe6-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f3fe6-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f3fe6-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="f3fe6-128">-LicenseType</span></span>
<span data-ttu-id="f3fe6-129">Typ licencji dla bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-129">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="f3fe6-131">Nazwa pomocniczej bazy danych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-131">The name of the secondary database to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="f3fe6-133">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-134">-PartnerServerName</span></span>
<span data-ttu-id="f3fe6-135">Określa nazwę serwera bazy danych Azure SQL, który ma pełnić nazwę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-136">-ResourceGroupName</span></span>
<span data-ttu-id="f3fe6-137">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="f3fe6-138">-SecondaryCompute Zwyrodnienie</span><span class="sxs-lookup"><span data-stu-id="f3fe6-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="f3fe6-139">Generowanie obliczeniowej pomocniczej bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-139">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="f3fe6-141">Określa nazwę puli elastycznej, w której ma być umieszczana pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="f3fe6-143">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="f3fe6-144">-SecondaryType</span></span>
<span data-ttu-id="f3fe6-145">Pomocniczy typ bazy danych, jeśli jest pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="f3fe6-146">Prawidłowe wartości to Geo i Named.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-147">- SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="f3fe6-147">-SecondaryVCore</span></span>
<span data-ttu-id="f3fe6-148">Numery vcore pomocniczej bazy danych Azure Sql Database.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3fe6-149">-ServerName</span></span>
<span data-ttu-id="f3fe6-150">Określa nazwę programu SQL Server podstawowej bazy danych SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="f3fe6-151">— Tagi</span><span class="sxs-lookup"><span data-stu-id="f3fe6-151">-Tags</span></span>
<span data-ttu-id="f3fe6-152">Określa pary klucz-wartość w postaci tabeli skrótu do skojarzenia z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="f3fe6-153">Na przykład: @{key0="value0";key1=$null;key2="wartość2"}</span><span class="sxs-lookup"><span data-stu-id="f3fe6-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe6-154">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3fe6-154">-Confirm</span></span>
<span data-ttu-id="f3fe6-155">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3fe6-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3fe6-156">-WhatIf</span></span>
<span data-ttu-id="f3fe6-157">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3fe6-158">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3fe6-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fe6-159">CommonParameters</span></span>
<span data-ttu-id="f3fe6-160">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fe6-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fe6-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f3fe6-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fe6-162">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3fe6-162">INPUTS</span></span>

### <span data-ttu-id="f3fe6-163">System.String</span><span class="sxs-lookup"><span data-stu-id="f3fe6-163">System.String</span></span>

## <span data-ttu-id="f3fe6-164">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3fe6-164">OUTPUTS</span></span>

### <span data-ttu-id="f3fe6-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="f3fe6-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="f3fe6-166">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f3fe6-166">NOTES</span></span>

## <span data-ttu-id="f3fe6-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3fe6-167">RELATED LINKS</span></span>

[<span data-ttu-id="f3fe6-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f3fe6-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f3fe6-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="f3fe6-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="f3fe6-170">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f3fe6-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
