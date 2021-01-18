---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: af11442edfc5acb2d7e9683bc71d7d2e2c87bd5f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502352"
---
# <span data-ttu-id="96230-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="96230-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="96230-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96230-102">SYNOPSIS</span></span>
<span data-ttu-id="96230-103">Pobiera listę konfiguracji aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="96230-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="96230-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96230-104">SYNTAX</span></span>

### <span data-ttu-id="96230-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="96230-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96230-106">ByName</span><span class="sxs-lookup"><span data-stu-id="96230-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="96230-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="96230-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96230-108">Opis</span><span class="sxs-lookup"><span data-stu-id="96230-108">DESCRIPTION</span></span>
<span data-ttu-id="96230-109">Get-AzAutomationSoftwareUpdateConfiguration zwraca listę konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="96230-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="96230-110">Aby uzyskać określoną konfigurację aktualizacji oprogramowania, określ parametr name (nazwa).</span><span class="sxs-lookup"><span data-stu-id="96230-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="96230-111">Możesz również wyświetlić listę konfiguracji aktualizacji oprogramowania ukierunkowanych na określoną maszynę wirtualną platformy Azure przez określenie identyfikatora zasobu platformy Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96230-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="96230-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96230-112">EXAMPLES</span></span>

### <span data-ttu-id="96230-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="96230-113">Example 1</span></span>
<span data-ttu-id="96230-114">Uzyskaj konfigurację aktualizacji oprogramowania platformy Azure Automation według nazwy.</span><span class="sxs-lookup"><span data-stu-id="96230-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Succeeded
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:37 AM +00:00
Description           :
```

## <span data-ttu-id="96230-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96230-115">PARAMETERS</span></span>

### <span data-ttu-id="96230-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="96230-116">-AutomationAccountName</span></span>
<span data-ttu-id="96230-117">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="96230-117">The automation account name.</span></span>

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

### <span data-ttu-id="96230-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="96230-118">-AzureVMResourceId</span></span>
<span data-ttu-id="96230-119">Identyfikator zasobu platformy Azure maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96230-119">Azure resource Id of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVMId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96230-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96230-120">-DefaultProfile</span></span>
<span data-ttu-id="96230-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="96230-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96230-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="96230-122">-Name</span></span>
<span data-ttu-id="96230-123">Nazwa konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="96230-123">Name of the software update configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96230-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96230-124">-ResourceGroupName</span></span>
<span data-ttu-id="96230-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="96230-125">The resource group name.</span></span>

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

### <span data-ttu-id="96230-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96230-126">CommonParameters</span></span>
<span data-ttu-id="96230-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96230-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96230-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96230-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96230-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96230-129">INPUTS</span></span>

### <span data-ttu-id="96230-130">System. String</span><span class="sxs-lookup"><span data-stu-id="96230-130">System.String</span></span>

## <span data-ttu-id="96230-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96230-131">OUTPUTS</span></span>

### <span data-ttu-id="96230-132">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="96230-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="96230-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96230-133">NOTES</span></span>

## <span data-ttu-id="96230-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96230-134">RELATED LINKS</span></span>
