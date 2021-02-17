---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StreamAnalytics.dll-Help.xml
Module Name: Az.StreamAnalytics
ms.assetid: 8FF53426-D4AE-455E-A182-D7FBC7262FE1
online version: https://docs.microsoft.com/en-us/powershell/module/az.streamanalytics/new-azstreamanalyticstransformation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StreamAnalytics/StreamAnalytics/help/New-AzStreamAnalyticsTransformation.md
ms.openlocfilehash: 017c084e98d8983343ae1f8c19464cc254b26e2e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182962"
---
# <span data-ttu-id="b83f0-101">New-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b83f0-101">New-AzStreamAnalyticsTransformation</span></span>

## <span data-ttu-id="b83f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b83f0-102">SYNOPSIS</span></span>
<span data-ttu-id="b83f0-103">Tworzy lub aktualizuje przekształcenie w zadaniu.</span><span class="sxs-lookup"><span data-stu-id="b83f0-103">Creates or updates a transformation within a job.</span></span>

## <span data-ttu-id="b83f0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b83f0-104">SYNTAX</span></span>

```
New-AzStreamAnalyticsTransformation [-JobName] <String> [[-Name] <String>] [-File] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b83f0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b83f0-105">DESCRIPTION</span></span>
<span data-ttu-id="b83f0-106">Polecenie **cmdlet New-AzStreamAnalyticsTransformation** tworzy przekształcenie w zadaniu analizy strumienia lub aktualizuje istniejącą transformację.</span><span class="sxs-lookup"><span data-stu-id="b83f0-106">The **New-AzStreamAnalyticsTransformation** cmdlet creates a transformation within a Stream Analytics job or updates the existing transformation.</span></span>
<span data-ttu-id="b83f0-107">Nazwę przekształcenia można określić w pliku . Plik JSON lub w wierszu polecenia.</span><span class="sxs-lookup"><span data-stu-id="b83f0-107">The name of the transformation can be specified in the .JSON file or on the command line.</span></span>
<span data-ttu-id="b83f0-108">Jeśli oba te pola zostaną określone, nazwa w wierszu polecenia musi być dopasowana do nazwy w pliku.</span><span class="sxs-lookup"><span data-stu-id="b83f0-108">If both are specified, the name on command line must match the name in the file.</span></span>
<span data-ttu-id="b83f0-109">Jeśli określisz przekształcenie, które już istnieje i nie określisz parametru Force, polecenie cmdlet zapyta, czy zamienić istniejącą transformację.</span><span class="sxs-lookup"><span data-stu-id="b83f0-109">If you specify a transformation that already exists and do not specify the Force parameter, the cmdlet will ask whether or not to replace the existing transformation.</span></span>
<span data-ttu-id="b83f0-110">Jeśli określisz parametr *Force* i określisz nazwę istniejącej transformacji, przekształcenie zostanie zastąpione bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="b83f0-110">If you specify the *Force* parameter and specify an existing transformation name, the transformation will be replaced without confirmation.</span></span>

## <span data-ttu-id="b83f0-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b83f0-111">EXAMPLES</span></span>

### <span data-ttu-id="b83f0-112">Przykład 1. Tworzenie lub zamienianie przekształcenia w zadaniu</span><span class="sxs-lookup"><span data-stu-id="b83f0-112">Example 1: Create or replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform"
```

<span data-ttu-id="b83f0-113">To polecenie tworzy przekształcenie o nazwie StreamingJobTransform w zadaniu o nazwie StreamingJob.</span><span class="sxs-lookup"><span data-stu-id="b83f0-113">This command creates a transformation called StreamingJobTransform in the job called StreamingJob.</span></span>
<span data-ttu-id="b83f0-114">Jeśli istniejąca transformacja jest już zdefiniowana przy użyciu tej nazwy, polecenie cmdlet zapyta, czy chcesz ją zamienić.</span><span class="sxs-lookup"><span data-stu-id="b83f0-114">If an existing transformation is already defined with that name, the cmdlet will ask whether or not to replace it.</span></span>

### <span data-ttu-id="b83f0-115">Przykład 2. Zamienianie przekształcenia w zadaniu</span><span class="sxs-lookup"><span data-stu-id="b83f0-115">Example 2: Replace a transformation in a job</span></span>
```powershell
PS C:\>New-AzStreamAnalyticsTransformation -ResourceGroupName "StreamAnalytics-Default-West-US" -File "C:\Transformation.json" -JobName "StreamingJob" -Name "StreamingJobTransform" -Force
```

<span data-ttu-id="b83f0-116">To polecenie zastępuje definicję usługi StreamingJobTransform w zadaniu StreamingJob bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="b83f0-116">This command replaces the definition of StreamingJobTransform in the job StreamingJob without confirmation.</span></span>

## <span data-ttu-id="b83f0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b83f0-117">PARAMETERS</span></span>

### <span data-ttu-id="b83f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b83f0-118">-DefaultProfile</span></span>
<span data-ttu-id="b83f0-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b83f0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b83f0-120">— Plik</span><span class="sxs-lookup"><span data-stu-id="b83f0-120">-File</span></span>
<span data-ttu-id="b83f0-121">Określa ścieżkę do pliku JSON zawierającego reprezentację JSON przekształcenia usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b83f0-121">Specifies the path to a JSON file that contains the JSON representation of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="b83f0-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b83f0-122">-Force</span></span>
<span data-ttu-id="b83f0-123">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b83f0-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b83f0-124">— JobName</span><span class="sxs-lookup"><span data-stu-id="b83f0-124">-JobName</span></span>
<span data-ttu-id="b83f0-125">Określa nazwę zadania Azure Stream Analytics, w ramach którego ma być tworzyć transformację usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b83f0-125">Specifies the name of the Azure Stream Analytics job under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="b83f0-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b83f0-126">-Name</span></span>
<span data-ttu-id="b83f0-127">Określa nazwę przekształcenia usługi Azure Stream Analytics do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="b83f0-127">Specifies the name of the Azure Stream Analytics transformation to create.</span></span>

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

### <span data-ttu-id="b83f0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b83f0-128">-ResourceGroupName</span></span>
<span data-ttu-id="b83f0-129">Określa nazwę grupy zasobów, w ramach której ma być tworzyć transformację usługi Azure Stream Analytics.</span><span class="sxs-lookup"><span data-stu-id="b83f0-129">Specifies the name of the resource group under which to create the Azure Stream Analytics transformation.</span></span>

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

### <span data-ttu-id="b83f0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b83f0-130">-Confirm</span></span>
<span data-ttu-id="b83f0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b83f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b83f0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b83f0-132">-WhatIf</span></span>
<span data-ttu-id="b83f0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b83f0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b83f0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b83f0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b83f0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b83f0-135">CommonParameters</span></span>
<span data-ttu-id="b83f0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b83f0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b83f0-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b83f0-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b83f0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b83f0-138">INPUTS</span></span>

### <span data-ttu-id="b83f0-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b83f0-139">System.String</span></span>

## <span data-ttu-id="b83f0-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b83f0-140">OUTPUTS</span></span>

### <span data-ttu-id="b83f0-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span><span class="sxs-lookup"><span data-stu-id="b83f0-141">Microsoft.Azure.Commands.StreamAnalytics.Models.PSTransformation</span></span>

## <span data-ttu-id="b83f0-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b83f0-142">NOTES</span></span>

## <span data-ttu-id="b83f0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b83f0-143">RELATED LINKS</span></span>

[<span data-ttu-id="b83f0-144">Get-AzStreamAnalyticsTransformation</span><span class="sxs-lookup"><span data-stu-id="b83f0-144">Get-AzStreamAnalyticsTransformation</span></span>](./Get-AzStreamAnalyticsTransformation.md)


