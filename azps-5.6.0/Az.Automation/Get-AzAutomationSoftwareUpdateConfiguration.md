---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 99f2c14cbc3c3f652df062bb3bf806e89ca05f06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014193"
---
# <span data-ttu-id="f7e43-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7e43-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f7e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7e43-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e43-103">Pobiera listę konfiguracji aktualizacji oprogramowania azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f7e43-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="f7e43-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f7e43-104">SYNTAX</span></span>

### <span data-ttu-id="f7e43-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="f7e43-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7e43-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f7e43-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7e43-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="f7e43-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7e43-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f7e43-108">DESCRIPTION</span></span>
<span data-ttu-id="f7e43-109">Funkcja Get-AzAutomationSoftwareUpdateConfiguration zwraca listę konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="f7e43-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="f7e43-110">Aby uzyskać określoną konfigurację aktualizacji oprogramowania, określ parametr nazwy.</span><span class="sxs-lookup"><span data-stu-id="f7e43-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="f7e43-111">Możesz również wyświetlić konfiguracje aktualizacji oprogramowania kierowane do określonej maszyny wirtualnej platformy Azure, określając identyfikator zasobu Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7e43-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="f7e43-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f7e43-112">EXAMPLES</span></span>

### <span data-ttu-id="f7e43-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7e43-113">Example 1</span></span>
<span data-ttu-id="f7e43-114">Uzyskaj konfigurację aktualizacji oprogramowania Azure Automation według nazwy.</span><span class="sxs-lookup"><span data-stu-id="f7e43-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="f7e43-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7e43-115">PARAMETERS</span></span>

### <span data-ttu-id="f7e43-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f7e43-116">-AutomationAccountName</span></span>
<span data-ttu-id="f7e43-117">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f7e43-117">The automation account name.</span></span>

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

### <span data-ttu-id="f7e43-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="f7e43-118">-AzureVMResourceId</span></span>
<span data-ttu-id="f7e43-119">Identyfikator zasobu Azure maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f7e43-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="f7e43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e43-120">-DefaultProfile</span></span>
<span data-ttu-id="f7e43-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f7e43-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7e43-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f7e43-122">-Name</span></span>
<span data-ttu-id="f7e43-123">Nazwa konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="f7e43-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="f7e43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e43-124">-ResourceGroupName</span></span>
<span data-ttu-id="f7e43-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7e43-125">The resource group name.</span></span>

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

### <span data-ttu-id="f7e43-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e43-126">CommonParameters</span></span>
<span data-ttu-id="f7e43-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7e43-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e43-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7e43-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e43-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7e43-129">INPUTS</span></span>

### <span data-ttu-id="f7e43-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f7e43-130">System.String</span></span>

## <span data-ttu-id="f7e43-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7e43-131">OUTPUTS</span></span>

### <span data-ttu-id="f7e43-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="f7e43-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="f7e43-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f7e43-133">NOTES</span></span>

## <span data-ttu-id="f7e43-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7e43-134">RELATED LINKS</span></span>
