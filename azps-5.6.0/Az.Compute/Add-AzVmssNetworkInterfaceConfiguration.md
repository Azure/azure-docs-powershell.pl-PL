---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: c85c4292fcae081e50ba98ff873f967f8e32fbac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969553"
---
# <span data-ttu-id="e7d56-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7d56-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="e7d56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7d56-102">SYNOPSIS</span></span>
<span data-ttu-id="e7d56-103">Dodaje konfigurację interfejsu sieciowego do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7d56-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e7d56-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e7d56-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7d56-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e7d56-105">DESCRIPTION</span></span>
<span data-ttu-id="e7d56-106">Polecenie **cmdlet Add-AzVmssNetworkInterfaceConfiguration** dodaje konfigurację interfejsu sieciowego do zestawu skal maszyny wirtualnej (VIRTUAL Machine Scale Set).</span><span class="sxs-lookup"><span data-stu-id="e7d56-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="e7d56-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e7d56-107">EXAMPLES</span></span>

### <span data-ttu-id="e7d56-108">Przykład 1. Dodawanie konfiguracji interfejsu sieciowego do usług MASZYNY WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="e7d56-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="e7d56-109">To polecenie dodaje konfigurację interfejsu sieciowego do usług MASZYNY WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e7d56-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="e7d56-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e7d56-110">PARAMETERS</span></span>

### <span data-ttu-id="e7d56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7d56-111">-DefaultProfile</span></span>
<span data-ttu-id="e7d56-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e7d56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e7d56-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="e7d56-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="e7d56-114">Lista adresów IP serwera DNS dla ustawień dns.</span><span class="sxs-lookup"><span data-stu-id="e7d56-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="e7d56-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="e7d56-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="e7d56-116">Określa, czy interfejs sieciowy ma być przyspieszony z włączoną obsługą sieci.</span><span class="sxs-lookup"><span data-stu-id="e7d56-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="e7d56-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="e7d56-117">-EnableIPForwarding</span></span>
<span data-ttu-id="e7d56-118">Określa, czy dla tej nic nic nie jest włączone przesyłanie dalej adresów IP.</span><span class="sxs-lookup"><span data-stu-id="e7d56-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="e7d56-119">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="e7d56-119">-Id</span></span>
<span data-ttu-id="e7d56-120">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7d56-120">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="e7d56-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="e7d56-121">-IpConfiguration</span></span>
<span data-ttu-id="e7d56-122">Określa konfiguracje adresów IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e7d56-122">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="e7d56-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e7d56-123">-Name</span></span>
<span data-ttu-id="e7d56-124">Określa nazwę konfiguracji interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e7d56-124">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="e7d56-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="e7d56-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="e7d56-126">Identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="e7d56-126">Id of the network security group.</span></span>

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

### <span data-ttu-id="e7d56-127">— podstawowy</span><span class="sxs-lookup"><span data-stu-id="e7d56-127">-Primary</span></span>
<span data-ttu-id="e7d56-128">Wskazuje, czy interfejsy sieciowe utworzone na podstawie konfiguracji interfejsu sieciowego będą podstawowym centrum informacyjnym sieciowym (NIC) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e7d56-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="e7d56-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7d56-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="e7d56-130">Określa obiekt MASZYNY.MASZYNY.WIRTUALNE.</span><span class="sxs-lookup"><span data-stu-id="e7d56-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="e7d56-131">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig.](./New-AzVmssConfig.md)</span><span class="sxs-lookup"><span data-stu-id="e7d56-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="e7d56-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7d56-132">-Confirm</span></span>
<span data-ttu-id="e7d56-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7d56-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7d56-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7d56-134">-WhatIf</span></span>
<span data-ttu-id="e7d56-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7d56-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e7d56-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e7d56-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7d56-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7d56-137">CommonParameters</span></span>
<span data-ttu-id="e7d56-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7d56-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7d56-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7d56-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7d56-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7d56-140">INPUTS</span></span>

### <span data-ttu-id="e7d56-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7d56-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="e7d56-142">System.String</span><span class="sxs-lookup"><span data-stu-id="e7d56-142">System.String</span></span>

### <span data-ttu-id="e7d56-143">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e7d56-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e7d56-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="e7d56-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="e7d56-145">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e7d56-145">System.String[]</span></span>

## <span data-ttu-id="e7d56-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7d56-146">OUTPUTS</span></span>

### <span data-ttu-id="e7d56-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="e7d56-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="e7d56-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e7d56-148">NOTES</span></span>

## <span data-ttu-id="e7d56-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7d56-149">RELATED LINKS</span></span>

[<span data-ttu-id="e7d56-150">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="e7d56-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
