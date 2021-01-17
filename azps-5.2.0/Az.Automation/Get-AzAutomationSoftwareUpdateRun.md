---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373709"
---
# <span data-ttu-id="bca39-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bca39-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="bca39-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bca39-102">SYNOPSIS</span></span>
<span data-ttu-id="bca39-103">Pobiera listę uruchomionych aktualizacji oprogramowania Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="bca39-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="bca39-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bca39-104">SYNTAX</span></span>

### <span data-ttu-id="bca39-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bca39-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca39-106">ById</span><span class="sxs-lookup"><span data-stu-id="bca39-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bca39-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="bca39-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bca39-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="bca39-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bca39-109">Opis</span><span class="sxs-lookup"><span data-stu-id="bca39-109">DESCRIPTION</span></span>
<span data-ttu-id="bca39-110">Polecenie cmdlet Get-AzAutomationSoftwareUpdateRun zwraca listę uruchomionych aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="bca39-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="bca39-111">Ponieważ konfiguracja aktualizacji oprogramowania ma skojarzony harmonogram, można ją wyzwolić wiele razy.</span><span class="sxs-lookup"><span data-stu-id="bca39-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="bca39-112">Za każdym razem, gdy zostanie wyzwolony harmonogram, zostanie utworzony stan uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="bca39-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="bca39-113">Przebieg aktualizacji to zagregowany wynik wszystkich uruchomień komputera.</span><span class="sxs-lookup"><span data-stu-id="bca39-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="bca39-114">Aby uzyskać dostęp do określonej konfiguracji aktualizacji oprogramowania, możesz przekazać parametr SoftwareUpdateConfigurationName.</span><span class="sxs-lookup"><span data-stu-id="bca39-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="bca39-115">Aby uzyskać określone działania, należy przekazać parametr name.</span><span class="sxs-lookup"><span data-stu-id="bca39-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="bca39-116">Możesz również wyświetlić informacje o określonym stanie, uruchomić określony system operacyjny lub uruchomić po określonym czasie, przechodząc do odpowiedniego parametru.</span><span class="sxs-lookup"><span data-stu-id="bca39-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="bca39-117">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bca39-117">EXAMPLES</span></span>

### <span data-ttu-id="bca39-118">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bca39-118">Example 1</span></span>
<span data-ttu-id="bca39-119">W tym przykładzie przedstawiono wszystkie przebiegi aktualizacji wyzwalane przez określoną konfigurację aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="bca39-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="bca39-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bca39-120">PARAMETERS</span></span>

### <span data-ttu-id="bca39-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="bca39-121">-AutomationAccountName</span></span>
<span data-ttu-id="bca39-122">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="bca39-122">The automation account name.</span></span>

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

### <span data-ttu-id="bca39-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca39-123">-DefaultProfile</span></span>
<span data-ttu-id="bca39-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bca39-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca39-125">-ID</span><span class="sxs-lookup"><span data-stu-id="bca39-125">-Id</span></span>
<span data-ttu-id="bca39-126">Identyfikator procesu konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="bca39-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="bca39-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="bca39-127">-OperatingSystem</span></span>
<span data-ttu-id="bca39-128">System operacyjny uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="bca39-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca39-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca39-129">-ResourceGroupName</span></span>
<span data-ttu-id="bca39-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bca39-130">The resource group name.</span></span>

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

### <span data-ttu-id="bca39-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bca39-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="bca39-132">Konfiguracja aktualizacji oprogramowania wyzwoliła uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="bca39-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca39-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="bca39-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="bca39-134">Nazwa konfiguracji aktualizacji oprogramowania wyzwoliła uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="bca39-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca39-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="bca39-135">-StartTime</span></span>
<span data-ttu-id="bca39-136">Minimalna godzina rozpoczęcia biegu.</span><span class="sxs-lookup"><span data-stu-id="bca39-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca39-137">-Status</span><span class="sxs-lookup"><span data-stu-id="bca39-137">-Status</span></span>
<span data-ttu-id="bca39-138">Stan uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="bca39-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bca39-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca39-139">CommonParameters</span></span>
<span data-ttu-id="bca39-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bca39-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca39-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bca39-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca39-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bca39-142">INPUTS</span></span>

### <span data-ttu-id="bca39-143">System. GUID</span><span class="sxs-lookup"><span data-stu-id="bca39-143">System.Guid</span></span>

### <span data-ttu-id="bca39-144">System. String</span><span class="sxs-lookup"><span data-stu-id="bca39-144">System.String</span></span>

### <span data-ttu-id="bca39-145">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="bca39-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="bca39-146">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. model. UpdateManagement. OperatingSystemType, Microsoft. Azure. PowerShell. polecenia cmdlet. Automatyzacja, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bca39-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bca39-147">System. Nullable "1 [[Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateRunStatus, Microsoft. Azure. PowerShell. polecenia cmdlet. Automatyzacja, Version = 1.0.0.0, Culture = neutral; PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="bca39-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="bca39-148">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="bca39-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="bca39-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bca39-149">OUTPUTS</span></span>

### <span data-ttu-id="bca39-150">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bca39-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="bca39-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bca39-151">NOTES</span></span>

## <span data-ttu-id="bca39-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bca39-152">RELATED LINKS</span></span>
