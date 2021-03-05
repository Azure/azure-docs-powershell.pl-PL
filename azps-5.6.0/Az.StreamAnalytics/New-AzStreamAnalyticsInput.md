---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 6dfb659987178b4bfe65855552e1018d085de360
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973825"
---
# <span data-ttu-id="6ebbf-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6ebbf-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="6ebbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ebbf-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebbf-103">Tworzy lub aktualizuje dane wejściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="6ebbf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ebbf-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ebbf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ebbf-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebbf-106">Polecenie **cmdlet New-AzStreamAnalyticsInput** tworzy dane wejściowe w zadaniu Usługi Stream Analytics lub aktualizuje istniejące dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="6ebbf-107">Nazwę danych wejściowych można określić w pliku JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="6ebbf-108">Jeśli oba te pola zostaną określone, nazwa w wierszu polecenia musi być dopasowana do nazwy w pliku.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="6ebbf-109">Jeśli określisz dane wejściowe, które już istnieją i nie określisz parametru *Force,* polecenie cmdlet zapyta, czy zamienić istniejące dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="6ebbf-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę wprowadzania, dane wejściowe zostaną zastąpione bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="6ebbf-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ebbf-111">EXAMPLES</span></span>

### <span data-ttu-id="6ebbf-112">Przykład 1. Tworzenie danych wejściowych zadania z definicją z pliku</span><span class="sxs-lookup"><span data-stu-id="6ebbf-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="6ebbf-113">To polecenie umożliwia utworzenie danych wejściowych z Input.jspliku.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="6ebbf-114">Jeśli istniejące dane wejściowe o nazwie określonej w pliku definicji danych wejściowych są już zdefiniowane, polecenie cmdlet zapyta, czy ma zostać zamienione.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="6ebbf-115">Przykład 2. Tworzenie danych wejściowych zadania</span><span class="sxs-lookup"><span data-stu-id="6ebbf-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="6ebbf-116">To polecenie tworzy nowe dane wejściowe dla zadania o nazwie EntryStream.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="6ebbf-117">Jeśli dane wejściowe o tej nazwie są już zdefiniowane, polecenie cmdlet zapyta, czy ma zostać zamienione.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="6ebbf-118">Przykład 3. Zamienianie informacji o zadaniu na definicję z pliku</span><span class="sxs-lookup"><span data-stu-id="6ebbf-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="6ebbf-119">To polecenie zastępuje definicję istniejącego źródła wprowadzania o nazwie EntryStream definicją z pliku bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="6ebbf-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ebbf-120">PARAMETERS</span></span>

### <span data-ttu-id="6ebbf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebbf-121">-DefaultProfile</span></span>
<span data-ttu-id="6ebbf-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ebbf-123">— Plik</span><span class="sxs-lookup"><span data-stu-id="6ebbf-123">-File</span></span>
<span data-ttu-id="6ebbf-124">Określa ścieżkę do pliku JSON zawierającego reprezentacji JSON danych wejściowych usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="6ebbf-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6ebbf-125">-Force</span></span>
<span data-ttu-id="6ebbf-126">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6ebbf-127">— JobName</span><span class="sxs-lookup"><span data-stu-id="6ebbf-127">-JobName</span></span>
<span data-ttu-id="6ebbf-128">Określa nazwę zadania Azure Stream Analytics, w ramach którego mają być tworzyć dane wejściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="6ebbf-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6ebbf-129">-Name</span></span>
<span data-ttu-id="6ebbf-130">Określa nazwę danych wejściowych usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="6ebbf-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebbf-131">-ResourceGroupName</span></span>
<span data-ttu-id="6ebbf-132">Określa nazwę grupy zasobów, w ramach której mają być tworzyć dane wejściowe usługi Azure Streaming.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="6ebbf-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ebbf-133">-Confirm</span></span>
<span data-ttu-id="6ebbf-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ebbf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebbf-135">-WhatIf</span></span>
<span data-ttu-id="6ebbf-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebbf-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ebbf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebbf-138">CommonParameters</span></span>
<span data-ttu-id="6ebbf-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ebbf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebbf-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ebbf-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebbf-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ebbf-141">INPUTS</span></span>

### <span data-ttu-id="6ebbf-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6ebbf-142">System.String</span></span>

## <span data-ttu-id="6ebbf-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ebbf-143">OUTPUTS</span></span>

### <span data-ttu-id="6ebbf-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="6ebbf-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="6ebbf-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ebbf-145">NOTES</span></span>

## <span data-ttu-id="6ebbf-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ebbf-146">RELATED LINKS</span></span>

[<span data-ttu-id="6ebbf-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6ebbf-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="6ebbf-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6ebbf-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="6ebbf-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="6ebbf-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


