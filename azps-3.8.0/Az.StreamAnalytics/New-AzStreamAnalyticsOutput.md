---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: 69271f14994570b51e52ccbbb1a5db4bfd96b833
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894933"
---
# <span data-ttu-id="30ffd-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="30ffd-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="30ffd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="30ffd-103">Tworzenie lub aktualizowanie wyników dla zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="30ffd-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="30ffd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30ffd-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30ffd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="30ffd-106">Polecenie cmdlet **New-AzStreamAnalyticsOutput** umożliwia utworzenie danych wyjściowych w ramach zadania Stream Analytics lub zaktualizowanie istniejącego wyjścia.</span><span class="sxs-lookup"><span data-stu-id="30ffd-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="30ffd-107">Nazwę wyników można określić w polu. Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="30ffd-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="30ffd-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="30ffd-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="30ffd-109">Jeśli określisz dane wyjściowe, które już istnieją, i nie określisz parametru *Force* , polecenie cmdlet wyświetli pytanie o to, czy zamienić istniejące dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="30ffd-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="30ffd-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę wyjściową, wynik zostanie zastąpiony bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="30ffd-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="30ffd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30ffd-111">EXAMPLES</span></span>

### <span data-ttu-id="30ffd-112">PRZYKŁAD 1. Dodawanie wyników do zadania</span><span class="sxs-lookup"><span data-stu-id="30ffd-112">EXAMPLE 1: Add an output to a job</span></span>
```
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="30ffd-113">To polecenie tworzy nowe wyjście o nazwie dane wyjściowe w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="30ffd-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="30ffd-114">Jeśli istniejące wyjście o tej nazwie jest już zdefiniowane, polecenie cmdlet wyświetli pytanie o to, czy chcesz je zamienić.</span><span class="sxs-lookup"><span data-stu-id="30ffd-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="30ffd-115">PRZYKŁAD 2: zamiana definicji wyjściowej zadania</span><span class="sxs-lookup"><span data-stu-id="30ffd-115">EXAMPLE 2: Replace a job output definition</span></span>
```
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="30ffd-116">To polecenie zamienia definicję danych wyjściowych w zadaniu o nazwie StreamingJob bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="30ffd-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="30ffd-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30ffd-117">PARAMETERS</span></span>

### <span data-ttu-id="30ffd-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30ffd-118">-DefaultProfile</span></span>
<span data-ttu-id="30ffd-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="30ffd-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30ffd-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="30ffd-120">-File</span></span>
<span data-ttu-id="30ffd-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON funkcji Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="30ffd-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="30ffd-122">-Force</span><span class="sxs-lookup"><span data-stu-id="30ffd-122">-Force</span></span>
<span data-ttu-id="30ffd-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="30ffd-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="30ffd-124">-JobName</span><span class="sxs-lookup"><span data-stu-id="30ffd-124">-JobName</span></span>
<span data-ttu-id="30ffd-125">Określa nazwę zadania usługi Azure Stream Analytics, w którym można utworzyć dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="30ffd-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="30ffd-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="30ffd-126">-Name</span></span>
<span data-ttu-id="30ffd-127">Określa nazwę danych wyjściowych funkcji Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="30ffd-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="30ffd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30ffd-128">-ResourceGroupName</span></span>
<span data-ttu-id="30ffd-129">Określa nazwę grupy zasobów, w której należy utworzyć dane wyjściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="30ffd-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="30ffd-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30ffd-130">-Confirm</span></span>
<span data-ttu-id="30ffd-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30ffd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30ffd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30ffd-132">-WhatIf</span></span>
<span data-ttu-id="30ffd-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30ffd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30ffd-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30ffd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30ffd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30ffd-135">CommonParameters</span></span>
<span data-ttu-id="30ffd-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30ffd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30ffd-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30ffd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30ffd-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30ffd-138">INPUTS</span></span>

### <span data-ttu-id="30ffd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="30ffd-139">System.String</span></span>

## <span data-ttu-id="30ffd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30ffd-140">OUTPUTS</span></span>

### <span data-ttu-id="30ffd-141">Microsoft. Azure. Commands. StreamAnalytics. models. PSOutput</span><span class="sxs-lookup"><span data-stu-id="30ffd-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="30ffd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30ffd-142">NOTES</span></span>

## <span data-ttu-id="30ffd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30ffd-143">RELATED LINKS</span></span>

[<span data-ttu-id="30ffd-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="30ffd-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="30ffd-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="30ffd-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="30ffd-146">Test — AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="30ffd-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


