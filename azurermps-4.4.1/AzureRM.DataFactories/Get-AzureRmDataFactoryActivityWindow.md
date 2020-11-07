---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 95d0ce0ffe48f845c15f7f00de59a70bfc466fe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716700"
---
# <span data-ttu-id="4a9cc-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="4a9cc-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="4a9cc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4a9cc-102">SYNOPSIS</span></span>
<span data-ttu-id="4a9cc-103">Pobiera informacje o oknach działań skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4a9cc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4a9cc-104">SYNTAX</span></span>

### <span data-ttu-id="4a9cc-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4a9cc-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a9cc-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="4a9cc-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4a9cc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4a9cc-107">DESCRIPTION</span></span>
<span data-ttu-id="4a9cc-108">Polecenie cmdlet **Get-AzureRmDataFactoryActivityWindow** pobiera informacje o oknach aktywności skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="4a9cc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4a9cc-109">EXAMPLES</span></span>

### <span data-ttu-id="4a9cc-110">Przykład 1: uzyskiwanie okien aktywności skojarzonych z fabryką danych</span><span class="sxs-lookup"><span data-stu-id="4a9cc-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzureRmDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/17/2016 6:00:00 AM
WindowEnd         : 8/17/2016 7:00:00 AM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : BlobToSqlCopyActivity
ActivityType      : Copy
LinkedServiceName : 
WindowState       : Waiting
WindowSubstate    : ConcurrencyLimit
Duration          : 00:00:00
InputDatasets     : {DA_CuratedWikiData}
OutputDatasets    : {DA_WikiAggregatedData}
PercentComplete   : 0
RunAttempts       : 1
RunStart          : 8/17/2016 10:05:51 PM
RunEnd            : 8/17/2016 10:05:51 PM
WindowStart       : 8/16/2016 10:00:00 PM
WindowEnd         : 8/16/2016 11:00:00 PM


ResourceGroupName : ADF
DataFactoryName   : WikiADF
PipelineName      : DP_WikipediaSamplePipeline
ActivityName      : WikiHiveActivity
ActivityType      : HDInsightHive
LinkedServiceName : HDILinkedService
WindowState       : Ready
WindowSubstate    : 
Duration          : 00:03:37.8020000
InputDatasets     : {DA_WikipediaClickEvents}
OutputDatasets    : {DA_CuratedWikiData}
PercentComplete   : 100
RunAttempts       : 1
RunStart          : 8/17/2016 11:09:23 PM
RunEnd            : 8/17/2016 11:13:01 PM
WindowStart       : 8/17/2016 3:00:00 AM
WindowEnd         : 8/17/2016 4:00:00 AM
```

<span data-ttu-id="4a9cc-111">To polecenie pobiera informacje dotyczące wszystkich okien aktywności skojarzonych z fabryką danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="4a9cc-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4a9cc-112">PARAMETERS</span></span>

### <span data-ttu-id="4a9cc-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="4a9cc-113">-ActivityName</span></span>
<span data-ttu-id="4a9cc-114">Określa nazwę działania.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="4a9cc-115">To polecenie cmdlet umożliwia pobieranie okien aktywności dla działania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="4a9cc-116">-DataFactory</span></span>
<span data-ttu-id="4a9cc-117">Określa obiekt **PSDataFactory** zwrócony przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="4a9cc-118">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a9cc-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4a9cc-119">-DataFactoryName</span></span>
<span data-ttu-id="4a9cc-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="4a9cc-121">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a9cc-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="4a9cc-122">-DatasetName</span></span>
<span data-ttu-id="4a9cc-123">Określa nazwę zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="4a9cc-124">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do zestawu danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="4a9cc-125">-Filter</span></span>
<span data-ttu-id="4a9cc-126">Określa okno aktywności, korzystając z funkcji Gramatyka filtru usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-126">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="4a9cc-127">Aby uzyskać informacje o gramatyce, zobacz Składnia wyrażenia OData dla usługi Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) w witrynie MSDN.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-127">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="4a9cc-128">Lista działań w systemie Windows jest filtrowana według ciągu wyszukiwania, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-128">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-129">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="4a9cc-129">-OrderBy</span></span>
<span data-ttu-id="4a9cc-130">Określa kolejność odpowiedzi według jednej z parametrów listy okna działania.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-130">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="4a9cc-131">To jest lista właściwości rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-131">This is a list of comma separated properties.</span></span>
<span data-ttu-id="4a9cc-132">Na przykład: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-132">For example: WindowStart, PercentComplete.</span></span>

<span data-ttu-id="4a9cc-133">Domyślnie jest to kolejność rosnąca (ASC).</span><span class="sxs-lookup"><span data-stu-id="4a9cc-133">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="4a9cc-134">Określ opis, jeśli chcesz zamówić listę w kolejności malejącej.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-134">Specify DESC if you want to order the list in descending order.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-135">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="4a9cc-135">-PipelineName</span></span>
<span data-ttu-id="4a9cc-136">Określa nazwę potoku.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="4a9cc-137">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do rurociągu określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-137">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a9cc-138">-ResourceGroupName</span></span>
<span data-ttu-id="4a9cc-139">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-139">Specifies the name of the resource group.</span></span>
<span data-ttu-id="4a9cc-140">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-140">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4a9cc-141">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="4a9cc-141">-RunEnd</span></span>
<span data-ttu-id="4a9cc-142">Określa godzinę zakończenia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-142">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="4a9cc-143">To polecenie cmdlet umożliwia pobieranie okien aktywności, których czasy pracy są między *RunStart* i *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="4a9cc-143">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-144">-RunStart</span><span class="sxs-lookup"><span data-stu-id="4a9cc-144">-RunStart</span></span>
<span data-ttu-id="4a9cc-145">Określa godzinę rozpoczęcia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-145">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="4a9cc-146">To polecenie cmdlet umożliwia pobieranie okien aktywności, których czasy pracy są między *RunStart* i *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="4a9cc-146">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-147">-Początek</span><span class="sxs-lookup"><span data-stu-id="4a9cc-147">-Top</span></span>
<span data-ttu-id="4a9cc-148">Określa maksymalną liczbę okien aktywności, które zwróci polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-148">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-149">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="4a9cc-149">-WindowEnd</span></span>
<span data-ttu-id="4a9cc-150">Umożliwia określenie godziny zakończenia okna działania.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-150">Specifies the end time of activity window.</span></span>
<span data-ttu-id="4a9cc-151">To polecenie cmdlet umożliwia pobieranie okien aktywności, których godziny mieszczą się między *WindowStart* i *WindowEnd* godzin.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-151">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-152">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="4a9cc-152">-WindowStart</span></span>
<span data-ttu-id="4a9cc-153">Umożliwia określenie godziny rozpoczęcia działania okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-153">Specifies the start time of activity window.</span></span>
<span data-ttu-id="4a9cc-154">To polecenie cmdlet umożliwia pobieranie okien aktywności, których godziny mieszczą się między *WindowStart* i *WindowEnd* godzin.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-154">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-155">-WindowState</span><span class="sxs-lookup"><span data-stu-id="4a9cc-155">-WindowState</span></span>
<span data-ttu-id="4a9cc-156">Określa stan okna działania.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-156">Specifies the state of the activity window.</span></span>
<span data-ttu-id="4a9cc-157">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4a9cc-157">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a9cc-158">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4a9cc-158">None</span></span>
- <span data-ttu-id="4a9cc-159">Czekać</span><span class="sxs-lookup"><span data-stu-id="4a9cc-159">Waiting</span></span>
- <span data-ttu-id="4a9cc-160">W trakcie</span><span class="sxs-lookup"><span data-stu-id="4a9cc-160">InProgress</span></span>
- <span data-ttu-id="4a9cc-161">Dostarczenia</span><span class="sxs-lookup"><span data-stu-id="4a9cc-161">Ready</span></span>
- <span data-ttu-id="4a9cc-162">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="4a9cc-162">Failed</span></span>
- <span data-ttu-id="4a9cc-163">Pominięte</span><span class="sxs-lookup"><span data-stu-id="4a9cc-163">Skipped</span></span>

<span data-ttu-id="4a9cc-164">To polecenie cmdlet umożliwia pobieranie okien aktywności, które są w stanie, w jakim ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-164">This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-165">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="4a9cc-165">-WindowSubstate</span></span>
<span data-ttu-id="4a9cc-166">Określa podstan okna działania.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-166">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="4a9cc-167">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="4a9cc-167">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4a9cc-168">Anulować</span><span class="sxs-lookup"><span data-stu-id="4a9cc-168">Canceled</span></span>
- <span data-ttu-id="4a9cc-169">timedOut</span><span class="sxs-lookup"><span data-stu-id="4a9cc-169">timedOut</span></span>
- <span data-ttu-id="4a9cc-170">Trwa</span><span class="sxs-lookup"><span data-stu-id="4a9cc-170">Validating</span></span>

<span data-ttu-id="4a9cc-171">To polecenie cmdlet umożliwia pobieranie okien aktywności, które są w podstanach określanych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-171">This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a9cc-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a9cc-172">-DefaultProfile</span></span>
<span data-ttu-id="4a9cc-173">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-173">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a9cc-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a9cc-174">CommonParameters</span></span>
<span data-ttu-id="4a9cc-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a9cc-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a9cc-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a9cc-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a9cc-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4a9cc-177">INPUTS</span></span>

## <span data-ttu-id="4a9cc-178">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4a9cc-178">OUTPUTS</span></span>

### <span data-ttu-id="4a9cc-179">System. Collections. Generic. list ' 1 [[Microsoft. platformy windowsazure. Commands. Utilities. PSActivyWindow; Microsoft. platformy windowsazure. Commands. w wersji = 0.8.2.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="4a9cc-179">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSActivyWindow, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="4a9cc-180">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4a9cc-180">NOTES</span></span>

## <span data-ttu-id="4a9cc-181">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4a9cc-181">RELATED LINKS</span></span>

[<span data-ttu-id="4a9cc-182">Polecenia cmdlet dotyczące fabryki danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="4a9cc-182">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


