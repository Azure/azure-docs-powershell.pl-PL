---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/register-azurermautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Register-AzureRmAutomationDscNode.md
ms.openlocfilehash: 567ac6012465508fbaf03d603a79d2abb04ed6c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547636"
---
# <span data-ttu-id="25753-101">Register-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="25753-101">Register-AzureRmAutomationDscNode</span></span>

## <span data-ttu-id="25753-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25753-102">SYNOPSIS</span></span>
<span data-ttu-id="25753-103">Rejestruje maszynę wirtualną platformy Azure jako węzeł DSC dla konta usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="25753-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="25753-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25753-104">SYNTAX</span></span>

```
Register-AzureRmAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25753-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25753-105">DESCRIPTION</span></span>
<span data-ttu-id="25753-106">Polecenie cmdlet **register-AzureRmAutomationDscNode** rejestruje maszynę wirtualną platformy Azure jako węzeł programu APS (Konfiguracja stanu żądanego) na koncie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="25753-106">The **Register-AzureRmAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="25753-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25753-107">EXAMPLES</span></span>

### <span data-ttu-id="25753-108">Przykład 1: rejestrowanie maszyny wirtualnej platformy Azure jako węzła usługi Azure DSC</span><span class="sxs-lookup"><span data-stu-id="25753-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzureRmAutomationDscNode -AutomationAccountName "Contoso17" -AzureVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="25753-109">To polecenie rejestruje maszynę wirtualną platformy Azure o nazwie VirtualMachine01 jako węzeł DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="25753-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="25753-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25753-110">PARAMETERS</span></span>

### <span data-ttu-id="25753-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="25753-111">-ActionAfterReboot</span></span>
<span data-ttu-id="25753-112">Określa akcję wykonywaną po ponownym uruchomieniu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="25753-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="25753-113">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="25753-113">Valid values are:</span></span> 
- <span data-ttu-id="25753-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="25753-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="25753-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="25753-115">StopConfiguration</span></span>

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

### <span data-ttu-id="25753-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="25753-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="25753-117">Określa, czy nowe konfiguracje, które mają zostać pobrane z tego węzła DSC z serwera ściągania usługi Azure Automation DSC, zastępują istniejące moduły już dostępne w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="25753-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="25753-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="25753-118">-AutomationAccountName</span></span>
<span data-ttu-id="25753-119">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="25753-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="25753-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="25753-120">-AzureVMLocation</span></span>
<span data-ttu-id="25753-121">Określa lokalizację, w której to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="25753-121">Specifies the location in which this cmdlet registers a virtual machine.</span></span>
<span data-ttu-id="25753-122">Aby uzyskać prawidłowe lokalizacje, użyj polecenia cmdlet Get-AzureRMLocation.</span><span class="sxs-lookup"><span data-stu-id="25753-122">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="25753-123">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="25753-123">-AzureVMName</span></span>
<span data-ttu-id="25753-124">Określa nazwę maszyny wirtualnej platformy Azure, którą to polecenie cmdlet rejestruje w celu zarządzania.</span><span class="sxs-lookup"><span data-stu-id="25753-124">Specifies the name of the Azure virtual machine that this cmdlet registers for management.</span></span>

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

### <span data-ttu-id="25753-125">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="25753-125">-AzureVMResourceGroup</span></span>
<span data-ttu-id="25753-126">Określa nazwę grupy zasobów maszyny wirtualnej platformy Azure, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="25753-126">Specifies the name of the resource group of the Azure virtual machine that this cmdlet registers.</span></span>

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

### <span data-ttu-id="25753-127">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="25753-127">-ConfigurationMode</span></span>
<span data-ttu-id="25753-128">Określa tryb konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="25753-128">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="25753-129">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="25753-129">Valid values are:</span></span> 
- <span data-ttu-id="25753-130">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="25753-130">ApplyAndMonitor</span></span> 
- <span data-ttu-id="25753-131">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="25753-131">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="25753-132">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="25753-132">ApplyOnly</span></span>

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

### <span data-ttu-id="25753-133">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="25753-133">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="25753-134">Określa częstotliwość, w minutach, z jaką aplikacja DSC w tle próbuje zaimplementować bieżącą konfigurację w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="25753-134">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="25753-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25753-135">-DefaultProfile</span></span>
<span data-ttu-id="25753-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25753-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25753-137">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="25753-137">-NodeConfigurationName</span></span>
<span data-ttu-id="25753-138">Określa nazwę konfiguracji węzła, którą to polecenie cmdlet skonfiguruje maszynę wirtualną do ściągania z usługi Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="25753-138">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="25753-139">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="25753-139">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="25753-140">Określa, czy w razie potrzeby należy ponownie uruchomić maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="25753-140">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="25753-141">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="25753-141">-RefreshFrequencyMins</span></span>
<span data-ttu-id="25753-142">Określa częstotliwość, w minutach, z jaką lokalny Menedżer konfiguracji kontaktuje się z serwerem ściągania usługi Azure Automation DSC w celu pobrania najnowszej konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="25753-142">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="25753-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25753-143">-ResourceGroupName</span></span>
<span data-ttu-id="25753-144">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25753-144">Specifies the name of a resource group.</span></span>
<span data-ttu-id="25753-145">Konto usługi Automation, za pomocą którego to polecenie cmdlet rejestruje maszynę wirtualną, należy do grupy zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="25753-145">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="25753-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25753-146">CommonParameters</span></span>
<span data-ttu-id="25753-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25753-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25753-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25753-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25753-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25753-149">INPUTS</span></span>

### <span data-ttu-id="25753-150">System. String</span><span class="sxs-lookup"><span data-stu-id="25753-150">System.String</span></span>

### <span data-ttu-id="25753-151">System. Int32</span><span class="sxs-lookup"><span data-stu-id="25753-151">System.Int32</span></span>

### <span data-ttu-id="25753-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="25753-152">System.Boolean</span></span>

## <span data-ttu-id="25753-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25753-153">OUTPUTS</span></span>

### <span data-ttu-id="25753-154">System. void</span><span class="sxs-lookup"><span data-stu-id="25753-154">System.Void</span></span>

## <span data-ttu-id="25753-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25753-155">NOTES</span></span>

## <span data-ttu-id="25753-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25753-156">RELATED LINKS</span></span>

[<span data-ttu-id="25753-157">Get-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="25753-157">Get-AzureRmAutomationDscNode</span></span>](./Get-AzureRmAutomationDscNode.md)

[<span data-ttu-id="25753-158">Set-AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="25753-158">Set-AzureRmAutomationDscNode</span></span>](./Set-AzureRmAutomationDscNode.md)

[<span data-ttu-id="25753-159">Wyrejestrowanie — AzureRmAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="25753-159">Unregister-AzureRmAutomationDscNode</span></span>](./Unregister-AzureRmAutomationDscNode.md)

