---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053862"
---
# <span data-ttu-id="241a6-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="241a6-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="241a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="241a6-102">SYNOPSIS</span></span>
<span data-ttu-id="241a6-103">Dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="241a6-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="241a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="241a6-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="241a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="241a6-105">DESCRIPTION</span></span>
<span data-ttu-id="241a6-106">Polecenie cmdlet **Add-AzVmssNetworkInterfaceConfiguration** umożliwia dodanie konfiguracji interfejsu sieciowego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="241a6-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="241a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="241a6-107">EXAMPLES</span></span>

### <span data-ttu-id="241a6-108">Przykład 1: Dodawanie konfiguracji interfejsu sieciowego do VMSS</span><span class="sxs-lookup"><span data-stu-id="241a6-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="241a6-109">To polecenie dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="241a6-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="241a6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="241a6-110">PARAMETERS</span></span>

### <span data-ttu-id="241a6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="241a6-111">-DefaultProfile</span></span>
<span data-ttu-id="241a6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="241a6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="241a6-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="241a6-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="241a6-114">Lista adresów IP serwerów DNS dla ustawień DNS.</span><span class="sxs-lookup"><span data-stu-id="241a6-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="241a6-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="241a6-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="241a6-116">Określa, czy interfejs sieciowy jest włączony do przyspieszania obsługi sieci.</span><span class="sxs-lookup"><span data-stu-id="241a6-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="241a6-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="241a6-117">-EnableIPForwarding</span></span>
<span data-ttu-id="241a6-118">Określa, czy włączono przekierowywanie IP na tej karcie NIC.</span><span class="sxs-lookup"><span data-stu-id="241a6-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="241a6-119">-ID</span><span class="sxs-lookup"><span data-stu-id="241a6-119">-Id</span></span>
<span data-ttu-id="241a6-120">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="241a6-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="241a6-121">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="241a6-121">-IpConfiguration</span></span>
<span data-ttu-id="241a6-122">Określa konfiguracje IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="241a6-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="241a6-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="241a6-123">-Name</span></span>
<span data-ttu-id="241a6-124">Określa nazwę konfiguracji interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="241a6-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="241a6-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="241a6-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="241a6-126">Identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="241a6-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="241a6-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="241a6-127">-Primary</span></span>
<span data-ttu-id="241a6-128">Wskazuje, czy interfejsy sieciowe utworzone na podstawie konfiguracji interfejsu sieciowego będą podstawowym centrum informacyjnym (Network Information Center) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="241a6-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="241a6-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="241a6-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="241a6-130">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="241a6-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="241a6-131">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="241a6-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="241a6-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="241a6-132">-Confirm</span></span>
<span data-ttu-id="241a6-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241a6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="241a6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="241a6-134">-WhatIf</span></span>
<span data-ttu-id="241a6-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="241a6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="241a6-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="241a6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="241a6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="241a6-137">CommonParameters</span></span>
<span data-ttu-id="241a6-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="241a6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="241a6-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="241a6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="241a6-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="241a6-140">INPUTS</span></span>

### <span data-ttu-id="241a6-141">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="241a6-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="241a6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="241a6-142">System.String</span></span>

### <span data-ttu-id="241a6-143">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="241a6-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="241a6-144">Microsoft. Azure. Management. COMPUTE. MODELES. VirtualMachineScaleSetIPConfiguration []</span><span class="sxs-lookup"><span data-stu-id="241a6-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="241a6-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="241a6-145">System.String[]</span></span>

## <span data-ttu-id="241a6-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="241a6-146">OUTPUTS</span></span>

### <span data-ttu-id="241a6-147">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="241a6-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="241a6-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="241a6-148">NOTES</span></span>

## <span data-ttu-id="241a6-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="241a6-149">RELATED LINKS</span></span>

[<span data-ttu-id="241a6-150">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="241a6-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
