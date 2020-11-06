---
external help file: Microsoft.Azure.Commands.StreamAnalytics.dll-Help.xml
Module Name: AzureRM.StreamAnalytics
ms.assetid: F281B351-F7C7-47D1-9745-FFE4BAA840FD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/StreamAnalytics/Commands.StreamAnalytics/help/New-AzureRmStreamAnalyticsJob.md
ms.openlocfilehash: 5d56c0523077ee8a45b2a41175ca54c5a0e10907
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553737"
---
# <span data-ttu-id="d8404-101">New-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8404-101">New-AzureRmStreamAnalyticsJob</span></span>

## <span data-ttu-id="d8404-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8404-102">SYNOPSIS</span></span>
<span data-ttu-id="d8404-103">Umożliwia utworzenie lub zaktualizowanie zadania Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8404-103">Creates or updates a Stream Analytics job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8404-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8404-104">SYNTAX</span></span>

```
New-AzureRmStreamAnalyticsJob [[-Name] <String>] [-File] <String> [-Force] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8404-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d8404-105">DESCRIPTION</span></span>
<span data-ttu-id="d8404-106">Polecenie cmdlet **New-AzureRmStreamAnalyticsJob** tworzy nowe zadanie analizy strumienia na platformie Azure lub aktualizuje definicję istniejącego określonego zadania.</span><span class="sxs-lookup"><span data-stu-id="d8404-106">The **New-AzureRmStreamAnalyticsJob** cmdlet creates a new Stream Analytics job in Azure or updates the definition of an existing specified job.</span></span>
<span data-ttu-id="d8404-107">Nazwę zadania można określić w polu. Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="d8404-107">The name of the job can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="d8404-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="d8404-108">If both are specified, the name on command line must match the name in the file.</span></span>

<span data-ttu-id="d8404-109">Jeśli określisz nazwę zadania, która już istnieje, i nie określisz parametru *Force* , polecenie cmdlet wyświetli pytanie o to, czy zamienić istniejące zadanie.</span><span class="sxs-lookup"><span data-stu-id="d8404-109">If you specify a job name that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing job.</span></span>

<span data-ttu-id="d8404-110">Jeśli określisz parametr *Force* i określisz nazwę istniejącego zadania, definicja zadania zostanie zastąpiona bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="d8404-110">If you specify the *Force* parameter and specify an existing job name, the job definition will be replaced without confirmation.</span></span>

## <span data-ttu-id="d8404-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8404-111">EXAMPLES</span></span>

### <span data-ttu-id="d8404-112">PRZYKŁAD 1. Tworzenie zadania</span><span class="sxs-lookup"><span data-stu-id="d8404-112">EXAMPLE 1: Create a job</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json"
```

<span data-ttu-id="d8404-113">To polecenie tworzy zadanie na podstawie definicji w JobDefinition.js.</span><span class="sxs-lookup"><span data-stu-id="d8404-113">This command creates a job from the definition in JobDefinition.json.</span></span>
<span data-ttu-id="d8404-114">Jeśli istniejące zadanie o określonej nazwie w pliku definicji zadania jest już zdefiniowane, polecenie cmdlet wyświetli pytanie o to, czy chcesz je zamienić.</span><span class="sxs-lookup"><span data-stu-id="d8404-114">If an existing job with the specified name in the job definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="d8404-115">PRZYKŁAD 2: zamienianie definicji zadania</span><span class="sxs-lookup"><span data-stu-id="d8404-115">EXAMPLE 2: Replace a job definition</span></span>
```
PS C:\>New-AzureRmStreamAnalyticsJob -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\JobDefinition.json" -Name "StreamingJob" -Force
```

<span data-ttu-id="d8404-116">To polecenie zamienia definicję zadania dla StreamingJob bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="d8404-116">This command replaces the job definition for StreamingJob without confirmation.</span></span>

## <span data-ttu-id="d8404-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8404-117">PARAMETERS</span></span>

### <span data-ttu-id="d8404-118">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="d8404-118">-File</span></span>
<span data-ttu-id="d8404-119">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON zadania usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="d8404-119">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="d8404-120">-Force</span><span class="sxs-lookup"><span data-stu-id="d8404-120">-Force</span></span>
<span data-ttu-id="d8404-121">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d8404-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d8404-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8404-122">-Name</span></span>
<span data-ttu-id="d8404-123">Określa nazwę zadania usługi Azure Stream Analytics, które ma zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="d8404-123">Specifies the name of the Azure Stream Analytics job to create.</span></span>

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

### <span data-ttu-id="d8404-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8404-124">-ResourceGroupName</span></span>
<span data-ttu-id="d8404-125">Określa nazwę grupy zasobów, do której ma należeć zadanie usługa Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="d8404-125">Specifies the name of the resource group to which the Azure Stream Analytics job should belong.</span></span>

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

### <span data-ttu-id="d8404-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8404-126">-Confirm</span></span>
<span data-ttu-id="d8404-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8404-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8404-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8404-128">-WhatIf</span></span>
<span data-ttu-id="d8404-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8404-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8404-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8404-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8404-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8404-131">-DefaultProfile</span></span>
<span data-ttu-id="d8404-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8404-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8404-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8404-133">CommonParameters</span></span>
<span data-ttu-id="d8404-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8404-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8404-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8404-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8404-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8404-136">INPUTS</span></span>

## <span data-ttu-id="d8404-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8404-137">OUTPUTS</span></span>

### <span data-ttu-id="d8404-138">Microsoft. Azure. Commands. StreamAnalytics. models. PSJob</span><span class="sxs-lookup"><span data-stu-id="d8404-138">Microsoft.Azure.Commands.StreamAnalytics.Models.PSJob</span></span>

## <span data-ttu-id="d8404-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8404-139">NOTES</span></span>

## <span data-ttu-id="d8404-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8404-140">RELATED LINKS</span></span>

[<span data-ttu-id="d8404-141">Get-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8404-141">Get-AzureRmStreamAnalyticsJob</span></span>](./Get-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d8404-142">Remove-AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8404-142">Remove-AzureRmStreamAnalyticsJob</span></span>](./Remove-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d8404-143">Start — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8404-143">Start-AzureRmStreamAnalyticsJob</span></span>](./Start-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d8404-144">Zatrzymaj — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8404-144">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)

[<span data-ttu-id="d8404-145">Zatrzymaj — AzureRmStreamAnalyticsJob</span><span class="sxs-lookup"><span data-stu-id="d8404-145">Stop-AzureRmStreamAnalyticsJob</span></span>](./Stop-AzureRmStreamAnalyticsJob.md)


