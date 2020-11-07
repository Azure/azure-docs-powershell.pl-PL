---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 43d7040543beb049f46fce45cab69d9128a8954e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893862"
---
# <span data-ttu-id="ae699-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae699-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="ae699-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae699-102">SYNOPSIS</span></span>
<span data-ttu-id="ae699-103">Dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae699-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="ae699-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae699-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae699-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae699-105">DESCRIPTION</span></span>
<span data-ttu-id="ae699-106">Polecenie cmdlet **Add-AzVmssNetworkInterfaceConfiguration** umożliwia dodanie konfiguracji interfejsu sieciowego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="ae699-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="ae699-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae699-107">EXAMPLES</span></span>

### <span data-ttu-id="ae699-108">Przykład 1: Dodawanie konfiguracji interfejsu sieciowego do VMSS</span><span class="sxs-lookup"><span data-stu-id="ae699-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="ae699-109">To polecenie dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae699-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="ae699-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae699-110">PARAMETERS</span></span>

### <span data-ttu-id="ae699-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae699-111">-DefaultProfile</span></span>
<span data-ttu-id="ae699-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ae699-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="ae699-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="ae699-114">Lista adresów IP serwerów DNS dla ustawień DNS.</span><span class="sxs-lookup"><span data-stu-id="ae699-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="ae699-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="ae699-116">Określa, czy interfejs sieciowy jest włączony do przyspieszania obsługi sieci.</span><span class="sxs-lookup"><span data-stu-id="ae699-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="ae699-117">-EnableIPForwarding</span></span>
<span data-ttu-id="ae699-118">Określa, czy włączono przekierowywanie IP na tej karcie NIC.</span><span class="sxs-lookup"><span data-stu-id="ae699-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ae699-119">-Id</span></span>
<span data-ttu-id="ae699-120">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae699-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-121">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae699-121">-IpConfiguration</span></span>
<span data-ttu-id="ae699-122">Określa konfiguracje IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="ae699-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ae699-123">-Name</span></span>
<span data-ttu-id="ae699-124">Określa nazwę konfiguracji interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="ae699-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="ae699-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="ae699-126">Identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="ae699-126">Id of the network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-127">-Primary</span><span class="sxs-lookup"><span data-stu-id="ae699-127">-Primary</span></span>
<span data-ttu-id="ae699-128">Wskazuje, czy interfejsy sieciowe utworzone na podstawie konfiguracji interfejsu sieciowego będą podstawowym centrum informacyjnym (Network Information Center) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae699-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ae699-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="ae699-130">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="ae699-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="ae699-131">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="ae699-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae699-132">-Confirm</span></span>
<span data-ttu-id="ae699-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae699-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae699-134">-WhatIf</span></span>
<span data-ttu-id="ae699-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae699-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae699-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae699-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae699-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae699-137">CommonParameters</span></span>
<span data-ttu-id="ae699-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae699-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae699-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae699-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae699-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae699-140">INPUTS</span></span>

### <span data-ttu-id="ae699-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="ae699-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="ae699-142">Parametr "VirtualMachineScaleSet" akceptuje wartość typu "VirtualMachineScaleSet" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ae699-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="ae699-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae699-143">OUTPUTS</span></span>

###  
<span data-ttu-id="ae699-144">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="ae699-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ae699-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae699-145">NOTES</span></span>

## <span data-ttu-id="ae699-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae699-146">RELATED LINKS</span></span>

[<span data-ttu-id="ae699-147">Nowe — AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="ae699-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
