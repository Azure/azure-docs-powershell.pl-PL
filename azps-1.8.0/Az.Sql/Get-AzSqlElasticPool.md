---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPool.md
ms.openlocfilehash: f0c6de30f0bb38d20f30599a37c1e9a9be378f8b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707959"
---
# <span data-ttu-id="06ec1-101">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06ec1-101">Get-AzSqlElasticPool</span></span>

## <span data-ttu-id="06ec1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06ec1-102">SYNOPSIS</span></span>
<span data-ttu-id="06ec1-103">Pobiera pule elastyczne i wartości ich właściwości w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="06ec1-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

## <span data-ttu-id="06ec1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06ec1-104">SYNTAX</span></span>

```
Get-AzSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06ec1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06ec1-105">DESCRIPTION</span></span>
<span data-ttu-id="06ec1-106">Polecenie cmdlet **Get-AzSqlElasticPool** pobiera elastyczne pule i ich wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="06ec1-106">The **Get-AzSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="06ec1-107">Określ nazwę istniejącej puli elastycznej, aby wyświetlić wartości właściwości tylko dla tej puli.</span><span class="sxs-lookup"><span data-stu-id="06ec1-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="06ec1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06ec1-108">EXAMPLES</span></span>

### <span data-ttu-id="06ec1-109">Przykład 1: pobieranie wszystkich pul elastycznych</span><span class="sxs-lookup"><span data-stu-id="06ec1-109">Example 1: Get all elastic pools</span></span>
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

<span data-ttu-id="06ec1-110">To polecenie pobiera wszystkie pule elastyczne na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="06ec1-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="06ec1-111">Przykład 2: uzyskiwanie określonej elastyczności puli</span><span class="sxs-lookup"><span data-stu-id="06ec1-111">Example 2: Get a specific elastic pool</span></span>
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

<span data-ttu-id="06ec1-112">To polecenie pobiera elastyczną pulę o nazwie ElasticPool0127 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="06ec1-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="06ec1-113">Przykład 3: uzyskiwanie metryk dla puli Elastic Database w usłudze Azure SQL</span><span class="sxs-lookup"><span data-stu-id="06ec1-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
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

<span data-ttu-id="06ec1-114">To polecenie zwraca metryki dla puli Elastic Database usługi Azure SQL o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="06ec1-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

### <span data-ttu-id="06ec1-115">Przykład 4: uzyskiwanie wszystkich elastycznych pul przy użyciu funkcji Filter-ElasticPoolName "ElasticPool \*"</span><span class="sxs-lookup"><span data-stu-id="06ec1-115">Example 4: Get all elastic pools using filtering -ElasticPoolName "ElasticPool\*"</span></span>
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

<span data-ttu-id="06ec1-116">To polecenie pobiera wszystkie pule elastyczne na serwerze o nazwie Server01, których nazwa rozpoczyna się od "ElasticPool".</span><span class="sxs-lookup"><span data-stu-id="06ec1-116">This command gets all of the elastic pools on the server named Server01 that start with "ElasticPool".</span></span>

## <span data-ttu-id="06ec1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06ec1-117">PARAMETERS</span></span>

### <span data-ttu-id="06ec1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ec1-118">-DefaultProfile</span></span>
<span data-ttu-id="06ec1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="06ec1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06ec1-120">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="06ec1-120">-ElasticPoolName</span></span>
<span data-ttu-id="06ec1-121">Określa nazwę puli elastycznej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ec1-121">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="06ec1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06ec1-122">-ResourceGroupName</span></span>
<span data-ttu-id="06ec1-123">Określa nazwę grupy zasobów zawierającej pulę elastyczną, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ec1-123">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06ec1-124">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="06ec1-124">-ServerName</span></span>
<span data-ttu-id="06ec1-125">Określa nazwę serwera zawierającego pulę elastyczną, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ec1-125">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="06ec1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ec1-126">CommonParameters</span></span>
<span data-ttu-id="06ec1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ec1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ec1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06ec1-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ec1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ec1-129">INPUTS</span></span>

### <span data-ttu-id="06ec1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="06ec1-130">System.String</span></span>

## <span data-ttu-id="06ec1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06ec1-131">OUTPUTS</span></span>

### <span data-ttu-id="06ec1-132">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="06ec1-132">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="06ec1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06ec1-133">NOTES</span></span>

## <span data-ttu-id="06ec1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06ec1-134">RELATED LINKS</span></span>

[<span data-ttu-id="06ec1-135">Nowe — AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06ec1-135">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="06ec1-136">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06ec1-136">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="06ec1-137">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="06ec1-137">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)


