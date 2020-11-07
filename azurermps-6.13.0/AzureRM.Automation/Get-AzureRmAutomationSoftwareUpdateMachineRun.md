---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: f583ccfbfd0ef7178500d74f120f3907d083b8ef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717960"
---
# <span data-ttu-id="f0ea9-101">Get-AzureRmAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="f0ea9-101">Get-AzureRmAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="f0ea9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0ea9-102">SYNOPSIS</span></span>
<span data-ttu-id="f0ea9-103">Pobiera listę uruchamiania komputera konfiguracji aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-103">Gets a list of azure automation software update configuration machine runs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0ea9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0ea9-104">SYNTAX</span></span>

### <span data-ttu-id="f0ea9-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f0ea9-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>]
 [-TargetComputer <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0ea9-106">ById</span><span class="sxs-lookup"><span data-stu-id="f0ea9-106">ById</span></span>
```
Get-AzureRmAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0ea9-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="f0ea9-107">BySucrId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0ea9-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="f0ea9-108">BySucr</span></span>
```
Get-AzureRmAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0ea9-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f0ea9-109">DESCRIPTION</span></span>
<span data-ttu-id="f0ea9-110">To polecenie cmdlet zwraca listę uruchomień komputera.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="f0ea9-111">Każde uruchomienie aktualizacji oprogramowania wyzwoli uruchomienie komputera na każdym komputerze docelowym konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="f0ea9-112">Aby uruchomić określony komputer, należy przejść do parametru ID.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="f0ea9-113">Możesz wyświetlić listę wszystkich uruchomionych komputerów, wszystkie są uruchamiane dla określonego komputera, wszystkie działają z określonym stanem przez przekazanie odpowiednich parametrów.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="f0ea9-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0ea9-114">EXAMPLES</span></span>

### <span data-ttu-id="f0ea9-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f0ea9-115">Example 1</span></span>
<span data-ttu-id="f0ea9-116">W tym przykładzie jest zwracana wartość wszystkich nieudanych uruchomień komputera dla określonej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzureRmAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="f0ea9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0ea9-117">PARAMETERS</span></span>

### <span data-ttu-id="f0ea9-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f0ea9-118">-AutomationAccountName</span></span>
<span data-ttu-id="f0ea9-119">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-119">The automation account name.</span></span>

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

### <span data-ttu-id="f0ea9-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0ea9-120">-DefaultProfile</span></span>
<span data-ttu-id="f0ea9-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0ea9-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f0ea9-122">-Id</span></span>
<span data-ttu-id="f0ea9-123">Identyfikator uruchomienia komputera aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-123">Id of the software update machine run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0ea9-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0ea9-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-125">The resource group name.</span></span>

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

### <span data-ttu-id="f0ea9-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="f0ea9-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="f0ea9-127">Uruchomienie aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea9-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="f0ea9-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="f0ea9-129">Identyfikator procesu aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea9-130">-Status</span><span class="sxs-lookup"><span data-stu-id="f0ea9-130">-Status</span></span>
<span data-ttu-id="f0ea9-131">Stan uruchomienia komputera.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea9-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="f0ea9-132">-TargetComputer</span></span>
<span data-ttu-id="f0ea9-133">komputer docelowy jest uruchomiony na komputerze.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-133">target computer for the machine run.</span></span>
<span data-ttu-id="f0ea9-134">Może być nazwą komputera lub identyfikatorem zasobu maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-134">Can be either a non-azure computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0ea9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0ea9-135">CommonParameters</span></span>
<span data-ttu-id="f0ea9-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0ea9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0ea9-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0ea9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0ea9-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0ea9-138">INPUTS</span></span>

### <span data-ttu-id="f0ea9-139">System. GUID</span><span class="sxs-lookup"><span data-stu-id="f0ea9-139">System.Guid</span></span>

### <span data-ttu-id="f0ea9-140">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="f0ea9-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="f0ea9-141">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateMachineRunStatus, Microsoft. Azure. Commands. ResourceManager. Automation, wersja = 5.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f0ea9-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.Commands.ResourceManager.Automation, Version=5.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="f0ea9-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f0ea9-142">System.String</span></span>

## <span data-ttu-id="f0ea9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0ea9-143">OUTPUTS</span></span>

### <span data-ttu-id="f0ea9-144">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="f0ea9-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="f0ea9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0ea9-145">NOTES</span></span>

## <span data-ttu-id="f0ea9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0ea9-146">RELATED LINKS</span></span>
