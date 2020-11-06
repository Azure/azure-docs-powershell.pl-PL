---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: 79EB2AD9-BFE1-49BE-870F-7DFC99D6FE17
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsFunction.md
ms.openlocfilehash: 6b05bb1d379a5d9072cc286505a507d3718aa33e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544623"
---
# <span data-ttu-id="d7107-101">New-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d7107-101">New-AzureRmStreamAnalyticsFunction</span></span>

## <span data-ttu-id="d7107-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7107-102">SYNOPSIS</span></span>
<span data-ttu-id="d7107-103">Służy do tworzenia lub zamieniania funkcji w zadaniu Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7107-103">Creates or replaces a function in a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7107-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7107-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsFunction [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7107-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7107-105">DESCRIPTION</span></span>
<span data-ttu-id="d7107-106">Polecenie cmdlet **New-AzureRmStreamAnalyticsFunction** tworzy funkcję w zadaniu usługi Azure Stream Analytics lub zamienia istniejącą funkcję.</span><span class="sxs-lookup"><span data-stu-id="d7107-106">The **New-AzureRmStreamAnalyticsFunction** cmdlet creates a function in an Azure Stream Analytics job or replaces an existing function.</span></span>
<span data-ttu-id="d7107-107">Definiowanie funkcji w pliku notacji języka JavaScript (kod JSON).</span><span class="sxs-lookup"><span data-stu-id="d7107-107">Define the function in a JavaScript Object Notation (JSON) file.</span></span>

<span data-ttu-id="d7107-108">Nazwę funkcji można określić za pomocą parametru *name* lub pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="d7107-108">You can specify the name of the function by using the *Name* parameter or in the .json file.</span></span>
<span data-ttu-id="d7107-109">Jeśli nazwa zostanie określona w obu kierunkach, nazwy muszą być takie same.</span><span class="sxs-lookup"><span data-stu-id="d7107-109">If you specify the name in both ways, the names must match.</span></span>

<span data-ttu-id="d7107-110">Aby zamienić istniejącą pozycję, określ nazwę istniejącej funkcji.</span><span class="sxs-lookup"><span data-stu-id="d7107-110">To replace an existing function, specify the name of the existing function.</span></span>

## <span data-ttu-id="d7107-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7107-111">EXAMPLES</span></span>

### <span data-ttu-id="d7107-112">Przykład 1. Tworzenie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="d7107-112">Example 1: Create a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob07" -File "C:\Function07.json"
```

<span data-ttu-id="d7107-113">To polecenie tworzy działanie z pliku Function07.jsw programie.</span><span class="sxs-lookup"><span data-stu-id="d7107-113">This command creates a function from the file Function07.json.</span></span>
<span data-ttu-id="d7107-114">Nazwa funkcji jest przechowywana w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="d7107-114">The name of the function is stored in the .json file.</span></span>

### <span data-ttu-id="d7107-115">Przykład 2: Tworzenie funkcji Stream Analytics o nazwie ScoreTweet</span><span class="sxs-lookup"><span data-stu-id="d7107-115">Example 2: Create a Stream Analytics function named ScoreTweet</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet"
```

<span data-ttu-id="d7107-116">To polecenie umożliwia utworzenie funkcji w zadaniu o nazwie ScoreTweet.</span><span class="sxs-lookup"><span data-stu-id="d7107-116">This command creates a function on the job named ScoreTweet.</span></span>

### <span data-ttu-id="d7107-117">Przykład 3: zamienianie funkcji Stream Analytics</span><span class="sxs-lookup"><span data-stu-id="d7107-117">Example 3: Replace a Stream Analytics function</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsFunction -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamJob22" -File "C:\Function22.json" -Name "ScoreTweet" -Force
```

<span data-ttu-id="d7107-118">To polecenie zamienia definicję istniejącej funkcji o nazwie ScoreTweet na definicję w Function22.js.</span><span class="sxs-lookup"><span data-stu-id="d7107-118">This command replaces the definition of the existing function named ScoreTweet with the definition in Function22.json.</span></span>

## <span data-ttu-id="d7107-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7107-119">PARAMETERS</span></span>

### <span data-ttu-id="d7107-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="d7107-120">-File</span></span>
<span data-ttu-id="d7107-121">Określa ścieżkę pliku JSON zawierającego reprezentację w formacie JSON funkcji Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7107-121">Specifies the path of a .json file that contains the JSON representation of the Stream Analytics function.</span></span>

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

### <span data-ttu-id="d7107-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d7107-122">-Force</span></span>
<span data-ttu-id="d7107-123">Wskazuje, że to polecenie cmdlet zamienia istniejącą funkcję analizy strumienia bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d7107-123">Indicates that this cmdlet replaces an existing Stream Analytics function without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="d7107-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="d7107-124">-JobName</span></span>
<span data-ttu-id="d7107-125">Określa nazwę zadania Stream Analytics, w ramach którego to polecenie cmdlet tworzy funkcja Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7107-125">Specifies the name of the Stream Analytics job under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="d7107-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7107-126">-Name</span></span>
<span data-ttu-id="d7107-127">Określa nazwę funkcji Stream Analytics, którą to polecenie cmdlet tworzy.</span><span class="sxs-lookup"><span data-stu-id="d7107-127">Specifies the name of the Stream Analytics function that this cmdlet creates.</span></span>

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

### <span data-ttu-id="d7107-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7107-128">-ResourceGroupName</span></span>
<span data-ttu-id="d7107-129">Określa nazwę grupy zasobów, pod którą to polecenie cmdlet tworzy funkcją Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d7107-129">Specifies the name of the resource group under which this cmdlet creates a Stream Analytics function.</span></span>

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

### <span data-ttu-id="d7107-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7107-130">-Confirm</span></span>
<span data-ttu-id="d7107-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7107-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7107-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7107-132">-WhatIf</span></span>
<span data-ttu-id="d7107-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7107-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7107-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7107-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7107-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7107-135">-DefaultProfile</span></span>
<span data-ttu-id="d7107-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7107-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7107-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7107-137">CommonParameters</span></span>
<span data-ttu-id="d7107-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7107-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7107-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7107-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7107-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7107-140">INPUTS</span></span>

## <span data-ttu-id="d7107-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7107-141">OUTPUTS</span></span>

### <span data-ttu-id="d7107-142">Microsoft. Azure. Commands. StreamAnalytics. models. PSFunction</span><span class="sxs-lookup"><span data-stu-id="d7107-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSFunction</span></span>

## <span data-ttu-id="d7107-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7107-143">NOTES</span></span>

## <span data-ttu-id="d7107-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7107-144">RELATED LINKS</span></span>

[<span data-ttu-id="d7107-145">Get-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d7107-145">Get-AzureRmStreamAnalyticsFunction</span></span>](./Get-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="d7107-146">Remove-AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d7107-146">Remove-AzureRmStreamAnalyticsFunction</span></span>](./Remove-AzureRmStreamAnalyticsFunction.md)

[<span data-ttu-id="d7107-147">Test — AzureRmStreamAnalyticsFunction</span><span class="sxs-lookup"><span data-stu-id="d7107-147">Test-AzureRmStreamAnalyticsFunction</span></span>](./Test-AzureRmStreamAnalyticsFunction.md)


