---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationJobOutput.md
ms.openlocfilehash: 53ae09ba82de2a96bc9db17ad7ca538c48b23a47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502366"
---
# <span data-ttu-id="407d1-101">Get-AzAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="407d1-101">Get-AzAutomationJobOutput</span></span>

## <span data-ttu-id="407d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="407d1-102">SYNOPSIS</span></span>
<span data-ttu-id="407d1-103">Pobiera dane wyjściowe zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="407d1-103">Gets the output of an Automation job.</span></span>

## <span data-ttu-id="407d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="407d1-104">SYNTAX</span></span>

```
Get-AzAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="407d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="407d1-105">DESCRIPTION</span></span>
<span data-ttu-id="407d1-106">Polecenie cmdlet **Get-AzAutomationJobOutput** pobiera dane wyjściowe zadania usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="407d1-106">The **Get-AzAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="407d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="407d1-107">EXAMPLES</span></span>

### <span data-ttu-id="407d1-108">Przykład 1. Pobieranie danych wyjściowych zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="407d1-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="407d1-109">To polecenie pobiera wszystkie dane wyjściowe zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="407d1-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="407d1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="407d1-110">PARAMETERS</span></span>

### <span data-ttu-id="407d1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="407d1-111">-AutomationAccountName</span></span>
<span data-ttu-id="407d1-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="407d1-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="407d1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="407d1-113">-DefaultProfile</span></span>
<span data-ttu-id="407d1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="407d1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="407d1-115">-ID</span><span class="sxs-lookup"><span data-stu-id="407d1-115">-Id</span></span>
<span data-ttu-id="407d1-116">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="407d1-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="407d1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="407d1-117">-ResourceGroupName</span></span>
<span data-ttu-id="407d1-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="407d1-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="407d1-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="407d1-119">-StartTime</span></span>
<span data-ttu-id="407d1-120">Określa godzinę rozpoczęcia jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="407d1-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="407d1-121">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="407d1-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="407d1-122">Polecenie cmdlet umożliwia pobranie danych wyjściowych utworzonych po tym czasie.</span><span class="sxs-lookup"><span data-stu-id="407d1-122">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="407d1-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="407d1-123">-Stream</span></span>
<span data-ttu-id="407d1-124">Określa typ danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="407d1-124">Specifies the type of output.</span></span>
<span data-ttu-id="407d1-125">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="407d1-125">Valid values are:</span></span> 
- <span data-ttu-id="407d1-126">Jakieś</span><span class="sxs-lookup"><span data-stu-id="407d1-126">Any</span></span>
- <span data-ttu-id="407d1-127">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="407d1-127">Debug</span></span>
- <span data-ttu-id="407d1-128">Błędów</span><span class="sxs-lookup"><span data-stu-id="407d1-128">Error</span></span>
- <span data-ttu-id="407d1-129">Prowadzone</span><span class="sxs-lookup"><span data-stu-id="407d1-129">Output</span></span>
- <span data-ttu-id="407d1-130">Okres</span><span class="sxs-lookup"><span data-stu-id="407d1-130">Progress</span></span>
- <span data-ttu-id="407d1-131">Pełne</span><span class="sxs-lookup"><span data-stu-id="407d1-131">Verbose</span></span>
- <span data-ttu-id="407d1-132">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="407d1-132">Warning</span></span>

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

### <span data-ttu-id="407d1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="407d1-133">CommonParameters</span></span>
<span data-ttu-id="407d1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="407d1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="407d1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="407d1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="407d1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="407d1-136">INPUTS</span></span>

### <span data-ttu-id="407d1-137">System. GUID</span><span class="sxs-lookup"><span data-stu-id="407d1-137">System.Guid</span></span>

### <span data-ttu-id="407d1-138">Microsoft. Azure. Commands. Automation. Common. Streamtype</span><span class="sxs-lookup"><span data-stu-id="407d1-138">Microsoft.Azure.Commands.Automation.Common.StreamType</span></span>

### <span data-ttu-id="407d1-139">System. Nullable "1 [[System. DateTimeOffset, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="407d1-139">System.Nullable\`1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="407d1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="407d1-140">System.String</span></span>

## <span data-ttu-id="407d1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="407d1-141">OUTPUTS</span></span>

### <span data-ttu-id="407d1-142">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="407d1-142">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="407d1-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="407d1-143">NOTES</span></span>

## <span data-ttu-id="407d1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="407d1-144">RELATED LINKS</span></span>

[<span data-ttu-id="407d1-145">Get-AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="407d1-145">Get-AzAutomationJob</span></span>](./Get-AzAutomationJob.md)

[<span data-ttu-id="407d1-146">Życiorys — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="407d1-146">Resume-AzAutomationJob</span></span>](./Resume-AzAutomationJob.md)

[<span data-ttu-id="407d1-147">Zatrzymaj — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="407d1-147">Stop-AzAutomationJob</span></span>](./Stop-AzAutomationJob.md)

[<span data-ttu-id="407d1-148">Suspend — AzAutomationJob</span><span class="sxs-lookup"><span data-stu-id="407d1-148">Suspend-AzAutomationJob</span></span>](./Suspend-AzAutomationJob.md)


