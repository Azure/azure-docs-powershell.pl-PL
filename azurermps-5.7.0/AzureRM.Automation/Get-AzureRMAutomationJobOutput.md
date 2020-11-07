---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B39C4D6B-392A-4C8D-A6FB-886DA1A2BA58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationjoboutput
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationJobOutput.md
ms.openlocfilehash: d46dd2e314aa8064b305adb0501ae20480a34418
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716647"
---
# <span data-ttu-id="1d028-101">Get-AzureRmAutomationJobOutput</span><span class="sxs-lookup"><span data-stu-id="1d028-101">Get-AzureRmAutomationJobOutput</span></span>

## <span data-ttu-id="1d028-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d028-102">SYNOPSIS</span></span>
<span data-ttu-id="1d028-103">Pobiera dane wyjściowe zadania automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="1d028-103">Gets the output of an Automation job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d028-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d028-104">SYNTAX</span></span>

```
Get-AzureRmAutomationJobOutput [-Id] <Guid> [-Stream <StreamType>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d028-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d028-105">DESCRIPTION</span></span>
<span data-ttu-id="1d028-106">Polecenie cmdlet **Get-AzureRmAutomationJobOutput** pobiera dane wyjściowe zadania usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1d028-106">The **Get-AzureRmAutomationJobOutput** cmdlet gets the output of an Azure Automation job.</span></span>

## <span data-ttu-id="1d028-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d028-107">EXAMPLES</span></span>

### <span data-ttu-id="1d028-108">Przykład 1. Pobieranie danych wyjściowych zadania automatyzacji</span><span class="sxs-lookup"><span data-stu-id="1d028-108">Example 1: Get the output of an Automation job</span></span>
```
PS C:\>Get-AzureRmAutomationJobOutput -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64 -ResourceGroupName "ResourceGroup01" -Stream "Any"
```

<span data-ttu-id="1d028-109">To polecenie pobiera wszystkie dane wyjściowe zadania o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="1d028-109">This command gets all of the output of the job that has the specified ID.</span></span>

## <span data-ttu-id="1d028-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d028-110">PARAMETERS</span></span>

### <span data-ttu-id="1d028-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d028-111">-AutomationAccountName</span></span>
<span data-ttu-id="1d028-112">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="1d028-112">Specifies the name of an Automation account for which this cmdlet gets job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d028-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d028-113">-DefaultProfile</span></span>
<span data-ttu-id="1d028-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1d028-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1d028-115">-ID</span><span class="sxs-lookup"><span data-stu-id="1d028-115">-Id</span></span>
<span data-ttu-id="1d028-116">Określa identyfikator zadania, dla którego to polecenie cmdlet pobiera dane wyjściowe.</span><span class="sxs-lookup"><span data-stu-id="1d028-116">Specifies the ID of a job for which this cmdlet gets output.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d028-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d028-117">-ResourceGroupName</span></span>
<span data-ttu-id="1d028-118">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera dane wyjściowe zadania.</span><span class="sxs-lookup"><span data-stu-id="1d028-118">Specifies the name of a resource group for which this cmdlet gets job output.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d028-119">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1d028-119">-StartTime</span></span>
<span data-ttu-id="1d028-120">Określa godzinę rozpoczęcia jako obiekt **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="1d028-120">Specifies a start time as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="1d028-121">Możesz określić ciąg, który może być konwertowany na prawidłowy znak **DateTimeOffset**.</span><span class="sxs-lookup"><span data-stu-id="1d028-121">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="1d028-122">Polecenie cmdlet umożliwia pobranie danych wyjściowych utworzonych po tym czasie.</span><span class="sxs-lookup"><span data-stu-id="1d028-122">The cmdlet retrieves output created after this time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d028-123">-Stream</span><span class="sxs-lookup"><span data-stu-id="1d028-123">-Stream</span></span>
<span data-ttu-id="1d028-124">Określa typ danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1d028-124">Specifies the type of output.</span></span>
<span data-ttu-id="1d028-125">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="1d028-125">Valid values are:</span></span> 

- <span data-ttu-id="1d028-126">Jakieś</span><span class="sxs-lookup"><span data-stu-id="1d028-126">Any</span></span>
- <span data-ttu-id="1d028-127">Wykrywanie</span><span class="sxs-lookup"><span data-stu-id="1d028-127">Debug</span></span>
- <span data-ttu-id="1d028-128">Błędów</span><span class="sxs-lookup"><span data-stu-id="1d028-128">Error</span></span>
- <span data-ttu-id="1d028-129">Prowadzone</span><span class="sxs-lookup"><span data-stu-id="1d028-129">Output</span></span>
- <span data-ttu-id="1d028-130">Okres</span><span class="sxs-lookup"><span data-stu-id="1d028-130">Progress</span></span>
- <span data-ttu-id="1d028-131">Pełne</span><span class="sxs-lookup"><span data-stu-id="1d028-131">Verbose</span></span>
- <span data-ttu-id="1d028-132">Ostrzeżenie</span><span class="sxs-lookup"><span data-stu-id="1d028-132">Warning</span></span>

```yaml
Type: StreamType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, Progress, Output, Warning, Error, Debug, Verbose

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d028-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d028-133">CommonParameters</span></span>
<span data-ttu-id="1d028-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d028-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d028-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d028-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d028-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d028-136">INPUTS</span></span>

### <span data-ttu-id="1d028-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1d028-137">None</span></span>
<span data-ttu-id="1d028-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="1d028-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1d028-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d028-139">OUTPUTS</span></span>

### <span data-ttu-id="1d028-140">Microsoft. Azure. Commands. Automation. model. JobStream</span><span class="sxs-lookup"><span data-stu-id="1d028-140">Microsoft.Azure.Commands.Automation.Model.JobStream</span></span>

## <span data-ttu-id="1d028-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d028-141">NOTES</span></span>

## <span data-ttu-id="1d028-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d028-142">RELATED LINKS</span></span>

[<span data-ttu-id="1d028-143">Get-AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d028-143">Get-AzureRmAutomationJob</span></span>](./Get-AzureRMAutomationJob.md)

[<span data-ttu-id="1d028-144">Życiorys — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d028-144">Resume-AzureRmAutomationJob</span></span>](./Resume-AzureRMAutomationJob.md)

[<span data-ttu-id="1d028-145">Zatrzymaj — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d028-145">Stop-AzureRmAutomationJob</span></span>](./Stop-AzureRMAutomationJob.md)

[<span data-ttu-id="1d028-146">Suspend — AzureRmAutomationJob</span><span class="sxs-lookup"><span data-stu-id="1d028-146">Suspend-AzureRmAutomationJob</span></span>](./Suspend-AzureRMAutomationJob.md)


