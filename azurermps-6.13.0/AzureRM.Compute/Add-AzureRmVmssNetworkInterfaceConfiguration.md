---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 6789b2a0f3309e8011cc6e87a27dbf9f28579d05
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545496"
---
# <span data-ttu-id="f11b3-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f11b3-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="f11b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f11b3-102">SYNOPSIS</span></span>
<span data-ttu-id="f11b3-103">Dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f11b3-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f11b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f11b3-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11b3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f11b3-105">DESCRIPTION</span></span>
<span data-ttu-id="f11b3-106">Polecenie cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** umożliwia dodanie konfiguracji interfejsu sieciowego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f11b3-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="f11b3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f11b3-107">EXAMPLES</span></span>

### <span data-ttu-id="f11b3-108">Przykład 1: Dodawanie konfiguracji interfejsu sieciowego do VMSS</span><span class="sxs-lookup"><span data-stu-id="f11b3-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="f11b3-109">To polecenie dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="f11b3-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="f11b3-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f11b3-110">PARAMETERS</span></span>

### <span data-ttu-id="f11b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11b3-111">-DefaultProfile</span></span>
<span data-ttu-id="f11b3-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f11b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f11b3-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="f11b3-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="f11b3-114">Lista adresów IP serwerów DNS dla ustawień DNS.</span><span class="sxs-lookup"><span data-stu-id="f11b3-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="f11b3-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="f11b3-116">Określa, czy interfejs sieciowy jest włączony do przyspieszania obsługi sieci.</span><span class="sxs-lookup"><span data-stu-id="f11b3-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="f11b3-117">-EnableIPForwarding</span></span>
<span data-ttu-id="f11b3-118">Określa, czy włączono przekierowywanie IP na tej karcie NIC.</span><span class="sxs-lookup"><span data-stu-id="f11b3-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="f11b3-119">-Id</span></span>
<span data-ttu-id="f11b3-120">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f11b3-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-121">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="f11b3-121">-IpConfiguration</span></span>
<span data-ttu-id="f11b3-122">Określa konfiguracje IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f11b3-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f11b3-123">-Name</span></span>
<span data-ttu-id="f11b3-124">Określa nazwę konfiguracji interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f11b3-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="f11b3-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="f11b3-126">Identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="f11b3-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="f11b3-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="f11b3-127">-Primary</span></span>
<span data-ttu-id="f11b3-128">Wskazuje, czy interfejsy sieciowe utworzone na podstawie konfiguracji interfejsu sieciowego będą podstawowym centrum informacyjnym (Network Information Center) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f11b3-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f11b3-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f11b3-130">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="f11b3-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="f11b3-131">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="f11b3-131">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f11b3-132">-Confirm</span></span>
<span data-ttu-id="f11b3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f11b3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f11b3-134">-WhatIf</span></span>
<span data-ttu-id="f11b3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f11b3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f11b3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f11b3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f11b3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11b3-137">CommonParameters</span></span>
<span data-ttu-id="f11b3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f11b3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11b3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f11b3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11b3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f11b3-140">INPUTS</span></span>

### <span data-ttu-id="f11b3-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f11b3-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="f11b3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f11b3-142">System.String</span></span>

### <span data-ttu-id="f11b3-143">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f11b3-143">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f11b3-144">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="f11b3-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="f11b3-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="f11b3-145">System.String[]</span></span>

## <span data-ttu-id="f11b3-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f11b3-146">OUTPUTS</span></span>

### <span data-ttu-id="f11b3-147">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f11b3-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="f11b3-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f11b3-148">NOTES</span></span>

## <span data-ttu-id="f11b3-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f11b3-149">RELATED LINKS</span></span>

[<span data-ttu-id="f11b3-150">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="f11b3-150">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
