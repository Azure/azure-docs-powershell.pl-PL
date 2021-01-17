---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 8b2c55a069463120b861f1ea928ac0163a4c37df
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362308"
---
# <span data-ttu-id="eb25b-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="eb25b-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="eb25b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb25b-102">SYNOPSIS</span></span>
<span data-ttu-id="eb25b-103">Ustawia stan wycinków dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="eb25b-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="eb25b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb25b-104">SYNTAX</span></span>

### <span data-ttu-id="eb25b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb25b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb25b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="eb25b-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb25b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="eb25b-107">DESCRIPTION</span></span>
<span data-ttu-id="eb25b-108">Polecenie cmdlet **Set-AzDataFactorySliceStatus** ustawia stan wycinków dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="eb25b-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="eb25b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb25b-109">EXAMPLES</span></span>

### <span data-ttu-id="eb25b-110">Przykład 1. Ustawianie stanu wszystkich wycinków</span><span class="sxs-lookup"><span data-stu-id="eb25b-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="eb25b-111">To polecenie ustawia stan wszystkich wycinków dla zestawu danych o nazwie DAWikiAggregatedData, aby oczekiwać w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="eb25b-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="eb25b-112">Parametr *UpdateType* ma wartość UpstreamInPipeline, więc polecenie ustawia stan każdego wycinka dla zestawu danych i wszystkich zależnych zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="eb25b-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="eb25b-113">Zależne zestawy danych są używane jako dane wejściowe dla działań w potoku.</span><span class="sxs-lookup"><span data-stu-id="eb25b-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="eb25b-114">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="eb25b-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="eb25b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb25b-115">PARAMETERS</span></span>

### <span data-ttu-id="eb25b-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="eb25b-116">-DataFactory</span></span>
<span data-ttu-id="eb25b-117">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="eb25b-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="eb25b-118">To polecenie cmdlet modyfikuje stan wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eb25b-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb25b-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="eb25b-119">-DataFactoryName</span></span>
<span data-ttu-id="eb25b-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="eb25b-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="eb25b-121">To polecenie cmdlet modyfikuje stan wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eb25b-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb25b-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="eb25b-122">-DatasetName</span></span>
<span data-ttu-id="eb25b-123">Określa nazwę zestawu danych, dla którego to polecenie cmdlet modyfikuje wycinki.</span><span class="sxs-lookup"><span data-stu-id="eb25b-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="eb25b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb25b-124">-DefaultProfile</span></span>
<span data-ttu-id="eb25b-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eb25b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eb25b-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="eb25b-126">-EndDateTime</span></span>
<span data-ttu-id="eb25b-127">Określa koniec okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="eb25b-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="eb25b-128">Ten czas to koniec wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="eb25b-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="eb25b-129">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="eb25b-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="eb25b-130">*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00 – 08:00 (czas standardowy)</span><span class="sxs-lookup"><span data-stu-id="eb25b-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="eb25b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb25b-131">-ResourceGroupName</span></span>
<span data-ttu-id="eb25b-132">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eb25b-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="eb25b-133">To polecenie cmdlet modyfikuje stan wycinków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="eb25b-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="eb25b-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="eb25b-134">-StartDateTime</span></span>
<span data-ttu-id="eb25b-135">Określa początek okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="eb25b-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="eb25b-136">Ten czas to początek wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="eb25b-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="eb25b-137">-Status</span><span class="sxs-lookup"><span data-stu-id="eb25b-137">-Status</span></span>
<span data-ttu-id="eb25b-138">Określa stan przypisania do wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="eb25b-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="eb25b-139">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eb25b-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb25b-140">Czekać.</span><span class="sxs-lookup"><span data-stu-id="eb25b-140">Waiting.</span></span>
<span data-ttu-id="eb25b-141">Przed przetworzeniem wycinka danych czeka na sprawdzenie zasad sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="eb25b-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="eb25b-142">Dostarczenia.</span><span class="sxs-lookup"><span data-stu-id="eb25b-142">Ready.</span></span>
<span data-ttu-id="eb25b-143">Przetwarzanie danych zostało ukończone i wycinek danych jest gotowy.</span><span class="sxs-lookup"><span data-stu-id="eb25b-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="eb25b-144">W trakcie.</span><span class="sxs-lookup"><span data-stu-id="eb25b-144">InProgress.</span></span>
<span data-ttu-id="eb25b-145">Przetwarzanie danych jest w toku.</span><span class="sxs-lookup"><span data-stu-id="eb25b-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="eb25b-146">Nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="eb25b-146">Failed.</span></span>
<span data-ttu-id="eb25b-147">Przetwarzanie danych nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="eb25b-147">Data processing failed.</span></span>
- <span data-ttu-id="eb25b-148">Pominięte.</span><span class="sxs-lookup"><span data-stu-id="eb25b-148">Skipped.</span></span>
<span data-ttu-id="eb25b-149">Pominięto przetwarzanie wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="eb25b-149">Skipped processing the data slice.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb25b-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="eb25b-150">-UpdateType</span></span>
<span data-ttu-id="eb25b-151">Określa typ aktualizacji wycinka.</span><span class="sxs-lookup"><span data-stu-id="eb25b-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="eb25b-152">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eb25b-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eb25b-153">Określonym.</span><span class="sxs-lookup"><span data-stu-id="eb25b-153">Individual.</span></span>
<span data-ttu-id="eb25b-154">Ustawia stan każdego wycinka dla zestawu danych w określonym zakresie czasu.</span><span class="sxs-lookup"><span data-stu-id="eb25b-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="eb25b-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="eb25b-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="eb25b-156">Ustawia stan każdego wycinka dla zestawu danych i wszystkich zależnych zestawów danych, które są używane jako zestawy danych wejściowych dla działań w potoku.</span><span class="sxs-lookup"><span data-stu-id="eb25b-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb25b-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb25b-157">CommonParameters</span></span>
<span data-ttu-id="eb25b-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb25b-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb25b-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb25b-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb25b-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb25b-160">INPUTS</span></span>

### <span data-ttu-id="eb25b-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="eb25b-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="eb25b-162">System. String</span><span class="sxs-lookup"><span data-stu-id="eb25b-162">System.String</span></span>

## <span data-ttu-id="eb25b-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb25b-163">OUTPUTS</span></span>

### <span data-ttu-id="eb25b-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb25b-164">System.Boolean</span></span>

## <span data-ttu-id="eb25b-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb25b-165">NOTES</span></span>
* <span data-ttu-id="eb25b-166">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="eb25b-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="eb25b-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb25b-167">RELATED LINKS</span></span>

[<span data-ttu-id="eb25b-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="eb25b-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


