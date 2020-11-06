---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Get-AzureRmDataFactorySlice.md
ms.openlocfilehash: 038f611edbbec0f5f6bb1be433a1c1cee8fa2990
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527690"
---
# <span data-ttu-id="cbee1-101">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="cbee1-101">Get-AzureRmDataFactorySlice</span></span>

## <span data-ttu-id="cbee1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cbee1-102">SYNOPSIS</span></span>
<span data-ttu-id="cbee1-103">Pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cbee1-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbee1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cbee1-104">SYNTAX</span></span>

### <span data-ttu-id="cbee1-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cbee1-105">ByFactoryName (Default)</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbee1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="cbee1-106">ByFactoryObject</span></span>
```
Get-AzureRmDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbee1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cbee1-107">DESCRIPTION</span></span>
<span data-ttu-id="cbee1-108">Polecenie cmdlet **Get-AzureRmDataFactorySlice** pobiera wycinków danych dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="cbee1-108">The **Get-AzureRmDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="cbee1-109">Określ godzinę rozpoczęcia i godzinę zakończenia w celu zdefiniowania zakresu wycinków danych do wyświetlenia.</span><span class="sxs-lookup"><span data-stu-id="cbee1-109">Specify a start time and an end time to define a range of data slices to view.</span></span>

<span data-ttu-id="cbee1-110">Stan wycinka danych jest jednym z następujących wartości:</span><span class="sxs-lookup"><span data-stu-id="cbee1-110">The status of a data slice is one of the following values:</span></span> 

- <span data-ttu-id="cbee1-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="cbee1-111">PendingExecution.</span></span>
<span data-ttu-id="cbee1-112">Nie rozpoczęto przetwarzania danych.</span><span class="sxs-lookup"><span data-stu-id="cbee1-112">Data processing has not started.</span></span> 
- <span data-ttu-id="cbee1-113">W trakcie.</span><span class="sxs-lookup"><span data-stu-id="cbee1-113">InProgress.</span></span>
<span data-ttu-id="cbee1-114">Trwa przetwarzanie danych.</span><span class="sxs-lookup"><span data-stu-id="cbee1-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="cbee1-115">Dostarczenia.</span><span class="sxs-lookup"><span data-stu-id="cbee1-115">Ready.</span></span>
<span data-ttu-id="cbee1-116">Przetwarzanie danych zostało zakończone.</span><span class="sxs-lookup"><span data-stu-id="cbee1-116">Data processing is completed.</span></span>
<span data-ttu-id="cbee1-117">Wycinek danych jest gotowy do użycia w wycinkach zależnych.</span><span class="sxs-lookup"><span data-stu-id="cbee1-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="cbee1-118">Nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="cbee1-118">Failed.</span></span>
<span data-ttu-id="cbee1-119">Uruchomienie tego wycinka nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="cbee1-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="cbee1-120">Przeskok.</span><span class="sxs-lookup"><span data-stu-id="cbee1-120">Skip.</span></span>
<span data-ttu-id="cbee1-121">Fabryka danych pomija przetwarzanie wycinka.</span><span class="sxs-lookup"><span data-stu-id="cbee1-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="cbee1-122">Ponów.</span><span class="sxs-lookup"><span data-stu-id="cbee1-122">Retry.</span></span>
<span data-ttu-id="cbee1-123">Ponowna instalacja fabryki danych, która tworzy plasterek.</span><span class="sxs-lookup"><span data-stu-id="cbee1-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="cbee1-124">Przekroczenie limitu czasu. Upłynął limit czasu przetwarzania danych.</span><span class="sxs-lookup"><span data-stu-id="cbee1-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="cbee1-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="cbee1-125">PendingValidation.</span></span>
<span data-ttu-id="cbee1-126">Przed przetworzeniem wycinka danych czeka na sprawdzenie poprawności.</span><span class="sxs-lookup"><span data-stu-id="cbee1-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="cbee1-127">Spróbuj ponownie wykonać weryfikację.</span><span class="sxs-lookup"><span data-stu-id="cbee1-127">Retry Validation.</span></span>
<span data-ttu-id="cbee1-128">Fabryka danych ponawia weryfikację wycinka.</span><span class="sxs-lookup"><span data-stu-id="cbee1-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="cbee1-129">Sprawdzanie poprawności nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="cbee1-129">Failed Validation.</span></span>
<span data-ttu-id="cbee1-130">Sprawdzanie poprawności wycinka nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="cbee1-130">Validation of the slice failed.</span></span>

<span data-ttu-id="cbee1-131">W przypadku każdego wycinka możesz wyświetlić więcej informacji na temat uruchamiania, które tworzą plasterek przy użyciu Get-AzureRmDataFactoryRun polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cbee1-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzureRmDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="cbee1-132">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cbee1-132">EXAMPLES</span></span>

### <span data-ttu-id="cbee1-133">Przykład 1: pobieranie wycinków danych dla zestawu danych</span><span class="sxs-lookup"><span data-stu-id="cbee1-133">Example 1: Get data slices for a dataset</span></span>
```
PS C:\>Get-AzureRmDataFactorySlice -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-20T10:00:00Z
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

<span data-ttu-id="cbee1-134">To polecenie pobiera wszystkie wycinki danych dla zestawu danych o nazwie WikiAggregatedData w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="cbee1-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="cbee1-135">Polecenie pobiera wycinków wygenerowanych po upływie czasu, który określa parametr StartDateTime.</span><span class="sxs-lookup"><span data-stu-id="cbee1-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="cbee1-136">Poniższy przykładowy kod określa dostępność tego zestawu danych co godzinę w pliku notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="cbee1-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>

                        availability: 
                        {
                        period: "Hour",
                        periodMultiplier: 1
                        }

                    Some of the results are Ready and others are PendingExecution.
<span data-ttu-id="cbee1-137">Gotowe plasterki są już uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cbee1-137">Ready slices have already run.</span></span>
<span data-ttu-id="cbee1-138">Oczekujące plasterki oczekują na wykonanie na końcu każdej godziny w interwale, w którym określono polecenie cmdlet Set-AzureRmDataFactoryPipelineActivePeriod.</span><span class="sxs-lookup"><span data-stu-id="cbee1-138">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzureRmDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="cbee1-139">W tym przykładzie zarówno okresy rozpoczęcia i zakończenia rurociągu oraz wycinka mają wartość jednego dnia (24 godziny).</span><span class="sxs-lookup"><span data-stu-id="cbee1-139">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

## <span data-ttu-id="cbee1-140">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cbee1-140">PARAMETERS</span></span>

### <span data-ttu-id="cbee1-141">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="cbee1-141">-DataFactory</span></span>
<span data-ttu-id="cbee1-142">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="cbee1-142">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="cbee1-143">To polecenie cmdlet umożliwia pobieranie wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cbee1-143">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbee1-144">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="cbee1-144">-DataFactoryName</span></span>
<span data-ttu-id="cbee1-145">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="cbee1-145">Specifies the name of a data factory.</span></span>
<span data-ttu-id="cbee1-146">To polecenie cmdlet umożliwia pobieranie wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cbee1-146">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbee1-147">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="cbee1-147">-DatasetName</span></span>
<span data-ttu-id="cbee1-148">Określa nazwę zestawu danych, dla którego to polecenie cmdlet pobiera plasterki.</span><span class="sxs-lookup"><span data-stu-id="cbee1-148">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="cbee1-149">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="cbee1-149">-EndDateTime</span></span>
<span data-ttu-id="cbee1-150">Określa koniec okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="cbee1-150">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="cbee1-151">To polecenie cmdlet umożliwia pobieranie wycinków wyprodukowanych przed upływem czasu, jaki ten parametr określi.</span><span class="sxs-lookup"><span data-stu-id="cbee1-151">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="cbee1-152">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="cbee1-152">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="cbee1-153">*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach:</span><span class="sxs-lookup"><span data-stu-id="cbee1-153">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="cbee1-154">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00 – 08 – 00 (pacyficzny czas standardowy)</span><span class="sxs-lookup"><span data-stu-id="cbee1-154">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="cbee1-155">Domyślnym wyznaczaniem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="cbee1-155">The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="cbee1-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbee1-156">-ResourceGroupName</span></span>
<span data-ttu-id="cbee1-157">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cbee1-157">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="cbee1-158">To polecenie cmdlet umożliwia pobieranie wycinków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="cbee1-158">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbee1-159">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="cbee1-159">-StartDateTime</span></span>
<span data-ttu-id="cbee1-160">Określa początek okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="cbee1-160">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="cbee1-161">To polecenie cmdlet umożliwia pobieranie wycinków wygenerowanych po upływie czasu, jaki ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="cbee1-161">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="cbee1-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbee1-162">-DefaultProfile</span></span>
<span data-ttu-id="cbee1-163">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cbee1-163">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbee1-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbee1-164">CommonParameters</span></span>
<span data-ttu-id="cbee1-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbee1-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbee1-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbee1-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbee1-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cbee1-167">INPUTS</span></span>

## <span data-ttu-id="cbee1-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cbee1-168">OUTPUTS</span></span>

### <span data-ttu-id="cbee1-169">System. Collections. Generic. list ' 1 [[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft. platformy windowsazure. Commands. Commands, Version = 0.8.2.0, Culture = neutral; PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="cbee1-169">System.Collections.Generic.List\`1[[Microsoft.WindowsAzure.Commands.Utilities.PSDataSlice, Microsoft.WindowsAzure.Commands.Utilities, Version=0.8.2.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="cbee1-170">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cbee1-170">NOTES</span></span>
* <span data-ttu-id="cbee1-171">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="cbee1-171">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="cbee1-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cbee1-172">RELATED LINKS</span></span>

[<span data-ttu-id="cbee1-173">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="cbee1-173">Set-AzureRmDataFactorySliceStatus</span></span>](./Set-AzureRmDataFactorySliceStatus.md)

[<span data-ttu-id="cbee1-174">Get-AzureRmDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="cbee1-174">Get-AzureRmDataFactoryRun</span></span>](./Get-AzureRmDataFactoryRun.md)

[<span data-ttu-id="cbee1-175">Set-AzureRmDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="cbee1-175">Set-AzureRmDataFactoryPipelineActivePeriod</span></span>](./Set-AzureRmDataFactoryPipelineActivePeriod.md)


