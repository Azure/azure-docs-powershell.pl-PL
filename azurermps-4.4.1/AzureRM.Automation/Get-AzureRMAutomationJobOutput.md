---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: dd80c745c99c98d6ea5b551ab454661d4370cebd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719539"
---
# <span data-ttu-id="c6226-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="c6226-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="c6226-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6226-102">SYNOPSIS</span></span>
<span data-ttu-id="c6226-103">Pobiera dane wyjściowe zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c6226-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6226-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6226-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6226-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c6226-105">DESCRIPTION</span></span>
<span data-ttu-id="c6226-106">Polecenie cmdlet **Get-AzureRmAutomationJobOutput** pobiera dane wyjściowe zadania usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c6226-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="c6226-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6226-107">EXAMPLES</span></span>

### <span data-ttu-id="c6226-108">Przykład 1. Pobieranie danych wyjściowych zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="c6226-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="c6226-109">To polecenie pobiera wszystkie dane wyjściowe zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="c6226-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="c6226-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6226-110">PARAMETERS</span></span>

### <span data-ttu-id="c6226-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c6226-111">-AutomationAccountName</span></span>
<span data-ttu-id="c6226-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="c6226-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c6226-113">-ID</span><span class="sxs-lookup"><span data-stu-id="c6226-113">-Id</span></span>
<span data-ttu-id="c6226-114">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="c6226-114">Specifies the ID of a job for which this cmdlet gets output.</span></span>

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

### <span data-ttu-id="c6226-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6226-115">-ResourceGroupName</span></span>
<span data-ttu-id="c6226-116">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="c6226-116">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

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

### <span data-ttu-id="c6226-117">-StartTime</span><span class="sxs-lookup"><span data-stu-id="c6226-117">-StartTime</span></span>
<span data-ttu-id="c6226-118">Określa godzinę rozpoczęcia jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="c6226-118">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="c6226-119">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="c6226-119">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="c6226-120">Polecenie cmdlet umożliwia pobranie danych wyjściowych utworzonych po tym czasie.</span><span class="sxs-lookup"><span data-stu-id="c6226-120">The cmdlet retrieves output created after this time.</span></span>

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

### <span data-ttu-id="c6226-121">-Stream</span><span class="sxs-lookup"><span data-stu-id="c6226-121">-Stream</span></span>
<span data-ttu-id="c6226-122">Określa typ danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="c6226-122">Specifies the type of output.</span></span>
<span data-ttu-id="c6226-123">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="c6226-123">Valid values are:</span></span> 

- <span data-ttu-id="c6226-124">Jakieś</span><span class="sxs-lookup"><span data-stu-id="c6226-124">Any</span></span>
- <span data-ttu-id="c6226-125">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="c6226-125">Debug</span></span>
- <span data-ttu-id="c6226-126">Błędów</span><span class="sxs-lookup"><span data-stu-id="c6226-126">Error</span></span>
- <span data-ttu-id="c6226-127">Prowadzone</span><span class="sxs-lookup"><span data-stu-id="c6226-127">Output</span></span>
- <span data-ttu-id="c6226-128">Okres</span><span class="sxs-lookup"><span data-stu-id="c6226-128">Progress</span></span>
- <span data-ttu-id="c6226-129">Pełne</span><span class="sxs-lookup"><span data-stu-id="c6226-129">Verbose</span></span>
- <span data-ttu-id="c6226-130">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="c6226-130">Warning</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6226-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6226-131">-DefaultProfile</span></span>
<span data-ttu-id="c6226-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c6226-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6226-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6226-133">CommonParameters</span></span>
<span data-ttu-id="c6226-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6226-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6226-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6226-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6226-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6226-136">INPUTS</span></span>

## <span data-ttu-id="c6226-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6226-137">OUTPUTS</span></span>

### <span data-ttu-id="c6226-138">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="c6226-138">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="c6226-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6226-139">NOTES</span></span>

## <span data-ttu-id="c6226-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6226-140">RELATED LINKS</span></span>

[<span data-ttu-id="c6226-141">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6226-141">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="c6226-142">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6226-142">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="c6226-143">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6226-143">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="c6226-144">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="c6226-144">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


