---
external help file: Microsoft.Azure.Commands.DataFactories.dll-Help.xml
Module Name: AzureRM.DataFactories
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactories/help/Set-AzureRmDataFactorySliceStatus.md
ms.openlocfilehash: 8e1d189173c9825876018351ef36a2b73f285a24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526870"
---
# <span data-ttu-id="0e3e9-101">Set-AzureRmDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="0e3e9-101">Set-AzureRmDataFactorySliceStatus</span></span>

## <span data-ttu-id="0e3e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0e3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="0e3e9-103">Ustawia stan wycinków dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e3e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0e3e9-104">SYNTAX</span></span>

### <span data-ttu-id="0e3e9-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e3e9-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="0e3e9-106">ByFactoryObject</span></span>
```
Set-AzureRmDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e3e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0e3e9-107">DESCRIPTION</span></span>
<span data-ttu-id="0e3e9-108">Polecenie cmdlet **Set-AzureRmDataFactorySliceStatus** ustawia stan wycinków dla zestawu danych w fabryce Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-108">The **Set-AzureRmDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="0e3e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0e3e9-109">EXAMPLES</span></span>

### <span data-ttu-id="0e3e9-110">Przykład 1. Ustawianie stanu wszystkich wycinków</span><span class="sxs-lookup"><span data-stu-id="0e3e9-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzureRmDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="0e3e9-111">To polecenie ustawia stan wszystkich wycinków dla zestawu danych o nazwie DAWikiAggregatedData, aby oczekiwać w fabryce danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="0e3e9-112">Parametr *UpdateType* ma wartość UpstreamInPipeline, więc polecenie ustawia stan każdego wycinka dla zestawu danych i wszystkich zależnych zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="0e3e9-113">Zależne zestawy danych są używane jako dane wejściowe dla działań w potoku.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="0e3e9-114">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="0e3e9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0e3e9-115">PARAMETERS</span></span>

### <span data-ttu-id="0e3e9-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="0e3e9-116">-DataFactory</span></span>
<span data-ttu-id="0e3e9-117">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="0e3e9-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="0e3e9-118">To polecenie cmdlet modyfikuje stan wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e3e9-119">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="0e3e9-119">-DataFactoryName</span></span>
<span data-ttu-id="0e3e9-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="0e3e9-121">To polecenie cmdlet modyfikuje stan wycinków należących do fabryki danych, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e3e9-122">-DataSetName</span><span class="sxs-lookup"><span data-stu-id="0e3e9-122">-DatasetName</span></span>
<span data-ttu-id="0e3e9-123">Określa nazwę zestawu danych, dla którego to polecenie cmdlet modyfikuje wycinki.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="0e3e9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e3e9-124">-DefaultProfile</span></span>
<span data-ttu-id="0e3e9-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0e3e9-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e3e9-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="0e3e9-126">-EndDateTime</span></span>
<span data-ttu-id="0e3e9-127">Określa koniec okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="0e3e9-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="0e3e9-128">Ten czas to koniec wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="0e3e9-129">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="0e3e9-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="0e3e9-130">*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples:</span></span> 

<span data-ttu-id="0e3e9-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000 Z (UTC) 2015-01-01T00:00:00 – 08 – 00 (pacyficzny czas standardowy)</span><span class="sxs-lookup"><span data-stu-id="0e3e9-131">2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time)</span></span>

<span data-ttu-id="0e3e9-132">Domyślnym wyznaczaniem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-132">The default time zone designator is UTC.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e9-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e3e9-133">-ResourceGroupName</span></span>
<span data-ttu-id="0e3e9-134">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-134">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="0e3e9-135">To polecenie cmdlet modyfikuje stan wycinków należących do grupy, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-135">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e3e9-136">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="0e3e9-136">-StartDateTime</span></span>
<span data-ttu-id="0e3e9-137">Określa początek okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="0e3e9-137">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="0e3e9-138">Ten czas to początek wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-138">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="0e3e9-139">-Status</span><span class="sxs-lookup"><span data-stu-id="0e3e9-139">-Status</span></span>
<span data-ttu-id="0e3e9-140">Określa stan przypisania do wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-140">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="0e3e9-141">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-141">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e3e9-142">Czekać.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-142">Waiting.</span></span>
<span data-ttu-id="0e3e9-143">Przed przetworzeniem wycinka danych czeka na sprawdzenie zasad sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-143">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="0e3e9-144">Dostarczenia.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-144">Ready.</span></span>
<span data-ttu-id="0e3e9-145">Przetwarzanie danych zostało ukończone i wycinek danych jest gotowy.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-145">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="0e3e9-146">W trakcie.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-146">InProgress.</span></span>
<span data-ttu-id="0e3e9-147">Przetwarzanie danych jest w toku.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-147">Data processing is in-progress.</span></span> 
- <span data-ttu-id="0e3e9-148">Nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-148">Failed.</span></span>
<span data-ttu-id="0e3e9-149">Przetwarzanie danych nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-149">Data processing failed.</span></span>
- <span data-ttu-id="0e3e9-150">Pominięte.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-150">Skipped.</span></span>
<span data-ttu-id="0e3e9-151">Pominięto przetwarzanie wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-151">Skipped processing the data slice.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Failed, InProgress, Ready, Skipped, Waiting

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e9-152">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="0e3e9-152">-UpdateType</span></span>
<span data-ttu-id="0e3e9-153">Określa typ aktualizacji wycinka.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-153">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="0e3e9-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0e3e9-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0e3e9-155">Określonym.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-155">Individual.</span></span>
<span data-ttu-id="0e3e9-156">Ustawia stan każdego wycinka dla zestawu danych w określonym zakresie czasu.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-156">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="0e3e9-157">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-157">UpstreamInPipeline.</span></span>
<span data-ttu-id="0e3e9-158">Ustawia stan każdego wycinka dla zestawu danych i wszystkich zależnych zestawów danych, które są używane jako zestawy danych wejściowych dla działań w potoku.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-158">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Individual, UpstreamInPipeline

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e3e9-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e3e9-159">CommonParameters</span></span>
<span data-ttu-id="0e3e9-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e3e9-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e3e9-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e3e9-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e3e9-162">INPUTS</span></span>

### <span data-ttu-id="0e3e9-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0e3e9-163">None</span></span>
<span data-ttu-id="0e3e9-164">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0e3e9-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0e3e9-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0e3e9-165">OUTPUTS</span></span>

### <span data-ttu-id="0e3e9-166">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0e3e9-166">System.Boolean</span></span>

## <span data-ttu-id="0e3e9-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0e3e9-167">NOTES</span></span>
* <span data-ttu-id="0e3e9-168">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="0e3e9-168">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="0e3e9-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e3e9-169">RELATED LINKS</span></span>

[<span data-ttu-id="0e3e9-170">Get-AzureRmDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="0e3e9-170">Get-AzureRmDataFactorySlice</span></span>](./Get-AzureRmDataFactorySlice.md)


