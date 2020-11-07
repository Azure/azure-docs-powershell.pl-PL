---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: 549818e8dfe04730ef8387779d38921fa965e8b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710563"
---
# <span data-ttu-id="3a1c5-101">Get-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a1c5-101">Get-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3a1c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a1c5-102">SYNOPSIS</span></span>
<span data-ttu-id="3a1c5-103">Pobiera listę konfiguracji aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-103">Gets a list of azure automation software update configurations.</span></span>

## <span data-ttu-id="3a1c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a1c5-104">SYNTAX</span></span>

### <span data-ttu-id="3a1c5-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a1c5-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1c5-106">ByName</span><span class="sxs-lookup"><span data-stu-id="3a1c5-106">ByName</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3a1c5-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="3a1c5-107">ByVMId</span></span>
```
Get-AzAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a1c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3a1c5-108">DESCRIPTION</span></span>
<span data-ttu-id="3a1c5-109">Get-AzAutomationSoftwareUpdateConfiguration zwraca listę konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-109">The Get-AzAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="3a1c5-110">Aby uzyskać określoną konfigurację aktualizacji oprogramowania, określ parametr name (nazwa).</span><span class="sxs-lookup"><span data-stu-id="3a1c5-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="3a1c5-111">Możesz również wyświetlić listę konfiguracji aktualizacji oprogramowania ukierunkowanych na określoną maszynę wirtualną platformy Azure przez określenie identyfikatora zasobu platformy Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="3a1c5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a1c5-112">EXAMPLES</span></span>

### <span data-ttu-id="3a1c5-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a1c5-113">Example 1</span></span>
<span data-ttu-id="3a1c5-114">Uzyskaj konfigurację aktualizacji oprogramowania platformy Azure Automation według nazwy.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-114">Get an azure automation software update configuration by name.</span></span>

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

## <span data-ttu-id="3a1c5-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a1c5-115">PARAMETERS</span></span>

### <span data-ttu-id="3a1c5-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="3a1c5-116">-AutomationAccountName</span></span>
<span data-ttu-id="3a1c5-117">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-117">The automation account name.</span></span>

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

### <span data-ttu-id="3a1c5-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="3a1c5-118">-AzureVMResourceId</span></span>
<span data-ttu-id="3a1c5-119">Identyfikator zasobu platformy Azure maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="3a1c5-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a1c5-120">-DefaultProfile</span></span>
<span data-ttu-id="3a1c5-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a1c5-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a1c5-122">-Name</span></span>
<span data-ttu-id="3a1c5-123">Nazwa konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="3a1c5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a1c5-124">-ResourceGroupName</span></span>
<span data-ttu-id="3a1c5-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-125">The resource group name.</span></span>

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

### <span data-ttu-id="3a1c5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a1c5-126">CommonParameters</span></span>
<span data-ttu-id="3a1c5-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a1c5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a1c5-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a1c5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a1c5-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a1c5-129">INPUTS</span></span>

### <span data-ttu-id="3a1c5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="3a1c5-130">System.String</span></span>

## <span data-ttu-id="3a1c5-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a1c5-131">OUTPUTS</span></span>

### <span data-ttu-id="3a1c5-132">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="3a1c5-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="3a1c5-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a1c5-133">NOTES</span></span>

## <span data-ttu-id="3a1c5-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a1c5-134">RELATED LINKS</span></span>