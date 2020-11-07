---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: B2D9FF7B-EA3B-4853-814C-00FC4E328957
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRMAutomationRunbook.md
ms.openlocfilehash: 46544d42cb28f5fca046586696b95286cdd7f3ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717951"
---
# <span data-ttu-id="c0148-101">Start-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-101">Start-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="c0148-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0148-102">SYNOPSIS</span></span>
<span data-ttu-id="c0148-103">Rozpoczyna zadanie elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="c0148-103">Starts a runbook job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0148-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0148-104">SYNTAX</span></span>

### <span data-ttu-id="c0148-105">ByAsynchronousReturnJob (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c0148-105">ByAsynchronousReturnJob (Default)</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c0148-106">BySynchronousReturnJobOutput</span><span class="sxs-lookup"><span data-stu-id="c0148-106">BySynchronousReturnJobOutput</span></span>
```
Start-AzureRmAutomationRunbook [-Name] <String> [-Parameters <IDictionary>] [-RunOn <String>] [-Wait]
 [-MaxWaitSeconds <Int32>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c0148-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0148-107">DESCRIPTION</span></span>
<span data-ttu-id="c0148-108">Polecenie cmdlet **Start-AzureRmAutomationRunbook** rozpoczyna zadanie elementu Runbook usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c0148-108">The **Start-AzureRmAutomationRunbook** cmdlet starts an Azure Automation runbook job.</span></span>
<span data-ttu-id="c0148-109">Określ identyfikator lub nazwę elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="c0148-109">Specify the ID or name of a runbook.</span></span>

## <span data-ttu-id="c0148-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0148-110">EXAMPLES</span></span>

### <span data-ttu-id="c0148-111">Przykład 1. Rozpocznij zadanie elementu Runbook</span><span class="sxs-lookup"><span data-stu-id="c0148-111">Example 1: Start a runbook job</span></span>
```
PS C:\>Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c0148-112">To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0148-112">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="c0148-113">Przykład 2: Rozpoczynanie zadania elementu Runbook i oczekiwanie na wyniki</span><span class="sxs-lookup"><span data-stu-id="c0148-113">Example 2: Start a runbook job and wait for results</span></span>
```
Start-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -MaxWaitSeconds 1000 -Wait
```

<span data-ttu-id="c0148-114">To polecenie uruchamia zadanie elementu Runbook o nazwie Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c0148-114">This command starts a runbook job for the runbook named Runbk01 in the Azure Automation account named Contoso17.</span></span>
<span data-ttu-id="c0148-115">To polecenie określa parametr _oczekiwania_ .</span><span class="sxs-lookup"><span data-stu-id="c0148-115">This command specifies the _Wait_ parameter.</span></span>
<span data-ttu-id="c0148-116">Dlatego zwraca on wyniki po wykonaniu zadania.</span><span class="sxs-lookup"><span data-stu-id="c0148-116">Therefore, it returns results after the job is completed.</span></span>
<span data-ttu-id="c0148-117">Polecenie cmdlet czeka maksymalnie 1000 sekund na wyniki.</span><span class="sxs-lookup"><span data-stu-id="c0148-117">The cmdlet waits up to 1000 seconds for the results.</span></span>

## <span data-ttu-id="c0148-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0148-118">PARAMETERS</span></span>

### <span data-ttu-id="c0148-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0148-119">-AutomationAccountName</span></span>
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

### <span data-ttu-id="c0148-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0148-120">-DefaultProfile</span></span>
<span data-ttu-id="c0148-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c0148-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0148-122">-MaxWaitSeconds</span><span class="sxs-lookup"><span data-stu-id="c0148-122">-MaxWaitSeconds</span></span>
<span data-ttu-id="c0148-123">Określa liczbę sekund, przez jaką to polecenie cmdlet oczekuje na zakończenie zadania, zanim odrzuca to zadanie.</span><span class="sxs-lookup"><span data-stu-id="c0148-123">Specifies the number of seconds this cmdlet waits for a job to finish before it abandons the job.</span></span>
<span data-ttu-id="c0148-124">Wartość domyślna to 10800 lub trzy godziny.</span><span class="sxs-lookup"><span data-stu-id="c0148-124">The default value is 10800, or three hours.</span></span>

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

### <span data-ttu-id="c0148-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0148-125">-Name</span></span>
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

### <span data-ttu-id="c0148-126">— Parametry</span><span class="sxs-lookup"><span data-stu-id="c0148-126">-Parameters</span></span>
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

### <span data-ttu-id="c0148-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0148-127">-ResourceGroupName</span></span>
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

### <span data-ttu-id="c0148-128">-RunOn</span><span class="sxs-lookup"><span data-stu-id="c0148-128">-RunOn</span></span>
<span data-ttu-id="c0148-129">Określa grupę hybrydowych procesów roboczych, na której ma zostać uruchomiony element Runbook.</span><span class="sxs-lookup"><span data-stu-id="c0148-129">Specifies which Hybrid Worker Group on which to run the runbook.</span></span>

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

### <span data-ttu-id="c0148-130">-Czekaj</span><span class="sxs-lookup"><span data-stu-id="c0148-130">-Wait</span></span>
<span data-ttu-id="c0148-131">Wskazuje, że to polecenie cmdlet oczekuje na ukończenie zadania, zawieszenie lub niepowodzenie, a następnie zwróci kontrolę do środowiska Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c0148-131">Indicates that this cmdlet waits for job to complete, suspend, or fail, and then returns control to Azure PowerShell.</span></span>

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

### <span data-ttu-id="c0148-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0148-132">CommonParameters</span></span>
<span data-ttu-id="c0148-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0148-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0148-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0148-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0148-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0148-135">INPUTS</span></span>

### <span data-ttu-id="c0148-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c0148-136">System.String</span></span>

## <span data-ttu-id="c0148-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0148-137">OUTPUTS</span></span>

### <span data-ttu-id="c0148-138">Microsoft. Azure. Commands. Automation. model. job</span><span class="sxs-lookup"><span data-stu-id="c0148-138">Microsoft.Azure.Commands.Automation.Model.Job</span></span>
<span data-ttu-id="c0148-139">-To polecenie cmdlet zwraca obiekt **zadania** , chyba że podano parametr _wait_ .</span><span class="sxs-lookup"><span data-stu-id="c0148-139">-This cmdlet returns a **Job** object, unless you specify the _Wait_ parameter.</span></span>
<span data-ttu-id="c0148-140">-Jeśli nie określisz funkcji _czekaj_ , środowisko Azure PowerShell zwraca obiekt **zadania** natychmiast.</span><span class="sxs-lookup"><span data-stu-id="c0148-140">-If you do not specify _Wait_ , Azure PowerShell returns a **Job** object immediately.</span></span>
<span data-ttu-id="c0148-141">-Jeśli określisz pozycję _czekaj_ , środowisko Azure PowerShell zakończy zadanie, a następnie zwróci wynik.</span><span class="sxs-lookup"><span data-stu-id="c0148-141">-If you specify _Wait_ , Azure PowerShell completes the job, and then returns the result.</span></span>
<span data-ttu-id="c0148-142">-Wynik nie jest obiektem **zadania** .</span><span class="sxs-lookup"><span data-stu-id="c0148-142">-The result is not a **Job** object.</span></span>

### <span data-ttu-id="c0148-143">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c0148-143">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c0148-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0148-144">NOTES</span></span>

## <span data-ttu-id="c0148-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0148-145">RELATED LINKS</span></span>

[<span data-ttu-id="c0148-146">Eksportowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-146">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-147">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-147">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-148">Import — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-148">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-149">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-149">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-150">Nowe — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-150">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-151">Publikowanie — AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-151">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-152">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-152">Remove-AzureRmAutomationRunbook</span></span>](./Remove-AzureRMAutomationRunbook.md)

[<span data-ttu-id="c0148-153">Set-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="c0148-153">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)
