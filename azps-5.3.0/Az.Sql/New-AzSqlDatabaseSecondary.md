---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498365"
---
# <span data-ttu-id="49a68-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="49a68-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="49a68-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="49a68-102">SYNOPSIS</span></span>
<span data-ttu-id="49a68-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="49a68-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="49a68-104">SYNTAX</span></span>

### <span data-ttu-id="49a68-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="49a68-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49a68-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="49a68-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49a68-107">Opis</span><span class="sxs-lookup"><span data-stu-id="49a68-107">DESCRIPTION</span></span>
<span data-ttu-id="49a68-108">Polecenie cmdlet **New-AzSqlDatabaseSecondary** zastępuje polecenie cmdlet Start-AzSqlDatabaseCopy, jeśli jest używane do konfigurowania replikacji Geo dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="49a68-109">Zwraca obiekt link replikacji geograficznej z podstawowego do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="49a68-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="49a68-110">EXAMPLES</span></span>

### <span data-ttu-id="49a68-111">Przykład 1: ustalanie aktywnego Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="49a68-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="49a68-112">Przykład 2: ustanawianie aktywnego Geo-Replication i Określanie nazwy bazy danych partnera innej niż nazwa źródłowej bazy danych</span><span class="sxs-lookup"><span data-stu-id="49a68-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="49a68-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="49a68-113">PARAMETERS</span></span>

### <span data-ttu-id="49a68-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="49a68-114">-AllowConnections</span></span>
<span data-ttu-id="49a68-115">Określa cel przeczytania pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49a68-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="49a68-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="49a68-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="49a68-117">Ma</span><span class="sxs-lookup"><span data-stu-id="49a68-117">No</span></span>
- <span data-ttu-id="49a68-118">Cały</span><span class="sxs-lookup"><span data-stu-id="49a68-118">All</span></span>

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

### <span data-ttu-id="49a68-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49a68-119">-AsJob</span></span>
<span data-ttu-id="49a68-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="49a68-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49a68-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="49a68-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="49a68-122">Nadmiarowość miejsca do magazynowania kopii zapasowej używana do przechowywania kopii zapasowych bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="49a68-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="49a68-123">Dostępne opcje: local, Zone i geo.</span><span class="sxs-lookup"><span data-stu-id="49a68-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="49a68-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="49a68-124">-DatabaseName</span></span>
<span data-ttu-id="49a68-125">Określa nazwę bazy danych, która ma pełnić rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="49a68-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="49a68-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49a68-126">-DefaultProfile</span></span>
<span data-ttu-id="49a68-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="49a68-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49a68-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="49a68-128">-LicenseType</span></span>
<span data-ttu-id="49a68-129">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49a68-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="49a68-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="49a68-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="49a68-131">Nazwa pomocniczej bazy danych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="49a68-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="49a68-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a68-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="49a68-133">Określa nazwę grupy zasobów platformy Azure, z którą to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="49a68-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="49a68-134">-PartnerServerName</span></span>
<span data-ttu-id="49a68-135">Określa nazwę serwera bazy danych SQL Azure, który ma pełnić rolę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="49a68-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="49a68-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49a68-136">-ResourceGroupName</span></span>
<span data-ttu-id="49a68-137">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="49a68-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="49a68-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="49a68-139">Generowanie obliczeniowe pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49a68-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="49a68-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="49a68-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="49a68-141">Określa nazwę puli elastycznej, w której ma zostać umieszczona pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="49a68-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="49a68-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="49a68-143">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="49a68-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="49a68-144">-Drugorzędny</span><span class="sxs-lookup"><span data-stu-id="49a68-144">-SecondaryType</span></span>
<span data-ttu-id="49a68-145">Pomocniczy typ bazy danych, jeśli jest pomocniczy.</span><span class="sxs-lookup"><span data-stu-id="49a68-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="49a68-146">Prawidłowe wartości to Geo i Named.</span><span class="sxs-lookup"><span data-stu-id="49a68-146">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="49a68-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="49a68-147">-SecondaryVCore</span></span>
<span data-ttu-id="49a68-148">Numery vCore pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="49a68-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="49a68-149">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="49a68-149">-ServerName</span></span>
<span data-ttu-id="49a68-150">Określa nazwę programu SQL Server podstawowej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="49a68-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="49a68-151">-Tagi</span><span class="sxs-lookup"><span data-stu-id="49a68-151">-Tags</span></span>
<span data-ttu-id="49a68-152">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="49a68-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="49a68-153">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="49a68-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="49a68-154">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="49a68-154">-Confirm</span></span>
<span data-ttu-id="49a68-155">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49a68-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49a68-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49a68-156">-WhatIf</span></span>
<span data-ttu-id="49a68-157">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49a68-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49a68-158">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="49a68-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49a68-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49a68-159">CommonParameters</span></span>
<span data-ttu-id="49a68-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49a68-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49a68-161">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49a68-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49a68-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49a68-162">INPUTS</span></span>

### <span data-ttu-id="49a68-163">System. String</span><span class="sxs-lookup"><span data-stu-id="49a68-163">System.String</span></span>

## <span data-ttu-id="49a68-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="49a68-164">OUTPUTS</span></span>

### <span data-ttu-id="49a68-165">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="49a68-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="49a68-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="49a68-166">NOTES</span></span>

## <span data-ttu-id="49a68-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49a68-167">RELATED LINKS</span></span>

[<span data-ttu-id="49a68-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="49a68-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="49a68-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="49a68-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="49a68-170">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="49a68-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
