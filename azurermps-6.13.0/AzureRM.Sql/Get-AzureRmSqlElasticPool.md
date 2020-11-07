---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 350E19F6-5B1C-4D3F-B4CD-7225CDC984C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlElasticPool.md
ms.openlocfilehash: e40510745ea7de39df4e15d0b1be7516d0fb33ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550184"
---
# <span data-ttu-id="e6e61-101">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e6e61-101">Get-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="e6e61-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6e61-102">SYNOPSIS</span></span>
<span data-ttu-id="e6e61-103">Pobiera pule elastyczne i wartości ich właściwości w bazie danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="e6e61-103">Gets elastic pools and their property values in an Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6e61-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6e61-104">SYNTAX</span></span>

```
Get-AzureRmSqlElasticPool [[-ElasticPoolName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6e61-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e6e61-105">DESCRIPTION</span></span>
<span data-ttu-id="e6e61-106">Polecenie cmdlet **Get-AzureRmSqlElasticPool** pobiera elastyczne pule i ich wartości właściwości.</span><span class="sxs-lookup"><span data-stu-id="e6e61-106">The **Get-AzureRmSqlElasticPool** cmdlet gets elastic pools and their property values.</span></span>
<span data-ttu-id="e6e61-107">Określ nazwę istniejącej puli elastycznej, aby wyświetlić wartości właściwości tylko dla tej puli.</span><span class="sxs-lookup"><span data-stu-id="e6e61-107">Specify the name of an existing elastic pool to see the property values for only that pool.</span></span>

## <span data-ttu-id="e6e61-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6e61-108">EXAMPLES</span></span>

### <span data-ttu-id="e6e61-109">Przykład 1: pobieranie wszystkich pul elastycznych</span><span class="sxs-lookup"><span data-stu-id="e6e61-109">Example 1: Get all elastic pools</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
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

<span data-ttu-id="e6e61-110">To polecenie pobiera wszystkie pule elastyczne na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="e6e61-110">This command gets all of the elastic pools on the server named Server01.</span></span>

### <span data-ttu-id="e6e61-111">Przykład 2: uzyskiwanie określonej elastyczności puli</span><span class="sxs-lookup"><span data-stu-id="e6e61-111">Example 2: Get a specific elastic pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool27"
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

<span data-ttu-id="e6e61-112">To polecenie pobiera elastyczną pulę o nazwie ElasticPool0127 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="e6e61-112">This command gets the elastic pool named ElasticPool0127 on the server named Server01.</span></span>

### <span data-ttu-id="e6e61-113">Przykład 3: uzyskiwanie metryk dla puli Elastic Database w usłudze Azure SQL</span><span class="sxs-lookup"><span data-stu-id="e6e61-113">Example 3: Get metrics for a Azure SQL Elastic Database Pool</span></span>
```
PS C:\>Get-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" | Get-Metrics -TimeGrain 0:5:0
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

<span data-ttu-id="e6e61-114">To polecenie zwraca metryki dla puli Elastic Database usługi Azure SQL o nazwie ElasticPool01.</span><span class="sxs-lookup"><span data-stu-id="e6e61-114">This command returns metrics for an Azure SQL elastic database pool named ElasticPool01.</span></span>

## <span data-ttu-id="e6e61-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6e61-115">PARAMETERS</span></span>

### <span data-ttu-id="e6e61-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6e61-116">-DefaultProfile</span></span>
<span data-ttu-id="e6e61-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e6e61-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e6e61-118">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="e6e61-118">-ElasticPoolName</span></span>
<span data-ttu-id="e6e61-119">Określa nazwę puli elastycznej, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e61-119">Specifies the name of the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e6e61-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6e61-120">-ResourceGroupName</span></span>
<span data-ttu-id="e6e61-121">Określa nazwę grupy zasobów zawierającej pulę elastyczną, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e61-121">Specifies the name of the resource group that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e6e61-122">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="e6e61-122">-ServerName</span></span>
<span data-ttu-id="e6e61-123">Określa nazwę serwera zawierającego pulę elastyczną, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6e61-123">Specifies the name of the server that contains the elastic pool that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e6e61-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6e61-124">CommonParameters</span></span>
<span data-ttu-id="e6e61-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6e61-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6e61-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6e61-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6e61-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6e61-127">INPUTS</span></span>

### <span data-ttu-id="e6e61-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e6e61-128">System.String</span></span>

## <span data-ttu-id="e6e61-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6e61-129">OUTPUTS</span></span>

### <span data-ttu-id="e6e61-130">Microsoft. Azure. Commands. SQL. ElasticPool. model. AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="e6e61-130">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="e6e61-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6e61-131">NOTES</span></span>

## <span data-ttu-id="e6e61-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6e61-132">RELATED LINKS</span></span>

[<span data-ttu-id="e6e61-133">Nowe — AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e6e61-133">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e6e61-134">Remove-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e6e61-134">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="e6e61-135">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="e6e61-135">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

