---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: D853A91F-95E7-4C36-AC0F-2C10DFCF68F8
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactorypipelineactiveperiod
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryPipelineActivePeriod.md
ms.openlocfilehash: 5cbb353a0a6349842878ef787b75c1ce34b1cfd3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964929"
---
# <span data-ttu-id="da43c-101">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="da43c-101">Set-AzDataFactoryPipelineActivePeriod</span></span>

## <span data-ttu-id="da43c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da43c-102">SYNOPSIS</span></span>
<span data-ttu-id="da43c-103">Konfiguruje aktywny okres dla wycinków danych.</span><span class="sxs-lookup"><span data-stu-id="da43c-103">Configures the active period for data slices.</span></span>

## <span data-ttu-id="da43c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da43c-104">SYNTAX</span></span>

### <span data-ttu-id="da43c-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="da43c-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactoryName] <String>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="da43c-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="da43c-106">ByFactoryObject</span></span>
```
Set-AzDataFactoryPipelineActivePeriod [-PipelineName] <String> [-DataFactory] <PSDataFactory>
 [-StartDateTime] <DateTime> [[-EndDateTime] <DateTime>] [-AutoResolve] [-ForceRecalculate]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da43c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="da43c-107">DESCRIPTION</span></span>
<span data-ttu-id="da43c-108">Polecenie cmdlet **Set-AzDataFactoryPipelineActivePeriod** konfiguruje aktywny okres dla wycinków danych, które są przetwarzane przez potok w usłudze Azure Data Factory.</span><span class="sxs-lookup"><span data-stu-id="da43c-108">The **Set-AzDataFactoryPipelineActivePeriod** cmdlet configures the active period for the data slices that are processed by a pipeline in Azure Data Factory.</span></span>
<span data-ttu-id="da43c-109">Jeśli użyjesz polecenia cmdlet Set-AzDataFactorySliceStatus w celu zmodyfikowania stanu wycinków dla zestawu danych, upewnij się, że godzina rozpoczęcia i godzina zakończenia wycinka znajdują się w aktywnym okresie potoku.</span><span class="sxs-lookup"><span data-stu-id="da43c-109">If you use the Set-AzDataFactorySliceStatus cmdlet to modify the status of slices for a dataset, make sure that the start time and end time for a slice are in the active period of the pipeline.</span></span>
<span data-ttu-id="da43c-110">Po utworzeniu potoku można określić okres przetwarzania danych.</span><span class="sxs-lookup"><span data-stu-id="da43c-110">After you create a pipeline, you can specify the period in which data processing occurs.</span></span>
<span data-ttu-id="da43c-111">Określenie okresu aktywnego dla potoku określa czas trwania, w którym wycinki  danych są przetwarzane na podstawie właściwości dostępności zdefiniowanych dla każdego zestawu danych usługi Data Factory.</span><span class="sxs-lookup"><span data-stu-id="da43c-111">Specifying the active period for a pipeline defines the time duration in which the data slices are processed based on the **Availability** properties that were defined for each Data Factory dataset.</span></span>

## <span data-ttu-id="da43c-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da43c-112">EXAMPLES</span></span>

### <span data-ttu-id="da43c-113">Przykład 1. Konfigurowanie aktywnego okresu</span><span class="sxs-lookup"><span data-stu-id="da43c-113">Example 1: Configure the active period</span></span>
```
PS C:\>Set-AzDataFactoryPipelineActivePeriod -ResourceGroupName "ADF" -PipelineName "DPWikisample" -DataFactoryName "WikiADF" -StartDateTime 2014-05-21T16:00:00Z -EndDateTime 2014-05-22T16:00:00Z
Confirm
Are you sure you want to set pipeline 'DPWikisample' active period from '05/21/2014 16:00:00' to
'05/22/2014 16:00:00'? 
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
True
```

<span data-ttu-id="da43c-114">To polecenie konfiguruje aktywny okres dla wycinków danych, które są przetwarzane w potoku o nazwie DPWikisample.</span><span class="sxs-lookup"><span data-stu-id="da43c-114">This command configures the active period for the data slices that the pipeline named DPWikisample processes.</span></span>
<span data-ttu-id="da43c-115">To polecenie udostępnia punkty początku i końca wycinków danych jako wartości.</span><span class="sxs-lookup"><span data-stu-id="da43c-115">The command provides beginning and end points for the data slices as values.</span></span>
<span data-ttu-id="da43c-116">Polecenie zwróci wartość $True.</span><span class="sxs-lookup"><span data-stu-id="da43c-116">The command returns a value of $True.</span></span>

## <span data-ttu-id="da43c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da43c-117">PARAMETERS</span></span>

### <span data-ttu-id="da43c-118">-AutoReszegorienie</span><span class="sxs-lookup"><span data-stu-id="da43c-118">-AutoResolve</span></span>
<span data-ttu-id="da43c-119">Wskazuje, że to polecenie cmdlet używa funkcji automatycznego rozpoznawania.</span><span class="sxs-lookup"><span data-stu-id="da43c-119">Indicates that this cmdlet uses auto resolve.</span></span>

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

### <span data-ttu-id="da43c-120">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="da43c-120">-DataFactory</span></span>
<span data-ttu-id="da43c-121">Określa obiekt **PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="da43c-121">Specifies a **PSDataFactory** object.</span></span>
<span data-ttu-id="da43c-122">To polecenie cmdlet zmodyfikuje aktywny okres dla potoku należącego do fabryki danych, który jest określony przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="da43c-122">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="da43c-123">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="da43c-123">-DataFactoryName</span></span>
<span data-ttu-id="da43c-124">Określa nazwę fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="da43c-124">Specifies the name of a data factory.</span></span>
<span data-ttu-id="da43c-125">To polecenie cmdlet zmodyfikuje aktywny okres dla potoku należącego do fabryki danych, który jest określony przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="da43c-125">This cmdlet modifies the active period for a pipeline that belongs to the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="da43c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da43c-126">-DefaultProfile</span></span>
<span data-ttu-id="da43c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="da43c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da43c-128">-EndDateTime</span><span class="sxs-lookup"><span data-stu-id="da43c-128">-EndDateTime</span></span>
<span data-ttu-id="da43c-129">Określa koniec okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="da43c-129">Specifies the end of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="da43c-130">Przetwarzanie danych odbywa się lub wycinki danych są przetwarzane w tym okresie.</span><span class="sxs-lookup"><span data-stu-id="da43c-130">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="da43c-131">Aby uzyskać więcej informacji na **temat obiektów DateTime,** wpisz `Get-Help Get-Date` tekst.</span><span class="sxs-lookup"><span data-stu-id="da43c-131">For more information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="da43c-132">*Wartość EndDateTime* musi zostać określona w formacie ISO8601, jak podano w poniższych przykładach: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (pacyficzny czas standardowy) Domyślnym projektem strefy czasowej jest czas UTC.</span><span class="sxs-lookup"><span data-stu-id="da43c-132">*EndDateTime* must be specified in the ISO8601 format as in the following examples: 2015-01-01Z 2015-01-01T00:00:00Z 2015-01-01T00:00:00.000Z (UTC) 2015-01-01T00:00:00-08:00 (Pacific Standard Time) The default time zone designator is UTC.</span></span>

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

### <span data-ttu-id="da43c-133">-ForceRecalculate</span><span class="sxs-lookup"><span data-stu-id="da43c-133">-ForceRecalculate</span></span>
<span data-ttu-id="da43c-134">Wskazuje, że to polecenie cmdlet używa wymuszania ponownego obliczania.</span><span class="sxs-lookup"><span data-stu-id="da43c-134">Indicates that this cmdlet uses force recalculate.</span></span>

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

### <span data-ttu-id="da43c-135">-PipelineName</span><span class="sxs-lookup"><span data-stu-id="da43c-135">-PipelineName</span></span>
<span data-ttu-id="da43c-136">Określa nazwę potoku.</span><span class="sxs-lookup"><span data-stu-id="da43c-136">Specifies the name of the pipeline.</span></span>
<span data-ttu-id="da43c-137">To polecenie cmdlet ustawia aktywny okres dla potoku, który określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="da43c-137">This cmdlet sets the active period for the pipeline that this parameter specifies.</span></span>

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

### <span data-ttu-id="da43c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da43c-138">-ResourceGroupName</span></span>
<span data-ttu-id="da43c-139">Określa nazwę grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="da43c-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="da43c-140">To polecenie cmdlet modyfikuje aktywny okres dla potoku należącego do grupy, która jest określana przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="da43c-140">This cmdlet modifies the active period for a pipeline that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="da43c-141">-StartDateTime</span><span class="sxs-lookup"><span data-stu-id="da43c-141">-StartDateTime</span></span>
<span data-ttu-id="da43c-142">Określa początek okresu jako obiekt **DateTime.**</span><span class="sxs-lookup"><span data-stu-id="da43c-142">Specifies the start of a time period as a **DateTime** object.</span></span>
<span data-ttu-id="da43c-143">Przetwarzanie danych odbywa się lub wycinki danych są przetwarzane w tym okresie.</span><span class="sxs-lookup"><span data-stu-id="da43c-143">Data processing occurs or data slices are processed within this period.</span></span>
<span data-ttu-id="da43c-144">*Wartość StartDateTime* musi zostać określona w formacie ISO8601.</span><span class="sxs-lookup"><span data-stu-id="da43c-144">*StartDateTime* must be specified in the ISO8601 format.</span></span>

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

### <span data-ttu-id="da43c-145">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da43c-145">-Confirm</span></span>
<span data-ttu-id="da43c-146">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="da43c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da43c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da43c-147">-WhatIf</span></span>
<span data-ttu-id="da43c-148">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da43c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da43c-149">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="da43c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da43c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da43c-150">CommonParameters</span></span>
<span data-ttu-id="da43c-151">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da43c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da43c-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da43c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da43c-153">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da43c-153">INPUTS</span></span>

### <span data-ttu-id="da43c-154">System.String</span><span class="sxs-lookup"><span data-stu-id="da43c-154">System.String</span></span>

### <span data-ttu-id="da43c-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="da43c-155">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="da43c-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da43c-156">OUTPUTS</span></span>

### <span data-ttu-id="da43c-157">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="da43c-157">System.Boolean</span></span>

## <span data-ttu-id="da43c-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da43c-158">NOTES</span></span>
* <span data-ttu-id="da43c-159">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="da43c-159">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="da43c-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da43c-160">RELATED LINKS</span></span>

[<span data-ttu-id="da43c-161">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="da43c-161">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="da43c-162">Set-AzDataFactorySliceStatus</span><span class="sxs-lookup"><span data-stu-id="da43c-162">Set-AzDataFactorySliceStatus</span></span>](./Set-AzDataFactorySliceStatus.md)


