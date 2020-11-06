---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: b23128d2ef55e971f20569e251601b410b218ec2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524814"
---
# <span data-ttu-id="a73d0-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a73d0-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="a73d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a73d0-102">SYNOPSIS</span></span>
<span data-ttu-id="a73d0-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a73d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a73d0-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a73d0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a73d0-105">DESCRIPTION</span></span>
<span data-ttu-id="a73d0-106">Polecenie cmdlet **New-AzureRMSqlDatabaseSecondary** zastępuje polecenie cmdlet Start-AzureSqlDatabaseCopy, jeśli jest używane do konfigurowania replikacji Geo dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="a73d0-107">Zwraca obiekt link replikacji geograficznej z podstawowego do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="a73d0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a73d0-108">EXAMPLES</span></span>

### <span data-ttu-id="a73d0-109">1: ustalanie aktywnych Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="a73d0-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="a73d0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a73d0-110">PARAMETERS</span></span>

### <span data-ttu-id="a73d0-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="a73d0-111">-AllowConnections</span></span>
<span data-ttu-id="a73d0-112">Określa cel przeczytania pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="a73d0-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="a73d0-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a73d0-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a73d0-114">Ma</span><span class="sxs-lookup"><span data-stu-id="a73d0-114">No</span></span>
- <span data-ttu-id="a73d0-115">Cały</span><span class="sxs-lookup"><span data-stu-id="a73d0-115">All</span></span>

```yaml
Type: AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a73d0-116">-AsJob</span></span>
<span data-ttu-id="a73d0-117">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a73d0-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a73d0-118">-DatabaseName</span></span>
<span data-ttu-id="a73d0-119">Określa nazwę bazy danych, która ma pełnić rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="a73d0-119">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a73d0-120">-DefaultProfile</span></span>
<span data-ttu-id="a73d0-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a73d0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-122">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73d0-122">-PartnerResourceGroupName</span></span>
<span data-ttu-id="a73d0-123">Określa nazwę grupy zasobów platformy Azure, z którą to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-124">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="a73d0-124">-PartnerServerName</span></span>
<span data-ttu-id="a73d0-125">Określa nazwę serwera bazy danych SQL Azure, który ma pełnić rolę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="a73d0-125">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a73d0-126">-ResourceGroupName</span></span>
<span data-ttu-id="a73d0-127">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-127">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-128">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a73d0-128">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="a73d0-129">Określa nazwę puli elastycznej, w której ma zostać umieszczona pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-129">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-130">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="a73d0-130">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="a73d0-131">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-131">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-132">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a73d0-132">-ServerName</span></span>
<span data-ttu-id="a73d0-133">Określa nazwę programu SQL Server podstawowej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a73d0-133">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-134">-Tagi</span><span class="sxs-lookup"><span data-stu-id="a73d0-134">-Tags</span></span>
<span data-ttu-id="a73d0-135">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="a73d0-135">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="a73d0-136">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="a73d0-136">For example:</span></span>

<span data-ttu-id="a73d0-137">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="a73d0-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a73d0-138">-Confirm</span></span>
<span data-ttu-id="a73d0-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a73d0-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a73d0-140">-WhatIf</span></span>
<span data-ttu-id="a73d0-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a73d0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a73d0-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a73d0-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a73d0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a73d0-143">CommonParameters</span></span>
<span data-ttu-id="a73d0-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a73d0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a73d0-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a73d0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a73d0-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a73d0-146">INPUTS</span></span>

### <span data-ttu-id="a73d0-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a73d0-147">None</span></span>
<span data-ttu-id="a73d0-148">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a73d0-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a73d0-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a73d0-149">OUTPUTS</span></span>

### <span data-ttu-id="a73d0-150">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="a73d0-150">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="a73d0-151">To polecenie cmdlet zwraca **ReplicationLink** obiekty.</span><span class="sxs-lookup"><span data-stu-id="a73d0-151">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="a73d0-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a73d0-152">NOTES</span></span>

## <span data-ttu-id="a73d0-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a73d0-153">RELATED LINKS</span></span>

[<span data-ttu-id="a73d0-154">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a73d0-154">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a73d0-155">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="a73d0-155">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="a73d0-156">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="a73d0-156">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
