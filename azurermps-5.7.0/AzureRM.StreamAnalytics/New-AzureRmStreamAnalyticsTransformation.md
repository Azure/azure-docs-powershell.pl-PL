---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsTransformation.md
ms.openlocfilehash: a235619452966aa4dbce8381fdb22ea6c5f5fedc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547815"
---
# <span data-ttu-id="11acf-101">New-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="11acf-101">New-AzureRmStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="11acf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11acf-102">SYNOPSIS</span></span>
<span data-ttu-id="11acf-103">Umożliwia utworzenie lub zaktualizowanie transformacji w ramach zadania.</span><span class="sxs-lookup"><span data-stu-id="11acf-103">Creates or updates a transformation within a job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11acf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11acf-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11acf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11acf-105">DESCRIPTION</span></span>
<span data-ttu-id="11acf-106">Polecenie cmdlet **New-AzureRmStreamAnalyticsTransformation** tworzy transformację w ramach zadania Stream Analytics lub aktualizuje istniejące przekształcenie.</span><span class="sxs-lookup"><span data-stu-id="11acf-106">The **New-AzureRmStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="11acf-107">Nazwę przekształcenia można określić w polu. Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="11acf-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="11acf-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="11acf-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="11acf-109">Jeśli określisz już istniejącą transformację i nie określisz parametru Force, zostanie wyświetlony monit z pytaniem o to, czy zamienić istniejące przekształcenie.</span><span class="sxs-lookup"><span data-stu-id="11acf-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>

<span data-ttu-id="11acf-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę przekształcenia, transformacja zostanie zastąpiona bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="11acf-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="11acf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11acf-111">EXAMPLES</span></span>

### <span data-ttu-id="11acf-112">PRZYKŁAD 1. Tworzenie lub zamienianie przekształcenia w zadaniu</span><span class="sxs-lookup"><span data-stu-id="11acf-112">EXAMPLE 1: Create or replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="11acf-113">To polecenie tworzy transformację o nazwie StreamingJobTransform w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="11acf-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="11acf-114">Jeśli istniejące przekształcenie jest już zdefiniowane w tej nazwie, zostanie wyświetlony monit z pytaniem, czy chcesz go zamienić.</span><span class="sxs-lookup"><span data-stu-id="11acf-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="11acf-115">PRZYKŁAD 2: zamiana transformacji w zadaniu</span><span class="sxs-lookup"><span data-stu-id="11acf-115">EXAMPLE 2: Replace a transformation in a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="11acf-116">To polecenie zamienia definicję StreamingJobTransform w StreamingJob zadania bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="11acf-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="11acf-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11acf-117">PARAMETERS</span></span>

### <span data-ttu-id="11acf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11acf-118">-DefaultProfile</span></span>
<span data-ttu-id="11acf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11acf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11acf-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="11acf-120">-File</span></span>
<span data-ttu-id="11acf-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON transformacji usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="11acf-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-122">-Force</span><span class="sxs-lookup"><span data-stu-id="11acf-122">-Force</span></span>
<span data-ttu-id="11acf-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="11acf-123">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="11acf-124">-JobName</span></span>
<span data-ttu-id="11acf-125">Określa nazwę zadania usługi Azure Stream Analytics, w którym można utworzyć transformację analizy strumienia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11acf-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="11acf-126">-Name</span></span>
<span data-ttu-id="11acf-127">Określa nazwę przekształcenia usługi Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="11acf-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11acf-128">-ResourceGroupName</span></span>
<span data-ttu-id="11acf-129">Określa nazwę grupy zasobów, w której ma zostać utworzone przekształcanie analizy strumienia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="11acf-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="11acf-130">-Confirm</span></span>
<span data-ttu-id="11acf-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11acf-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11acf-132">-WhatIf</span></span>
<span data-ttu-id="11acf-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="11acf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11acf-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="11acf-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11acf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11acf-135">CommonParameters</span></span>
<span data-ttu-id="11acf-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11acf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11acf-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11acf-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11acf-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11acf-138">INPUTS</span></span>

### <span data-ttu-id="11acf-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="11acf-139">None</span></span>
<span data-ttu-id="11acf-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="11acf-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="11acf-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11acf-141">OUTPUTS</span></span>

### <span data-ttu-id="11acf-142">Microsoft. Azure. Commands. StreamAnalytics. models. PSTransformation</span><span class="sxs-lookup"><span data-stu-id="11acf-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="11acf-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11acf-143">NOTES</span></span>

## <span data-ttu-id="11acf-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11acf-144">RELATED LINKS</span></span>

[<span data-ttu-id="11acf-145">Get-AzureRmStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="11acf-145">Get-AzureRmStreamAnalyticsTransformation</span></span>](./Get-AzureRmStreamAnalyticsTransformation.md)


