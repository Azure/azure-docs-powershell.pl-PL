---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 71a6267b06ce47ee36f220033ec598af3680deeb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182994"
---
# <span data-ttu-id="ccfb3-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ccfb3-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="ccfb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccfb3-102">SYNOPSIS</span></span>
<span data-ttu-id="ccfb3-103">Tworzy lub zamienia funkcję w zadaniu Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="ccfb3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ccfb3-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ccfb3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ccfb3-105">DESCRIPTION</span></span>
<span data-ttu-id="ccfb3-106">Polecenie **cmdlet New-AzStreamAnalyticsFunction** tworzy funkcję w zadaniu Azure Stream Analytics lub zastępuje istniejącą funkcję.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="ccfb3-107">Zdefiniuj funkcję w pliku JavaScript Object Notation (JSON).</span><span class="sxs-lookup"><span data-stu-id="ccfb3-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="ccfb3-108">Nazwę funkcji można określić za pomocą *parametru Name* lub w pliku json.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="ccfb3-109">Jeśli określisz nazwę w obie strony, nazwy muszą być zgodne.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="ccfb3-110">Aby zamienić istniejącą funkcję, określ nazwę istniejącej funkcji.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="ccfb3-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ccfb3-111">EXAMPLES</span></span>

### <span data-ttu-id="ccfb3-112">Przykład 1. Tworzenie funkcji Analiza strumienia</span><span class="sxs-lookup"><span data-stu-id="ccfb3-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="ccfb3-113">To polecenie tworzy funkcję z pliku, Function07.jswł.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="ccfb3-114">Nazwa funkcji jest przechowywana w pliku json.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="ccfb3-115">Przykład 2. Tworzenie funkcji analizy strumienia o nazwie ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="ccfb3-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="ccfb3-116">To polecenie tworzy funkcję w zadaniu o nazwie ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="ccfb3-117">Przykład 3. Zamienianie funkcji Analiza strumienia</span><span class="sxs-lookup"><span data-stu-id="ccfb3-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="ccfb3-118">To polecenie zastępuje definicję istniejącej funkcji o nazwie ScoreTweet definicją z tabeli Function22.jswł.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="ccfb3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccfb3-119">PARAMETERS</span></span>

### <span data-ttu-id="ccfb3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccfb3-120">-DefaultProfile</span></span>
<span data-ttu-id="ccfb3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ccfb3-122">— Plik</span><span class="sxs-lookup"><span data-stu-id="ccfb3-122">-File</span></span>
<span data-ttu-id="ccfb3-123">Określa ścieżkę pliku json zawierającego reprezentację JSON funkcji Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccfb3-124">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ccfb3-124">-Force</span></span>
<span data-ttu-id="ccfb3-125">Wskazuje, że to polecenie cmdlet zastępuje istniejącą funkcję Analizy strumienia bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="ccfb3-126">— JobName</span><span class="sxs-lookup"><span data-stu-id="ccfb3-126">-JobName</span></span>
<span data-ttu-id="ccfb3-127">Określa nazwę zadania analizy strumienia, pod którym to polecenie cmdlet tworzy funkcję Analizy strumienia.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccfb3-128">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ccfb3-128">-Name</span></span>
<span data-ttu-id="ccfb3-129">Określa nazwę funkcji Stream Analytics, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="ccfb3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccfb3-130">-ResourceGroupName</span></span>
<span data-ttu-id="ccfb3-131">Określa nazwę grupy zasobów, w ramach której to polecenie cmdlet tworzy funkcję Analiza strumienia.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccfb3-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ccfb3-132">-Confirm</span></span>
<span data-ttu-id="ccfb3-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccfb3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccfb3-134">-WhatIf</span></span>
<span data-ttu-id="ccfb3-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccfb3-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccfb3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccfb3-137">CommonParameters</span></span>
<span data-ttu-id="ccfb3-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccfb3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccfb3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccfb3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccfb3-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccfb3-140">INPUTS</span></span>

### <span data-ttu-id="ccfb3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ccfb3-141">System.String</span></span>

## <span data-ttu-id="ccfb3-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccfb3-142">OUTPUTS</span></span>

### <span data-ttu-id="ccfb3-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span><span class="sxs-lookup"><span data-stu-id="ccfb3-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="ccfb3-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ccfb3-144">NOTES</span></span>

## <span data-ttu-id="ccfb3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccfb3-145">RELATED LINKS</span></span>

[<span data-ttu-id="ccfb3-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ccfb3-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="ccfb3-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ccfb3-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="ccfb3-148">Test-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="ccfb3-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


