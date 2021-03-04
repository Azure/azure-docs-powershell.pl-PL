---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryRun.md
ms.openlocfilehash: 2dbab7978716d6bb960c1804abf9e86246571e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975329"
---
# <span data-ttu-id="cab4c-101">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="cab4c-101">Get-AzDataFactoryRun</span></span>

## <span data-ttu-id="cab4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab4c-102">SYNOPSIS</span></span>
<span data-ttu-id="cab4c-103">Działa dla wycinka danych zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cab4c-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="cab4c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cab4c-104">SYNTAX</span></span>

### <span data-ttu-id="cab4c-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="cab4c-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cab4c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cab4c-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cab4c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cab4c-107">DESCRIPTION</span></span>
<span data-ttu-id="cab4c-108">Polecenie **cmdlet Get-AzDataFactoryRun** pobiera uruchamiany dla wycinka danych zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cab4c-108">The **Get-AzDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="cab4c-109">Zestaw danych w zakładzie danych składa się z wycinków na osi czasu.</span><span class="sxs-lookup"><span data-stu-id="cab4c-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="cab4c-110">Szerokość wycinka jest ustalana na podstawie harmonogramu co godzinę lub raz dziennie.</span><span class="sxs-lookup"><span data-stu-id="cab4c-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="cab4c-111">Uruchomienie to jednostka przetwarzania wycinka.</span><span class="sxs-lookup"><span data-stu-id="cab4c-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="cab4c-112">W przypadku ponownego uruchomień wycinków może być jedno lub więcej uruchomień dla wycinków w przypadku ponownego uruchomień z powodu niepowodzeń.</span><span class="sxs-lookup"><span data-stu-id="cab4c-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="cab4c-113">Wycinek jest oznaczony godziną rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="cab4c-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="cab4c-114">Aby uzyskać czas rozpoczęcia wycinka, użyj Get-AzDataFactorySlice cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cab4c-114">To obtain the start time of a slice, use the Get-AzDataFactorySlice cmdlet.</span></span>
<span data-ttu-id="cab4c-115">Aby na przykład uruchomić poniższy wycinek, użyj godziny rozpoczęcia 2015-04-02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="cab4c-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>
<span data-ttu-id="cab4c-116">ResourceGroupName: ADF DataFactoryName: SPDataFactory0924 DatasetName: MarketingDataaignEffectivenessBlobDataset Start: 2014-05-02 8:00:00 End: 2014-05-03 8:00:00: 0 Status: Ready LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="cab4c-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="cab4c-117">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cab4c-117">EXAMPLES</span></span>

### <span data-ttu-id="cab4c-118">Przykład 1. Uzyskiwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="cab4c-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
Id                  : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ResourceGroupName   : ADF
DataFactoryName     : WikiADF
DatasetName           : DAWikiAggregatedData
PipelineName        : 249ea141-ca00-8597-fad9-a148e5e7bdba
ActivityId          : fcefe2bd-39b1-2d7a-7b35-bcc2b0432300
ResumptionToken     : a7c4913c-9623-49b3-ae1e-3e45e2b68819
ContinuationToken   : 
ProcessingStartTime : 5/21/2014 5:02:41 PM
ProcessingEndTime   : 5/21/2014 5:04:12 PM
PercentComplete     : 100
DataSliceStart      : 5/21/2014 4:00:00 PM
DataSliceEnd        : 5/21/2014 5:00:00 PM
Status              : Succeeded
Timestamp           : 5/21/2014 5:02:41 PM
RetryAttempt        : 0
Properties          : {[errors, ]} 
ErrorMessage        :
```

<span data-ttu-id="cab4c-119">To polecenie pobiera wszystkie uruchomienia dla wycinków zestawu danych o nazwie DAWikiAggregatedData w fabrycznej bazie danych o nazwie WikiADF, których data rozpoczęcia się od 16:00 gmt 2014-05-21.</span><span class="sxs-lookup"><span data-stu-id="cab4c-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="cab4c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cab4c-120">PARAMETERS</span></span>

### <span data-ttu-id="cab4c-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cab4c-121">-DataFactory</span></span>
<span data-ttu-id="cab4c-122">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="cab4c-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cab4c-123">To polecenie cmdlet jest uruchamiane dla wycinków należących do fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cab4c-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab4c-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="cab4c-124">-DataFactoryName</span></span>
<span data-ttu-id="cab4c-125">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cab4c-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cab4c-126">To polecenie cmdlet jest uruchamiane dla wycinków należących do fabrycznych danych określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cab4c-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab4c-127">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="cab4c-127">-DatasetName</span></span>
<span data-ttu-id="cab4c-128">Określa nazwę zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="cab4c-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="cab4c-129">To polecenie cmdlet jest uruchamiane dla wycinków należących do zestawu danych, który jest określany przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cab4c-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="cab4c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab4c-130">-DefaultProfile</span></span>
<span data-ttu-id="cab4c-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="cab4c-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cab4c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab4c-132">-ResourceGroupName</span></span>
<span data-ttu-id="cab4c-133">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cab4c-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cab4c-134">To polecenie cmdlet powoduje, że jest uruchamiane fabryczne dla wycinków należących do grupy, które określono dla tego parametru.</span><span class="sxs-lookup"><span data-stu-id="cab4c-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cab4c-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="cab4c-135">-StartDateTime</span></span>
<span data-ttu-id="cab4c-136">Określa początek okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="cab4c-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="cab4c-137">To polecenie cmdlet jest uruchamiane dla wycinków danych, które pasują do tego okresu.</span><span class="sxs-lookup"><span data-stu-id="cab4c-137">This cmdlet gets runs for the data slices that match this time period.</span></span>
<span data-ttu-id="cab4c-138">*Wartość StartDateTime* musi zostać określona w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01 01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (pacyficzny czas standardowy) Domyślnym projektem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="cab4c-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cab4c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab4c-139">CommonParameters</span></span>
<span data-ttu-id="cab4c-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab4c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab4c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cab4c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab4c-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cab4c-142">INPUTS</span></span>

### <span data-ttu-id="cab4c-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="cab4c-143">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="cab4c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cab4c-144">System.String</span></span>

## <span data-ttu-id="cab4c-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cab4c-145">OUTPUTS</span></span>

### <span data-ttu-id="cab4c-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span><span class="sxs-lookup"><span data-stu-id="cab4c-146">Microsoft.Azure.Commands.DataFactories.Models.PSDataSliceRun</span></span>

## <span data-ttu-id="cab4c-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cab4c-147">NOTES</span></span>
* <span data-ttu-id="cab4c-148">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cab4c-148">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cab4c-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cab4c-149">RELATED LINKS</span></span>

[<span data-ttu-id="cab4c-150">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="cab4c-150">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


