---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: d2af2095198cf0a1102e3422716013f2f2e02fc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543371"
---
# <span data-ttu-id="b5ad6-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5ad6-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="b5ad6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="b5ad6-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5ad6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5ad6-104">SYNTAX</span></span>

### <span data-ttu-id="b5ad6-105">DtuBasedDatabase (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b5ad6-105">DtuBasedDatabase (Default)</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-LicenseType <String>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5ad6-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="b5ad6-106">VcoreBasedDatabase</span></span>
```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b5ad6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b5ad6-107">DESCRIPTION</span></span>
<span data-ttu-id="b5ad6-108">Polecenie cmdlet **New-AzureRMSqlDatabaseSecondary** zastępuje polecenie cmdlet Start-AzureSqlDatabaseCopy, jeśli jest używane do konfigurowania replikacji Geo dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-108">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="b5ad6-109">Zwraca obiekt link replikacji geograficznej z podstawowego do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="b5ad6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5ad6-110">EXAMPLES</span></span>

### <span data-ttu-id="b5ad6-111">1: ustalanie aktywnych Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="b5ad6-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="b5ad6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="b5ad6-113">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="b5ad6-113">-AllowConnections</span></span>
<span data-ttu-id="b5ad6-114">Określa cel przeczytania pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-114">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="b5ad6-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b5ad6-115">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b5ad6-116">Ma</span><span class="sxs-lookup"><span data-stu-id="b5ad6-116">No</span></span>
- <span data-ttu-id="b5ad6-117">Cały</span><span class="sxs-lookup"><span data-stu-id="b5ad6-117">All</span></span>

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

### <span data-ttu-id="b5ad6-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b5ad6-118">-AsJob</span></span>
<span data-ttu-id="b5ad6-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b5ad6-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b5ad6-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b5ad6-120">-DatabaseName</span></span>
<span data-ttu-id="b5ad6-121">Określa nazwę bazy danych, która ma pełnić rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-121">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="b5ad6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5ad6-122">-DefaultProfile</span></span>
<span data-ttu-id="b5ad6-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b5ad6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b5ad6-124">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="b5ad6-124">-LicenseType</span></span>
<span data-ttu-id="b5ad6-125">Typ licencji dla bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-125">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="b5ad6-126">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ad6-126">-PartnerResourceGroupName</span></span>
<span data-ttu-id="b5ad6-127">Określa nazwę grupy zasobów platformy Azure, z którą to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="b5ad6-128">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="b5ad6-128">-PartnerServerName</span></span>
<span data-ttu-id="b5ad6-129">Określa nazwę serwera bazy danych SQL Azure, który ma pełnić rolę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-129">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="b5ad6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5ad6-130">-ResourceGroupName</span></span>
<span data-ttu-id="b5ad6-131">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-131">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="b5ad6-132">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="b5ad6-132">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="b5ad6-133">Generowanie obliczeniowe pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-133">The compute generation of teh Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="b5ad6-134">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b5ad6-134">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="b5ad6-135">Określa nazwę puli elastycznej, w której ma zostać umieszczona pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-135">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="b5ad6-136">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="b5ad6-136">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="b5ad6-137">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-137">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="b5ad6-138">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="b5ad6-138">-SecondaryVCore</span></span>
<span data-ttu-id="b5ad6-139">Numery vCore pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-139">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="b5ad6-140">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="b5ad6-140">-ServerName</span></span>
<span data-ttu-id="b5ad6-141">Określa nazwę programu SQL Server podstawowej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-141">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="b5ad6-142">-Tagi</span><span class="sxs-lookup"><span data-stu-id="b5ad6-142">-Tags</span></span>
<span data-ttu-id="b5ad6-143">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-143">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="b5ad6-144">Na przykład: @ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="b5ad6-144">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b5ad6-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5ad6-145">-Confirm</span></span>
<span data-ttu-id="b5ad6-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5ad6-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5ad6-147">-WhatIf</span></span>
<span data-ttu-id="b5ad6-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5ad6-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5ad6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5ad6-150">CommonParameters</span></span>
<span data-ttu-id="b5ad6-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5ad6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5ad6-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5ad6-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5ad6-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5ad6-153">INPUTS</span></span>

### <span data-ttu-id="b5ad6-154">System. String</span><span class="sxs-lookup"><span data-stu-id="b5ad6-154">System.String</span></span>

## <span data-ttu-id="b5ad6-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5ad6-155">OUTPUTS</span></span>

### <span data-ttu-id="b5ad6-156">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="b5ad6-156">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="b5ad6-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5ad6-157">NOTES</span></span>

## <span data-ttu-id="b5ad6-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5ad6-158">RELATED LINKS</span></span>

[<span data-ttu-id="b5ad6-159">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5ad6-159">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b5ad6-160">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="b5ad6-160">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="b5ad6-161">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b5ad6-161">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
