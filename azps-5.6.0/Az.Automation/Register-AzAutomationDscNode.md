---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: ceae5a9e7dec9913d90aae836784c6bfe66b680f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010001"
---
# <span data-ttu-id="28723-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="28723-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="28723-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28723-102">SYNOPSIS</span></span>
<span data-ttu-id="28723-103">Rejestruje maszynę wirtualną platformy Azure z systemem operacyjnym Windows jako węzeł dsc dla konta automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="28723-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="28723-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28723-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28723-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="28723-105">DESCRIPTION</span></span>
<span data-ttu-id="28723-106">Polecenie cmdlet **Register-AzAutomationDscNode** rejestruje maszynę wirtualną platformy Azure jako węzeł APS Desired State Configuration (DSC) na koncie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="28723-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="28723-107">To polecenie cmdlet zarejestruje tylko maszyny wirtualne z systemem operacyjnym Windows jako węzeł automatyzacji DSC dla konta.</span><span class="sxs-lookup"><span data-stu-id="28723-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="28723-108">Jeśli chcesz zarejestrować węzeł do konta automatyzacji w innej subskrypcji, musisz użyć szablonu ARM zamiast polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28723-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="28723-109">Aby uzyskać więcej szczegółowych [informacji,](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) zapoznaj się z dokumentacją usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="28723-109">See the Azure Automation [documentation](https://docs.microsoft.com/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="28723-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28723-110">EXAMPLES</span></span>

### <span data-ttu-id="28723-111">Przykład 1. Rejestrowanie maszyny wirtualnej platformy Azure jako węzła usługi Azure DSC</span><span class="sxs-lookup"><span data-stu-id="28723-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="28723-112">To polecenie rejestruje maszynę wirtualną platformy Azure o nazwie VirtualMachine01 jako węzeł DSC w koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="28723-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="28723-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28723-113">PARAMETERS</span></span>

### <span data-ttu-id="28723-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="28723-114">-ActionAfterReboot</span></span>
<span data-ttu-id="28723-115">Określa akcję, która zostanie uruchomiona przez maszynę wirtualną po jej ponownym uruchomieniu.</span><span class="sxs-lookup"><span data-stu-id="28723-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="28723-116">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="28723-116">Valid values are:</span></span> 
- <span data-ttu-id="28723-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="28723-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="28723-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="28723-118">StopConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="28723-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="28723-120">Określa, czy nowe konfiguracje pobierane przez ten węzeł dsc z serwera pobierania dsc automatyzacji Azure zastępują istniejące moduły już w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="28723-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="28723-121">-AutomationAccountName</span></span>
<span data-ttu-id="28723-122">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="28723-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="28723-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="28723-123">-AzureVMLocation</span></span>
<span data-ttu-id="28723-124">Lokalizacja maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28723-124">The Azure VM location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-125">—AzureVMName</span><span class="sxs-lookup"><span data-stu-id="28723-125">-AzureVMName</span></span>
<span data-ttu-id="28723-126">Nazwa maszyny wirtualnej platformy Azure, która ma być zarejestrowana w celu zarządzania w usłudze Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="28723-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="28723-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="28723-128">Nazwa grupy zasobów maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="28723-128">The Azure VM resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-129">- ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="28723-129">-ConfigurationMode</span></span>
<span data-ttu-id="28723-130">Określa tryb konfiguracji dsc.</span><span class="sxs-lookup"><span data-stu-id="28723-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="28723-131">Prawidłowe wartości to:</span><span class="sxs-lookup"><span data-stu-id="28723-131">Valid values are:</span></span> 
- <span data-ttu-id="28723-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="28723-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="28723-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="28723-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="28723-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="28723-134">ApplyOnly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="28723-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="28723-136">Określa częstotliwość (w minutach), z jaką aplikacja dsc w tle próbuje zaimplementować bieżącą konfigurację w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="28723-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28723-137">-DefaultProfile</span></span>
<span data-ttu-id="28723-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="28723-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28723-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="28723-139">-NodeConfigurationName</span></span>
<span data-ttu-id="28723-140">Określa nazwę konfiguracji węzła, która jest konfigurowana przez to polecenie cmdlet w celu skonfigurowania maszyny wirtualnej do ściągania z centrum ds. automatyzacji Azure.</span><span class="sxs-lookup"><span data-stu-id="28723-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="28723-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="28723-142">Określa, czy w razie potrzeby uruchomić ponownie maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="28723-142">Specifies whether to restart the virtual machine, if needed.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="28723-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="28723-144">Określa częstotliwość w minutach, z którą lokalny Menedżer konfiguracji kontaktuje się z serwerem pobierania dsc automatyzacji Azure, aby pobrać najnowszą konfigurację węzła.</span><span class="sxs-lookup"><span data-stu-id="28723-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28723-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28723-145">-ResourceGroupName</span></span>
<span data-ttu-id="28723-146">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="28723-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="28723-147">Konto automatyzacji, za pomocą którego to polecenie cmdlet rejestruje maszynę wirtualną, należy do grupy zasobów, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="28723-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="28723-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28723-148">CommonParameters</span></span>
<span data-ttu-id="28723-149">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28723-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28723-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28723-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28723-151">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28723-151">INPUTS</span></span>

### <span data-ttu-id="28723-152">System.String</span><span class="sxs-lookup"><span data-stu-id="28723-152">System.String</span></span>

### <span data-ttu-id="28723-153">System.Int32</span><span class="sxs-lookup"><span data-stu-id="28723-153">System.Int32</span></span>

### <span data-ttu-id="28723-154">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="28723-154">System.Boolean</span></span>

## <span data-ttu-id="28723-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28723-155">OUTPUTS</span></span>

### <span data-ttu-id="28723-156">System.Void</span><span class="sxs-lookup"><span data-stu-id="28723-156">System.Void</span></span>

## <span data-ttu-id="28723-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28723-157">NOTES</span></span>

## <span data-ttu-id="28723-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28723-158">RELATED LINKS</span></span>

[<span data-ttu-id="28723-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="28723-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="28723-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="28723-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="28723-161">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="28723-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


