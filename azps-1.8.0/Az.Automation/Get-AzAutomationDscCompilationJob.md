---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 8742b9967720948118f132de23fd07dbfdcb5f0a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710597"
---
# <span data-ttu-id="e9669-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e9669-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="e9669-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9669-102">SYNOPSIS</span></span>
<span data-ttu-id="e9669-103">Pobiera zadania kompilacji DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e9669-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="e9669-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9669-104">SYNTAX</span></span>

### <span data-ttu-id="e9669-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e9669-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e9669-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="e9669-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9669-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e9669-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9669-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e9669-108">DESCRIPTION</span></span>
<span data-ttu-id="e9669-109">Polecenie cmdlet **Get-AzAutomationDscCompilationJob** pobiera zadania kompilacji pożądanej konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e9669-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="e9669-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9669-110">EXAMPLES</span></span>

### <span data-ttu-id="e9669-111">Przykład 1: pobieranie wszystkich zadań kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="e9669-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="e9669-112">To polecenie pobiera wszystkie zadania kompilacji na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e9669-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e9669-113">Przykład 2: pobieranie zadań kompilacji DSC dla konfiguracji</span><span class="sxs-lookup"><span data-stu-id="e9669-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="e9669-114">To polecenie pobiera wszystkie zadania kompilacji dla konfiguracji DSC o nazwie ContosoConfiguration na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e9669-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="e9669-115">Przykład 3: uzyskiwanie określonego zadania kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="e9669-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="e9669-116">To polecenie pobiera zadanie kompilacji z określonym IDENTYFIKATORem na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e9669-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="e9669-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9669-117">PARAMETERS</span></span>

### <span data-ttu-id="e9669-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e9669-118">-AutomationAccountName</span></span>
<span data-ttu-id="e9669-119">Określa nazwę konta automatyzacji zawierającego zadania kompilacji DSC, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9669-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e9669-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="e9669-120">-ConfigurationName</span></span>
<span data-ttu-id="e9669-121">Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera zadania kompilacji.</span><span class="sxs-lookup"><span data-stu-id="e9669-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9669-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9669-122">-DefaultProfile</span></span>
<span data-ttu-id="e9669-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e9669-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e9669-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e9669-124">-EndTime</span></span>
<span data-ttu-id="e9669-125">Określa godzinę zakończenia.</span><span class="sxs-lookup"><span data-stu-id="e9669-125">Specifies an end time.</span></span>
<span data-ttu-id="e9669-126">To polecenie cmdlet umożliwia pobieranie zadań kompilacji, które zostały uruchomione do momentu, gdy ten parametr określi.</span><span class="sxs-lookup"><span data-stu-id="e9669-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9669-127">-ID</span><span class="sxs-lookup"><span data-stu-id="e9669-127">-Id</span></span>
<span data-ttu-id="e9669-128">Określa unikatowy identyfikator zadania kompilacji DSC, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9669-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9669-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9669-129">-ResourceGroupName</span></span>
<span data-ttu-id="e9669-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="e9669-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="e9669-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e9669-131">-StartTime</span></span>
<span data-ttu-id="e9669-132">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="e9669-132">Specifies a start time.</span></span>
<span data-ttu-id="e9669-133">To polecenie cmdlet pobiera zadania, które zaczynają się od godziny lub po upływie tego parametru.</span><span class="sxs-lookup"><span data-stu-id="e9669-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll, ByConfigurationName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9669-134">-Status</span><span class="sxs-lookup"><span data-stu-id="e9669-134">-Status</span></span>
<span data-ttu-id="e9669-135">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9669-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="e9669-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="e9669-136">Valid values are:</span></span> 
- <span data-ttu-id="e9669-137">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="e9669-137">Completed</span></span> 
- <span data-ttu-id="e9669-138">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="e9669-138">Failed</span></span> 
- <span data-ttu-id="e9669-139">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="e9669-139">Queued</span></span> 
- <span data-ttu-id="e9669-140">Czynając</span><span class="sxs-lookup"><span data-stu-id="e9669-140">Starting</span></span> 
- <span data-ttu-id="e9669-141">Działanie</span><span class="sxs-lookup"><span data-stu-id="e9669-141">Resuming</span></span> 
- <span data-ttu-id="e9669-142">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="e9669-142">Running</span></span> 
- <span data-ttu-id="e9669-143">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="e9669-143">Stopped</span></span> 
- <span data-ttu-id="e9669-144">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="e9669-144">Stopping</span></span> 
- <span data-ttu-id="e9669-145">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="e9669-145">Suspended</span></span> 
- <span data-ttu-id="e9669-146">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="e9669-146">Suspending</span></span> 
- <span data-ttu-id="e9669-147">Ponownego</span><span class="sxs-lookup"><span data-stu-id="e9669-147">Activating</span></span>
- <span data-ttu-id="e9669-148">Nowy</span><span class="sxs-lookup"><span data-stu-id="e9669-148">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating, New

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9669-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9669-149">CommonParameters</span></span>
<span data-ttu-id="e9669-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9669-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9669-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9669-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9669-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9669-152">INPUTS</span></span>

### <span data-ttu-id="e9669-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="e9669-153">System.Guid</span></span>

### <span data-ttu-id="e9669-154">System. String</span><span class="sxs-lookup"><span data-stu-id="e9669-154">System.String</span></span>

## <span data-ttu-id="e9669-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9669-155">OUTPUTS</span></span>

### <span data-ttu-id="e9669-156">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="e9669-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="e9669-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9669-157">NOTES</span></span>

## <span data-ttu-id="e9669-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9669-158">RELATED LINKS</span></span>

[<span data-ttu-id="e9669-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="e9669-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="e9669-160">Start — AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e9669-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


