---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D704BAC0-D89E-4F15-ACF8-FA2C1F0D1B8F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscCompilationJob.md
ms.openlocfilehash: 59263dab3037e050229bab2a69c43559c2c1827b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550111"
---
# <span data-ttu-id="b77c3-101">Get-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b77c3-101">Get-AzureRmAutomationDscCompilationJob</span></span>

## <span data-ttu-id="b77c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b77c3-102">SYNOPSIS</span></span>
<span data-ttu-id="b77c3-103">Pobiera zadania kompilacji DSC w automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b77c3-103">Gets DSC compilation jobs in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b77c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b77c3-104">SYNTAX</span></span>

### <span data-ttu-id="b77c3-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b77c3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscCompilationJob [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77c3-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="b77c3-106">ByJobId</span></span>
```
Get-AzureRmAutomationDscCompilationJob -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b77c3-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b77c3-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscCompilationJob -ConfigurationName <String> [-Status <String>]
 [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b77c3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b77c3-108">DESCRIPTION</span></span>
<span data-ttu-id="b77c3-109">Polecenie cmdlet **Get-AzureRmAutomationDscCompilationJob** pobiera zadania kompilacji pożądanej konfiguracji stanu (DSC) w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b77c3-109">The **Get-AzureRmAutomationDscCompilationJob** cmdlet gets APS Desired State Configuration (DSC) compilation jobs in Azure Automation.</span></span>

## <span data-ttu-id="b77c3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b77c3-110">EXAMPLES</span></span>

### <span data-ttu-id="b77c3-111">Przykład 1: pobieranie wszystkich zadań kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="b77c3-111">Example 1: Get all DSC compilation jobs</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b77c3-112">To polecenie pobiera wszystkie zadania kompilacji na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b77c3-112">This command gets all compilation jobs in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b77c3-113">Przykład 2: pobieranie zadań kompilacji DSC dla konfiguracji</span><span class="sxs-lookup"><span data-stu-id="b77c3-113">Example 2: Get DSC compilation jobs for a configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="b77c3-114">To polecenie pobiera wszystkie zadania kompilacji dla konfiguracji DSC o nazwie ContosoConfiguration na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b77c3-114">This command gets all compilation jobs for the DSC configuration named ContosoConfiguration in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b77c3-115">Przykład 3: uzyskiwanie określonego zadania kompilacji DSC</span><span class="sxs-lookup"><span data-stu-id="b77c3-115">Example 3: Get a specific DSC compilation job</span></span>
```
PS C:\>Get-AzureRmAutomationDscCompilationJob -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="b77c3-116">To polecenie pobiera zadanie kompilacji z określonym IDENTYFIKATORem na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b77c3-116">This command gets the compilation job with the specified ID in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="b77c3-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b77c3-117">PARAMETERS</span></span>

### <span data-ttu-id="b77c3-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b77c3-118">-AutomationAccountName</span></span>
<span data-ttu-id="b77c3-119">Określa nazwę konta automatyzacji zawierającego zadania kompilacji DSC, które są dostępne w tym poleceniu cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b77c3-119">Specifies the name of the Automation account that contains DSC compilation jobs that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b77c3-120">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b77c3-120">-ConfigurationName</span></span>
<span data-ttu-id="b77c3-121">Określa nazwę konfiguracji DSC, dla której to polecenie cmdlet pobiera zadania kompilacji.</span><span class="sxs-lookup"><span data-stu-id="b77c3-121">Specifies the name of the DSC configuration for which this cmdlet gets compilation jobs.</span></span>

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

### <span data-ttu-id="b77c3-122">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b77c3-122">-EndTime</span></span>
<span data-ttu-id="b77c3-123">Określa godzinę zakończenia.</span><span class="sxs-lookup"><span data-stu-id="b77c3-123">Specifies an end time.</span></span>
<span data-ttu-id="b77c3-124">To polecenie cmdlet umożliwia pobieranie zadań kompilacji, które zostały uruchomione do momentu, gdy ten parametr określi.</span><span class="sxs-lookup"><span data-stu-id="b77c3-124">This cmdlet gets compilations jobs that started up to the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="b77c3-125">-ID</span><span class="sxs-lookup"><span data-stu-id="b77c3-125">-Id</span></span>
<span data-ttu-id="b77c3-126">Określa unikatowy identyfikator zadania kompilacji DSC, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b77c3-126">Specifies the unique ID of the DSC compilation job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="b77c3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b77c3-127">-ResourceGroupName</span></span>
<span data-ttu-id="b77c3-128">Określa nazwę grupy zasobów, w której to polecenie cmdlet pobiera zadania kompilacji DSC.</span><span class="sxs-lookup"><span data-stu-id="b77c3-128">Specifies the name of a resource group in which this cmdlet gets DSC compilation jobs.</span></span>

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

### <span data-ttu-id="b77c3-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b77c3-129">-StartTime</span></span>
<span data-ttu-id="b77c3-130">Określa godzinę rozpoczęcia.</span><span class="sxs-lookup"><span data-stu-id="b77c3-130">Specifies a start time.</span></span>
<span data-ttu-id="b77c3-131">To polecenie cmdlet pobiera zadania, które zaczynają się od godziny lub po upływie tego parametru.</span><span class="sxs-lookup"><span data-stu-id="b77c3-131">This cmdlet gets jobs that start at or after the time that this parameter specifies.</span></span>

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

### <span data-ttu-id="b77c3-132">-Status</span><span class="sxs-lookup"><span data-stu-id="b77c3-132">-Status</span></span>
<span data-ttu-id="b77c3-133">Określa stan zadań pobieranych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b77c3-133">Specifies the status of jobs that this cmdlet gets.</span></span>
<span data-ttu-id="b77c3-134">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="b77c3-134">Valid values are:</span></span> 

- <span data-ttu-id="b77c3-135">Zakończyć</span><span class="sxs-lookup"><span data-stu-id="b77c3-135">Completed</span></span> 
- <span data-ttu-id="b77c3-136">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="b77c3-136">Failed</span></span> 
- <span data-ttu-id="b77c3-137">Oczekuje</span><span class="sxs-lookup"><span data-stu-id="b77c3-137">Queued</span></span> 
- <span data-ttu-id="b77c3-138">Czynając</span><span class="sxs-lookup"><span data-stu-id="b77c3-138">Starting</span></span> 
- <span data-ttu-id="b77c3-139">Działanie</span><span class="sxs-lookup"><span data-stu-id="b77c3-139">Resuming</span></span> 
- <span data-ttu-id="b77c3-140">Wykonywania</span><span class="sxs-lookup"><span data-stu-id="b77c3-140">Running</span></span> 
- <span data-ttu-id="b77c3-141">Trzymywanie</span><span class="sxs-lookup"><span data-stu-id="b77c3-141">Stopped</span></span> 
- <span data-ttu-id="b77c3-142">Trzymywany</span><span class="sxs-lookup"><span data-stu-id="b77c3-142">Stopping</span></span> 
- <span data-ttu-id="b77c3-143">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="b77c3-143">Suspended</span></span> 
- <span data-ttu-id="b77c3-144">Zawieszeniem</span><span class="sxs-lookup"><span data-stu-id="b77c3-144">Suspending</span></span> 
- <span data-ttu-id="b77c3-145">Ponownego</span><span class="sxs-lookup"><span data-stu-id="b77c3-145">Activating</span></span>
- <span data-ttu-id="b77c3-146">Nowy</span><span class="sxs-lookup"><span data-stu-id="b77c3-146">New</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases: 
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b77c3-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b77c3-147">-DefaultProfile</span></span>
<span data-ttu-id="b77c3-148">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b77c3-148">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b77c3-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b77c3-149">CommonParameters</span></span>
<span data-ttu-id="b77c3-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b77c3-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b77c3-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b77c3-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b77c3-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b77c3-152">INPUTS</span></span>

## <span data-ttu-id="b77c3-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b77c3-153">OUTPUTS</span></span>

### <span data-ttu-id="b77c3-154">Microsoft. Azure. Commands. Automation. model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="b77c3-154">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="b77c3-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b77c3-155">NOTES</span></span>

## <span data-ttu-id="b77c3-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b77c3-156">RELATED LINKS</span></span>

[<span data-ttu-id="b77c3-157">Get-AzureRmAutomationDscCompilationJobOutput</span><span class="sxs-lookup"><span data-stu-id="b77c3-157">Get-AzureRmAutomationDscCompilationJobOutput</span></span>](./Get-AzureRmAutomationDscCompilationJobOutput.md)

[<span data-ttu-id="b77c3-158">Start — AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="b77c3-158">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)


