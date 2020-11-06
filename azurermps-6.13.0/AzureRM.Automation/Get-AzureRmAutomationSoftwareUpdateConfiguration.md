---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f4d17fa6cdcb64aab2ab373420891f686facfdf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551415"
---
# <span data-ttu-id="2cf9f-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cf9f-101">Get-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2cf9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2cf9f-102">SYNOPSIS</span></span>
<span data-ttu-id="2cf9f-103">Pobiera listę konfiguracji aktualizacji oprogramowania platformy Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-103">Gets a list of azure automation software update configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cf9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2cf9f-104">SYNTAX</span></span>

### <span data-ttu-id="2cf9f-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2cf9f-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf9f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="2cf9f-106">ByName</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cf9f-107">ByVMId</span><span class="sxs-lookup"><span data-stu-id="2cf9f-107">ByVMId</span></span>
```
Get-AzureRmAutomationSoftwareUpdateConfiguration -AzureVMResourceId <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cf9f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2cf9f-108">DESCRIPTION</span></span>
<span data-ttu-id="2cf9f-109">Get-AzureRmAutomationSoftwareUpdateConfiguration zwraca listę konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-109">The Get-AzureRmAutomationSoftwareUpdateConfiguration returns a list of software update configurations.</span></span> <span data-ttu-id="2cf9f-110">Aby uzyskać określoną konfigurację aktualizacji oprogramowania, określ parametr name (nazwa).</span><span class="sxs-lookup"><span data-stu-id="2cf9f-110">To get a specific software update configuration, specify the name parameter.</span></span> <span data-ttu-id="2cf9f-111">Możesz również wyświetlić listę konfiguracji aktualizacji oprogramowania ukierunkowanych na określoną maszynę wirtualną platformy Azure przez określenie identyfikatora zasobu platformy Azure dla tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-111">You can also list software update configurations targeting specific azure virtual machine by specifying the azure resource Id for this virtual machine.</span></span>

## <span data-ttu-id="2cf9f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2cf9f-112">EXAMPLES</span></span>

### <span data-ttu-id="2cf9f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2cf9f-113">Example 1</span></span>
<span data-ttu-id="2cf9f-114">Uzyskaj konfigurację aktualizacji oprogramowania platformy Azure Automation według nazwy.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-114">Get an azure automation software update configuration by name.</span></span>

```powershell
PS C:\> Get-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" -AutomationAccountName "myaccount" -Name "MyWeeklySchedule"

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

## <span data-ttu-id="2cf9f-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2cf9f-115">PARAMETERS</span></span>

### <span data-ttu-id="2cf9f-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2cf9f-116">-AutomationAccountName</span></span>
<span data-ttu-id="2cf9f-117">Nazwa konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-117">The automation account name.</span></span>

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

### <span data-ttu-id="2cf9f-118">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="2cf9f-118">-AzureVMResourceId</span></span>
<span data-ttu-id="2cf9f-119">Identyfikator zasobu platformy Azure maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-119">Azure resource Id of the virtual machine.</span></span>

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

### <span data-ttu-id="2cf9f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cf9f-120">-DefaultProfile</span></span>
<span data-ttu-id="2cf9f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cf9f-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2cf9f-122">-Name</span></span>
<span data-ttu-id="2cf9f-123">Nazwa konfiguracji aktualizacji oprogramowania.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-123">Name of the software update configuration.</span></span>

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

### <span data-ttu-id="2cf9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cf9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="2cf9f-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-125">The resource group name.</span></span>

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

### <span data-ttu-id="2cf9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cf9f-126">CommonParameters</span></span>
<span data-ttu-id="2cf9f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cf9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cf9f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cf9f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cf9f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2cf9f-129">INPUTS</span></span>

### <span data-ttu-id="2cf9f-130">System. String</span><span class="sxs-lookup"><span data-stu-id="2cf9f-130">System.String</span></span>

## <span data-ttu-id="2cf9f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2cf9f-131">OUTPUTS</span></span>

### <span data-ttu-id="2cf9f-132">Microsoft. Azure. Commands. Automation. model. UpdateManagement. SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="2cf9f-132">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="2cf9f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2cf9f-133">NOTES</span></span>

## <span data-ttu-id="2cf9f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2cf9f-134">RELATED LINKS</span></span>
