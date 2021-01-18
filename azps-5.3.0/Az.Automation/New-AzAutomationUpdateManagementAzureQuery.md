---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationupdatemanagementazurequery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationUpdateManagementAzureQuery.md
ms.openlocfilehash: 68139ff184df62583b3077a38fbc2e26fd5eae09
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502307"
---
# <span data-ttu-id="3c911-101">New-AzAutomationUpdateManagementAzureQuery</span><span class="sxs-lookup"><span data-stu-id="3c911-101">New-AzAutomationUpdateManagementAzureQuery</span></span>

## <span data-ttu-id="3c911-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3c911-102">SYNOPSIS</span></span>
<span data-ttu-id="3c911-103">Tworzy obiekt zapytania usługi Azure konfiguracji aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3c911-103">Creates azure automation software update configuration azure query object.</span></span>

## <span data-ttu-id="3c911-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3c911-104">SYNTAX</span></span>

```
New-AzAutomationUpdateManagementAzureQuery -Scope <String[]> [-Location <String[]>] [-Tag <Hashtable>]
 [-FilterOperator <TagOperators>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3c911-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3c911-105">DESCRIPTION</span></span>
<span data-ttu-id="3c911-106">Tworzy obiekt zapytania platformy Azure konfiguracji aktualizacji oprogramowania, który zostanie wykorzystany do utworzenia konfiguracji aktualizacji oprogramowania, która będzie uruchamiana według harmonogramu w celu zaktualizowania listy dynamicznie rozwiązanej listy maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3c911-106">Creates a software update configuration azure queries object that will be used to create a software update configuration which will runs on a schedule to update a list of dynamically resolved list of azure virtual machines.</span></span>

## <span data-ttu-id="3c911-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3c911-107">EXAMPLES</span></span>

### <span data-ttu-id="3c911-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3c911-108">Example 1</span></span>
```powershell
PS C:\>$query1Scope = @(        
"/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/resourceGroupName",
"/subscriptions/32e2445a-0984-4fa5-86a4-0280d76c4b2d/"
    )
PS C:\>$query1Location =@("Japan East", "UK South")
PS C:\>$query1FilterOperator = "All"
PS C:\>$tag1 = @{"tag1"= @("tag1Value1", "tag1Value2")}
PS C:\>$tag1.add("tag2", "tag2Value")
PS C:\>$azq = New-AzAutomationUpdateManagementAzureQuery -ResourceGroupName "mygroup" `
                                       -AutomationAccountName "myaccount" `
                                       -Scope $query1Scope `
                                       -Location $query1Location `
                                       -Tag $tag1
PS C:\>$AzureQueries = @($azq)
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"

PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `                                                 
                                                 -AzureQuery $AzureQueries `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :

```

## <span data-ttu-id="3c911-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3c911-109">PARAMETERS</span></span>

### <span data-ttu-id="3c911-110">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3c911-110">-AutomationAccountName</span></span>
<span data-ttu-id="3c911-111">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3c911-111">The automation account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c911-112">-DefaultProfile</span></span>
<span data-ttu-id="3c911-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3c911-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-114">-FilterOperator</span><span class="sxs-lookup"><span data-stu-id="3c911-114">-FilterOperator</span></span>
<span data-ttu-id="3c911-115">Operator filtru znacznika.</span><span class="sxs-lookup"><span data-stu-id="3c911-115">Tag filter operator.</span></span>

```yaml
Type: TagOperators
Parameter Sets: (All)
Aliases:
Accepted values: All, Any

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3c911-116">-Location</span></span>
<span data-ttu-id="3c911-117">Lista lokalizacji maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3c911-117">List of locations for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c911-118">-ResourceGroupName</span></span>
<span data-ttu-id="3c911-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3c911-119">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-120">-Zakres</span><span class="sxs-lookup"><span data-stu-id="3c911-120">-Scope</span></span>
<span data-ttu-id="3c911-121">Identyfikatory zasobów dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3c911-121">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="3c911-122">-Tag</span></span>
<span data-ttu-id="3c911-123">Znacznik dla maszyn wirtualnych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3c911-123">Tag for azure virtual machines.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="3c911-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c911-124">CommonParameters</span></span>
<span data-ttu-id="3c911-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c911-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="3c911-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c911-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c911-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3c911-127">INPUTS</span></span>

### <span data-ttu-id="3c911-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="3c911-128">System.String[]</span></span>

### <span data-ttu-id="3c911-129">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="3c911-129">System.Collections.Hashtable</span></span>

### <span data-ttu-id="3c911-130">Microsoft. Azure. Commands. Automation. model. UpdateManagement. TagOperators</span><span class="sxs-lookup"><span data-stu-id="3c911-130">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.TagOperators</span></span>

### <span data-ttu-id="3c911-131">System. String</span><span class="sxs-lookup"><span data-stu-id="3c911-131">System.String</span></span>

## <span data-ttu-id="3c911-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3c911-132">OUTPUTS</span></span>

### <span data-ttu-id="3c911-133">Microsoft. Azure. Commands. Automation. model. UpdateManagement. AzureQueryProperties</span><span class="sxs-lookup"><span data-stu-id="3c911-133">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties</span></span>

## <span data-ttu-id="3c911-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3c911-134">NOTES</span></span>

## <span data-ttu-id="3c911-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3c911-135">RELATED LINKS</span></span>
