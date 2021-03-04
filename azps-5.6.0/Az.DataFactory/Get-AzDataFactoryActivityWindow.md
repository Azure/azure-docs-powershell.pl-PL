---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryActivityWindow.md
ms.openlocfilehash: 009f7033b7ecfe26e314a105d0bf88a7433962c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954746"
---
# <span data-ttu-id="0672a-101">Get-AzDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="0672a-101">Get-AzDataFactoryActivityWindow</span></span>

## <span data-ttu-id="0672a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0672a-102">SYNOPSIS</span></span>
<span data-ttu-id="0672a-103">Pobiera informacje o oknach aktywności skojarzonych z fabryczną danymi.</span><span class="sxs-lookup"><span data-stu-id="0672a-103">Gets information about activity windows associated with a data factory.</span></span>

## <span data-ttu-id="0672a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0672a-104">SYNTAX</span></span>

### <span data-ttu-id="0672a-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="0672a-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0672a-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0672a-106">ByFactoryObject</span></span>
```
Get-AzDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0672a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0672a-107">DESCRIPTION</span></span>
<span data-ttu-id="0672a-108">Polecenie **cmdlet Get-AzDataFactoryActivityWindow** pobiera informacje o oknach działań skojarzonych z fabryczną danymi.</span><span class="sxs-lookup"><span data-stu-id="0672a-108">The **Get-AzDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="0672a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0672a-109">EXAMPLES</span></span>

### <span data-ttu-id="0672a-110">Przykład 1. Uzyskiwanie okien aktywności skojarzonych z fabryczną danymi</span><span class="sxs-lookup"><span data-stu-id="0672a-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="0672a-111">To polecenie pobiera informacje o wszystkich oknach działań skojarzonych z fabryczną danymi o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0672a-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="0672a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0672a-112">PARAMETERS</span></span>

### <span data-ttu-id="0672a-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="0672a-113">-ActivityName</span></span>
<span data-ttu-id="0672a-114">Określa nazwę działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="0672a-115">To polecenie cmdlet pobiera okna aktywności dla działania, które ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="0672a-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0672a-116">-DataFactory</span></span>
<span data-ttu-id="0672a-117">Określa obiekt **PSDataFactory zwrócony** przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0672a-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="0672a-118">To polecenie cmdlet pobiera okna działań, które należą do fabrycznych danych określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="0672a-119">-DataFactoryName</span></span>
<span data-ttu-id="0672a-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0672a-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="0672a-121">To polecenie cmdlet pobiera okna działań, które należą do fabrycznych danych określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="0672a-122">-DatasetName</span></span>
<span data-ttu-id="0672a-123">Określa nazwę zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="0672a-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="0672a-124">To polecenie cmdlet pobiera okna działań, które należą do zestawu danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0672a-125">-DefaultProfile</span></span>
<span data-ttu-id="0672a-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0672a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0672a-127">— Filtr</span><span class="sxs-lookup"><span data-stu-id="0672a-127">-Filter</span></span>
<span data-ttu-id="0672a-128">Określa okno aktywności wyrażane przy użyciu gramatyki filtru usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="0672a-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="0672a-129">Aby uzyskać informacje na temat gramatyki, zobacz Składnia wyrażeń OData dla usługi Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) (w witrynie MSDN).</span><span class="sxs-lookup"><span data-stu-id="0672a-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="0672a-130">Lista okien działań jest filtrowana według ciągu wyszukiwania, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="0672a-131">-OrderBy</span></span>
<span data-ttu-id="0672a-132">Określa kolejność odpowiedzi według jednego z parametrów listy w oknie działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="0672a-133">Jest to lista właściwości oddzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="0672a-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="0672a-134">Na przykład: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="0672a-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="0672a-135">Domyślnie kolejność jest rosnąca (ASC).</span><span class="sxs-lookup"><span data-stu-id="0672a-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="0672a-136">Określ desc, jeśli lista ma być uporządkowana w kolejności malejącej.</span><span class="sxs-lookup"><span data-stu-id="0672a-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="0672a-137">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="0672a-137">-PipelineName</span></span>
<span data-ttu-id="0672a-138">Określa nazwę potoku.</span><span class="sxs-lookup"><span data-stu-id="0672a-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="0672a-139">To polecenie cmdlet pobiera okna działań, które należą do potoku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0672a-140">-ResourceGroupName</span></span>
<span data-ttu-id="0672a-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0672a-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="0672a-142">To polecenie cmdlet pobiera okna działań, które należą do grupy zasobów, która określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="0672a-143">-RunEnd</span></span>
<span data-ttu-id="0672a-144">Określa czas zakończenia uruchomienia okna działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="0672a-145">To polecenie cmdlet pobiera okna działań, których czasy uruchamiania należą między *godzinami RunStart* i *RunEnd.*</span><span class="sxs-lookup"><span data-stu-id="0672a-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="0672a-146">- RunStart</span><span class="sxs-lookup"><span data-stu-id="0672a-146">-RunStart</span></span>
<span data-ttu-id="0672a-147">Określa czas rozpoczęcia uruchomienia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="0672a-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="0672a-148">To polecenie cmdlet pobiera okna działań, których czasy uruchamiania należą między *godzinami RunStart* i *RunEnd.*</span><span class="sxs-lookup"><span data-stu-id="0672a-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="0672a-149">— Na górze</span><span class="sxs-lookup"><span data-stu-id="0672a-149">-Top</span></span>
<span data-ttu-id="0672a-150">Określa maksymalną liczbę okien działań zwracanych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0672a-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="0672a-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="0672a-151">-WindowEnd</span></span>
<span data-ttu-id="0672a-152">Określa czas zakończenia okna działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="0672a-153">To polecenie cmdlet pobiera okna aktywności, których godziny należą między *godzinami WindowStart* i *WindowEnd.*</span><span class="sxs-lookup"><span data-stu-id="0672a-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="0672a-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="0672a-154">-WindowStart</span></span>
<span data-ttu-id="0672a-155">Określa czas rozpoczęcia okna działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="0672a-156">To polecenie cmdlet pobiera okna aktywności, których godziny należą między *godzinami WindowStart* i *WindowEnd.*</span><span class="sxs-lookup"><span data-stu-id="0672a-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="0672a-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="0672a-157">-WindowState</span></span>
<span data-ttu-id="0672a-158">Określa stan okna działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="0672a-159">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0672a-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0672a-160">Brak</span><span class="sxs-lookup"><span data-stu-id="0672a-160">None</span></span>
- <span data-ttu-id="0672a-161">Oczekiwanie</span><span class="sxs-lookup"><span data-stu-id="0672a-161">Waiting</span></span>
- <span data-ttu-id="0672a-162">InProgress</span><span class="sxs-lookup"><span data-stu-id="0672a-162">InProgress</span></span>
- <span data-ttu-id="0672a-163">Gotowe</span><span class="sxs-lookup"><span data-stu-id="0672a-163">Ready</span></span>
- <span data-ttu-id="0672a-164">Niepowodzenie</span><span class="sxs-lookup"><span data-stu-id="0672a-164">Failed</span></span>
- <span data-ttu-id="0672a-165">To polecenie cmdlet pominięte pobiera okna działań, które znajdują się w stanie, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="0672a-166">-WindowSubstate</span></span>
<span data-ttu-id="0672a-167">Określa stan podrzędny okna działania.</span><span class="sxs-lookup"><span data-stu-id="0672a-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="0672a-168">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0672a-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0672a-169">Anulowano</span><span class="sxs-lookup"><span data-stu-id="0672a-169">Canceled</span></span>
- <span data-ttu-id="0672a-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="0672a-170">timedOut</span></span>
- <span data-ttu-id="0672a-171">Sprawdzania poprawności tego polecenia cmdlet pobiera okna działań, które znajdują się w stanie podrzędnym, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0672a-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="0672a-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0672a-172">CommonParameters</span></span>
<span data-ttu-id="0672a-173">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0672a-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0672a-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0672a-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0672a-175">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0672a-175">INPUTS</span></span>

### <span data-ttu-id="0672a-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="0672a-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="0672a-177">System.String</span><span class="sxs-lookup"><span data-stu-id="0672a-177">System.String</span></span>

### <span data-ttu-id="0672a-178">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0672a-178">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0672a-179">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0672a-179">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0672a-180">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0672a-180">OUTPUTS</span></span>

### <span data-ttu-id="0672a-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="0672a-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="0672a-182">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0672a-182">NOTES</span></span>

## <span data-ttu-id="0672a-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0672a-183">RELATED LINKS</span></span>

[<span data-ttu-id="0672a-184">Polecenia cmdlet usługi Azure Data Factories</span><span class="sxs-lookup"><span data-stu-id="0672a-184">Azure Data Factories Cmdlets</span></span>](./Az.DataFactory.md)


