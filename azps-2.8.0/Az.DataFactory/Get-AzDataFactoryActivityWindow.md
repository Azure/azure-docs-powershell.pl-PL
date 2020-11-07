---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 3e79f4c11a5df5da8c01c323405f78c36aa5245b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706055"
---
# <span data-ttu-id="57e95-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="57e95-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="57e95-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="57e95-102">SYNOPSIS</span></span>
<span data-ttu-id="57e95-103">Pobiera informacje o oknach działań skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="57e95-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="57e95-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="57e95-104">SYNTAX</span></span>

### <span data-ttu-id="57e95-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="57e95-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e95-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="57e95-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57e95-107">Opis</span><span class="sxs-lookup"><span data-stu-id="57e95-107">DESCRIPTION</span></span>
<span data-ttu-id="57e95-108">Polecenie cmdlet **Get-AzDataFactoryActivityWindow** pobiera informacje o oknach aktywności skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="57e95-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="57e95-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="57e95-109">EXAMPLES</span></span>

### <span data-ttu-id="57e95-110">Przykład 1: uzyskiwanie okien aktywności skojarzonych z fabryką danych</span><span class="sxs-lookup"><span data-stu-id="57e95-110">Example 1: Get activity windows associated with a data factory</span></span>
```
PS C:\>Get-AzDataFactoryActivityWindow -DataFactoryName "WikiADF" -ResourceGroupName "ADF" -Top 3
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

<span data-ttu-id="57e95-111">To polecenie pobiera informacje dotyczące wszystkich okien aktywności skojarzonych z fabryką danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="57e95-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="57e95-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="57e95-112">PARAMETERS</span></span>

### <span data-ttu-id="57e95-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="57e95-113">-ActivityName</span></span>
<span data-ttu-id="57e95-114">Określa nazwę działania.</span><span class="sxs-lookup"><span data-stu-id="57e95-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="57e95-115">To polecenie cmdlet umożliwia pobieranie okien aktywności dla działania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="57e95-116">-DataFactory</span></span>
<span data-ttu-id="57e95-117">Określa obiekt **PSDataFactory** zwrócony przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e95-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="57e95-118">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="57e95-119">-DataFactoryName</span></span>
<span data-ttu-id="57e95-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="57e95-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="57e95-121">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="57e95-122">-DatasetName</span></span>
<span data-ttu-id="57e95-123">Określa nazwę zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="57e95-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="57e95-124">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do zestawu danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e95-125">-DefaultProfile</span></span>
<span data-ttu-id="57e95-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="57e95-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57e95-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="57e95-127">-Filter</span></span>
<span data-ttu-id="57e95-128">Określa okno aktywności, korzystając z funkcji Gramatyka filtru usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="57e95-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="57e95-129">Aby uzyskać informacje o gramatyce, zobacz Składnia wyrażenia OData dla usługi Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) w witrynie MSDN.</span><span class="sxs-lookup"><span data-stu-id="57e95-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="57e95-130">Lista działań w systemie Windows jest filtrowana według ciągu wyszukiwania, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="57e95-131">-OrderBy</span></span>
<span data-ttu-id="57e95-132">Określa kolejność odpowiedzi według jednej z parametrów listy okna działania.</span><span class="sxs-lookup"><span data-stu-id="57e95-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="57e95-133">To jest lista właściwości rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="57e95-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="57e95-134">Na przykład: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="57e95-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="57e95-135">Domyślnie jest to kolejność rosnąca (ASC).</span><span class="sxs-lookup"><span data-stu-id="57e95-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="57e95-136">Określ opis, jeśli chcesz zamówić listę w kolejności malejącej.</span><span class="sxs-lookup"><span data-stu-id="57e95-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="57e95-137">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="57e95-137">-PipelineName</span></span>
<span data-ttu-id="57e95-138">Określa nazwę potoku.</span><span class="sxs-lookup"><span data-stu-id="57e95-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="57e95-139">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do rurociągu określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e95-140">-ResourceGroupName</span></span>
<span data-ttu-id="57e95-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="57e95-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="57e95-142">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="57e95-143">-RunEnd</span></span>
<span data-ttu-id="57e95-144">Określa godzinę zakończenia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="57e95-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="57e95-145">To polecenie cmdlet umożliwia pobieranie okien aktywności, których czasy pracy są między *RunStart* i *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="57e95-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="57e95-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="57e95-146">-RunStart</span></span>
<span data-ttu-id="57e95-147">Określa godzinę rozpoczęcia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="57e95-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="57e95-148">To polecenie cmdlet umożliwia pobieranie okien aktywności, których czasy pracy są między *RunStart* i *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="57e95-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="57e95-149">-Początek</span><span class="sxs-lookup"><span data-stu-id="57e95-149">-Top</span></span>
<span data-ttu-id="57e95-150">Określa maksymalną liczbę okien aktywności, które zwróci polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="57e95-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="57e95-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="57e95-151">-WindowEnd</span></span>
<span data-ttu-id="57e95-152">Umożliwia określenie godziny zakończenia okna działania.</span><span class="sxs-lookup"><span data-stu-id="57e95-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="57e95-153">To polecenie cmdlet umożliwia pobieranie okien aktywności, których godziny mieszczą się między *WindowStart* i *WindowEnd* godzin.</span><span class="sxs-lookup"><span data-stu-id="57e95-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="57e95-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="57e95-154">-WindowStart</span></span>
<span data-ttu-id="57e95-155">Umożliwia określenie godziny rozpoczęcia działania okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="57e95-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="57e95-156">To polecenie cmdlet umożliwia pobieranie okien aktywności, których godziny mieszczą się między *WindowStart* i *WindowEnd* godzin.</span><span class="sxs-lookup"><span data-stu-id="57e95-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="57e95-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="57e95-157">-WindowState</span></span>
<span data-ttu-id="57e95-158">Określa stan okna działania.</span><span class="sxs-lookup"><span data-stu-id="57e95-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="57e95-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="57e95-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="57e95-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="57e95-160">None</span></span>
- <span data-ttu-id="57e95-161">Czekać</span><span class="sxs-lookup"><span data-stu-id="57e95-161">Waiting</span></span>
- <span data-ttu-id="57e95-162">W trakcie</span><span class="sxs-lookup"><span data-stu-id="57e95-162">InProgress</span></span>
- <span data-ttu-id="57e95-163">Dostarczenia</span><span class="sxs-lookup"><span data-stu-id="57e95-163">Ready</span></span>
- <span data-ttu-id="57e95-164">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="57e95-164">Failed</span></span>
- <span data-ttu-id="57e95-165">Pominięto to polecenie cmdlet umożliwia pobieranie okien aktywności, które są w stanie, w jakim ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="57e95-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="57e95-166">-WindowSubstate</span></span>
<span data-ttu-id="57e95-167">Określa podstan okna działania.</span><span class="sxs-lookup"><span data-stu-id="57e95-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="57e95-168">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="57e95-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="57e95-169">Anulować</span><span class="sxs-lookup"><span data-stu-id="57e95-169">Canceled</span></span>
- <span data-ttu-id="57e95-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="57e95-170">timedOut</span></span>
- <span data-ttu-id="57e95-171">Sprawdzanie, czy to polecenie cmdlet umożliwia pobieranie okien aktywności, które są w podstanach, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="57e95-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="57e95-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e95-172">CommonParameters</span></span>
<span data-ttu-id="57e95-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e95-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e95-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e95-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e95-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="57e95-175">INPUTS</span></span>

### <span data-ttu-id="57e95-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="57e95-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="57e95-177">System. String</span><span class="sxs-lookup"><span data-stu-id="57e95-177">System.String</span></span>

### <span data-ttu-id="57e95-178">System. Nullable "1 [[System. DateTime, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57e95-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="57e95-179">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="57e95-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="57e95-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="57e95-180">OUTPUTS</span></span>

### <span data-ttu-id="57e95-181">Microsoft. Azure. Commands. datafactors. models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="57e95-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="57e95-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="57e95-182">NOTES</span></span>

## <span data-ttu-id="57e95-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="57e95-183">RELATED LINKS</span></span>

[<span data-ttu-id="57e95-184">Polecenia cmdlet dotyczące fabryki danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="57e95-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


