---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsfunction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsFunction.md
ms.openlocfilehash: 38d0c63dba4ac5cdc6b64ea3013f24a19bc048fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888193"
---
# <span data-ttu-id="53d26-101">New-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53d26-101">New-AzStreamAnalyticsFunction</span></span>

## <span data-ttu-id="53d26-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53d26-102">SYNOPSIS</span></span>
<span data-ttu-id="53d26-103">Służy do tworzenia lub zamieniania funkcji w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53d26-103">Creates or replaces a function in a Stream Analytics job.</span></span>

## <span data-ttu-id="53d26-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53d26-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53d26-105">Opis</span><span class="sxs-lookup"><span data-stu-id="53d26-105">DESCRIPTION</span></span>
<span data-ttu-id="53d26-106">Polecenie cmdlet **New-AzStreamAnalyticsFunction** tworzy funkcję w zadaniu usługi Azure Stream Analytics lub zamienia istniejącą funkcję.</span><span class="sxs-lookup"><span data-stu-id="53d26-106">The **New-AzStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="53d26-107">Definiowanie funkcji w pliku notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="53d26-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>
<span data-ttu-id="53d26-108">Nazwę funkcji można określić za pomocą parametru *name* lub pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="53d26-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="53d26-109">Jeśli nazwa zostanie określona w obu kierunkach, nazwy muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="53d26-109">If you specify the name in both ways, the names must match.</span></span>
<span data-ttu-id="53d26-110">Aby zamienić istniejącą pozycję, określ nazwę istniejącej funkcji.</span><span class="sxs-lookup"><span data-stu-id="53d26-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="53d26-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53d26-111">EXAMPLES</span></span>

### <span data-ttu-id="53d26-112">Przykład 1. Tworzenie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="53d26-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="53d26-113">To polecenie tworzy działanie z pliku Function07.jsw programie.</span><span class="sxs-lookup"><span data-stu-id="53d26-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="53d26-114">Nazwa funkcji jest przechowywana w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="53d26-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="53d26-115">Przykład 2: Tworzenie funkcji Stream Analytics o nazwie ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="53d26-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="53d26-116">To polecenie umożliwia utworzenie funkcji w zadaniu o nazwie ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="53d26-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="53d26-117">Przykład 3: zamienianie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="53d26-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="53d26-118">To polecenie zamienia definicję istniejącej funkcji o nazwie ScoreTweet na definicję w Function22.js.</span><span class="sxs-lookup"><span data-stu-id="53d26-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="53d26-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53d26-119">PARAMETERS</span></span>

### <span data-ttu-id="53d26-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53d26-120">-DefaultProfile</span></span>
<span data-ttu-id="53d26-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53d26-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53d26-122">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="53d26-122">-File</span></span>
<span data-ttu-id="53d26-123">Określa ścieżkę pliku JSON zawierającego reprezentację w formacie JSON funkcji Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53d26-123">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="53d26-124">-Force</span><span class="sxs-lookup"><span data-stu-id="53d26-124">-Force</span></span>
<span data-ttu-id="53d26-125">Wskazuje, że to polecenie cmdlet zamienia istniejącą funkcję analizy strumienia bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="53d26-125">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="53d26-126">-JobName</span><span class="sxs-lookup"><span data-stu-id="53d26-126">-JobName</span></span>
<span data-ttu-id="53d26-127">Określa nazwę zadania Stream Analytics, w ramach którego to polecenie cmdlet tworzy funkcja Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53d26-127">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="53d26-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53d26-128">-Name</span></span>
<span data-ttu-id="53d26-129">Określa nazwę funkcji Stream Analytics, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="53d26-129">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="53d26-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53d26-130">-ResourceGroupName</span></span>
<span data-ttu-id="53d26-131">Określa nazwę grupy zasobów, pod którą to polecenie cmdlet tworzy funkcją Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="53d26-131">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="53d26-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53d26-132">-Confirm</span></span>
<span data-ttu-id="53d26-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53d26-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53d26-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53d26-134">-WhatIf</span></span>
<span data-ttu-id="53d26-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53d26-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53d26-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="53d26-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53d26-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53d26-137">CommonParameters</span></span>
<span data-ttu-id="53d26-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53d26-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53d26-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53d26-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53d26-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53d26-140">INPUTS</span></span>

### <span data-ttu-id="53d26-141">System. String</span><span class="sxs-lookup"><span data-stu-id="53d26-141">System.String</span></span>

## <span data-ttu-id="53d26-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53d26-142">OUTPUTS</span></span>

### <span data-ttu-id="53d26-143">Microsoft. Azure. Commands. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="53d26-143">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="53d26-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53d26-144">NOTES</span></span>

## <span data-ttu-id="53d26-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53d26-145">RELATED LINKS</span></span>

[<span data-ttu-id="53d26-146">Get-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53d26-146">Get-AzStreamAnalyticsFunction</span></span>](./Get-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="53d26-147">Remove-AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53d26-147">Remove-AzStreamAnalyticsFunction</span></span>](./Remove-AzStreamAnalyticsFunction.md)

[<span data-ttu-id="53d26-148">Test — AzStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="53d26-148">Test-AzStreamAnalyticsFunction</span></span>](./Test-AzStreamAnalyticsFunction.md)


