---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRMAutomationScheduledRunbook.md
ms.openlocfilehash: deb6611fedbb1f88b9668b4750e096056ea8b1b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717277"
---
# <span data-ttu-id="99893-101">Register-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="99893-101">Register-AzureRmAutomationScheduledRunbook</span></span>

## <span data-ttu-id="99893-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="99893-102">SYNOPSIS</span></span>
<span data-ttu-id="99893-103">Kojarzy element Runbook z harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="99893-103">Associates a runbook to a schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="99893-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="99893-104">SYNTAX</span></span>

### <span data-ttu-id="99893-105">ByRunbookName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="99893-105">ByRunbookName (Default)</span></span>
```
Register-AzureRmAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99893-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="99893-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzureRmAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String>
 [-Parameters <IDictionary>] [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="99893-107">Opis</span><span class="sxs-lookup"><span data-stu-id="99893-107">DESCRIPTION</span></span>
<span data-ttu-id="99893-108">Polecenie cmdlet **register-AzureRmAutomationScheduledRunbook** kojarzy element Runbook usługi Azure Automation z harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="99893-108">The **Register-AzureRmAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="99893-109">Element Runbook rozpoczyna się według harmonogramu określonego za pomocą parametru *ScheduleName* .</span><span class="sxs-lookup"><span data-stu-id="99893-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="99893-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="99893-110">EXAMPLES</span></span>

### <span data-ttu-id="99893-111">Przykład 1: Kojarzenie elementu Runbook z harmonogramem</span><span class="sxs-lookup"><span data-stu-id="99893-111">Example 1: Associate a runbook with a schedule</span></span>
```
PS C:\>Register-AzureRmAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="99893-112">To polecenie kojarzy element Runbook o nazwie Runbk01 z harmonogramem o nazwie Sched01 na koncie usługi Azure Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="99893-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="99893-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="99893-113">PARAMETERS</span></span>

### <span data-ttu-id="99893-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="99893-114">-AutomationAccountName</span></span>
<span data-ttu-id="99893-115">Określa konto usługi Automation dla elementu Runbook, dla którego działa to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99893-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="99893-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99893-116">-DefaultProfile</span></span>
<span data-ttu-id="99893-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="99893-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99893-118">— Parametry</span><span class="sxs-lookup"><span data-stu-id="99893-118">-Parameters</span></span>
<span data-ttu-id="99893-119">Określa tabelę skrótów par klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="99893-119">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="99893-120">Klucze są nazwami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="99893-120">The keys are runbook parameter names.</span></span>
<span data-ttu-id="99893-121">Wartości są wartościami parametrów elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="99893-121">The values are runbook parameter values.</span></span>
<span data-ttu-id="99893-122">Po uruchomieniu elementu Runbook w odpowiedzi na skojarzony harmonogram te parametry są przekazywane do elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="99893-122">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99893-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99893-123">-ResourceGroupName</span></span>
<span data-ttu-id="99893-124">Określa nazwę grupy zasobów dla zaplanowanego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="99893-124">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="99893-125">-Element runbookname</span><span class="sxs-lookup"><span data-stu-id="99893-125">-RunbookName</span></span>
<span data-ttu-id="99893-126">Określa nazwę elementu Runbook, który jest skojarzony z harmonogramem tego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="99893-126">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99893-127">-RunOn</span><span class="sxs-lookup"><span data-stu-id="99893-127">-RunOn</span></span>
<span data-ttu-id="99893-128">Nazwa grupy hybrydowego procesu roboczego elementu Runbook.</span><span class="sxs-lookup"><span data-stu-id="99893-128">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99893-129">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="99893-129">-ScheduleName</span></span>
<span data-ttu-id="99893-130">Określa nazwę harmonogramu, do którego to polecenie cmdlet kojarzy element Runbook.</span><span class="sxs-lookup"><span data-stu-id="99893-130">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99893-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99893-131">CommonParameters</span></span>
<span data-ttu-id="99893-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99893-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99893-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="99893-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99893-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="99893-134">INPUTS</span></span>

### <span data-ttu-id="99893-135">System. String</span><span class="sxs-lookup"><span data-stu-id="99893-135">System.String</span></span>

## <span data-ttu-id="99893-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="99893-136">OUTPUTS</span></span>

### <span data-ttu-id="99893-137">Microsoft. Azure. Commands. Automation. model. JobSchedule</span><span class="sxs-lookup"><span data-stu-id="99893-137">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="99893-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="99893-138">NOTES</span></span>

## <span data-ttu-id="99893-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="99893-139">RELATED LINKS</span></span>

[<span data-ttu-id="99893-140">Get-AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="99893-140">Get-AzureRmAutomationScheduledRunbook</span></span>](./Get-AzureRMAutomationScheduledRunbook.md)

[<span data-ttu-id="99893-141">Wyrejestrowanie — AzureRmAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="99893-141">Unregister-AzureRmAutomationScheduledRunbook</span></span>](./Unregister-AzureRMAutomationScheduledRunbook.md)


