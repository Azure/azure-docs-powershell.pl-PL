---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 1D07222C-17D1-421C-8C9B-37043CBCF517
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryslicestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactorySliceStatus.md
ms.openlocfilehash: 80a471b88856ff4c7425e89fd6e5b73168370789
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998509"
---
# <span data-ttu-id="bf911-101">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="bf911-101">Set-AzDataFactorySliceStatus</span></span>

## <span data-ttu-id="bf911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf911-102">SYNOPSIS</span></span>
<span data-ttu-id="bf911-103">Ustawia stan wycinków dla zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bf911-103">Sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="bf911-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bf911-104">SYNTAX</span></span>

### <span data-ttu-id="bf911-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="bf911-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactoryName] <String> [-DatasetName] <String> [-StartDateTime] <DateTime> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bf911-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="bf911-106">ByFactoryObject</span></span>
```
Set-AzDataFactorySliceStatus [[-EndDateTime] <DateTime>] [-Status] <String> [[-UpdateType] <String>]
 [-DataFactory] <PSDataFactory> [-DatasetName] <String> [-StartDateTime] <DateTime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf911-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="bf911-107">DESCRIPTION</span></span>
<span data-ttu-id="bf911-108">Polecenie **cmdlet Set-AzDataFactorySliceStatus** ustawia stan wycinków dla zestawu danych w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="bf911-108">The **Set-AzDataFactorySliceStatus** cmdlet sets the status of slices for a dataset in Azure Data Factory.</span></span>

## <span data-ttu-id="bf911-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bf911-109">EXAMPLES</span></span>

### <span data-ttu-id="bf911-110">Przykład 1. Ustawianie stanu wszystkich wycinków</span><span class="sxs-lookup"><span data-stu-id="bf911-110">Example 1: Set the status of all slices</span></span>
```
PS C:\>Set-AzDataFactorySliceStatus -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -DatasetName "DAWikiAggregatedData" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-21T20:00:00Z -Status "Waiting" -UpdateType "UpstreamInPipeline"
True
```

<span data-ttu-id="bf911-111">To polecenie ustawia stan wszystkich wycinków dla zestawu danych o nazwie DAWikiAggregatedData do oczekiwania w fabrycznej bazie danych o nazwie WikiADF.</span><span class="sxs-lookup"><span data-stu-id="bf911-111">This command sets the status of all slices for the dataset named DAWikiAggregatedData to Waiting in the data factory named WikiADF.</span></span>
<span data-ttu-id="bf911-112">Parametr *UpdateType* ma wartość UpstreamInPipeline, więc polecenie ustawia stan każdego wycinka dla zestawu danych i wszystkich zestawów danych zależnych.</span><span class="sxs-lookup"><span data-stu-id="bf911-112">The *UpdateType* parameter has a value of UpstreamInPipeline, and so the command sets the status of each slice for the dataset and all dependent datasets.</span></span>
<span data-ttu-id="bf911-113">Zestawy danych zależnych są używane jako zestawy danych wejściowych dla działań w potoku.</span><span class="sxs-lookup"><span data-stu-id="bf911-113">Dependent datasets are used as input datasets for activities in the pipeline.</span></span>
<span data-ttu-id="bf911-114">To polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="bf911-114">This command returns a value of $True.</span></span>

## <span data-ttu-id="bf911-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf911-115">PARAMETERS</span></span>

### <span data-ttu-id="bf911-116">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="bf911-116">-DataFactory</span></span>
<span data-ttu-id="bf911-117">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="bf911-117">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="bf911-118">To polecenie cmdlet modyfikuje stan wycinków należących do fabrycznej transmisji danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bf911-118">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf911-119">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="bf911-119">-DataFactoryName</span></span>
<span data-ttu-id="bf911-120">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="bf911-120">Specifies the name of a data factory.</span></span>
<span data-ttu-id="bf911-121">To polecenie cmdlet modyfikuje stan wycinków należących do fabrycznej transmisji danych, które określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bf911-121">This cmdlet modifies the status of slices that belong to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf911-122">-DatasetName</span><span class="sxs-lookup"><span data-stu-id="bf911-122">-DatasetName</span></span>
<span data-ttu-id="bf911-123">Określa nazwę zestawu danych, dla którego to polecenie cmdlet modyfikuje wycinki.</span><span class="sxs-lookup"><span data-stu-id="bf911-123">Specifies the name of the dataset for which this cmdlet modifies slices.</span></span>

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

### <span data-ttu-id="bf911-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf911-124">-DefaultProfile</span></span>
<span data-ttu-id="bf911-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="bf911-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf911-126">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="bf911-126">-EndDateTime</span></span>
<span data-ttu-id="bf911-127">Określa koniec okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="bf911-127">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="bf911-128">Tym razem jest to koniec wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="bf911-128">This time is the end of a data slice.</span></span>
<span data-ttu-id="bf911-129">Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.</span><span class="sxs-lookup"><span data-stu-id="bf911-129">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="bf911-130">*Wartość EndDateTime* musi zostać określona w formacie ISO8601, jak podano w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (pacyficzny czas standardowy) Domyślnym projektem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="bf911-130">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="bf911-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf911-131">-ResourceGroupName</span></span>
<span data-ttu-id="bf911-132">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bf911-132">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="bf911-133">To polecenie cmdlet modyfikuje stan wycinków należących do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="bf911-133">This cmdlet modifies the status of slices that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf911-134">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="bf911-134">-StartDateTime</span></span>
<span data-ttu-id="bf911-135">Określa początek okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="bf911-135">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="bf911-136">Tym razem jest to początek wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="bf911-136">This time is the beginning of a data slice.</span></span>

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

### <span data-ttu-id="bf911-137">— Status</span><span class="sxs-lookup"><span data-stu-id="bf911-137">-Status</span></span>
<span data-ttu-id="bf911-138">Określa stan, który ma zostać przypisany do wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="bf911-138">Specifies a status to assign to the data slice.</span></span>
<span data-ttu-id="bf911-139">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bf911-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf911-140">Oczekiwanie.</span><span class="sxs-lookup"><span data-stu-id="bf911-140">Waiting.</span></span>
<span data-ttu-id="bf911-141">Wycinek danych oczekuje na weryfikację przed przetworzeniem przez zasady sprawdzania poprawności.</span><span class="sxs-lookup"><span data-stu-id="bf911-141">Data slice is waiting for validation against validation policies before being processed.</span></span> 
- <span data-ttu-id="bf911-142">Gotowe.</span><span class="sxs-lookup"><span data-stu-id="bf911-142">Ready.</span></span>
<span data-ttu-id="bf911-143">Przetwarzanie danych zostało ukończone, a wycinek danych jest gotowy.</span><span class="sxs-lookup"><span data-stu-id="bf911-143">Data processing has completed and the data slice is ready.</span></span>
- <span data-ttu-id="bf911-144">InProgress (Ruch wychodzący).</span><span class="sxs-lookup"><span data-stu-id="bf911-144">InProgress.</span></span>
<span data-ttu-id="bf911-145">Przetwarzanie danych jest w toku.</span><span class="sxs-lookup"><span data-stu-id="bf911-145">Data processing is in-progress.</span></span> 
- <span data-ttu-id="bf911-146">Niepowodzenie.</span><span class="sxs-lookup"><span data-stu-id="bf911-146">Failed.</span></span>
<span data-ttu-id="bf911-147">Przetwarzanie danych nie powiodło się.</span><span class="sxs-lookup"><span data-stu-id="bf911-147">Data processing failed.</span></span>
- <span data-ttu-id="bf911-148">Pominięte.</span><span class="sxs-lookup"><span data-stu-id="bf911-148">Skipped.</span></span>
<span data-ttu-id="bf911-149">Pominięto przetwarzanie wycinka danych.</span><span class="sxs-lookup"><span data-stu-id="bf911-149">Skipped processing the data slice.</span></span>

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

### <span data-ttu-id="bf911-150">-UpdateType</span><span class="sxs-lookup"><span data-stu-id="bf911-150">-UpdateType</span></span>
<span data-ttu-id="bf911-151">Określa typ aktualizacji wycinka.</span><span class="sxs-lookup"><span data-stu-id="bf911-151">Specifies the type of update to the slice.</span></span>
<span data-ttu-id="bf911-152">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bf911-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bf911-153">Osoba.</span><span class="sxs-lookup"><span data-stu-id="bf911-153">Individual.</span></span>
<span data-ttu-id="bf911-154">Ustawia stan każdego wycinka dla zestawu danych w określonym zakresie czasu.</span><span class="sxs-lookup"><span data-stu-id="bf911-154">Sets the status of each slice for the dataset in the specified time range.</span></span> 
- <span data-ttu-id="bf911-155">UpstreamInPipeline.</span><span class="sxs-lookup"><span data-stu-id="bf911-155">UpstreamInPipeline.</span></span>
<span data-ttu-id="bf911-156">Ustawia stan każdego wycinka dla zestawu danych i wszystkich zależnych zestawów danych, które są używane jako zestawy danych wejściowych dla działań w potoku.</span><span class="sxs-lookup"><span data-stu-id="bf911-156">Sets the status of each slice for the dataset and all the dependent datasets, which are used as input datasets for activities in the pipeline.</span></span>

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

### <span data-ttu-id="bf911-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf911-157">CommonParameters</span></span>
<span data-ttu-id="bf911-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf911-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf911-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf911-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf911-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf911-160">INPUTS</span></span>

### <span data-ttu-id="bf911-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="bf911-161">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="bf911-162">System.String</span><span class="sxs-lookup"><span data-stu-id="bf911-162">System.String</span></span>

## <span data-ttu-id="bf911-163">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf911-163">OUTPUTS</span></span>

### <span data-ttu-id="bf911-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bf911-164">System.Boolean</span></span>

## <span data-ttu-id="bf911-165">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bf911-165">NOTES</span></span>
* <span data-ttu-id="bf911-166">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="bf911-166">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="bf911-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf911-167">RELATED LINKS</span></span>

[<span data-ttu-id="bf911-168">Get-AzDataFactorySlice</span><span class="sxs-lookup"><span data-stu-id="bf911-168">Get-AzDataFactorySlice</span></span>](./Get-AzDataFactorySlice.md)


