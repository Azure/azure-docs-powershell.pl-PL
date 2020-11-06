---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: c3c59c8c4f503b090a77a93014f50dd7e2ce01dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542752"
---
# <span data-ttu-id="3518d-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="3518d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3518d-102">SYNOPSIS</span></span>
<span data-ttu-id="3518d-103">Rozpoczyna zadanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3518d-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3518d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3518d-104">SYNTAX</span></span>

### <span data-ttu-id="3518d-105">ByAsynchronousReturnJob (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3518d-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3518d-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="3518d-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3518d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3518d-107">DESCRIPTION</span></span>
<span data-ttu-id="3518d-108">Polecenie cmdlet **Start-AzureRmAutomationRunbook** rozpoczyna zadanie elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3518d-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="3518d-109">Określ identyfikator lub nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="3518d-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="3518d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3518d-110">EXAMPLES</span></span>

### <span data-ttu-id="3518d-111">Przykład 1. Rozpocznij zadanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="3518d-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="3518d-112">To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3518d-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="3518d-113">Przykład 2: Rozpoczynanie zadania elementu Runbook i oczekiwanie na wyniki</span><span class="sxs-lookup"><span data-stu-id="3518d-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="3518d-114">To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="3518d-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="3518d-115">To polecenie określa parametr _oczekiwania_ .</span><span class="sxs-lookup"><span data-stu-id="3518d-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="3518d-116">Dlatego zwraca on wyniki po wykonaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="3518d-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="3518d-117">Polecenie cmdlet czeka maksymalnie 1000 sekund na wyniki.</span><span class="sxs-lookup"><span data-stu-id="3518d-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="3518d-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3518d-118">PARAMETERS</span></span>

### <span data-ttu-id="3518d-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3518d-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="3518d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3518d-120">-DefaultProfile</span></span>
<span data-ttu-id="3518d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3518d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3518d-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="3518d-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="3518d-123">Określa liczbę sekund, przez jaką to polecenie cmdlet oczekuje na zakończenie zadania, zanim odrzuca to zadanie.</span><span class="sxs-lookup"><span data-stu-id="3518d-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="3518d-124">Wartość domyślna to 10800 lub trzy godziny.</span><span class="sxs-lookup"><span data-stu-id="3518d-124">The default value is 10800, or three hours.</span></span>

```yaml
Type: Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3518d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3518d-125">-Name</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3518d-126">— Parametry</span><span class="sxs-lookup"><span data-stu-id="3518d-126">-Parameters</span></span>
```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3518d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3518d-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="3518d-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="3518d-128">-RunOn</span></span>
<span data-ttu-id="3518d-129">Określa grupę hybrydowych procesów roboczych, na której ma zostać uruchomiony element Runbook.</span><span class="sxs-lookup"><span data-stu-id="3518d-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3518d-130">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="3518d-130">-Wait</span></span>
<span data-ttu-id="3518d-131">Wskazuje, że to polecenie cmdlet oczekuje na ukończenie zadania, zawieszenie lub niepowodzenie, a następnie zwróci kontrolę do środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="3518d-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3518d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3518d-132">CommonParameters</span></span>
<span data-ttu-id="3518d-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3518d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3518d-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3518d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3518d-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3518d-135">INPUTS</span></span>

### <span data-ttu-id="3518d-136">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3518d-136">None</span></span>
<span data-ttu-id="3518d-137">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3518d-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3518d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3518d-138">OUTPUTS</span></span>

### <span data-ttu-id="3518d-139">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="3518d-139">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="3518d-140">To polecenie cmdlet zwraca obiekt **zadania** , chyba że podano parametr _wait_ .</span><span class="sxs-lookup"><span data-stu-id="3518d-140">This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>

<span data-ttu-id="3518d-141">Jeśli nie określisz funkcji _czekaj_ , środowisko Azure PowerShell zwraca obiekt **zadania** natychmiast.</span><span class="sxs-lookup"><span data-stu-id="3518d-141">If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="3518d-142">Jeśli określisz pozycję _czekaj_ , środowisko Azure PowerShell zakończy zadanie, a następnie zwróci wynik.</span><span class="sxs-lookup"><span data-stu-id="3518d-142">If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="3518d-143">Wynik nie jest obiektem **zadania** .</span><span class="sxs-lookup"><span data-stu-id="3518d-143">The result is not a **Job** object.</span></span>

## <span data-ttu-id="3518d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3518d-144">NOTES</span></span>

## <span data-ttu-id="3518d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3518d-145">RELATED LINKS</span></span>

[<span data-ttu-id="3518d-146">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-148">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-149">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-150">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-151">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="3518d-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="3518d-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
