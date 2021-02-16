---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199627"
---
# <span data-ttu-id="5b691-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5b691-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="5b691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b691-102">SYNOPSIS</span></span>
<span data-ttu-id="5b691-103">Pobiera podręczniki uruchamiania automatyzacji i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="5b691-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="5b691-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5b691-104">SYNTAX</span></span>

### <span data-ttu-id="5b691-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5b691-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b691-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5b691-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b691-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="5b691-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b691-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="5b691-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b691-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="5b691-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b691-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="5b691-110">DESCRIPTION</span></span>
<span data-ttu-id="5b691-111">Polecenie **cmdlet Get-AzAutomationScheduledRunbook** pobiera co najmniej jeden podręcznik Azure Automation i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="5b691-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="5b691-112">Domyślnie to polecenie cmdlet pobiera wszystkie zaplanowane podręczniki runbooks.</span><span class="sxs-lookup"><span data-stu-id="5b691-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="5b691-113">Określ nazwę podręcznika lub harmonogramu albo oba te harmonogramy, aby wyświetlić określone harmonogramy tego podręcznika.</span><span class="sxs-lookup"><span data-stu-id="5b691-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="5b691-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5b691-114">EXAMPLES</span></span>

### <span data-ttu-id="5b691-115">Przykład 1. Uzyskiwanie wszystkich zaplanowanych runbooks</span><span class="sxs-lookup"><span data-stu-id="5b691-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5b691-116">To polecenie pobiera wszystkie zaplanowane podręczniki w ramach konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5b691-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="5b691-117">Przykład 2. Uzyskiwanie wszystkich harmonogramów skojarzonych z podręcznikiem uruchamiania</span><span class="sxs-lookup"><span data-stu-id="5b691-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="5b691-118">To polecenie pobiera wszystkie zaplanowane podręczniki runbook dla runbook Runbk01 na koncie automatyzacji platformy Azure o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5b691-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="5b691-119">Przykład 3. Uzyskiwanie wszystkich runbooków skojarzonych z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="5b691-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="5b691-120">To polecenie pobiera wszystkie zaplanowane podręczniki harmonogramów harmonogramu (Schedule01) na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="5b691-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="5b691-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b691-121">PARAMETERS</span></span>

### <span data-ttu-id="5b691-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5b691-122">-AutomationAccountName</span></span>
<span data-ttu-id="5b691-123">Określa konto automatyzacji dla podręcznika, na którym działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b691-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="5b691-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b691-124">-DefaultProfile</span></span>
<span data-ttu-id="5b691-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="5b691-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5b691-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="5b691-126">-JobScheduleId</span></span>
<span data-ttu-id="5b691-127">Określa identyfikator zaplanowanego zadania, które otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b691-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b691-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b691-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b691-129">Określa nazwę grupy zasobów dla zaplanowanych runbooków, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b691-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5b691-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="5b691-130">-RunbookName</span></span>
<span data-ttu-id="5b691-131">Określa nazwę podręcznika, dla którego to polecenie cmdlet pobiera zaplanowane podręczniki runbooks.</span><span class="sxs-lookup"><span data-stu-id="5b691-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="5b691-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="5b691-132">-ScheduleName</span></span>
<span data-ttu-id="5b691-133">Określa nazwę harmonogramu, dla którego to polecenie cmdlet pobiera zaplanowane podręczniki uruchamiania.</span><span class="sxs-lookup"><span data-stu-id="5b691-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="5b691-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b691-134">CommonParameters</span></span>
<span data-ttu-id="5b691-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b691-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b691-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b691-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b691-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b691-137">INPUTS</span></span>

### <span data-ttu-id="5b691-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="5b691-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="5b691-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5b691-139">System.String</span></span>

## <span data-ttu-id="5b691-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b691-140">OUTPUTS</span></span>

### <span data-ttu-id="5b691-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="5b691-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="5b691-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5b691-142">NOTES</span></span>

## <span data-ttu-id="5b691-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b691-143">RELATED LINKS</span></span>

[<span data-ttu-id="5b691-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5b691-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="5b691-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="5b691-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


