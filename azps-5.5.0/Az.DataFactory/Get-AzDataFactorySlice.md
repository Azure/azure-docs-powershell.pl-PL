---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: C102232A-C9C8-4CEE-8535-7C7A70057B06
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryslice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactorySlice.md
ms.openlocfilehash: a71ccc37fe1c6b6811b955c5d84353dfecd66c2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242826"
---
# <span data-ttu-id="d710c-101">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="d710c-101">Get-AzDataFactorySlice</span></span>

## <span data-ttu-id="d710c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d710c-102">SYNOPSIS</span></span>
<span data-ttu-id="d710c-103">Pobiera wycinki danych dla zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d710c-103">Gets data slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="d710c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d710c-104">SYNTAX</span></span>

### <span data-ttu-id="d710c-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="d710c-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactoryName] <String> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d710c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d710c-106">ByFactoryObject</span></span>
```
Get-AzDataFactorySlice [[-EndDateTime] <DateTime>] [-DataFactory] <PSDataFactory> [-DatasetName] <String>
 [-StartDateTime] <DateTime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d710c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d710c-107">DESCRIPTION</span></span>
<span data-ttu-id="d710c-108">Polecenie **cmdlet Get-AzDataFactorySlice** pobiera wycinki danych dla zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d710c-108">The **Get-AzDataFactorySlice** cmdlet gets data slices for a dataset in Azure Data Factory.</span></span>
<span data-ttu-id="d710c-109">Określ czas rozpoczęcia i czas zakończenia, aby zdefiniować zakres wycinków danych do wyświetlenia.</span><span class="sxs-lookup"><span data-stu-id="d710c-109">Specify a start time and an end time to define a range of data slices to view.</span></span>
<span data-ttu-id="d710c-110">Stan wycinka danych jest jedną z następujących wartości:</span><span class="sxs-lookup"><span data-stu-id="d710c-110">The status of a data slice is one of the following values:</span></span> 
- <span data-ttu-id="d710c-111">PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="d710c-111">PendingExecution.</span></span>
<span data-ttu-id="d710c-112">Przetwarzanie danych nie zostało rozpoczęte.</span><span class="sxs-lookup"><span data-stu-id="d710c-112">Data processing has not started.</span></span> 
- <span data-ttu-id="d710c-113">InProgress (Ruch wychodzący).</span><span class="sxs-lookup"><span data-stu-id="d710c-113">InProgress.</span></span>
<span data-ttu-id="d710c-114">Przetwarzanie danych jest w toku.</span><span class="sxs-lookup"><span data-stu-id="d710c-114">Data processing is in progress.</span></span> 
- <span data-ttu-id="d710c-115">Gotowe.</span><span class="sxs-lookup"><span data-stu-id="d710c-115">Ready.</span></span>
<span data-ttu-id="d710c-116">Przetwarzanie danych jest ukończone.</span><span class="sxs-lookup"><span data-stu-id="d710c-116">Data processing is completed.</span></span>
<span data-ttu-id="d710c-117">Wycinek danych jest gotowy do użycia przez zależne wycinki.</span><span class="sxs-lookup"><span data-stu-id="d710c-117">The data slice is ready for dependent slices to consume it.</span></span> 
- <span data-ttu-id="d710c-118">Niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="d710c-118">Failed.</span></span>
<span data-ttu-id="d710c-119">Uruchomienie, które daje wycinek nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d710c-119">The run that produces the slice failed.</span></span> 
- <span data-ttu-id="d710c-120">Pomiń.</span><span class="sxs-lookup"><span data-stu-id="d710c-120">Skip.</span></span>
<span data-ttu-id="d710c-121">Data Factory pomija przetwarzanie wycinka.</span><span class="sxs-lookup"><span data-stu-id="d710c-121">Data Factory skips processing of the slice.</span></span> 
- <span data-ttu-id="d710c-122">Ponów próbę.</span><span class="sxs-lookup"><span data-stu-id="d710c-122">Retry.</span></span>
<span data-ttu-id="d710c-123">Data Factory ponowne uruchomienie, które tworzy wycinek.</span><span class="sxs-lookup"><span data-stu-id="d710c-123">Data Factory retries the run that produces the slice.</span></span> 
- <span data-ttu-id="d710c-124">Uchylił czas. Przetwarzanie danych zostało uchylione.</span><span class="sxs-lookup"><span data-stu-id="d710c-124">Timed Out. Data processing has timed out.</span></span> 
- <span data-ttu-id="d710c-125">PendingValidation.</span><span class="sxs-lookup"><span data-stu-id="d710c-125">PendingValidation.</span></span>
<span data-ttu-id="d710c-126">Wycinek danych oczekuje na weryfikację przed jego przetworzeniem.</span><span class="sxs-lookup"><span data-stu-id="d710c-126">Data slice is waiting for validation before it is processed.</span></span> 
- <span data-ttu-id="d710c-127">Ponów próbę sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="d710c-127">Retry Validation.</span></span>
<span data-ttu-id="d710c-128">W układzie Data Factory jest ponowne sprawdzanie poprawności wycinka.</span><span class="sxs-lookup"><span data-stu-id="d710c-128">Data Factory retries the validation of the slice.</span></span> 
- <span data-ttu-id="d710c-129">Sprawdzanie poprawności nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d710c-129">Failed Validation.</span></span>
<span data-ttu-id="d710c-130">Sprawdzanie poprawności wycinka nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="d710c-130">Validation of the slice failed.</span></span>
<span data-ttu-id="d710c-131">W przypadku każdego wycinka można uzyskać więcej informacji o uruchomieniu, dzięki Get-AzDataFactoryRun cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d710c-131">For each of the slices, you can see more information about the run that produces the slice by using the Get-AzDataFactoryRun cmdlet.</span></span>

## <span data-ttu-id="d710c-132">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d710c-132">EXAMPLES</span></span>

### <span data-ttu-id="d710c-133">Przykład 1. Uzyskiwanie wycinków danych dla zestawu danych</span><span class="sxs-lookup"><span data-stu-id="d710c-133">Example 1: Get data slices for a dataset</span></span>
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

<span data-ttu-id="d710c-134">To polecenie pobiera wszystkie wycinki danych dla zestawu danych o nazwie WikiAggregatedData w fabrycznej bazie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="d710c-134">This command gets all the data slices for the dataset named WikiAggregatedData in the data factory named WikiADF.</span></span>
<span data-ttu-id="d710c-135">Po upływie czasu, który określa parametr StartDateTime, polecenie pobiera wycinki.</span><span class="sxs-lookup"><span data-stu-id="d710c-135">The command gets slices produced after the time that the StartDateTime parameter specifies.</span></span>
<span data-ttu-id="d710c-136">Poniższy przykładowy kod ustawia dostępność tego zestawu danych co godzinę w pliku JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="d710c-136">The following example code sets the availability for this dataset every hour in the JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="d710c-137">availability: { period: "Hour", periodMultiplier: 1 } Niektóre wyniki są gotowe, a inne to PendingExecution.</span><span class="sxs-lookup"><span data-stu-id="d710c-137">availability: { period: "Hour", periodMultiplier: 1 } Some of the results are Ready and others are PendingExecution.</span></span>
<span data-ttu-id="d710c-138">Gotowe wycinki zostały już uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d710c-138">Ready slices have already run.</span></span>
<span data-ttu-id="d710c-139">Oczekujące wycinki oczekują na uruchomienie na końcu każdej godziny w interwale, który określa Set-AzDataFactoryPipelineActivePeriod cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d710c-139">The pending slices are waiting to run at the end of each hour in the interval that the Set-AzDataFactoryPipelineActivePeriod cmdlet specifies.</span></span>
<span data-ttu-id="d710c-140">W tym przykładzie zarówno okresy rozpoczęcia, jak i zakończenia dla potoku i wycinka mają wartość jednego dnia (24 godziny).</span><span class="sxs-lookup"><span data-stu-id="d710c-140">In this example, both start and end periods for the pipeline and the slice have a value of one day (24 hours).</span></span>

### <span data-ttu-id="d710c-141">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d710c-141">Example 2</span></span>

<span data-ttu-id="d710c-142">Pobiera wycinki danych dla zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="d710c-142">Gets data slices for a dataset in Azure Data Factory.</span></span> <span data-ttu-id="d710c-143">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="d710c-143">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzDataFactorySlice -DataFactoryName 'WikiADF' -DatasetName 'DAWikiAggregatedData' -EndDateTime 2014-05-22T16:00:00Z -ResourceGroupName 'ADF' -StartDateTime 2014-05-20T10:00:00Z
```

## <span data-ttu-id="d710c-144">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d710c-144">PARAMETERS</span></span>

### <span data-ttu-id="d710c-145">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d710c-145">-DataFactory</span></span>
<span data-ttu-id="d710c-146">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="d710c-146">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="d710c-147">To polecenie cmdlet pobiera wycinki należące do fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d710c-147">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d710c-148">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d710c-148">-DataFactoryName</span></span>
<span data-ttu-id="d710c-149">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="d710c-149">Specifies the name of a data factory.</span></span>
<span data-ttu-id="d710c-150">To polecenie cmdlet pobiera wycinki należące do fabryki danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d710c-150">This cmdlet gets slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="d710c-151">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="d710c-151">-DatasetName</span></span>
<span data-ttu-id="d710c-152">Określa nazwę zestawu danych, dla którego to polecenie cmdlet pobiera wycinki.</span><span class="sxs-lookup"><span data-stu-id="d710c-152">Specifies the name of the dataset for which this cmdlet gets slices.</span></span>

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

### <span data-ttu-id="d710c-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d710c-153">-DefaultProfile</span></span>
<span data-ttu-id="d710c-154">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d710c-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d710c-155">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="d710c-155">-EndDateTime</span></span>
<span data-ttu-id="d710c-156">Określa koniec okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="d710c-156">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d710c-157">To polecenie cmdlet pobiera wycinki przed czasem, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d710c-157">This cmdlet gets slices produced before the time that this parameter specifies.</span></span>
<span data-ttu-id="d710c-158">Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.</span><span class="sxs-lookup"><span data-stu-id="d710c-158">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="d710c-159">*Wartość EndDateTime* musi zostać określona w formacie ISO8601, jak podano w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (pacyficzny czas standardowy) Domyślnym projektem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="d710c-159">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="d710c-160">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d710c-160">-ResourceGroupName</span></span>
<span data-ttu-id="d710c-161">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d710c-161">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="d710c-162">To polecenie cmdlet pobiera wycinki należące do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d710c-162">This cmdlet gets slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="d710c-163">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="d710c-163">-StartDateTime</span></span>
<span data-ttu-id="d710c-164">Określa początek okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="d710c-164">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="d710c-165">To polecenie cmdlet pobiera wycinki po upływie czasu, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="d710c-165">This cmdlet gets slices produced after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="d710c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d710c-166">CommonParameters</span></span>
<span data-ttu-id="d710c-167">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d710c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d710c-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d710c-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d710c-169">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d710c-169">INPUTS</span></span>

### <span data-ttu-id="d710c-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d710c-170">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="d710c-171">System.String</span><span class="sxs-lookup"><span data-stu-id="d710c-171">System.String</span></span>

## <span data-ttu-id="d710c-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d710c-172">OUTPUTS</span></span>

### <span data-ttu-id="d710c-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span><span class="sxs-lookup"><span data-stu-id="d710c-173">Microsoft.Azure.Commands.DataFactories.Models.PSDataSlice</span></span>

## <span data-ttu-id="d710c-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d710c-174">NOTES</span></span>
* <span data-ttu-id="d710c-175">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="d710c-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d710c-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d710c-176">RELATED LINKS</span></span>

[<span data-ttu-id="d710c-177">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="d710c-177">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)

[<span data-ttu-id="d710c-178">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="d710c-178">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="d710c-179">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="d710c-179">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)


