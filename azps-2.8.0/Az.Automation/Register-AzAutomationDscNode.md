---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5aec50c6203697ed21f8d475068752b35616eb52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706746"
---
# <span data-ttu-id="1e1fd-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1e1fd-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="1e1fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1e1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e1fd-103">Rejestruje maszynę wirtualną platformy Azure z uruchomionym systemem operacyjnym Windows jako węzeł DSC dla konta usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-103">Registers an Azure virtual machine running Windows OS as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="1e1fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1e1fd-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e1fd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1e1fd-105">DESCRIPTION</span></span>
<span data-ttu-id="1e1fd-106">Polecenie cmdlet **register-AzAutomationDscNode** rejestruje maszynę wirtualną platformy Azure jako węzeł programu APS (Konfiguracja stanu żądanego) na koncie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span> <span data-ttu-id="1e1fd-107">To polecenie cmdlet rejestruje tylko maszyny wirtualne z systemem operacyjnym Windows jako węzeł usługi Automation DSC dla konta.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-107">This cmdlet will only register VMs running Windows OS as an Automation DSC Node for an account.</span></span>

<span data-ttu-id="1e1fd-108">Jeśli konieczne jest zarejestrowanie węzła na koncie usługi Automation w innej subskrypcji, należy użyć szablonu ARM, a nie poleceń cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-108">If you need to register a node to an automation account in a different subscription, you will need to use an ARM template rather than cmdlets.</span></span> <span data-ttu-id="1e1fd-109">Aby uzyskać więcej informacji, zobacz [dokumentację](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-109">See the Azure Automation [documentation](https://docs.microsoft.com/en-us/azure/automation/automation-dsc-onboarding#registering-virtual-machines-across-azure-subscriptions) for more details.</span></span>

## <span data-ttu-id="1e1fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1e1fd-110">EXAMPLES</span></span>

### <span data-ttu-id="1e1fd-111">Przykład 1: rejestrowanie maszyny wirtualnej platformy Azure jako węzła usługi Azure DSC</span><span class="sxs-lookup"><span data-stu-id="1e1fd-111">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="1e1fd-112">To polecenie rejestruje maszynę wirtualną platformy Azure o nazwie VirtualMachine01 jako węzeł DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-112">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1e1fd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1e1fd-113">PARAMETERS</span></span>

### <span data-ttu-id="1e1fd-114">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="1e1fd-114">-ActionAfterReboot</span></span>
<span data-ttu-id="1e1fd-115">Określa akcję wykonywaną po ponownym uruchomieniu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-115">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="1e1fd-116">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-116">Valid values are:</span></span> 
- <span data-ttu-id="1e1fd-117">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e1fd-117">ContinueConfiguration</span></span> 
- <span data-ttu-id="1e1fd-118">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="1e1fd-118">StopConfiguration</span></span>

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

### <span data-ttu-id="1e1fd-119">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="1e1fd-119">-AllowModuleOverwrite</span></span>
<span data-ttu-id="1e1fd-120">Określa, czy nowe konfiguracje, które mają zostać pobrane z tego węzła DSC z serwera ściągania usługi Azure Automation DSC, zastępują istniejące moduły już dostępne w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-120">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="1e1fd-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1e1fd-121">-AutomationAccountName</span></span>
<span data-ttu-id="1e1fd-122">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-122">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="1e1fd-123">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="1e1fd-123">-AzureVMLocation</span></span>
<span data-ttu-id="1e1fd-124">Lokalizacja maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-124">The Azure VM location.</span></span>

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

### <span data-ttu-id="1e1fd-125">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="1e1fd-125">-AzureVMName</span></span>
<span data-ttu-id="1e1fd-126">Nazwa maszyny wirtualnej platformy Azure do zarejestrowania się do zarządzania z usługą Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-126">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="1e1fd-127">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1e1fd-127">-AzureVMResourceGroup</span></span>
<span data-ttu-id="1e1fd-128">Nazwa grupy zasobów maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-128">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="1e1fd-129">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="1e1fd-129">-ConfigurationMode</span></span>
<span data-ttu-id="1e1fd-130">Określa tryb konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-130">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="1e1fd-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="1e1fd-131">Valid values are:</span></span> 
- <span data-ttu-id="1e1fd-132">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="1e1fd-132">ApplyAndMonitor</span></span> 
- <span data-ttu-id="1e1fd-133">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="1e1fd-133">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="1e1fd-134">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="1e1fd-134">ApplyOnly</span></span>

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

### <span data-ttu-id="1e1fd-135">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="1e1fd-135">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="1e1fd-136">Określa częstotliwość, w minutach, z jaką aplikacja DSC w tle próbuje zaimplementować bieżącą konfigurację w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-136">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="1e1fd-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e1fd-137">-DefaultProfile</span></span>
<span data-ttu-id="1e1fd-138">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="1e1fd-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e1fd-139">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1e1fd-139">-NodeConfigurationName</span></span>
<span data-ttu-id="1e1fd-140">Określa nazwę konfiguracji węzła, którą to polecenie cmdlet skonfiguruje maszynę wirtualną do ściągania z usługi Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-140">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="1e1fd-141">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="1e1fd-141">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="1e1fd-142">Określa, czy w razie potrzeby należy ponownie uruchomić maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-142">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="1e1fd-143">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="1e1fd-143">-RefreshFrequencyMins</span></span>
<span data-ttu-id="1e1fd-144">Określa częstotliwość, w minutach, z jaką lokalny Menedżer konfiguracji kontaktuje się z serwerem ściągania usługi Azure Automation DSC w celu pobrania najnowszej konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-144">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="1e1fd-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e1fd-145">-ResourceGroupName</span></span>
<span data-ttu-id="1e1fd-146">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-146">Specifies the name of a resource group.</span></span>
<span data-ttu-id="1e1fd-147">Konto usługi Automation, za pomocą którego to polecenie cmdlet rejestruje maszynę wirtualną, należy do grupy zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-147">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="1e1fd-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e1fd-148">CommonParameters</span></span>
<span data-ttu-id="1e1fd-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e1fd-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e1fd-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e1fd-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e1fd-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e1fd-151">INPUTS</span></span>

### <span data-ttu-id="1e1fd-152">System. String</span><span class="sxs-lookup"><span data-stu-id="1e1fd-152">System.String</span></span>

### <span data-ttu-id="1e1fd-153">System. Int32</span><span class="sxs-lookup"><span data-stu-id="1e1fd-153">System.Int32</span></span>

### <span data-ttu-id="1e1fd-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1e1fd-154">System.Boolean</span></span>

## <span data-ttu-id="1e1fd-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1e1fd-155">OUTPUTS</span></span>

### <span data-ttu-id="1e1fd-156">System. void</span><span class="sxs-lookup"><span data-stu-id="1e1fd-156">System.Void</span></span>

## <span data-ttu-id="1e1fd-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1e1fd-157">NOTES</span></span>

## <span data-ttu-id="1e1fd-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e1fd-158">RELATED LINKS</span></span>

[<span data-ttu-id="1e1fd-159">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1e1fd-159">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="1e1fd-160">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1e1fd-160">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="1e1fd-161">Wyrejestrowanie — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="1e1fd-161">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


