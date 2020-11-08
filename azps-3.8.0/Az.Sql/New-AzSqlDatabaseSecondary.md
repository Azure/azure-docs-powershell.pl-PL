---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051434"
---
# <span data-ttu-id="355e9-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="355e9-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="355e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="355e9-102">SYNOPSIS</span></span>
<span data-ttu-id="355e9-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="355e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="355e9-104">SYNTAX</span></span>

### <span data-ttu-id="355e9-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="355e9-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="355e9-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="355e9-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="355e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="355e9-107">DESCRIPTION</span></span>
<span data-ttu-id="355e9-108">Polecenie cmdlet **New-AzSqlDatabaseSecondary** zastępuje polecenie cmdlet Start-AzSqlDatabaseCopy, jeśli jest używane do konfigurowania replikacji Geo dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="355e9-109">Zwraca obiekt link replikacji geograficznej z podstawowego do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="355e9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="355e9-110">EXAMPLES</span></span>

### <span data-ttu-id="355e9-111">1: ustalanie aktywnych Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="355e9-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="355e9-112">2: ustalanie aktywnego Geo-Replication i Określanie nazwy bazy danych partnera innej niż źródłowa Nazwa bazy danych</span><span class="sxs-lookup"><span data-stu-id="355e9-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="355e9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="355e9-113">PARAMETERS</span></span>

### <span data-ttu-id="355e9-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="355e9-114">-AllowConnections</span></span>
<span data-ttu-id="355e9-115">Określa cel przeczytania pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="355e9-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="355e9-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="355e9-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="355e9-117">Ma</span><span class="sxs-lookup"><span data-stu-id="355e9-117">No</span></span>
- <span data-ttu-id="355e9-118">Cały</span><span class="sxs-lookup"><span data-stu-id="355e9-118">All</span></span>

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

### <span data-ttu-id="355e9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="355e9-119">-AsJob</span></span>
<span data-ttu-id="355e9-120">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="355e9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="355e9-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="355e9-121">-DatabaseName</span></span>
<span data-ttu-id="355e9-122">Określa nazwę bazy danych, która ma pełnić rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="355e9-122">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="355e9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="355e9-123">-DefaultProfile</span></span>
<span data-ttu-id="355e9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="355e9-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="355e9-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="355e9-125">-LicenseType</span></span>
<span data-ttu-id="355e9-126">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="355e9-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="355e9-127">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="355e9-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="355e9-128">Nazwa pomocniczej bazy danych do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="355e9-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="355e9-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="355e9-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="355e9-130">Określa nazwę grupy zasobów platformy Azure, z którą to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="355e9-131">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="355e9-131">-PartnerServerName</span></span>
<span data-ttu-id="355e9-132">Określa nazwę serwera bazy danych SQL Azure, który ma pełnić rolę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="355e9-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="355e9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="355e9-133">-ResourceGroupName</span></span>
<span data-ttu-id="355e9-134">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="355e9-135">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="355e9-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="355e9-136">Generowanie obliczeniowe pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="355e9-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="355e9-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="355e9-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="355e9-138">Określa nazwę puli elastycznej, w której ma zostać umieszczona pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="355e9-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="355e9-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="355e9-140">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="355e9-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="355e9-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="355e9-141">-SecondaryVCore</span></span>
<span data-ttu-id="355e9-142">Numery vCore pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="355e9-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="355e9-143">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="355e9-143">-ServerName</span></span>
<span data-ttu-id="355e9-144">Określa nazwę programu SQL Server podstawowej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="355e9-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="355e9-145">-Tagi</span><span class="sxs-lookup"><span data-stu-id="355e9-145">-Tags</span></span>
<span data-ttu-id="355e9-146">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="355e9-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="355e9-147">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="355e9-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="355e9-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="355e9-148">-Confirm</span></span>
<span data-ttu-id="355e9-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="355e9-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="355e9-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="355e9-150">-WhatIf</span></span>
<span data-ttu-id="355e9-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="355e9-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="355e9-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="355e9-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="355e9-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="355e9-153">CommonParameters</span></span>
<span data-ttu-id="355e9-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="355e9-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="355e9-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="355e9-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="355e9-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="355e9-156">INPUTS</span></span>

### <span data-ttu-id="355e9-157">System. String</span><span class="sxs-lookup"><span data-stu-id="355e9-157">System.String</span></span>

## <span data-ttu-id="355e9-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="355e9-158">OUTPUTS</span></span>

### <span data-ttu-id="355e9-159">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="355e9-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="355e9-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="355e9-160">NOTES</span></span>

## <span data-ttu-id="355e9-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="355e9-161">RELATED LINKS</span></span>

[<span data-ttu-id="355e9-162">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="355e9-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="355e9-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="355e9-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="355e9-164">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="355e9-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
