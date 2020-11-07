---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseSecondary.md
ms.openlocfilehash: 226910b81da287c04adb05574b77713e97c6a045
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716660"
---
# <span data-ttu-id="1194c-101">New-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1194c-101">New-AzureRmSqlDatabaseSecondary</span></span>

## <span data-ttu-id="1194c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1194c-102">SYNOPSIS</span></span>
<span data-ttu-id="1194c-103">Tworzy pomocniczą bazę danych dla istniejącej bazy danych i uruchamia replikację danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-103">Creates a secondary database for an existing database and starts data replication.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1194c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1194c-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-AllowConnections <AllowConnections>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1194c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1194c-105">DESCRIPTION</span></span>
<span data-ttu-id="1194c-106">Polecenie cmdlet **New-AzureRMSqlDatabaseSecondary** zastępuje polecenie cmdlet Start-AzureSqlDatabaseCopy, jeśli jest używane do konfigurowania replikacji Geo dla bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-106">The **New-AzureRMSqlDatabaseSecondary** cmdlet replaces the Start-AzureSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="1194c-107">Zwraca obiekt link replikacji geograficznej z podstawowego do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-107">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="1194c-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1194c-108">EXAMPLES</span></span>

### <span data-ttu-id="1194c-109">1: ustalanie aktywnych Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="1194c-109">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzureRmSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzureRmSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

## <span data-ttu-id="1194c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1194c-110">PARAMETERS</span></span>

### <span data-ttu-id="1194c-111">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="1194c-111">-AllowConnections</span></span>
<span data-ttu-id="1194c-112">Określa cel przeczytania pomocniczej bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="1194c-112">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="1194c-113">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1194c-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1194c-114">Ma</span><span class="sxs-lookup"><span data-stu-id="1194c-114">No</span></span>
- <span data-ttu-id="1194c-115">Cały</span><span class="sxs-lookup"><span data-stu-id="1194c-115">All</span></span>

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

### <span data-ttu-id="1194c-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1194c-116">-DatabaseName</span></span>
<span data-ttu-id="1194c-117">Określa nazwę bazy danych, która ma pełnić rolę podstawową.</span><span class="sxs-lookup"><span data-stu-id="1194c-117">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="1194c-118">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1194c-118">-PartnerResourceGroupName</span></span>
<span data-ttu-id="1194c-119">Określa nazwę grupy zasobów platformy Azure, z którą to polecenie cmdlet przypisuje pomocniczą bazę danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-119">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="1194c-120">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="1194c-120">-PartnerServerName</span></span>
<span data-ttu-id="1194c-121">Określa nazwę serwera bazy danych SQL Azure, który ma pełnić rolę pomocniczą.</span><span class="sxs-lookup"><span data-stu-id="1194c-121">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="1194c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1194c-122">-ResourceGroupName</span></span>
<span data-ttu-id="1194c-123">Określa nazwę grupy zasobów platformy Azure, do której to polecenie cmdlet przypisuje podstawową bazę danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-123">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="1194c-124">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="1194c-124">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="1194c-125">Określa nazwę puli elastycznej, w której ma zostać umieszczona pomocnicza baza danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-125">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="1194c-126">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="1194c-126">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="1194c-127">Określa nazwę celu usługi, który ma zostać przypisany do pomocniczej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="1194c-127">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="1194c-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="1194c-128">-ServerName</span></span>
<span data-ttu-id="1194c-129">Określa nazwę programu SQL Server podstawowej bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="1194c-129">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="1194c-130">-Tagi</span><span class="sxs-lookup"><span data-stu-id="1194c-130">-Tags</span></span>
<span data-ttu-id="1194c-131">Określa pary klucz-wartość w formie tabeli skrótów, które mają zostać skojarzone z linkiem replikacji bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="1194c-131">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="1194c-132">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="1194c-132">For example:</span></span>

<span data-ttu-id="1194c-133">@ {Key0 = "value0"; KEY1 = $null; key2 = "wartość2"}</span><span class="sxs-lookup"><span data-stu-id="1194c-133">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="1194c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1194c-134">-Confirm</span></span>
<span data-ttu-id="1194c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1194c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1194c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1194c-136">-WhatIf</span></span>
<span data-ttu-id="1194c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1194c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1194c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1194c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1194c-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1194c-139">-DefaultProfile</span></span>
<span data-ttu-id="1194c-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1194c-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1194c-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1194c-141">CommonParameters</span></span>
<span data-ttu-id="1194c-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1194c-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1194c-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1194c-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1194c-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1194c-144">INPUTS</span></span>

## <span data-ttu-id="1194c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1194c-145">OUTPUTS</span></span>

### <span data-ttu-id="1194c-146">Microsoft. Azure. Commands. SQL. Replication. model. AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="1194c-146">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>
<span data-ttu-id="1194c-147">To polecenie cmdlet zwraca **ReplicationLink** obiekty.</span><span class="sxs-lookup"><span data-stu-id="1194c-147">This cmdlet returns **ReplicationLink** objects.</span></span>

## <span data-ttu-id="1194c-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1194c-148">NOTES</span></span>

## <span data-ttu-id="1194c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1194c-149">RELATED LINKS</span></span>

[<span data-ttu-id="1194c-150">Remove-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1194c-150">Remove-AzureRmSqlDatabaseSecondary</span></span>](./Remove-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="1194c-151">Set-AzureRmSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="1194c-151">Set-AzureRmSqlDatabaseSecondary</span></span>](./Set-AzureRmSqlDatabaseSecondary.md)

[<span data-ttu-id="1194c-152">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="1194c-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
