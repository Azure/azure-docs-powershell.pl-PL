---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsJob.md
ms.openlocfilehash: b50141c37c55d55f8fd8e823f09fefad49a55543
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707414"
---
# <span data-ttu-id="a122c-101">New-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a122c-101">New-AzStreamAnalyticsJob</span></span>

## <span data-ttu-id="a122c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a122c-102">SYNOPSIS</span></span>
<span data-ttu-id="a122c-103">Umożliwia utworzenie lub zaktualizowanie zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a122c-103">Creates or updates a Stream Analytics job.</span></span>

## <span data-ttu-id="a122c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a122c-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a122c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a122c-105">DESCRIPTION</span></span>
<span data-ttu-id="a122c-106">Polecenie cmdlet **New-AzStreamAnalyticsJob** tworzy nowe zadanie analizy strumienia na platformie Azure lub aktualizuje definicję istniejącego określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="a122c-106">The **New-AzStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="a122c-107">Nazwę zadania można określić w polu. Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="a122c-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="a122c-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="a122c-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="a122c-109">Jeśli określisz nazwę zadania, która już istnieje, i nie określisz parametru *Force* , polecenie cmdlet wyświetli pytanie o to, czy zamienić istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="a122c-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>
<span data-ttu-id="a122c-110">Jeśli określisz parametr *Force* i określisz nazwę istniejącego zadania, definicja zadania zostanie zastąpiona bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a122c-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="a122c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a122c-111">EXAMPLES</span></span>

### <span data-ttu-id="a122c-112">PRZYKŁAD 1. Tworzenie zadania</span><span class="sxs-lookup"><span data-stu-id="a122c-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="a122c-113">To polecenie tworzy zadanie na podstawie definicji w JobDefinition.js.</span><span class="sxs-lookup"><span data-stu-id="a122c-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="a122c-114">Jeśli istniejące zadanie o określonej nazwie w pliku definicji zadania jest już zdefiniowane, polecenie cmdlet wyświetli pytanie o to, czy chcesz je zamienić.</span><span class="sxs-lookup"><span data-stu-id="a122c-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="a122c-115">PRZYKŁAD 2: zamienianie definicji zadania</span><span class="sxs-lookup"><span data-stu-id="a122c-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="a122c-116">To polecenie zamienia definicję zadania dla StreamingJob bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="a122c-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="a122c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a122c-117">PARAMETERS</span></span>

### <span data-ttu-id="a122c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a122c-118">-DefaultProfile</span></span>
<span data-ttu-id="a122c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a122c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a122c-120">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="a122c-120">-File</span></span>
<span data-ttu-id="a122c-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON zadania usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="a122c-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a122c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="a122c-122">-Force</span></span>
<span data-ttu-id="a122c-123">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a122c-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a122c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a122c-124">-Name</span></span>
<span data-ttu-id="a122c-125">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="a122c-125">Specifies the name of the Azure Stream Analytics job to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a122c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a122c-126">-ResourceGroupName</span></span>
<span data-ttu-id="a122c-127">Określa nazwę grupy zasobów, do której ma należeć zadanie usługa Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="a122c-127">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="a122c-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a122c-128">-Confirm</span></span>
<span data-ttu-id="a122c-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a122c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a122c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a122c-130">-WhatIf</span></span>
<span data-ttu-id="a122c-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a122c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a122c-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a122c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a122c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a122c-133">CommonParameters</span></span>
<span data-ttu-id="a122c-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a122c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a122c-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a122c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a122c-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a122c-136">INPUTS</span></span>

### <span data-ttu-id="a122c-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a122c-137">System.String</span></span>

## <span data-ttu-id="a122c-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a122c-138">OUTPUTS</span></span>

### <span data-ttu-id="a122c-139">Microsoft. Azure. Commands. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="a122c-139">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="a122c-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a122c-140">NOTES</span></span>

## <span data-ttu-id="a122c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a122c-141">RELATED LINKS</span></span>

[<span data-ttu-id="a122c-142">Get-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a122c-142">Get-AzStreamAnalyticsJob</span></span>](./Get-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a122c-143">Remove-AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a122c-143">Remove-AzStreamAnalyticsJob</span></span>](./Remove-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a122c-144">Start — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a122c-144">Start-AzStreamAnalyticsJob</span></span>](./Start-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a122c-145">Zatrzymaj — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a122c-145">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)

[<span data-ttu-id="a122c-146">Zatrzymaj — AzStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="a122c-146">Stop-AzStreamAnalyticsJob</span></span>](./Stop-AzStreamAnalyticsJob.md)


