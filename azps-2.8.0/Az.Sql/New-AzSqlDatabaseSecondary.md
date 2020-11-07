---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 1ed31d2fedc44900d08a4108ea53220a29228a7c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887390"
---
# <span data-ttu-id="ce0d3-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce0d3-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="ce0d3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce0d3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce0d3-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="ce0d3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce0d3-104">SYNTAX</span></span>

### <span data-ttu-id="ce0d3-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ce0d3-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce0d3-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="ce0d3-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce0d3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ce0d3-107">DESCRIPTION</span></span>
<span data-ttu-id="ce0d3-108">Polecenie cmdlet **New-AzSqlDatabaseSecondary** zastępuje polecenie cmdlet Start-AzSqlDatabaseCopy, jeśli jest używane do konfigurowania replikacji Geo dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="ce0d3-109">Zwraca obiekt link replikacji geograficznej z podstawowego do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="ce0d3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce0d3-110">EXAMPLES</span></span>

### <span data-ttu-id="ce0d3-111">1: ustalanie aktywnych Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="ce0d3-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="ce0d3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce0d3-112">PARAMETERS</span></span>

### <span data-ttu-id="ce0d3-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="ce0d3-113">-AllowConnections</span></span>
<span data-ttu-id="ce0d3-114">Określa cel przeczytania pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="ce0d3-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ce0d3-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce0d3-116">Ma</span><span class="sxs-lookup"><span data-stu-id="ce0d3-116">No</span></span>
- <span data-ttu-id="ce0d3-117">Cały</span><span class="sxs-lookup"><span data-stu-id="ce0d3-117">All</span></span>

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

### <span data-ttu-id="ce0d3-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce0d3-118">-AsJob</span></span>
<span data-ttu-id="ce0d3-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="ce0d3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce0d3-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce0d3-120">-DatabaseName</span></span>
<span data-ttu-id="ce0d3-121">Określa nazwę bazy danych, która ma pełnić rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="ce0d3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce0d3-122">-DefaultProfile</span></span>
<span data-ttu-id="ce0d3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ce0d3-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce0d3-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="ce0d3-124">-LicenseType</span></span>
<span data-ttu-id="ce0d3-125">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="ce0d3-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0d3-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="ce0d3-127">Określa nazwę grupy zasobów platformy Azure, z którą to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="ce0d3-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="ce0d3-128">-PartnerServerName</span></span>
<span data-ttu-id="ce0d3-129">Określa nazwę serwera bazy danych SQL Azure, który ma pełnić rolę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="ce0d3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce0d3-130">-ResourceGroupName</span></span>
<span data-ttu-id="ce0d3-131">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="ce0d3-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="ce0d3-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="ce0d3-133">Generowanie obliczeniowe pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-133">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="ce0d3-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="ce0d3-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="ce0d3-135">Określa nazwę puli elastycznej, w której ma zostać umieszczona pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="ce0d3-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="ce0d3-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="ce0d3-137">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="ce0d3-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="ce0d3-138">-SecondaryVCore</span></span>
<span data-ttu-id="ce0d3-139">Numery vCore pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="ce0d3-140">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ce0d3-140">-ServerName</span></span>
<span data-ttu-id="ce0d3-141">Określa nazwę programu SQL Server podstawowej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="ce0d3-142">-Tagi</span><span class="sxs-lookup"><span data-stu-id="ce0d3-142">-Tags</span></span>
<span data-ttu-id="ce0d3-143">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="ce0d3-144">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="ce0d3-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ce0d3-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ce0d3-145">-Confirm</span></span>
<span data-ttu-id="ce0d3-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce0d3-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce0d3-147">-WhatIf</span></span>
<span data-ttu-id="ce0d3-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce0d3-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce0d3-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce0d3-150">CommonParameters</span></span>
<span data-ttu-id="ce0d3-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce0d3-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce0d3-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ce0d3-152">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce0d3-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce0d3-153">INPUTS</span></span>

### <span data-ttu-id="ce0d3-154">System. String</span><span class="sxs-lookup"><span data-stu-id="ce0d3-154">System.String</span></span>

## <span data-ttu-id="ce0d3-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce0d3-155">OUTPUTS</span></span>

### <span data-ttu-id="ce0d3-156">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="ce0d3-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="ce0d3-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce0d3-157">NOTES</span></span>

## <span data-ttu-id="ce0d3-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce0d3-158">RELATED LINKS</span></span>

[<span data-ttu-id="ce0d3-159">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce0d3-159">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ce0d3-160">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="ce0d3-160">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="ce0d3-161">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ce0d3-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
