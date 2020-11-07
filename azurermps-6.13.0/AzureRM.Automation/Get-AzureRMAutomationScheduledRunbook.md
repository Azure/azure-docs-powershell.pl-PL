---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: e2b458e7a1f739b7891768d197f1993da065d09f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717962"
---
# <span data-ttu-id="22cb0-101">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="22cb0-101">Get-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="22cb0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="22cb0-103">Pobiera elementy Runbook funkcji Automation i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="22cb0-103">Gets Automation runbooks and associated schedules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22cb0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22cb0-104">SYNTAX</span></span>

### <span data-ttu-id="22cb0-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22cb0-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cb0-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="22cb0-106">ByJobScheduleId</span></span>
```
Get-AzureRmAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cb0-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="22cb0-107">ByRunbookName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cb0-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="22cb0-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22cb0-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="22cb0-109">ByScheduleName</span></span>
```
Get-AzureRmAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="22cb0-110">Opis</span><span class="sxs-lookup"><span data-stu-id="22cb0-110">DESCRIPTION</span></span>
<span data-ttu-id="22cb0-111">Polecenie cmdlet **Get-AzureRmAutomationScheduledRunbook** pobiera co najmniej jeden element Runbook usługi Azure Automation i skojarzone harmonogramy.</span><span class="sxs-lookup"><span data-stu-id="22cb0-111">The **Get-AzureRmAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="22cb0-112">Domyślnie to polecenie cmdlet pobiera wszystkie zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="22cb0-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="22cb0-113">Określ nazwę elementu Runbook lub harmonogram albo oba te elementy, aby wyświetlić określone harmonogramy elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="22cb0-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="22cb0-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22cb0-114">EXAMPLES</span></span>

### <span data-ttu-id="22cb0-115">Przykład 1: pobieranie wszystkich zaplanowanych elementów Runbook</span><span class="sxs-lookup"><span data-stu-id="22cb0-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="22cb0-116">To polecenie pobiera wszystkie zaplanowane elementy Runbook z konta usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="22cb0-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="22cb0-117">Przykład 2: pobieranie wszystkich harmonogramów skojarzonych z elementem Runbook</span><span class="sxs-lookup"><span data-stu-id="22cb0-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="22cb0-118">To polecenie pobiera wszystkie zaplanowane elementy Runbook dla elementu Runbook Runbk01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="22cb0-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="22cb0-119">Przykład 3: pobieranie wszystkich elementów Runbook skojarzonych z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="22cb0-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="22cb0-120">To polecenie pobiera wszystkie zaplanowane elementy Runbook dla Schedule01 harmonogram na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="22cb0-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="22cb0-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22cb0-121">PARAMETERS</span></span>

### <span data-ttu-id="22cb0-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="22cb0-122">-AutomationAccountName</span></span>
<span data-ttu-id="22cb0-123">Określa konto usługi Automation dla elementu Runbook, dla którego działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22cb0-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="22cb0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cb0-124">-DefaultProfile</span></span>
<span data-ttu-id="22cb0-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="22cb0-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22cb0-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="22cb0-126">-JobScheduleId</span></span>
<span data-ttu-id="22cb0-127">Określa identyfikator zaplanowanego zadania, które jest pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22cb0-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="22cb0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cb0-128">-ResourceGroupName</span></span>
<span data-ttu-id="22cb0-129">Określa nazwę grupy zasobów dla zaplanowanych elementów Runbook, które są pobierane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22cb0-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="22cb0-130">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="22cb0-130">-RunbookName</span></span>
<span data-ttu-id="22cb0-131">Określa nazwę elementu Runbook, dla którego ten aplet polecenia pobiera zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="22cb0-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="22cb0-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="22cb0-132">-ScheduleName</span></span>
<span data-ttu-id="22cb0-133">Określa nazwę harmonogramu, dla którego ten aplet polecenia pobiera zaplanowane elementy Runbook.</span><span class="sxs-lookup"><span data-stu-id="22cb0-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="22cb0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cb0-134">CommonParameters</span></span>
<span data-ttu-id="22cb0-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cb0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cb0-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22cb0-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cb0-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22cb0-137">INPUTS</span></span>

### <span data-ttu-id="22cb0-138">System. Nullable "1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="22cb0-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="22cb0-139">System. String</span><span class="sxs-lookup"><span data-stu-id="22cb0-139">System.String</span></span>

## <span data-ttu-id="22cb0-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22cb0-140">OUTPUTS</span></span>

### <span data-ttu-id="22cb0-141">Microsoft. Azure. Commands. Automation. model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="22cb0-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="22cb0-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22cb0-142">NOTES</span></span>

## <span data-ttu-id="22cb0-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22cb0-143">RELATED LINKS</span></span>

[<span data-ttu-id="22cb0-144">Rejestr — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="22cb0-144">Register-AzureRmAutomationScheduledRunbook</span></span>](./Register-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="22cb0-145">Wyrejestrowanie — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="22cb0-145">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


