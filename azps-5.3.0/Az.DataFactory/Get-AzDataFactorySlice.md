---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501599"
---
# <span data-ttu-id="b4e78-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="b4e78-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="b4e78-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b4e78-102">SYNOPSIS</span></span>
<span data-ttu-id="b4e78-103">Pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b4e78-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="b4e78-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b4e78-104">SYNTAX</span></span>

### <span data-ttu-id="b4e78-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b4e78-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b4e78-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b4e78-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b4e78-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b4e78-107">DESCRIPTION</span></span>
<span data-ttu-id="b4e78-108">Polecenie cmdlet **Get-AzDataFactorySlice** pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b4e78-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="b4e78-109">Określ godzinę rozpoczęcia i godzinę zakończenia w celu zdefiniowania zakresu wycinków danych do wyświetlenia.</span><span class="sxs-lookup"><span data-stu-id="b4e78-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="b4e78-110">Stan wycinka danych jest jednym z następujących wartości:</span><span class="sxs-lookup"><span data-stu-id="b4e78-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="b4e78-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="b4e78-111">PendingExecution.</span></span>
<span data-ttu-id="b4e78-112">Nie rozpoczęto przetwarzania danych.</span><span class="sxs-lookup"><span data-stu-id="b4e78-112">Data processing has not started.</span></span> 
- <span data-ttu-id="b4e78-113">W trakcie.</span><span class="sxs-lookup"><span data-stu-id="b4e78-113">InProgress.</span></span>
<span data-ttu-id="b4e78-114">Trwa przetwarzanie danych.</span><span class="sxs-lookup"><span data-stu-id="b4e78-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="b4e78-115">Dostarczenia.</span><span class="sxs-lookup"><span data-stu-id="b4e78-115">Ready.</span></span>
<span data-ttu-id="b4e78-116">Przetwarzanie danych zostało zakończone.</span><span class="sxs-lookup"><span data-stu-id="b4e78-116">Data processing is completed.</span></span>
<span data-ttu-id="b4e78-117">Wycinek danych jest gotowy do użycia w wycinkach zależnych.</span><span class="sxs-lookup"><span data-stu-id="b4e78-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="b4e78-118">Nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b4e78-118">Failed.</span></span>
<span data-ttu-id="b4e78-119">Uruchomienie tego wycinka nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b4e78-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="b4e78-120">Przeskok.</span><span class="sxs-lookup"><span data-stu-id="b4e78-120">Skip.</span></span>
<span data-ttu-id="b4e78-121">Fabryka danych pomija przetwarzanie wycinka.</span><span class="sxs-lookup"><span data-stu-id="b4e78-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="b4e78-122">Ponów.</span><span class="sxs-lookup"><span data-stu-id="b4e78-122">Retry.</span></span>
<span data-ttu-id="b4e78-123">Ponowna instalacja fabryki danych, która tworzy plasterek.</span><span class="sxs-lookup"><span data-stu-id="b4e78-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="b4e78-124">Przekroczenie limitu czasu. Upłynął limit czasu przetwarzania danych.</span><span class="sxs-lookup"><span data-stu-id="b4e78-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="b4e78-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="b4e78-125">PendingValidation.</span></span>
<span data-ttu-id="b4e78-126">Przed przetworzeniem wycinka danych czeka na sprawdzenie poprawności.</span><span class="sxs-lookup"><span data-stu-id="b4e78-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="b4e78-127">Spróbuj ponownie wykonać weryfikację.</span><span class="sxs-lookup"><span data-stu-id="b4e78-127">Retry Validation.</span></span>
<span data-ttu-id="b4e78-128">Fabryka danych ponawia weryfikację wycinka.</span><span class="sxs-lookup"><span data-stu-id="b4e78-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="b4e78-129">Sprawdzanie poprawności nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b4e78-129">Failed Validation.</span></span>
<span data-ttu-id="b4e78-130">Sprawdzanie poprawności wycinka nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="b4e78-130">Validation of the slice failed.</span></span>
<span data-ttu-id="b4e78-131">W przypadku każdego wycinka możesz wyświetlić więcej informacji na temat uruchamiania, które tworzą plasterek przy użyciu Get-AzDataFactoryRun polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b4e78-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="b4e78-132">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b4e78-132">EXAMPLES</span></span>

### <span data-ttu-id="b4e78-133">Przykład 1: pobieranie wycinków danych dla zestawu danych</span><span class="sxs-lookup"><span data-stu-id="b4e78-133">Example 1: Get data slices for a dataset</span></span>
```powershell
PS C:\>Get-AzDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 1:00:00 AM
End               : 5/21/2014 2:00:00 AM
RetryCount        : 0
Status            : Ready

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 2:00:00 AM
End               : 5/21/2014 3:00:00 AM
RetryCount        : 0
Status            : Ready

. . . 

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 8:00:00 PM
End               : 5/21/2014 9:00:00 PM
RetryCount        : 0
Status            : PendingExecution

ResourceGroupName : ADF
DataFactoryName   : WikiADF
DatasetName         : DAWikiAggregatedData
Start             : 5/21/2014 9:00:00 PM
End               : 5/21/2014 10:00:00 PM
RetryCount        : 0
Status            : PendingExecution

. . .
```

<span data-ttu-id="b4e78-134">To polecenie pobiera wszystkie wycinki danych dla zestawu danych o nazwie WikiAggregatedData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="b4e78-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="b4e78-135">Polecenie pobiera wycinków wygenerowanych po upływie czasu, który określa parametr StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="b4e78-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="b4e78-136">Poniższy przykładowy kod określa dostępność tego zestawu danych co godzinę w pliku notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="b4e78-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="b4e78-137">dostępność: {period: "godzina"; periodMultiplier: 1} Niektóre wyniki są gotowe, a inne są PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="b4e78-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="b4e78-138">Gotowe plasterki są już uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b4e78-138">Ready slices have already run.</span></span>
<span data-ttu-id="b4e78-139">Oczekujące plasterki oczekują na wykonanie na końcu każdej godziny w interwale, w którym określono polecenie cmdlet Set-AzDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="b4e78-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="b4e78-140">W tym przykładzie zarówno okresy rozpoczęcia i zakończenia rurociągu oraz wycinka mają wartość jednego dnia (24 godziny).</span><span class="sxs-lookup"><span data-stu-id="b4e78-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="b4e78-141">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b4e78-141">Example 2</span></span>

<span data-ttu-id="b4e78-142">Pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="b4e78-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="b4e78-143">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="b4e78-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="b4e78-144">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b4e78-144">PARAMETERS</span></span>

### <span data-ttu-id="b4e78-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b4e78-145">-DataFactory</span></span>
<span data-ttu-id="b4e78-146">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="b4e78-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="b4e78-147">To polecenie cmdlet umożliwia pobieranie wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b4e78-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4e78-148">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="b4e78-148">-DataFactoryName</span></span>
<span data-ttu-id="b4e78-149">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="b4e78-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="b4e78-150">To polecenie cmdlet umożliwia pobieranie wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b4e78-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4e78-151">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="b4e78-151">-DatasetName</span></span>
<span data-ttu-id="b4e78-152">Określa nazwę zestawu danych, dla którego to polecenie cmdlet pobiera plasterki.</span><span class="sxs-lookup"><span data-stu-id="b4e78-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="b4e78-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4e78-153">-DefaultProfile</span></span>
<span data-ttu-id="b4e78-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="b4e78-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4e78-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="b4e78-155">-EndDateTime</span></span>
<span data-ttu-id="b4e78-156">Określa koniec okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="b4e78-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b4e78-157">To polecenie cmdlet umożliwia pobieranie wycinków wyprodukowanych przed upływem czasu, jaki ten parametr określi.</span><span class="sxs-lookup"><span data-stu-id="b4e78-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="b4e78-158">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b4e78-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b4e78-159">*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00 – 08:00 (czas standardowy)</span><span class="sxs-lookup"><span data-stu-id="b4e78-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4e78-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4e78-160">-ResourceGroupName</span></span>
<span data-ttu-id="b4e78-161">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b4e78-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="b4e78-162">To polecenie cmdlet umożliwia pobieranie wycinków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="b4e78-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4e78-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="b4e78-163">-StartDateTime</span></span>
<span data-ttu-id="b4e78-164">Określa początek okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="b4e78-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="b4e78-165">To polecenie cmdlet umożliwia pobieranie wycinków wygenerowanych po upływie czasu, jaki ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="b4e78-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="b4e78-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4e78-166">CommonParameters</span></span>
<span data-ttu-id="b4e78-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4e78-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4e78-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b4e78-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4e78-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b4e78-169">INPUTS</span></span>

### <span data-ttu-id="b4e78-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b4e78-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="b4e78-171">System. String</span><span class="sxs-lookup"><span data-stu-id="b4e78-171">System.String</span></span>

## <span data-ttu-id="b4e78-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b4e78-172">OUTPUTS</span></span>

### <span data-ttu-id="b4e78-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="b4e78-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="b4e78-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b4e78-174">NOTES</span></span>
* <span data-ttu-id="b4e78-175">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="b4e78-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b4e78-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b4e78-176">RELATED LINKS</span></span>

[<span data-ttu-id="b4e78-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="b4e78-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="b4e78-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="b4e78-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="b4e78-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="b4e78-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


