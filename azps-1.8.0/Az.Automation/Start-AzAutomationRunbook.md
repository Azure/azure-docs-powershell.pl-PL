---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 2f9b5354731a64a5cb614e173aa45be5349197d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710454"
---
# <span data-ttu-id="585a1-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="585a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="585a1-102">SYNOPSIS</span></span>
<span data-ttu-id="585a1-103">Rozpoczyna zadanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="585a1-103">Starts a runbook job.</span></span>

## <span data-ttu-id="585a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="585a1-104">SYNTAX</span></span>

### <span data-ttu-id="585a1-105">ByAsynchronousReturnJob (domyślny)</span><span class="sxs-lookup"><span data-stu-id="585a1-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="585a1-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="585a1-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="585a1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="585a1-107">DESCRIPTION</span></span>
<span data-ttu-id="585a1-108">Polecenie cmdlet **Start-AzAutomationRunbook** rozpoczyna zadanie elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="585a1-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="585a1-109">Określ identyfikator lub nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="585a1-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="585a1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="585a1-110">EXAMPLES</span></span>

### <span data-ttu-id="585a1-111">Przykład 1. Rozpocznij zadanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="585a1-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="585a1-112">To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="585a1-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="585a1-113">Przykład 2: Rozpoczynanie zadania elementu Runbook języka Python 2 przy użyciu parametrów</span><span class="sxs-lookup"><span data-stu-id="585a1-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="585a1-114">To polecenie uruchamia zadanie elementu Runbook dla elementu Runbook języka Python 2 o nazwie RunbkPy01 na koncie usługi Azure Automation o nazwie Contoso17 z nazwą "ValueForPosition1" jako pierwszym parametrem pozycyjnym i "ValueForPosition2" dla drugiego.</span><span class="sxs-lookup"><span data-stu-id="585a1-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="585a1-115">Przykład 3: Rozpoczynanie zadania elementu Runbook i oczekiwanie na wyniki</span><span class="sxs-lookup"><span data-stu-id="585a1-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="585a1-116">To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="585a1-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="585a1-117">To polecenie określa parametr _oczekiwania_ .</span><span class="sxs-lookup"><span data-stu-id="585a1-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="585a1-118">Dlatego zwraca on wyniki po wykonaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="585a1-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="585a1-119">Polecenie cmdlet czeka maksymalnie 1000 sekund na wyniki.</span><span class="sxs-lookup"><span data-stu-id="585a1-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="585a1-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="585a1-120">PARAMETERS</span></span>

### <span data-ttu-id="585a1-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="585a1-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="585a1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="585a1-122">-DefaultProfile</span></span>
<span data-ttu-id="585a1-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="585a1-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="585a1-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="585a1-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="585a1-125">Określa liczbę sekund, przez jaką to polecenie cmdlet oczekuje na zakończenie zadania, zanim odrzuca to zadanie.</span><span class="sxs-lookup"><span data-stu-id="585a1-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="585a1-126">Wartość domyślna to 10800 lub trzy godziny.</span><span class="sxs-lookup"><span data-stu-id="585a1-126">The default value is 10800, or three hours.</span></span>

```yaml
Type: System.Int32
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585a1-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="585a1-127">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585a1-128">— Parametry</span><span class="sxs-lookup"><span data-stu-id="585a1-128">-Parameters</span></span>
```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: JobParameters

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585a1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="585a1-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="585a1-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="585a1-130">-RunOn</span></span>
<span data-ttu-id="585a1-131">Określa grupę hybrydowych procesów roboczych, na której ma zostać uruchomiony element Runbook.</span><span class="sxs-lookup"><span data-stu-id="585a1-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="585a1-132">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="585a1-132">-Wait</span></span>
<span data-ttu-id="585a1-133">Wskazuje, że to polecenie cmdlet oczekuje na ukończenie zadania, zawieszenie lub niepowodzenie, a następnie zwróci kontrolę do środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="585a1-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySynchronousReturnJobOutput
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="585a1-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="585a1-134">CommonParameters</span></span>
<span data-ttu-id="585a1-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="585a1-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="585a1-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="585a1-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="585a1-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="585a1-137">INPUTS</span></span>

### <span data-ttu-id="585a1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="585a1-138">System.String</span></span>

## <span data-ttu-id="585a1-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="585a1-139">OUTPUTS</span></span>

### <span data-ttu-id="585a1-140">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="585a1-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="585a1-141">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="585a1-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="585a1-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="585a1-142">NOTES</span></span>

## <span data-ttu-id="585a1-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="585a1-143">RELATED LINKS</span></span>

[<span data-ttu-id="585a1-144">Eksportowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-146">Import — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-147">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-148">Nowe — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-149">Publikowanie — AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="585a1-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="585a1-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)