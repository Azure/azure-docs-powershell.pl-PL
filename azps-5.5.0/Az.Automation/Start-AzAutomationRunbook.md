---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationRunbook.md
ms.openlocfilehash: 70d322b46f8aa9dc90696cbd813e576cc9dd9fbd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182091"
---
# <span data-ttu-id="2b97c-101">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-101">Start-AzAutomationRunbook</span></span>

## <span data-ttu-id="2b97c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b97c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b97c-103">Uruchamia zadanie podręcznika.</span><span class="sxs-lookup"><span data-stu-id="2b97c-103">Starts a runbook job.</span></span>

## <span data-ttu-id="2b97c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2b97c-104">SYNTAX</span></span>

### <span data-ttu-id="2b97c-105">ByAsynchronousReturnJob (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="2b97c-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b97c-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="2b97c-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b97c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2b97c-107">DESCRIPTION</span></span>
<span data-ttu-id="2b97c-108">Polecenie **cmdlet Start-AzAutomationRunbook** uruchamia zadanie podręcznika Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2b97c-108">The **Start-AzAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="2b97c-109">Określ identyfikator lub nazwę podręcznika.</span><span class="sxs-lookup"><span data-stu-id="2b97c-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="2b97c-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2b97c-110">EXAMPLES</span></span>

### <span data-ttu-id="2b97c-111">Przykład 1. Uruchamianie zadania podręcznika</span><span class="sxs-lookup"><span data-stu-id="2b97c-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2b97c-112">To polecenie uruchamia zadanie podręcznika uruchamiania o nazwie Runbk01 na koncie automatyzacji platformy Azure o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2b97c-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="2b97c-113">Przykład 2. Uruchamianie zadania w języku Python 2 runbook z parametrami</span><span class="sxs-lookup"><span data-stu-id="2b97c-113">Example 2: Start a Python 2 runbook job with parameters</span></span>
```
PS C:\>Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "RunbkPy01" -ResourceGroupName "ResourceGroup01" -Parameters @{"Key1"="ValueForPosition1";"Key2"="ValueForPosition2"}
```

<span data-ttu-id="2b97c-114">To polecenie uruchamia zadanie podręcznika uruchamiania dla podręcznika Python 2 o nazwie RunbkPy01 na koncie automatyzacji platformy Azure o nazwie Contoso17 z parametrem "ValueForPosition1" jako pierwszym parametrem pozytowym i parametrem "ValueForPosition2" drugiego.</span><span class="sxs-lookup"><span data-stu-id="2b97c-114">This command starts a runbook job for the Python 2 runbook named RunbkPy01 in the Azure Automation account named Contoso17 with "ValueForPosition1" as the first positional parameter and "ValueForPosition2" for the second one.</span></span>

### <span data-ttu-id="2b97c-115">Przykład 3. Uruchamianie zadania podręcznika i oczekiwanie na wyniki</span><span class="sxs-lookup"><span data-stu-id="2b97c-115">Example 3: Start a runbook job and wait for results</span></span>
```
Start-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="2b97c-116">To polecenie uruchamia zadanie podręcznika uruchamiania o nazwie Runbk01 na koncie automatyzacji platformy Azure o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2b97c-116">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="2b97c-117">To polecenie określa parametr _Wait (Czekaj)._</span><span class="sxs-lookup"><span data-stu-id="2b97c-117">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="2b97c-118">Dlatego zwraca wyniki po zakończeniu zadania.</span><span class="sxs-lookup"><span data-stu-id="2b97c-118">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="2b97c-119">Polecenie cmdlet czeka do 1000 sekund na wyniki.</span><span class="sxs-lookup"><span data-stu-id="2b97c-119">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="2b97c-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b97c-120">PARAMETERS</span></span>

### <span data-ttu-id="2b97c-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2b97c-121">-AutomationAccountName</span></span>
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

### <span data-ttu-id="2b97c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b97c-122">-DefaultProfile</span></span>
<span data-ttu-id="2b97c-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2b97c-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b97c-124">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="2b97c-124">-MaxWaitSeconds</span></span>
<span data-ttu-id="2b97c-125">Określa liczbę sekund oczekiwania na zakończenie zadania przez to polecenie cmdlet, zanim je porzuci.</span><span class="sxs-lookup"><span data-stu-id="2b97c-125">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="2b97c-126">Wartość domyślna to 10800, czyli trzy godziny.</span><span class="sxs-lookup"><span data-stu-id="2b97c-126">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="2b97c-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2b97c-127">-Name</span></span>
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

### <span data-ttu-id="2b97c-128">— Parametry</span><span class="sxs-lookup"><span data-stu-id="2b97c-128">-Parameters</span></span>
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

### <span data-ttu-id="2b97c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b97c-129">-ResourceGroupName</span></span>
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

### <span data-ttu-id="2b97c-130">- RunOn</span><span class="sxs-lookup"><span data-stu-id="2b97c-130">-RunOn</span></span>
<span data-ttu-id="2b97c-131">Określa grupę pracowników hybrydowych, w której ma być uruchamiany podręcznik.</span><span class="sxs-lookup"><span data-stu-id="2b97c-131">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="2b97c-132">— Czekanie</span><span class="sxs-lookup"><span data-stu-id="2b97c-132">-Wait</span></span>
<span data-ttu-id="2b97c-133">Wskazuje, że to polecenie cmdlet czeka na ukończenie, zawieszenie lub niepowodzenie zadania, a następnie zwraca kontrolkę do programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2b97c-133">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="2b97c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b97c-134">CommonParameters</span></span>
<span data-ttu-id="2b97c-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b97c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b97c-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b97c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b97c-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b97c-137">INPUTS</span></span>

### <span data-ttu-id="2b97c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="2b97c-138">System.String</span></span>

## <span data-ttu-id="2b97c-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b97c-139">OUTPUTS</span></span>

### <span data-ttu-id="2b97c-140">Microsoft.Azure.Commands.Automation.Model.Job</span><span class="sxs-lookup"><span data-stu-id="2b97c-140">Microsoft.Azure.Commands.Automation.Model.Job</span></span>

### <span data-ttu-id="2b97c-141">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="2b97c-141">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2b97c-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2b97c-142">NOTES</span></span>

## <span data-ttu-id="2b97c-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b97c-143">RELATED LINKS</span></span>

[<span data-ttu-id="2b97c-144">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-144">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-145">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-145">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-146">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-146">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-147">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-147">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-148">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-148">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-149">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-149">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-150">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-150">Remove-AzAutomationRunbook</span></span>](./Remove-AzAutomationRunbook.md)

[<span data-ttu-id="2b97c-151">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2b97c-151">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)
