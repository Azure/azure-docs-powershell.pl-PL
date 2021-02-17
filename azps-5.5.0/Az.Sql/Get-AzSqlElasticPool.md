---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: ebc9386df78af1a730578c57e3957a869bbc299b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176923"
---
# <span data-ttu-id="f77a2-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f77a2-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="f77a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f77a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f77a2-103">Pobiera pule elastyczne i wartości ich właściwości w usłudze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="f77a2-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="f77a2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f77a2-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f77a2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f77a2-105">DESCRIPTION</span></span>
<span data-ttu-id="f77a2-106">Polecenie **cmdlet Get-AzSqlElasticPool** pobiera pule elastyczne i ich wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="f77a2-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="f77a2-107">Określ nazwę istniejącej puli elastycznej, aby wyświetlić wartości właściwości tylko dla tej puli.</span><span class="sxs-lookup"><span data-stu-id="f77a2-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="f77a2-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f77a2-108">EXAMPLES</span></span>

### <span data-ttu-id="f77a2-109">Przykład 1. Uzyskaj wszystkie pule elastyczne</span><span class="sxs-lookup"><span data-stu-id="f77a2-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="f77a2-110">To polecenie pobiera wszystkie pule elastyczne na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="f77a2-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="f77a2-111">Przykład 2. Uzyskiwanie konkretnej puli elastycznej</span><span class="sxs-lookup"><span data-stu-id="f77a2-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="f77a2-112">To polecenie pobiera elastyczną pulę o nazwiePool0127 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="f77a2-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="f77a2-113">Przykład 3. Uzyskiwanie metryk dla puli bazy danych Azure SQL Wszędniowa baza danych</span><span class="sxs-lookup"><span data-stu-id="f77a2-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-AzMetric -TimeGrain 0:5:0 -MetricName storage_percent
DimensionName  : 
DimensionValue : 
Name           : cpu_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : physical_data_read_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : log_write_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : dtu_consumption_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent

DimensionName  : 
DimensionValue : 
Name           : storage_percent
EndTime        : 8/27/2015 5:22:25 PM
MetricValues   : {Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue, Microsoft.Azure.Insights.Models.MetricValue...} 
Properties     : {}
ResourceId     : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
StartTime      : 8/27/2015 4:20:00 PM
TimeGrain      : 00:05:00
Unit           : Percent
```

<span data-ttu-id="f77a2-114">To polecenie zwraca metryki puli bazy danych elastycznej języka Azure SQL o nazwie 1000000000000000000000000000000000000000</span><span class="sxs-lookup"><span data-stu-id="f77a2-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="f77a2-115">Przykład 4. Uzyskaj wszystkie pule elastyczne przy użyciu filtrowania —NazwaDeksowa_buforu ciepowierniowego"\*"</span><span class="sxs-lookup"><span data-stu-id="f77a2-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              : 

ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool02
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool02
Location          : Central US
CreationDate      : 8/26/2015 11:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="f77a2-116">To polecenie pobiera wszystkie pule elastyczne na serwerze o nazwie Server01, których nazwy zaczynają się od "Szemokidne bufory".</span><span class="sxs-lookup"><span data-stu-id="f77a2-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="f77a2-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f77a2-117">PARAMETERS</span></span>

### <span data-ttu-id="f77a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f77a2-118">-DefaultProfile</span></span>
<span data-ttu-id="f77a2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="f77a2-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f77a2-120">-Nawiązywane_buforyNazwa</span><span class="sxs-lookup"><span data-stu-id="f77a2-120">-ElasticPoolName</span></span>
<span data-ttu-id="f77a2-121">Określa nazwę puli elastycznej, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f77a2-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f77a2-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f77a2-122">-ResourceGroupName</span></span>
<span data-ttu-id="f77a2-123">Określa nazwę grupy zasobów zawierającej elastyczną pulę, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f77a2-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f77a2-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f77a2-124">-ServerName</span></span>
<span data-ttu-id="f77a2-125">Określa nazwę serwera zawierającego elastyczną pulę, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f77a2-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f77a2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f77a2-126">CommonParameters</span></span>
<span data-ttu-id="f77a2-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f77a2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f77a2-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f77a2-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f77a2-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f77a2-129">INPUTS</span></span>

### <span data-ttu-id="f77a2-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f77a2-130">System.String</span></span>

## <span data-ttu-id="f77a2-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f77a2-131">OUTPUTS</span></span>

### <span data-ttu-id="f77a2-132">Microsoft.Azure.Commands.Sql.NawiązywekPoola.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="f77a2-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="f77a2-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f77a2-133">NOTES</span></span>

## <span data-ttu-id="f77a2-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f77a2-134">RELATED LINKS</span></span>

[<span data-ttu-id="f77a2-135">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f77a2-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="f77a2-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f77a2-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="f77a2-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="f77a2-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


