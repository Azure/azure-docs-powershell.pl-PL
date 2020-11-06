---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: F8C67F7B-64C5-45E4-A0BF-32212BEBE885
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryactivitywindow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactoryActivityWindow.md
ms.openlocfilehash: 79ac0191f7fe381be4985d53ed719fdeff9d0b88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552155"
---
# <span data-ttu-id="58cea-101">Get-AzureRmDataFactoryActivityWindow</span><span class="sxs-lookup"><span data-stu-id="58cea-101">Get-AzureRmDataFactoryActivityWindow</span></span>

## <span data-ttu-id="58cea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="58cea-102">SYNOPSIS</span></span>
<span data-ttu-id="58cea-103">Pobiera informacje o oknach działań skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="58cea-103">Gets information about activity windows associated with a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="58cea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="58cea-104">SYNTAX</span></span>

### <span data-ttu-id="58cea-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="58cea-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactoryName] <String> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58cea-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="58cea-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactoryActivityWindow [-DataFactory] <PSDataFactory> [[-DatasetName] <String>]
 [[-PipelineName] <String>] [[-ActivityName] <String>] [-WindowState <String>] [-WindowSubstate <String>]
 [-Filter <String>] [-OrderBy <String>] [-WindowStart <DateTime>] [-WindowEnd <DateTime>]
 [-RunStart <DateTime>] [-RunEnd <DateTime>] [-Top <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58cea-107">Opis</span><span class="sxs-lookup"><span data-stu-id="58cea-107">DESCRIPTION</span></span>
<span data-ttu-id="58cea-108">Polecenie cmdlet **Get-AzureRmDataFactoryActivityWindow** pobiera informacje o oknach aktywności skojarzonych z fabryką danych.</span><span class="sxs-lookup"><span data-stu-id="58cea-108">The **Get-AzureRmDataFactoryActivityWindow** cmdlet gets information about the activity windows associated with a data factory.</span></span>

## <span data-ttu-id="58cea-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="58cea-109">EXAMPLES</span></span>

### <span data-ttu-id="58cea-110">Przykład 1: uzyskiwanie okien aktywności skojarzonych z fabryką danych</span><span class="sxs-lookup"><span data-stu-id="58cea-110">Example 1: Get activity windows associated with a data factory</span></span>
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

<span data-ttu-id="58cea-111">To polecenie pobiera informacje dotyczące wszystkich okien aktywności skojarzonych z fabryką danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="58cea-111">This command gets information about all activity window associated with the data factory named WikiADF.</span></span>

## <span data-ttu-id="58cea-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="58cea-112">PARAMETERS</span></span>

### <span data-ttu-id="58cea-113">-ActivityName</span><span class="sxs-lookup"><span data-stu-id="58cea-113">-ActivityName</span></span>
<span data-ttu-id="58cea-114">Określa nazwę działania.</span><span class="sxs-lookup"><span data-stu-id="58cea-114">Specifies the name of the activity.</span></span>
<span data-ttu-id="58cea-115">To polecenie cmdlet umożliwia pobieranie okien aktywności dla działania, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-115">This cmdlet gets activity windows for the activity that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="58cea-116">-DataFactory</span></span>
<span data-ttu-id="58cea-117">Określa obiekt **PSDataFactory** zwrócony przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58cea-117">Specifies a **PSDataFactory** object returned by a cmdlet.</span></span>
<span data-ttu-id="58cea-118">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-118">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="58cea-119">-DataFactoryName</span></span>
<span data-ttu-id="58cea-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="58cea-120">Specifies the name of the data factory.</span></span>
<span data-ttu-id="58cea-121">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-121">This cmdlet gets activity windows that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="58cea-122">-DatasetName</span></span>
<span data-ttu-id="58cea-123">Określa nazwę zestawu danych.</span><span class="sxs-lookup"><span data-stu-id="58cea-123">Specifies the name of the dataset.</span></span>
<span data-ttu-id="58cea-124">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do zestawu danych, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-124">This cmdlet gets activity windows that belong to the dataset that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58cea-125">-DefaultProfile</span></span>
<span data-ttu-id="58cea-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="58cea-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58cea-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="58cea-127">-Filter</span></span>
<span data-ttu-id="58cea-128">Określa okno aktywności, korzystając z funkcji Gramatyka filtru usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="58cea-128">Specifies the activity window expressed by using Azure Search filter grammar.</span></span>
<span data-ttu-id="58cea-129">Aby uzyskać informacje o gramatyce, zobacz Składnia wyrażenia OData dla usługi Azure Search https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx ( https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) w witrynie MSDN.</span><span class="sxs-lookup"><span data-stu-id="58cea-129">For information about the grammar, see OData Expression Syntax for Azure Searchhttps://msdn.microsoft.com/en-us/library/azure/dn798921.aspx (https://msdn.microsoft.com/en-us/library/azure/dn798921.aspx) in MSDN.</span></span>
<span data-ttu-id="58cea-130">Lista działań w systemie Windows jest filtrowana według ciągu wyszukiwania, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-130">The activity windows list is filtered by the search string that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-131">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="58cea-131">-OrderBy</span></span>
<span data-ttu-id="58cea-132">Określa kolejność odpowiedzi według jednej z parametrów listy okna działania.</span><span class="sxs-lookup"><span data-stu-id="58cea-132">Specifies to order the response by one of the activity window list parameters.</span></span>
<span data-ttu-id="58cea-133">To jest lista właściwości rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="58cea-133">This is a list of comma separated properties.</span></span>
<span data-ttu-id="58cea-134">Na przykład: WindowStart, PercentComplete.</span><span class="sxs-lookup"><span data-stu-id="58cea-134">For example: WindowStart, PercentComplete.</span></span>
<span data-ttu-id="58cea-135">Domyślnie jest to kolejność rosnąca (ASC).</span><span class="sxs-lookup"><span data-stu-id="58cea-135">By default, the order is ascending order (ASC).</span></span>
<span data-ttu-id="58cea-136">Określ opis, jeśli chcesz zamówić listę w kolejności malejącej.</span><span class="sxs-lookup"><span data-stu-id="58cea-136">Specify DESC if you want to order the list in descending order.</span></span>

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

### <span data-ttu-id="58cea-137">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="58cea-137">-PipelineName</span></span>
<span data-ttu-id="58cea-138">Określa nazwę potoku.</span><span class="sxs-lookup"><span data-stu-id="58cea-138">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="58cea-139">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do rurociągu określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-139">This cmdlet gets activity windows that belong to the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58cea-140">-ResourceGroupName</span></span>
<span data-ttu-id="58cea-141">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="58cea-141">Specifies the name of the resource group.</span></span>
<span data-ttu-id="58cea-142">To polecenie cmdlet umożliwia pobieranie okien aktywności należących do grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-142">This cmdlet gets activity windows that belong to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-143">-RunEnd</span><span class="sxs-lookup"><span data-stu-id="58cea-143">-RunEnd</span></span>
<span data-ttu-id="58cea-144">Określa godzinę zakończenia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="58cea-144">Specifies the end time of the activity window run.</span></span>
<span data-ttu-id="58cea-145">To polecenie cmdlet umożliwia pobieranie okien aktywności, których czasy pracy są między *RunStart* i *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="58cea-145">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="58cea-146">-RunStart</span><span class="sxs-lookup"><span data-stu-id="58cea-146">-RunStart</span></span>
<span data-ttu-id="58cea-147">Określa godzinę rozpoczęcia okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="58cea-147">Specifies the start time of the activity window run.</span></span>
<span data-ttu-id="58cea-148">To polecenie cmdlet umożliwia pobieranie okien aktywności, których czasy pracy są między *RunStart* i *RunEnd* .</span><span class="sxs-lookup"><span data-stu-id="58cea-148">This cmdlet gets activity windows whose run times fall between *RunStart* and *RunEnd* times.</span></span>

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

### <span data-ttu-id="58cea-149">-Początek</span><span class="sxs-lookup"><span data-stu-id="58cea-149">-Top</span></span>
<span data-ttu-id="58cea-150">Określa maksymalną liczbę okien aktywności, które zwróci polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="58cea-150">Specifies the maximum number of activity windows that this cmdlet returns.</span></span>

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

### <span data-ttu-id="58cea-151">-WindowEnd</span><span class="sxs-lookup"><span data-stu-id="58cea-151">-WindowEnd</span></span>
<span data-ttu-id="58cea-152">Umożliwia określenie godziny zakończenia okna działania.</span><span class="sxs-lookup"><span data-stu-id="58cea-152">Specifies the end time of activity window.</span></span>
<span data-ttu-id="58cea-153">To polecenie cmdlet umożliwia pobieranie okien aktywności, których godziny mieszczą się między *WindowStart* i *WindowEnd* godzin.</span><span class="sxs-lookup"><span data-stu-id="58cea-153">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="58cea-154">-WindowStart</span><span class="sxs-lookup"><span data-stu-id="58cea-154">-WindowStart</span></span>
<span data-ttu-id="58cea-155">Umożliwia określenie godziny rozpoczęcia działania okna aktywności.</span><span class="sxs-lookup"><span data-stu-id="58cea-155">Specifies the start time of activity window.</span></span>
<span data-ttu-id="58cea-156">To polecenie cmdlet umożliwia pobieranie okien aktywności, których godziny mieszczą się między *WindowStart* i *WindowEnd* godzin.</span><span class="sxs-lookup"><span data-stu-id="58cea-156">This cmdlet gets activity windows whose times fall between *WindowStart* and *WindowEnd* times.</span></span>

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

### <span data-ttu-id="58cea-157">-WindowState</span><span class="sxs-lookup"><span data-stu-id="58cea-157">-WindowState</span></span>
<span data-ttu-id="58cea-158">Określa stan okna działania.</span><span class="sxs-lookup"><span data-stu-id="58cea-158">Specifies the state of the activity window.</span></span>
<span data-ttu-id="58cea-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58cea-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58cea-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="58cea-160">None</span></span>
- <span data-ttu-id="58cea-161">Czekać</span><span class="sxs-lookup"><span data-stu-id="58cea-161">Waiting</span></span>
- <span data-ttu-id="58cea-162">W trakcie</span><span class="sxs-lookup"><span data-stu-id="58cea-162">InProgress</span></span>
- <span data-ttu-id="58cea-163">Dostarczenia</span><span class="sxs-lookup"><span data-stu-id="58cea-163">Ready</span></span>
- <span data-ttu-id="58cea-164">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="58cea-164">Failed</span></span>
- <span data-ttu-id="58cea-165">Pominięto to polecenie cmdlet umożliwia pobieranie okien aktywności, które są w stanie, w jakim ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="58cea-165">Skipped This cmdlet gets activity windows that are in the state that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-166">-WindowSubstate</span><span class="sxs-lookup"><span data-stu-id="58cea-166">-WindowSubstate</span></span>
<span data-ttu-id="58cea-167">Określa podstan okna działania.</span><span class="sxs-lookup"><span data-stu-id="58cea-167">Specifies the substate of the activity window.</span></span>
<span data-ttu-id="58cea-168">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="58cea-168">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58cea-169">Anulować</span><span class="sxs-lookup"><span data-stu-id="58cea-169">Canceled</span></span>
- <span data-ttu-id="58cea-170">timedOut</span><span class="sxs-lookup"><span data-stu-id="58cea-170">timedOut</span></span>
- <span data-ttu-id="58cea-171">Sprawdzanie, czy to polecenie cmdlet umożliwia pobieranie okien aktywności, które są w podstanach, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="58cea-171">Validating This cmdlet gets activity windows that are in the substate that this parameter specifies.</span></span>

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

### <span data-ttu-id="58cea-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58cea-172">CommonParameters</span></span>
<span data-ttu-id="58cea-173">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58cea-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58cea-174">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58cea-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58cea-175">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58cea-175">INPUTS</span></span>

### <span data-ttu-id="58cea-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="58cea-176">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="58cea-177">System. String</span><span class="sxs-lookup"><span data-stu-id="58cea-177">System.String</span></span>

### <span data-ttu-id="58cea-178">System. Nullable "1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="58cea-178">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="58cea-179">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="58cea-179">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="58cea-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="58cea-180">OUTPUTS</span></span>

### <span data-ttu-id="58cea-181">Microsoft. Azure. Commands. datafactors. models. PSActivityWindow</span><span class="sxs-lookup"><span data-stu-id="58cea-181">Microsoft.Azure.Commands.DataFactories.Models.PSActivityWindow</span></span>

## <span data-ttu-id="58cea-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="58cea-182">NOTES</span></span>

## <span data-ttu-id="58cea-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58cea-183">RELATED LINKS</span></span>

[<span data-ttu-id="58cea-184">Polecenia cmdlet dotyczące fabryki danych platformy Azure</span><span class="sxs-lookup"><span data-stu-id="58cea-184">Azure Data Factories Cmdlets</span></span>](./AzureRM.DataFactories.md)


