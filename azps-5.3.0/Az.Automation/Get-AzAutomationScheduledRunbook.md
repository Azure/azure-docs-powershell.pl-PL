---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502353"
---
# <span data-ttu-id="893dd-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="893dd-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="893dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="893dd-102">SYNOPSIS</span></span>
<span data-ttu-id="893dd-103">Pobiera elementy Runbook funkcji Automation i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="893dd-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="893dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="893dd-104">SYNTAX</span></span>

### <span data-ttu-id="893dd-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="893dd-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="893dd-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="893dd-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="893dd-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="893dd-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="893dd-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="893dd-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="893dd-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="893dd-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="893dd-110">Opis</span><span class="sxs-lookup"><span data-stu-id="893dd-110">DESCRIPTION</span></span>
<span data-ttu-id="893dd-111">Polecenie cmdlet **Get-AzAutomationScheduledRunbook** pobiera co najmniej jeden element Runbook usługi Azure Automation i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="893dd-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="893dd-112">Domyślnie to polecenie cmdlet pobiera wszystkie zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="893dd-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="893dd-113">Określ nazwę elementu Runbook lub harmonogram albo oba te elementy, aby wyświetlić określone harmonogramy elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="893dd-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="893dd-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="893dd-114">EXAMPLES</span></span>

### <span data-ttu-id="893dd-115">Przykład 1: pobieranie wszystkich zaplanowanych elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="893dd-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="893dd-116">To polecenie pobiera wszystkie zaplanowane elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="893dd-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="893dd-117">Przykład 2: pobieranie wszystkich harmonogramów skojarzonych z elementem Runbook</span><span class="sxs-lookup"><span data-stu-id="893dd-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="893dd-118">To polecenie pobiera wszystkie zaplanowane elementy Runbook dla elementu Runbook Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="893dd-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="893dd-119">Przykład 3: pobieranie wszystkich elementów Runbook skojarzonych z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="893dd-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="893dd-120">To polecenie pobiera wszystkie zaplanowane elementy Runbook dla Schedule01 harmonogram na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="893dd-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="893dd-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="893dd-121">PARAMETERS</span></span>

### <span data-ttu-id="893dd-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="893dd-122">-AutomationAccountName</span></span>
<span data-ttu-id="893dd-123">Określa konto usługi Automation dla elementu Runbook, dla którego działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="893dd-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="893dd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="893dd-124">-DefaultProfile</span></span>
<span data-ttu-id="893dd-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="893dd-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="893dd-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="893dd-126">-JobScheduleId</span></span>
<span data-ttu-id="893dd-127">Określa identyfikator zaplanowanego zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="893dd-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="893dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="893dd-129">Określa nazwę grupy zasobów dla zaplanowanych elementów Runbook, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="893dd-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="893dd-130">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="893dd-130">-RunbookName</span></span>
<span data-ttu-id="893dd-131">Określa nazwę elementu Runbook, dla którego ten aplet polecenia pobiera zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="893dd-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893dd-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="893dd-132">-ScheduleName</span></span>
<span data-ttu-id="893dd-133">Określa nazwę harmonogramu, dla którego ten aplet polecenia pobiera zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="893dd-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="893dd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="893dd-134">CommonParameters</span></span>
<span data-ttu-id="893dd-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="893dd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="893dd-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="893dd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="893dd-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="893dd-137">INPUTS</span></span>

### <span data-ttu-id="893dd-138">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="893dd-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="893dd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="893dd-139">System.String</span></span>

## <span data-ttu-id="893dd-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="893dd-140">OUTPUTS</span></span>

### <span data-ttu-id="893dd-141">Microsoft. Azure. Commands. Automation. model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="893dd-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="893dd-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="893dd-142">NOTES</span></span>

## <span data-ttu-id="893dd-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="893dd-143">RELATED LINKS</span></span>

[<span data-ttu-id="893dd-144">Rejestr — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="893dd-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="893dd-145">Wyrejestrowanie — AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="893dd-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


