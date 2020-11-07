---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 903e375c1272023d2d9b606325cae62103fbbc75
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896306"
---
# <span data-ttu-id="c765b-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="c765b-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="c765b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c765b-102">SYNOPSIS</span></span>
<span data-ttu-id="c765b-103">Umożliwia skonfigurowanie aktywnego okresu wycinków danych.</span><span class="sxs-lookup"><span data-stu-id="c765b-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="c765b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c765b-104">SYNTAX</span></span>

### <span data-ttu-id="c765b-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c765b-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c765b-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="c765b-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c765b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c765b-107">DESCRIPTION</span></span>
<span data-ttu-id="c765b-108">Polecenie cmdlet **Set-AzDataFactoryPipelineActivePeriod** umożliwia skonfigurowanie aktywnego okresu dla wycinków danych, które są przetwarzane przez potok w fabryce danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c765b-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="c765b-109">Jeśli używasz polecenia cmdlet Set-AzDataFactorySliceStatus, aby zmodyfikować stan wycinków dla zestawu danych, upewnij się, że godzina rozpoczęcia i godzina zakończenia wycinka są w aktywnym okresie potoku.</span><span class="sxs-lookup"><span data-stu-id="c765b-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="c765b-110">Po utworzeniu rurociągu możesz określić okres, w którym odbywa się przetwarzanie danych.</span><span class="sxs-lookup"><span data-stu-id="c765b-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="c765b-111">Określenie aktywnego okresu dla rurociągu określa czas trwania, w którym wycinki danych są przetwarzane na podstawie właściwości **dostępności** , które zostały zdefiniowane dla każdego zestawu danych fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c765b-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="c765b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c765b-112">EXAMPLES</span></span>

### <span data-ttu-id="c765b-113">Przykład 1: Konfigurowanie aktywnego okresu</span><span class="sxs-lookup"><span data-stu-id="c765b-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="c765b-114">To polecenie umożliwia skonfigurowanie aktywnego okresu wycinków danych, które potok o nazwie DPWikisample procesów.</span><span class="sxs-lookup"><span data-stu-id="c765b-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="c765b-115">Polecenie udostępnia punkty początkowe i końcowe wycinków danych jako wartości.</span><span class="sxs-lookup"><span data-stu-id="c765b-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="c765b-116">Polecenie zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="c765b-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="c765b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c765b-117">PARAMETERS</span></span>

### <span data-ttu-id="c765b-118">-Autorozpoznawanie</span><span class="sxs-lookup"><span data-stu-id="c765b-118">-AutoResolve</span></span>
<span data-ttu-id="c765b-119">Wskazuje, że w tym poleceniu cmdlet jest używane automatyczne rozpoznawanie.</span><span class="sxs-lookup"><span data-stu-id="c765b-119">Indicates that this cmdlet uses auto resolve.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c765b-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="c765b-120">-DataFactory</span></span>
<span data-ttu-id="c765b-121">Określa obiekt **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="c765b-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="c765b-122">To polecenie cmdlet modyfikuje aktywny okres dla rurociągu należącego do fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c765b-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c765b-123">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c765b-123">-DataFactoryName</span></span>
<span data-ttu-id="c765b-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c765b-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="c765b-125">To polecenie cmdlet modyfikuje aktywny okres dla rurociągu należącego do fabryki danych, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c765b-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="c765b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c765b-126">-DefaultProfile</span></span>
<span data-ttu-id="c765b-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c765b-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c765b-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="c765b-128">-EndDateTime</span></span>
<span data-ttu-id="c765b-129">Określa koniec okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c765b-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="c765b-130">Przetwarzanie danych lub wycinki danych są przetwarzane w tym okresie.</span><span class="sxs-lookup"><span data-stu-id="c765b-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="c765b-131">Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c765b-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="c765b-132">*EndDateTime* należy określić w formacie ISO8601, tak jak w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z z 2015-01-01T00:00:00.000 z (UTC) 2015-01-01T00:00:00 – 08:00 (czas standardowy)</span><span class="sxs-lookup"><span data-stu-id="c765b-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="c765b-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="c765b-133">-ForceRecalculate</span></span>
<span data-ttu-id="c765b-134">Wskazuje, że polecenie cmdlet Wymusza ponowne obliczenie.</span><span class="sxs-lookup"><span data-stu-id="c765b-134">Indicates that this cmdlet uses force recalculate.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c765b-135">-Pipelinename</span><span class="sxs-lookup"><span data-stu-id="c765b-135">-PipelineName</span></span>
<span data-ttu-id="c765b-136">Określa nazwę potoku.</span><span class="sxs-lookup"><span data-stu-id="c765b-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="c765b-137">To polecenie cmdlet ustawia aktywny okres dla rurociągu określanego przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c765b-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c765b-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c765b-138">-ResourceGroupName</span></span>
<span data-ttu-id="c765b-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c765b-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="c765b-140">To polecenie cmdlet modyfikuje aktywny okres dla rurociągu należącego do grupy, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="c765b-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="c765b-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="c765b-141">-StartDateTime</span></span>
<span data-ttu-id="c765b-142">Określa początek okresu jako obiekt **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="c765b-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="c765b-143">Przetwarzanie danych lub wycinki danych są przetwarzane w tym okresie.</span><span class="sxs-lookup"><span data-stu-id="c765b-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="c765b-144">*StartDateTime* należy określić w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="c765b-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="c765b-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c765b-145">-Confirm</span></span>
<span data-ttu-id="c765b-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c765b-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c765b-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c765b-147">-WhatIf</span></span>
<span data-ttu-id="c765b-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c765b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c765b-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c765b-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c765b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c765b-150">CommonParameters</span></span>
<span data-ttu-id="c765b-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c765b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c765b-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c765b-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c765b-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c765b-153">INPUTS</span></span>

### <span data-ttu-id="c765b-154">System. String</span><span class="sxs-lookup"><span data-stu-id="c765b-154">System.String</span></span>

### <span data-ttu-id="c765b-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="c765b-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="c765b-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c765b-156">OUTPUTS</span></span>

### <span data-ttu-id="c765b-157">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c765b-157">System.Boolean</span></span>

## <span data-ttu-id="c765b-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c765b-158">NOTES</span></span>
* <span data-ttu-id="c765b-159">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="c765b-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="c765b-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c765b-160">RELATED LINKS</span></span>

[<span data-ttu-id="c765b-161">Nowe — AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="c765b-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="c765b-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="c765b-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


