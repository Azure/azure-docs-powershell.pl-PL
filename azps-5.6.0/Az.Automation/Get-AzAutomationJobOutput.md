---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: f49c0bbf17ed87d782b03052d9caeb5aba51eeff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996962"
---
# <span data-ttu-id="dcf32-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="dcf32-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="dcf32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf32-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf32-103">Pobiera dane wyjściowe zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="dcf32-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="dcf32-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dcf32-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf32-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dcf32-105">DESCRIPTION</span></span>
<span data-ttu-id="dcf32-106">Polecenie **cmdlet Get-AzAutomationJobOutput** pobiera dane wyjściowe zadania automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf32-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="dcf32-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dcf32-107">EXAMPLES</span></span>

### <span data-ttu-id="dcf32-108">Przykład 1. Uzyskiwanie wyniku zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="dcf32-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="dcf32-109">To polecenie pobiera wszystkie dane wyjściowe zadania o określonym identyfikatorze.</span><span class="sxs-lookup"><span data-stu-id="dcf32-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="dcf32-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcf32-110">PARAMETERS</span></span>

### <span data-ttu-id="dcf32-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dcf32-111">-AutomationAccountName</span></span>
<span data-ttu-id="dcf32-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet uzyskuje dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="dcf32-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="dcf32-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf32-113">-DefaultProfile</span></span>
<span data-ttu-id="dcf32-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="dcf32-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dcf32-115">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="dcf32-115">-Id</span></span>
<span data-ttu-id="dcf32-116">Określa identyfikator zadania, dla którego to polecenie cmdlet uzyskuje dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="dcf32-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf32-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf32-117">-ResourceGroupName</span></span>
<span data-ttu-id="dcf32-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet uzyskuje dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="dcf32-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="dcf32-119">— StartTime</span><span class="sxs-lookup"><span data-stu-id="dcf32-119">-StartTime</span></span>
<span data-ttu-id="dcf32-120">Określa czas rozpoczęcia jako obiekt **DateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="dcf32-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="dcf32-121">Możesz określić ciąg, który może zostać przekonwertowany na prawidłowy **dateTimeOffset.**</span><span class="sxs-lookup"><span data-stu-id="dcf32-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="dcf32-122">Polecenie cmdlet pobiera dane wyjściowe utworzone po tym czasie.</span><span class="sxs-lookup"><span data-stu-id="dcf32-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf32-123">— Stream</span><span class="sxs-lookup"><span data-stu-id="dcf32-123">-Stream</span></span>
<span data-ttu-id="dcf32-124">Określa typ danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="dcf32-124">Specifies the type of output.</span></span>
<span data-ttu-id="dcf32-125">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="dcf32-125">Valid values are:</span></span> 
- <span data-ttu-id="dcf32-126">Dowolna</span><span class="sxs-lookup"><span data-stu-id="dcf32-126">Any</span></span>
- <span data-ttu-id="dcf32-127">Debugowanie</span><span class="sxs-lookup"><span data-stu-id="dcf32-127">Debug</span></span>
- <span data-ttu-id="dcf32-128">Błąd</span><span class="sxs-lookup"><span data-stu-id="dcf32-128">Error</span></span>
- <span data-ttu-id="dcf32-129">Dane wyjściowe</span><span class="sxs-lookup"><span data-stu-id="dcf32-129">Output</span></span>
- <span data-ttu-id="dcf32-130">Postęp</span><span class="sxs-lookup"><span data-stu-id="dcf32-130">Progress</span></span>
- <span data-ttu-id="dcf32-131">Pełne słownictwo</span><span class="sxs-lookup"><span data-stu-id="dcf32-131">Verbose</span></span>
- <span data-ttu-id="dcf32-132">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="dcf32-132">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases:
Accepted values: Any, Progress, Output, Warning, Error, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf32-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf32-133">CommonParameters</span></span>
<span data-ttu-id="dcf32-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf32-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf32-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf32-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf32-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcf32-136">INPUTS</span></span>

### <span data-ttu-id="dcf32-137">System.Guid</span><span class="sxs-lookup"><span data-stu-id="dcf32-137">System.Guid</span></span>

### <span data-ttu-id="dcf32-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span><span class="sxs-lookup"><span data-stu-id="dcf32-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="dcf32-139">System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dcf32-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="dcf32-140">System.String</span><span class="sxs-lookup"><span data-stu-id="dcf32-140">System.String</span></span>

## <span data-ttu-id="dcf32-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dcf32-141">OUTPUTS</span></span>

### <span data-ttu-id="dcf32-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span><span class="sxs-lookup"><span data-stu-id="dcf32-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="dcf32-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dcf32-143">NOTES</span></span>

## <span data-ttu-id="dcf32-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dcf32-144">RELATED LINKS</span></span>

[<span data-ttu-id="dcf32-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dcf32-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="dcf32-146">Resume-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dcf32-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="dcf32-147">Stop-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dcf32-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="dcf32-148">Suspend-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="dcf32-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


