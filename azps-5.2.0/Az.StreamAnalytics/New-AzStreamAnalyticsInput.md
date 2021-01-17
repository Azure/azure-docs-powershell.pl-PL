---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366368"
---
# <span data-ttu-id="60556-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="60556-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="60556-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60556-102">SYNOPSIS</span></span>
<span data-ttu-id="60556-103">Tworzy lub aktualizuje dane wejściowe zlecenia.</span><span class="sxs-lookup"><span data-stu-id="60556-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="60556-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60556-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60556-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60556-105">DESCRIPTION</span></span>
<span data-ttu-id="60556-106">Polecenie cmdlet **New-AzStreamAnalyticsInput** tworzy wejście w ramach zadania Stream Analytics lub aktualizuje istniejące dane.</span><span class="sxs-lookup"><span data-stu-id="60556-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="60556-107">Nazwę danych wejściowych można określić w pliku JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="60556-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="60556-108">Jeśli oba te pola są określone, nazwa w wierszu polecenia musi być zgodna z nazwą w pliku.</span><span class="sxs-lookup"><span data-stu-id="60556-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="60556-109">Jeśli określisz dane wejściowe, które już istnieją, i nie określisz parametru *Force* , polecenie cmdlet wyświetli pytanie o to, czy zamienić istniejące dane.</span><span class="sxs-lookup"><span data-stu-id="60556-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="60556-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę wejściową, dane wejściowe zostaną zastąpione bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="60556-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="60556-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60556-111">EXAMPLES</span></span>

### <span data-ttu-id="60556-112">Przykład 1. Tworzenie wsadu pracy z definicją z pliku</span><span class="sxs-lookup"><span data-stu-id="60556-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="60556-113">To polecenie tworzy dane wejściowe z pliku, Input.json.</span><span class="sxs-lookup"><span data-stu-id="60556-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="60556-114">Jeśli istniejące dane wejściowe o nazwie określonej w pliku definicji wejściowej są już zdefiniowane, polecenie cmdlet wyświetli pytanie o to, czy chcesz je zamienić.</span><span class="sxs-lookup"><span data-stu-id="60556-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="60556-115">Przykład 2: Tworzenie danych wejściowych zlecenia</span><span class="sxs-lookup"><span data-stu-id="60556-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="60556-116">To polecenie tworzy nowe dane wejściowe zadania o nazwie EntryStream.</span><span class="sxs-lookup"><span data-stu-id="60556-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="60556-117">Jeśli istniejące dane wejściowe o tej nazwie są już zdefiniowane, polecenie cmdlet zwróci pytanie o to, czy zamienić je.</span><span class="sxs-lookup"><span data-stu-id="60556-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="60556-118">Przykład 3: zamienianie wsadu pracy na definicję z pliku</span><span class="sxs-lookup"><span data-stu-id="60556-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="60556-119">To polecenie zamienia definicję istniejącego źródła danych o nazwie EntryStream na definicję z pliku bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="60556-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="60556-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60556-120">PARAMETERS</span></span>

### <span data-ttu-id="60556-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60556-121">-DefaultProfile</span></span>
<span data-ttu-id="60556-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60556-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60556-123">-File (plik)</span><span class="sxs-lookup"><span data-stu-id="60556-123">-File</span></span>
<span data-ttu-id="60556-124">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="60556-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="60556-125">-Force</span><span class="sxs-lookup"><span data-stu-id="60556-125">-Force</span></span>
<span data-ttu-id="60556-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="60556-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="60556-127">-JobName</span><span class="sxs-lookup"><span data-stu-id="60556-127">-JobName</span></span>
<span data-ttu-id="60556-128">Określa nazwę zadania usługi Azure Stream Analytics, w którym można utworzyć dane wejściowe funkcji Analiza strumienia Azure.</span><span class="sxs-lookup"><span data-stu-id="60556-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="60556-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="60556-129">-Name</span></span>
<span data-ttu-id="60556-130">Określa nazwę danych wejściowych funkcji Analiza strumienia Azure do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="60556-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="60556-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60556-131">-ResourceGroupName</span></span>
<span data-ttu-id="60556-132">Określa nazwę grupy zasobów, w której należy utworzyć dane wejściowe usługi Azure Streaming.</span><span class="sxs-lookup"><span data-stu-id="60556-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="60556-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="60556-133">-Confirm</span></span>
<span data-ttu-id="60556-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60556-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60556-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60556-135">-WhatIf</span></span>
<span data-ttu-id="60556-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60556-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60556-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="60556-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60556-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60556-138">CommonParameters</span></span>
<span data-ttu-id="60556-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60556-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60556-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60556-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60556-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60556-141">INPUTS</span></span>

### <span data-ttu-id="60556-142">System. String</span><span class="sxs-lookup"><span data-stu-id="60556-142">System.String</span></span>

## <span data-ttu-id="60556-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60556-143">OUTPUTS</span></span>

### <span data-ttu-id="60556-144">Microsoft. Azure. Commands. StreamAnalytics. models. PSInput</span><span class="sxs-lookup"><span data-stu-id="60556-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="60556-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60556-145">NOTES</span></span>

## <span data-ttu-id="60556-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60556-146">RELATED LINKS</span></span>

[<span data-ttu-id="60556-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="60556-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="60556-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="60556-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="60556-149">Test — AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="60556-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


