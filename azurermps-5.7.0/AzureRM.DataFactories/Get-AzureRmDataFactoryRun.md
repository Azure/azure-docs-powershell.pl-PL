---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 7100B5F0-A07B-4305-BF80-1F52647A03AB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryRun.md
ms.openlocfilehash: a430156dcd49e9bfd69766ab4cfe112c60aef549
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93546795"
---
# <span data-ttu-id="7294e-101">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="7294e-101">Get-AzureRmDataFactoryRun</span></span>

## <span data-ttu-id="7294e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7294e-102">SYNOPSIS</span></span>
<span data-ttu-id="7294e-103">Powoduje uruchomienie wycinka danych zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7294e-103">Gets runs for a data slice of a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7294e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7294e-104">SYNTAX</span></span>

### <span data-ttu-id="7294e-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7294e-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7294e-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="7294e-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryRun [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7294e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7294e-107">DESCRIPTION</span></span>
<span data-ttu-id="7294e-108">Polecenie cmdlet **Get-AzureRmDataFactoryRun** pobiera wycinek danych dla zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="7294e-108">The **Get-AzureRmDataFactoryRun** cmdlet gets the runs for a data slice of a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="7294e-109">Zestaw danych w fabryce danych składa się z wycinków na osi czasu.</span><span class="sxs-lookup"><span data-stu-id="7294e-109">A dataset in a data factory is composed of slices over the time axis.</span></span>
<span data-ttu-id="7294e-110">Szerokość wycinka jest określana przez harmonogram — co godzinę lub codziennie.</span><span class="sxs-lookup"><span data-stu-id="7294e-110">The width of a slice is determined by the schedule, either hourly or daily.</span></span>
<span data-ttu-id="7294e-111">Uruchomienie to jednostka przetwarzania wycinka.</span><span class="sxs-lookup"><span data-stu-id="7294e-111">A run is a unit of processing for a slice.</span></span>
<span data-ttu-id="7294e-112">W przypadku ponowienia prób lub ponownego uruchomienia wycinka z powodu błędów można wykonać co najmniej jeden z nich.</span><span class="sxs-lookup"><span data-stu-id="7294e-112">There could be one or more runs for a slice in case of retries or in case you rerun your slice due to failures.</span></span>
<span data-ttu-id="7294e-113">Plasterek jest identyfikowany według godziny rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="7294e-113">A slice is identified by its start time.</span></span>
<span data-ttu-id="7294e-114">Aby uzyskać godzinę rozpoczęcia wycinka, użyj polecenia cmdlet Get-AzureRmDataFactorySlice.</span><span class="sxs-lookup"><span data-stu-id="7294e-114">To obtain the start time of a slice, use the Get-AzureRmDataFactorySlice cmdlet.</span></span>

<span data-ttu-id="7294e-115">Aby na przykład uzyskać dostęp do następującego wycinka, użyj godziny rozpoczęcia 2015-04 — 02T20:00:00.</span><span class="sxs-lookup"><span data-stu-id="7294e-115">For example, to get a run for the following slice, use the start time 2015-04-02T20:00:00.</span></span>

<span data-ttu-id="7294e-116">ResourceGroupName: ADF datafactoryname: SPDataFactory0924 DataSetName: MarketingCampaignEffectivenessBlobDataset Start: 5/2/2014 8:00:00 PM koniec: 5/3/2014 8:00:00 PM RetryCount: 0 status: gotowe LatencyStatus:</span><span class="sxs-lookup"><span data-stu-id="7294e-116">ResourceGroupName  : ADF DataFactoryName : SPDataFactory0924 DatasetName : MarketingCampaignEffectivenessBlobDataset Start : 5/2/2014 8:00:00 PM End : 5/3/2014 8:00:00 PM RetryCount : 0 Status : Ready LatencyStatus :</span></span>

## <span data-ttu-id="7294e-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7294e-117">EXAMPLES</span></span>

### <span data-ttu-id="7294e-118">Przykład 1: uzyskiwanie zestawu danych</span><span class="sxs-lookup"><span data-stu-id="7294e-118">Example 1: Get a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactoryRun -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z
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

<span data-ttu-id="7294e-119">To polecenie pobiera wszystkie działania dla wycinków zestawu danych o nazwie DAWikiAggregatedData w fabryce danych o nazwie WikiADF, które zaczynają się od 4 PM GMT w 05/21/2014.</span><span class="sxs-lookup"><span data-stu-id="7294e-119">This command gets all runs for slices of the dataset named DAWikiAggregatedData in the data factory named WikiADF that start from 4 PM GMT on 05/21/2014.</span></span>

## <span data-ttu-id="7294e-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7294e-120">PARAMETERS</span></span>

### <span data-ttu-id="7294e-121">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="7294e-121">-DataFactory</span></span>
<span data-ttu-id="7294e-122">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="7294e-122">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="7294e-123">To polecenie cmdlet jest uruchamiane dla wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7294e-123">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: PSDataFactory
Parameter Sets: ByFactoryObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7294e-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="7294e-124">-DataFactoryName</span></span>
<span data-ttu-id="7294e-125">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="7294e-125">Specifies the name of a data factory.</span></span>
<span data-ttu-id="7294e-126">To polecenie cmdlet jest uruchamiane dla wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7294e-126">This cmdlet gets runs for slices that belong to the data factory that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7294e-127">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="7294e-127">-DatasetName</span></span>
<span data-ttu-id="7294e-128">Określa nazwę zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="7294e-128">Specifies the name of the dataset.</span></span>
<span data-ttu-id="7294e-129">To polecenie cmdlet jest uruchamiane dla wycinków należących do zestawu danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="7294e-129">This cmdlet gets runs for slices that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="7294e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7294e-130">-DefaultProfile</span></span>
<span data-ttu-id="7294e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7294e-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7294e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7294e-132">-ResourceGroupName</span></span>
<span data-ttu-id="7294e-133">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7294e-133">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="7294e-134">To polecenie cmdlet umożliwia uruchomienie fabryki dla wycinków należących do grupy, której ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="7294e-134">This cmdlet gets factory runs for slices that belong to the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7294e-135">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="7294e-135">-StartDateTime</span></span>
<span data-ttu-id="7294e-136">Określa początek okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="7294e-136">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="7294e-137">To polecenie cmdlet zostanie uruchomione dla wycinków danych, które pasują do tego przedziału czasu.</span><span class="sxs-lookup"><span data-stu-id="7294e-137">This cmdlet gets runs for the data slices that match this time period.</span></span>

<span data-ttu-id="7294e-138">*StartDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach:</span><span class="sxs-lookup"><span data-stu-id="7294e-138">*StartDateTime* must be specified in the ISO8601 format, as in the following examples:</span></span> 

<span data-ttu-id="7294e-139">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00 – 08 – 00 (pacyficzny czas standardowy)</span><span class="sxs-lookup"><span data-stu-id="7294e-139">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="7294e-140">Domyślnym wyznaczaniem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="7294e-140">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7294e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7294e-141">CommonParameters</span></span>
<span data-ttu-id="7294e-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7294e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7294e-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7294e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7294e-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7294e-144">INPUTS</span></span>

### <span data-ttu-id="7294e-145">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7294e-145">None</span></span>
<span data-ttu-id="7294e-146">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7294e-146">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7294e-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7294e-147">OUTPUTS</span></span>

### <span data-ttu-id="7294e-148">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft. platformy windowsazure. Commands. Commands, Version = 0.8.2.0, Culture = neutral; PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="7294e-148">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSliceRun, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="7294e-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7294e-149">NOTES</span></span>
* <span data-ttu-id="7294e-150">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="7294e-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="7294e-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7294e-151">RELATED LINKS</span></span>

[<span data-ttu-id="7294e-152">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="7294e-152">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


