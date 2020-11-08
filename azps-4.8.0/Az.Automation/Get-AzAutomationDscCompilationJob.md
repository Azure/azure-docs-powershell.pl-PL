---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdsccompilationjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscCompilationJob.md
ms.openlocfilehash: 5b2c8685596771cd7986d8cfa071808daa63435c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063690"
---
# <span data-ttu-id="5b244-101">Get-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5b244-101">Get-AzAutomationDscCompilationJob</span></span>

## <span data-ttu-id="5b244-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b244-102">SYNOPSIS</span></span>
<span data-ttu-id="5b244-103">Pobiera zadania kompilacji DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="5b244-103">Gets DSC compilation jobs in Automation.</span></span>

## <span data-ttu-id="5b244-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b244-104">SYNTAX</span></span>

### <span data-ttu-id="5b244-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5b244-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5b244-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="5b244-106">ByJobId</span></span>
```
Get-AzAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b244-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5b244-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b244-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5b244-108">DESCRIPTION</span></span>
<span data-ttu-id="5b244-109">Polecenie cmdlet **Get-AzAutomationDscCompilationJob** pobiera zadania kompilacji pożądanej konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="5b244-109">The **Get-AzAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="5b244-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b244-110">EXAMPLES</span></span>

### <span data-ttu-id="5b244-111">Przykład 1: pobieranie wszystkich zadań kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="5b244-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="5b244-112">To polecenie pobiera wszystkie zadania kompilacji na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5b244-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5b244-113">Przykład 2: pobieranie zadań kompilacji DSC dla konfiguracji</span><span class="sxs-lookup"><span data-stu-id="5b244-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="5b244-114">To polecenie pobiera wszystkie zadania kompilacji dla konfiguracji DSC o nazwie ContosoConfiguration na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5b244-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="5b244-115">Przykład 3: uzyskiwanie określonego zadania kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="5b244-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="5b244-116">To polecenie pobiera zadanie kompilacji z określonym IDENTYFIKATORem na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5b244-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="5b244-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b244-117">PARAMETERS</span></span>

### <span data-ttu-id="5b244-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5b244-118">-AutomationAccountName</span></span>
<span data-ttu-id="5b244-119">Określa nazwę konta automatyzacji zawierającego zadania kompilacji DSC, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b244-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b244-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5b244-120">-ConfigurationName</span></span>
<span data-ttu-id="5b244-121">Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera zadania kompilacji.</span><span class="sxs-lookup"><span data-stu-id="5b244-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="5b244-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b244-122">-DefaultProfile</span></span>
<span data-ttu-id="5b244-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5b244-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b244-124">-EndTime</span><span class="sxs-lookup"><span data-stu-id="5b244-124">-EndTime</span></span>
<span data-ttu-id="5b244-125">Określa godzinę zakończenia.</span><span class="sxs-lookup"><span data-stu-id="5b244-125">Specifies an end time.</span></span>
<span data-ttu-id="5b244-126">To polecenie cmdlet umożliwia pobieranie zadań kompilacji, które zostały uruchomione do momentu, gdy ten parametr określi.</span><span class="sxs-lookup"><span data-stu-id="5b244-126">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b244-127">-ID</span><span class="sxs-lookup"><span data-stu-id="5b244-127">-Id</span></span>
<span data-ttu-id="5b244-128">Określa unikatowy identyfikator zadania kompilacji DSC, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b244-128">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b244-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b244-129">-ResourceGroupName</span></span>
<span data-ttu-id="5b244-130">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="5b244-130">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="5b244-131">-StartTime</span><span class="sxs-lookup"><span data-stu-id="5b244-131">-StartTime</span></span>
<span data-ttu-id="5b244-132">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="5b244-132">Specifies a start time.</span></span>
<span data-ttu-id="5b244-133">To polecenie cmdlet pobiera zadania, które zaczynają się od godziny lub po upływie tego parametru.</span><span class="sxs-lookup"><span data-stu-id="5b244-133">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="5b244-134">-Status</span><span class="sxs-lookup"><span data-stu-id="5b244-134">-Status</span></span>
<span data-ttu-id="5b244-135">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b244-135">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="5b244-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="5b244-136">Valid values are:</span></span> 
- <span data-ttu-id="5b244-137">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="5b244-137">Completed</span></span> 
- <span data-ttu-id="5b244-138">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="5b244-138">Failed</span></span> 
- <span data-ttu-id="5b244-139">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="5b244-139">Queued</span></span> 
- <span data-ttu-id="5b244-140">Czynając</span><span class="sxs-lookup"><span data-stu-id="5b244-140">Starting</span></span> 
- <span data-ttu-id="5b244-141">Działanie</span><span class="sxs-lookup"><span data-stu-id="5b244-141">Resuming</span></span> 
- <span data-ttu-id="5b244-142">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="5b244-142">Running</span></span> 
- <span data-ttu-id="5b244-143">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="5b244-143">Stopped</span></span> 
- <span data-ttu-id="5b244-144">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="5b244-144">Stopping</span></span> 
- <span data-ttu-id="5b244-145">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="5b244-145">Suspended</span></span> 
- <span data-ttu-id="5b244-146">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="5b244-146">Suspending</span></span> 
- <span data-ttu-id="5b244-147">Ponownego</span><span class="sxs-lookup"><span data-stu-id="5b244-147">Activating</span></span>
- <span data-ttu-id="5b244-148">Nowy</span><span class="sxs-lookup"><span data-stu-id="5b244-148">New</span></span>

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

### <span data-ttu-id="5b244-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b244-149">CommonParameters</span></span>
<span data-ttu-id="5b244-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b244-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b244-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b244-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b244-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b244-152">INPUTS</span></span>

### <span data-ttu-id="5b244-153">System. GUID</span><span class="sxs-lookup"><span data-stu-id="5b244-153">System.Guid</span></span>

### <span data-ttu-id="5b244-154">System. String</span><span class="sxs-lookup"><span data-stu-id="5b244-154">System.String</span></span>

## <span data-ttu-id="5b244-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b244-155">OUTPUTS</span></span>

### <span data-ttu-id="5b244-156">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="5b244-156">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="5b244-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b244-157">NOTES</span></span>

## <span data-ttu-id="5b244-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b244-158">RELATED LINKS</span></span>

[<span data-ttu-id="5b244-159">Get-AzAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="5b244-159">Get-AzAutomationDscCompilationJobOutput</span></span>](./Get-AzAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="5b244-160">Start — AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5b244-160">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)


