---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710514"
---
# <span data-ttu-id="a0c01-101">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0c01-101">Register-AzAutomationDscNode</span></span>

## <span data-ttu-id="a0c01-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0c01-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c01-103">Rejestruje maszynę wirtualną platformy Azure jako węzeł DSC dla konta usługi Automation.</span><span class="sxs-lookup"><span data-stu-id="a0c01-103">Registers an Azure virtual machine as a DSC node for an Automation account.</span></span>

## <span data-ttu-id="a0c01-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0c01-104">SYNTAX</span></span>

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0c01-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a0c01-105">DESCRIPTION</span></span>
<span data-ttu-id="a0c01-106">Polecenie cmdlet **register-AzAutomationDscNode** rejestruje maszynę wirtualną platformy Azure jako węzeł programu APS (Konfiguracja stanu żądanego) na koncie usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a0c01-106">The **Register-AzAutomationDscNode** cmdlet registers an Azure virtual machine as an APS Desired State Configuration (DSC) node in an Azure Automation account.</span></span>

## <span data-ttu-id="a0c01-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0c01-107">EXAMPLES</span></span>

### <span data-ttu-id="a0c01-108">Przykład 1: rejestrowanie maszyny wirtualnej platformy Azure jako węzła usługi Azure DSC</span><span class="sxs-lookup"><span data-stu-id="a0c01-108">Example 1: Register an Azure virtual machine as an Azure DSC node</span></span>
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="a0c01-109">To polecenie rejestruje maszynę wirtualną platformy Azure o nazwie VirtualMachine01 jako węzeł DSC na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a0c01-109">This command registers the Azure virtual machine named VirtualMachine01 as a DSC node in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a0c01-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0c01-110">PARAMETERS</span></span>

### <span data-ttu-id="a0c01-111">-ActionAfterReboot</span><span class="sxs-lookup"><span data-stu-id="a0c01-111">-ActionAfterReboot</span></span>
<span data-ttu-id="a0c01-112">Określa akcję wykonywaną po ponownym uruchomieniu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a0c01-112">Specifies the action that the virtual machine takes after it restarts.</span></span>
<span data-ttu-id="a0c01-113">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a0c01-113">Valid values are:</span></span> 
- <span data-ttu-id="a0c01-114">ContinueConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c01-114">ContinueConfiguration</span></span> 
- <span data-ttu-id="a0c01-115">StopConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0c01-115">StopConfiguration</span></span>

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

### <span data-ttu-id="a0c01-116">-AllowModuleOverwrite</span><span class="sxs-lookup"><span data-stu-id="a0c01-116">-AllowModuleOverwrite</span></span>
<span data-ttu-id="a0c01-117">Określa, czy nowe konfiguracje, które mają zostać pobrane z tego węzła DSC z serwera ściągania usługi Azure Automation DSC, zastępują istniejące moduły już dostępne w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="a0c01-117">Specifies whether new configurations that this DSC node downloads from the Azure Automation DSC pull server replace the existing modules already on the target node.</span></span>

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

### <span data-ttu-id="a0c01-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a0c01-118">-AutomationAccountName</span></span>
<span data-ttu-id="a0c01-119">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet rejestruje maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="a0c01-119">Specifies the name of an Automation account in which this cmdlet registers a virtual machine.</span></span>

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

### <span data-ttu-id="a0c01-120">-AzureVMLocation</span><span class="sxs-lookup"><span data-stu-id="a0c01-120">-AzureVMLocation</span></span>
<span data-ttu-id="a0c01-121">Lokalizacja maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c01-121">The Azure VM location.</span></span>

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

### <span data-ttu-id="a0c01-122">-AzureVMName</span><span class="sxs-lookup"><span data-stu-id="a0c01-122">-AzureVMName</span></span>
<span data-ttu-id="a0c01-123">Nazwa maszyny wirtualnej platformy Azure do zarejestrowania się do zarządzania z usługą Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="a0c01-123">The name of the Azure virtual machine to register for management with Azure Automation DSC.</span></span>

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

### <span data-ttu-id="a0c01-124">-AzureVMResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0c01-124">-AzureVMResourceGroup</span></span>
<span data-ttu-id="a0c01-125">Nazwa grupy zasobów maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a0c01-125">The Azure VM resource group name.</span></span>

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

### <span data-ttu-id="a0c01-126">-ConfigurationMode</span><span class="sxs-lookup"><span data-stu-id="a0c01-126">-ConfigurationMode</span></span>
<span data-ttu-id="a0c01-127">Określa tryb konfiguracji DSC.</span><span class="sxs-lookup"><span data-stu-id="a0c01-127">Specifies the DSC configuration mode.</span></span>
<span data-ttu-id="a0c01-128">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="a0c01-128">Valid values are:</span></span> 
- <span data-ttu-id="a0c01-129">ApplyAndMonitor</span><span class="sxs-lookup"><span data-stu-id="a0c01-129">ApplyAndMonitor</span></span> 
- <span data-ttu-id="a0c01-130">ApplyAndAutocorrect</span><span class="sxs-lookup"><span data-stu-id="a0c01-130">ApplyAndAutocorrect</span></span> 
- <span data-ttu-id="a0c01-131">ApplyOnly</span><span class="sxs-lookup"><span data-stu-id="a0c01-131">ApplyOnly</span></span>

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

### <span data-ttu-id="a0c01-132">-ConfigurationModeFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="a0c01-132">-ConfigurationModeFrequencyMins</span></span>
<span data-ttu-id="a0c01-133">Określa częstotliwość, w minutach, z jaką aplikacja DSC w tle próbuje zaimplementować bieżącą konfigurację w węźle docelowym.</span><span class="sxs-lookup"><span data-stu-id="a0c01-133">Specifies the frequency, in minutes, at which the background application of DSC attempts to implement the current configuration on the target node.</span></span>

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

### <span data-ttu-id="a0c01-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c01-134">-DefaultProfile</span></span>
<span data-ttu-id="a0c01-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a0c01-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0c01-136">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="a0c01-136">-NodeConfigurationName</span></span>
<span data-ttu-id="a0c01-137">Określa nazwę konfiguracji węzła, którą to polecenie cmdlet skonfiguruje maszynę wirtualną do ściągania z usługi Azure Automation DSC.</span><span class="sxs-lookup"><span data-stu-id="a0c01-137">Specifies the name of the node configuration that this cmdlet configures the virtual machine to pull from Azure Automation DSC.</span></span>

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

### <span data-ttu-id="a0c01-138">-RebootNodeIfNeeded</span><span class="sxs-lookup"><span data-stu-id="a0c01-138">-RebootNodeIfNeeded</span></span>
<span data-ttu-id="a0c01-139">Określa, czy w razie potrzeby należy ponownie uruchomić maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="a0c01-139">Specifies whether to restart the virtual machine, if needed.</span></span>

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

### <span data-ttu-id="a0c01-140">-RefreshFrequencyMins</span><span class="sxs-lookup"><span data-stu-id="a0c01-140">-RefreshFrequencyMins</span></span>
<span data-ttu-id="a0c01-141">Określa częstotliwość, w minutach, z jaką lokalny Menedżer konfiguracji kontaktuje się z serwerem ściągania usługi Azure Automation DSC w celu pobrania najnowszej konfiguracji węzła.</span><span class="sxs-lookup"><span data-stu-id="a0c01-141">Specifies the frequency, in minutes, at which the local Configuration Manager contacts the Azure Automation DSC pull server to download the latest node configuration.</span></span>

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

### <span data-ttu-id="a0c01-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0c01-142">-ResourceGroupName</span></span>
<span data-ttu-id="a0c01-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0c01-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="a0c01-144">Konto usługi Automation, za pomocą którego to polecenie cmdlet rejestruje maszynę wirtualną, należy do grupy zasobów, którą ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="a0c01-144">The Automation account with which this cmdlet registers a virtual machine belongs to the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="a0c01-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c01-145">CommonParameters</span></span>
<span data-ttu-id="a0c01-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0c01-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c01-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c01-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c01-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0c01-148">INPUTS</span></span>

### <span data-ttu-id="a0c01-149">System. String</span><span class="sxs-lookup"><span data-stu-id="a0c01-149">System.String</span></span>

### <span data-ttu-id="a0c01-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="a0c01-150">System.Int32</span></span>

### <span data-ttu-id="a0c01-151">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0c01-151">System.Boolean</span></span>

## <span data-ttu-id="a0c01-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0c01-152">OUTPUTS</span></span>

### <span data-ttu-id="a0c01-153">System. void</span><span class="sxs-lookup"><span data-stu-id="a0c01-153">System.Void</span></span>

## <span data-ttu-id="a0c01-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0c01-154">NOTES</span></span>

## <span data-ttu-id="a0c01-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0c01-155">RELATED LINKS</span></span>

[<span data-ttu-id="a0c01-156">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0c01-156">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="a0c01-157">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0c01-157">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="a0c01-158">Wyrejestrowanie — AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="a0c01-158">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


