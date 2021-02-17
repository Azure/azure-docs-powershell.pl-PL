---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 35CE5C5F-F8D4-426F-A33A-4F9EA50E9B83
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticsinput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsInput.md
ms.openlocfilehash: 74145a6d65fdaa9634d7681133e10b2496b5f903
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182979"
---
# <span data-ttu-id="75319-101">New-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="75319-101">New-AzStreamAnalyticsInput</span></span>

## <span data-ttu-id="75319-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75319-102">SYNOPSIS</span></span>
<span data-ttu-id="75319-103">Tworzy lub aktualizuje dane wejściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="75319-103">Creates or updates a job input.</span></span>

## <span data-ttu-id="75319-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="75319-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsInput [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="75319-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="75319-105">DESCRIPTION</span></span>
<span data-ttu-id="75319-106">Polecenie **cmdlet New-AzStreamAnalyticsInput** tworzy dane wejściowe w zadaniu Usługi Stream Analytics lub aktualizuje istniejące dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="75319-106">The **New-AzStreamAnalyticsInput** cmdlet creates an input within a Stream Analytics job or updates an existing input.</span></span>
<span data-ttu-id="75319-107">Nazwę danych wejściowych można określić w pliku JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="75319-107">The name of the input can be specified in the JSON file or on the command line.</span></span>
<span data-ttu-id="75319-108">Jeśli oba te pola zostaną określone, nazwa w wierszu polecenia musi być dopasowana do nazwy w pliku.</span><span class="sxs-lookup"><span data-stu-id="75319-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="75319-109">Jeśli określisz dane wejściowe, które już istnieją i nie określisz parametru *Force,* polecenie cmdlet zapyta, czy zamienić istniejące dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="75319-109">If you specify an input that already exists and do not specify the *Force* parameter, the cmdlet will ask whether or not to replace the existing input.</span></span>
<span data-ttu-id="75319-110">Jeśli określisz parametr *Force* i określisz istniejącą nazwę wprowadzania, dane wejściowe zostaną zastąpione bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="75319-110">If you specify the *Force* parameter and specify an existing input name, the input will be replaced without confirmation.</span></span>

## <span data-ttu-id="75319-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="75319-111">EXAMPLES</span></span>

### <span data-ttu-id="75319-112">Przykład 1. Tworzenie danych wejściowych zadania z definicją z pliku</span><span class="sxs-lookup"><span data-stu-id="75319-112">Example 1: Create a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json"
```

<span data-ttu-id="75319-113">To polecenie umożliwia utworzenie danych wejściowych z Input.jspliku.</span><span class="sxs-lookup"><span data-stu-id="75319-113">This command creates an input from the file Input.json.</span></span>
<span data-ttu-id="75319-114">Jeśli istniejące dane wejściowe o nazwie określonej w pliku definicji danych wejściowych są już zdefiniowane, polecenie cmdlet zapyta, czy ma zostać zamienione.</span><span class="sxs-lookup"><span data-stu-id="75319-114">If an existing input with the name specified in the input definition file is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="75319-115">Przykład 2. Tworzenie informacji o zadaniu</span><span class="sxs-lookup"><span data-stu-id="75319-115">Example 2: Create a job input</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream"
```

<span data-ttu-id="75319-116">To polecenie tworzy nowe dane wejściowe dla zadania o nazwie EntryStream.</span><span class="sxs-lookup"><span data-stu-id="75319-116">This command creates a new input on the job called EntryStream.</span></span>
<span data-ttu-id="75319-117">Jeśli dane wejściowe o tej nazwie są już zdefiniowane, polecenie cmdlet zapyta, czy ma zostać zamienione.</span><span class="sxs-lookup"><span data-stu-id="75319-117">If an existing input with this name is already defined, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="75319-118">Przykład 3. Zamienianie informacji o zadaniu na definicję z pliku</span><span class="sxs-lookup"><span data-stu-id="75319-118">Example 3: Replace a job input with a definition from a file</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsInput -ResourceGroupName "StreamAnalytics-Default-West-US" -JobName "StreamingJob" -File "C:\Input.json" -Name "EntryStream" -Force
```

<span data-ttu-id="75319-119">To polecenie zastępuje definicję istniejącego źródła wprowadzania o nazwie EntryStream definicją z pliku bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="75319-119">This command replaces the definition of the existing input source called EntryStream with the definition from file without confirmation.</span></span>

## <span data-ttu-id="75319-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="75319-120">PARAMETERS</span></span>

### <span data-ttu-id="75319-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75319-121">-DefaultProfile</span></span>
<span data-ttu-id="75319-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="75319-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75319-123">— Plik</span><span class="sxs-lookup"><span data-stu-id="75319-123">-File</span></span>
<span data-ttu-id="75319-124">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON danych wejściowych usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="75319-124">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="75319-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="75319-125">-Force</span></span>
<span data-ttu-id="75319-126">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="75319-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="75319-127">— JobName</span><span class="sxs-lookup"><span data-stu-id="75319-127">-JobName</span></span>
<span data-ttu-id="75319-128">Określa nazwę zadania Azure Stream Analytics, w ramach którego mają być tworzyć dane wejściowe usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="75319-128">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics input.</span></span>

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

### <span data-ttu-id="75319-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="75319-129">-Name</span></span>
<span data-ttu-id="75319-130">Określa nazwę danych wejściowych usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="75319-130">Specifies the name of the Azure Stream Analytics input to create.</span></span>

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

### <span data-ttu-id="75319-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75319-131">-ResourceGroupName</span></span>
<span data-ttu-id="75319-132">Określa nazwę grupy zasobów, w ramach której mają być tworzyć dane wejściowe usługi Azure Streaming.</span><span class="sxs-lookup"><span data-stu-id="75319-132">Specifies the name of the resource group under which to create the Azure Streaming input.</span></span>

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

### <span data-ttu-id="75319-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="75319-133">-Confirm</span></span>
<span data-ttu-id="75319-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="75319-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75319-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75319-135">-WhatIf</span></span>
<span data-ttu-id="75319-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="75319-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75319-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="75319-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75319-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75319-138">CommonParameters</span></span>
<span data-ttu-id="75319-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75319-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75319-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75319-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75319-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75319-141">INPUTS</span></span>

### <span data-ttu-id="75319-142">System.String</span><span class="sxs-lookup"><span data-stu-id="75319-142">System.String</span></span>

## <span data-ttu-id="75319-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="75319-143">OUTPUTS</span></span>

### <span data-ttu-id="75319-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span><span class="sxs-lookup"><span data-stu-id="75319-144">Microsoft.Azure.Commands.StreamAnalytics.Models.PSInput</span></span>

## <span data-ttu-id="75319-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="75319-145">NOTES</span></span>

## <span data-ttu-id="75319-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="75319-146">RELATED LINKS</span></span>

[<span data-ttu-id="75319-147">Get-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="75319-147">Get-AzStreamAnalyticsInput</span></span>](./Get-AzStreamAnalyticsInput.md)

[<span data-ttu-id="75319-148">Remove-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="75319-148">Remove-AzStreamAnalyticsInput</span></span>](./Remove-AzStreamAnalyticsInput.md)

[<span data-ttu-id="75319-149">Test-AzStreamAnalyticsInput</span><span class="sxs-lookup"><span data-stu-id="75319-149">Test-AzStreamAnalyticsInput</span></span>](./Test-AzStreamAnalyticsInput.md)


