---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.streamanalytics/new-azurermstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsOutput.md
ms.openlocfilehash: 7b18513a6a9e7ebbf82892500344d13f9cbc8185
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547819"
---
# <span data-ttu-id="da7b5-101">New-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="da7b5-101">New-AzureRmStreamAnalyticsOutput</span></span>

## <span data-ttu-id="da7b5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="da7b5-103">Tworzenie lub aktualizowanie wyników dla zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="da7b5-103">Creates or updates outputs for a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da7b5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da7b5-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="da7b5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="da7b5-106">Polecenie cmdlet **New-AzureRmStreamAnalyticsOutput** umożliwia utworzenie danych wyjściowych w ramach zadania Stream Analytics lub zaktualizowanie istniejącego wyjścia.</span><span class="sxs-lookup"><span data-stu-id="da7b5-106">The **New-AzureRmStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="da7b5-107">Nazwę wyników można określić w polu. Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="da7b5-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="da7b5-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="da7b5-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="da7b5-109">Jeśli określisz dane wyjściowe, które już istnieją, i nie określisz parametru *Force* , polecenie cmdlet wyświetli pytanie o to, czy zamienić istniejące dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="da7b5-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>

<span data-ttu-id="da7b5-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę wyjściową, wynik zostanie zastąpiony bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="da7b5-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="da7b5-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da7b5-111">EXAMPLES</span></span>

### <span data-ttu-id="da7b5-112">PRZYKŁAD 1. Dodawanie wyników do zadania</span><span class="sxs-lookup"><span data-stu-id="da7b5-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="da7b5-113">To polecenie tworzy nowe wyjście o nazwie dane wyjściowe w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="da7b5-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="da7b5-114">Jeśli istniejące wyjście o tej nazwie jest już zdefiniowane, polecenie cmdlet wyświetli pytanie o to, czy chcesz je zamienić.</span><span class="sxs-lookup"><span data-stu-id="da7b5-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="da7b5-115">PRZYKŁAD 2: zamiana definicji wyjściowej zadania</span><span class="sxs-lookup"><span data-stu-id="da7b5-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="da7b5-116">To polecenie zamienia definicję danych wyjściowych w zadaniu o nazwie StreamingJob bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="da7b5-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="da7b5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da7b5-117">PARAMETERS</span></span>

### <span data-ttu-id="da7b5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da7b5-118">-DefaultProfile</span></span>
<span data-ttu-id="da7b5-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="da7b5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="da7b5-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="da7b5-120">-File</span></span>
<span data-ttu-id="da7b5-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON funkcji Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="da7b5-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="da7b5-122">-Force</span><span class="sxs-lookup"><span data-stu-id="da7b5-122">-Force</span></span>
<span data-ttu-id="da7b5-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="da7b5-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="da7b5-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="da7b5-124">-JobName</span></span>
<span data-ttu-id="da7b5-125">Określa nazwę zadania usługi Azure Stream Analytics, w którym można utworzyć dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="da7b5-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="da7b5-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="da7b5-126">-Name</span></span>
<span data-ttu-id="da7b5-127">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="da7b5-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="da7b5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da7b5-128">-ResourceGroupName</span></span>
<span data-ttu-id="da7b5-129">Określa nazwę grupy zasobów, w której należy utworzyć dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="da7b5-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="da7b5-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="da7b5-130">-Confirm</span></span>
<span data-ttu-id="da7b5-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7b5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da7b5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da7b5-132">-WhatIf</span></span>
<span data-ttu-id="da7b5-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da7b5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da7b5-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="da7b5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da7b5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da7b5-135">CommonParameters</span></span>
<span data-ttu-id="da7b5-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da7b5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da7b5-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da7b5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da7b5-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da7b5-138">INPUTS</span></span>

### <span data-ttu-id="da7b5-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="da7b5-139">None</span></span>
<span data-ttu-id="da7b5-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="da7b5-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="da7b5-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da7b5-141">OUTPUTS</span></span>

### <span data-ttu-id="da7b5-142">Microsoft. Azure. Commands. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="da7b5-142">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="da7b5-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da7b5-143">NOTES</span></span>

## <span data-ttu-id="da7b5-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da7b5-144">RELATED LINKS</span></span>

[<span data-ttu-id="da7b5-145">Get-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="da7b5-145">Get-AzureRmStreamAnalyticsOutput</span></span>](./Get-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="da7b5-146">Remove-AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="da7b5-146">Remove-AzureRmStreamAnalyticsOutput</span></span>](./Remove-AzureRmStreamAnalyticsOutput.md)

[<span data-ttu-id="da7b5-147">Test — AzureRmStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="da7b5-147">Test-AzureRmStreamAnalyticsOutput</span></span>](./Test-AzureRmStreamAnalyticsOutput.md)


