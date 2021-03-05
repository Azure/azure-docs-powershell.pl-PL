---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 43B2A4FD-DA74-403A-89D0-40FE9A3E5A7E
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsoutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsOutput.md
ms.openlocfilehash: b4484d06802a8b17fc08b359b5dafb7e0a406ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007530"
---
# <span data-ttu-id="2436a-101">New-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2436a-101">New-AzStreamAnalyticsOutput</span></span>

## <span data-ttu-id="2436a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2436a-102">SYNOPSIS</span></span>
<span data-ttu-id="2436a-103">Tworzy lub aktualizuje dane wyjściowe dla zadania usługi Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2436a-103">Creates or updates outputs for a Stream Analytics job.</span></span>

## <span data-ttu-id="2436a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2436a-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsOutput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2436a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2436a-105">DESCRIPTION</span></span>
<span data-ttu-id="2436a-106">Polecenie **cmdlet New-AzStreamAnalyticsOutput** tworzy dane wyjściowe w zadaniu Analizy strumienia lub aktualizuje istniejące dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="2436a-106">The **New-AzStreamAnalyticsOutput** cmdlet creates an output within a Stream Analytics job or updates an existing output.</span></span>
<span data-ttu-id="2436a-107">Nazwę danych wyjściowych można określić w Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="2436a-107">The name of the output can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="2436a-108">Jeśli oba te pola zostaną określone, nazwa w wierszu polecenia musi być dopasowana do nazwy w pliku.</span><span class="sxs-lookup"><span data-stu-id="2436a-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="2436a-109">Jeśli określisz dane wyjściowe, które już istnieją i nie określisz parametru *Force,* polecenie cmdlet zapyta, czy zamienić istniejące dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="2436a-109">If you specify an output that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing output.</span></span>
<span data-ttu-id="2436a-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę wyjściową, dane wyjściowe zostaną zastąpione bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="2436a-110">If you specify the *Force* parameter and specify an existing output name, the output will be replaced without confirmation.</span></span>

## <span data-ttu-id="2436a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2436a-111">EXAMPLES</span></span>

### <span data-ttu-id="2436a-112">Przykład 1. Dodawanie danych wyjściowych do zadania</span><span class="sxs-lookup"><span data-stu-id="2436a-112">Example 1: Add an output to a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output"
```

<span data-ttu-id="2436a-113">To polecenie tworzy nowe dane wyjściowe o nazwie Dane wyjściowe w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="2436a-113">This command creates a new output called Output in the job called StreamingJob.</span></span>
<span data-ttu-id="2436a-114">Jeśli istniejące dane wyjściowe o tej nazwie są już zdefiniowane, polecenie cmdlet zapyta, czy ma zostać zamienione.</span><span class="sxs-lookup"><span data-stu-id="2436a-114">If an existing output with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="2436a-115">Przykład 2. Zastępowanie definicji wyjściowej zadania</span><span class="sxs-lookup"><span data-stu-id="2436a-115">Example 2: Replace a job output definition</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsOutput -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Output.json" -JobName "StreamingJob" -Name "Output" -Force
```

<span data-ttu-id="2436a-116">To polecenie zastępuje definicję danych wyjściowych w zadaniu o nazwie StreamingJob bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="2436a-116">This command replaces the definition for Output in the job called StreamingJob without confirmation.</span></span>

## <span data-ttu-id="2436a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2436a-117">PARAMETERS</span></span>

### <span data-ttu-id="2436a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2436a-118">-DefaultProfile</span></span>
<span data-ttu-id="2436a-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2436a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2436a-120">— Plik</span><span class="sxs-lookup"><span data-stu-id="2436a-120">-File</span></span>
<span data-ttu-id="2436a-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON danych wyjściowych usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="2436a-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="2436a-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2436a-122">-Force</span></span>
<span data-ttu-id="2436a-123">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2436a-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2436a-124">— JobName</span><span class="sxs-lookup"><span data-stu-id="2436a-124">-JobName</span></span>
<span data-ttu-id="2436a-125">Określa nazwę zadania Azure Stream Analytics, w ramach którego ma być tworzyć dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2436a-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="2436a-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2436a-126">-Name</span></span>
<span data-ttu-id="2436a-127">Określa nazwę danych wyjściowych usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="2436a-127">Specifies the name of the Azure Stream Analytics output to create.</span></span>

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

### <span data-ttu-id="2436a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2436a-128">-ResourceGroupName</span></span>
<span data-ttu-id="2436a-129">Określa nazwę grupy zasobów, w ramach której mają być tworzyć dane wyjściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="2436a-129">Specifies the name of the resource group under which to create the Azure Stream Analytics output.</span></span>

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

### <span data-ttu-id="2436a-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2436a-130">-Confirm</span></span>
<span data-ttu-id="2436a-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2436a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2436a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2436a-132">-WhatIf</span></span>
<span data-ttu-id="2436a-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2436a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2436a-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2436a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2436a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2436a-135">CommonParameters</span></span>
<span data-ttu-id="2436a-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2436a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2436a-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2436a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2436a-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2436a-138">INPUTS</span></span>

### <span data-ttu-id="2436a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="2436a-139">System.String</span></span>

## <span data-ttu-id="2436a-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2436a-140">OUTPUTS</span></span>

### <span data-ttu-id="2436a-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span><span class="sxs-lookup"><span data-stu-id="2436a-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSOutput</span></span>

## <span data-ttu-id="2436a-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2436a-142">NOTES</span></span>

## <span data-ttu-id="2436a-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2436a-143">RELATED LINKS</span></span>

[<span data-ttu-id="2436a-144">Get-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2436a-144">Get-AzStreamAnalyticsOutput</span></span>](./Get-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="2436a-145">Remove-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2436a-145">Remove-AzStreamAnalyticsOutput</span></span>](./Remove-AzStreamAnalyticsOutput.md)

[<span data-ttu-id="2436a-146">Test-AzStreamAnalyticsOutput</span><span class="sxs-lookup"><span data-stu-id="2436a-146">Test-AzStreamAnalyticsOutput</span></span>](./Test-AzStreamAnalyticsOutput.md)


