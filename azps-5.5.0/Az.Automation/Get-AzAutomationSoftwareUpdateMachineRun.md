---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199626"
---
# <span data-ttu-id="a6ad5-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="a6ad5-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="a6ad5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6ad5-102">SYNOPSIS</span></span>
<span data-ttu-id="a6ad5-103">Pobiera listę uruchomionych maszyn do konfiguracji oprogramowania azure Automation Software Update.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="a6ad5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6ad5-104">SYNTAX</span></span>

### <span data-ttu-id="a6ad5-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a6ad5-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a6ad5-106">ById</span><span class="sxs-lookup"><span data-stu-id="a6ad5-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6ad5-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="a6ad5-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a6ad5-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="a6ad5-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a6ad5-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6ad5-109">DESCRIPTION</span></span>
<span data-ttu-id="a6ad5-110">To polecenie cmdlet zwraca listę uruchamianych na komputerze.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="a6ad5-111">Każde uruchomienie aktualizacji oprogramowania spowoduje uruchomienie komputera dla każdego komputera docelowego konfiguracji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="a6ad5-112">Aby uruchomić określony komputer, przekaż parametr Id.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="a6ad5-113">Możesz wyświetlić listę wszystkich urządzeń uruchamianych, wszystkie uruchamiane dla określonego komputera, wszystkie z określonym stanem przez podanie odpowiednich parametrów.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="a6ad5-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6ad5-114">EXAMPLES</span></span>

### <span data-ttu-id="a6ad5-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a6ad5-115">Example 1</span></span>
<span data-ttu-id="a6ad5-116">W tym przykładzie zwraca wszystkie nieudane maszyny uruchamiane dla określonej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
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

## <span data-ttu-id="a6ad5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6ad5-117">PARAMETERS</span></span>

### <span data-ttu-id="a6ad5-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6ad5-118">-AutomationAccountName</span></span>
<span data-ttu-id="a6ad5-119">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-119">The automation account name.</span></span>

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

### <span data-ttu-id="a6ad5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6ad5-120">-DefaultProfile</span></span>
<span data-ttu-id="a6ad5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6ad5-122">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="a6ad5-122">-Id</span></span>
<span data-ttu-id="a6ad5-123">Identyfikator uruchomienia komputera do aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="a6ad5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6ad5-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6ad5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-125">The resource group name.</span></span>

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

### <span data-ttu-id="a6ad5-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="a6ad5-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="a6ad5-127">Zostanie uruchomione aktualizowanie oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-127">The software update run.</span></span>

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

### <span data-ttu-id="a6ad5-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="a6ad5-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="a6ad5-129">Identyfikator uruchomienia aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-129">Id of the software update run.</span></span>

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

### <span data-ttu-id="a6ad5-130">— Status</span><span class="sxs-lookup"><span data-stu-id="a6ad5-130">-Status</span></span>
<span data-ttu-id="a6ad5-131">Stan uruchomienia komputera.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-131">Status of the machine run.</span></span>

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

### <span data-ttu-id="a6ad5-132">- TargetComputer</span><span class="sxs-lookup"><span data-stu-id="a6ad5-132">-TargetComputer</span></span>
<span data-ttu-id="a6ad5-133">komputera docelowego dla uruchomionego komputera.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-133">target computer for the machine run.</span></span>
<span data-ttu-id="a6ad5-134">Może być nazwą komputera innego niż az lub identyfikatorem zasobu azure MASZYNY WIRTUALNEj.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

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

### <span data-ttu-id="a6ad5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6ad5-135">CommonParameters</span></span>
<span data-ttu-id="a6ad5-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6ad5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6ad5-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6ad5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6ad5-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6ad5-138">INPUTS</span></span>

### <span data-ttu-id="a6ad5-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="a6ad5-139">System.Guid</span></span>

### <span data-ttu-id="a6ad5-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="a6ad5-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="a6ad5-141">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlet.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="a6ad5-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="a6ad5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a6ad5-142">System.String</span></span>

## <span data-ttu-id="a6ad5-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6ad5-143">OUTPUTS</span></span>

### <span data-ttu-id="a6ad5-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="a6ad5-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="a6ad5-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6ad5-145">NOTES</span></span>

## <span data-ttu-id="a6ad5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6ad5-146">RELATED LINKS</span></span>
