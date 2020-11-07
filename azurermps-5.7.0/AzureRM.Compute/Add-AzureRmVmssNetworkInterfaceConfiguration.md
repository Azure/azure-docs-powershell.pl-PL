---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716507"
---
# <span data-ttu-id="abb74-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="abb74-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="abb74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="abb74-102">SYNOPSIS</span></span>
<span data-ttu-id="abb74-103">Dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="abb74-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="abb74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="abb74-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="abb74-105">Opis</span><span class="sxs-lookup"><span data-stu-id="abb74-105">DESCRIPTION</span></span>
<span data-ttu-id="abb74-106">Polecenie cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** umożliwia dodanie konfiguracji interfejsu sieciowego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="abb74-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="abb74-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="abb74-107">EXAMPLES</span></span>

### <span data-ttu-id="abb74-108">Przykład 1: Dodawanie konfiguracji interfejsu sieciowego do VMSS</span><span class="sxs-lookup"><span data-stu-id="abb74-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="abb74-109">To polecenie dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="abb74-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="abb74-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="abb74-110">PARAMETERS</span></span>

### <span data-ttu-id="abb74-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="abb74-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="abb74-112">Lista adresów IP serwerów DNS dla ustawień DNS.</span><span class="sxs-lookup"><span data-stu-id="abb74-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="abb74-113">-ID</span><span class="sxs-lookup"><span data-stu-id="abb74-113">-Id</span></span>
<span data-ttu-id="abb74-114">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="abb74-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="abb74-115">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="abb74-115">-IpConfiguration</span></span>
<span data-ttu-id="abb74-116">Określa konfiguracje IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="abb74-116">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="abb74-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="abb74-117">-Name</span></span>
<span data-ttu-id="abb74-118">Określa nazwę konfiguracji interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="abb74-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="abb74-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="abb74-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="abb74-120">Identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="abb74-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="abb74-121">-Primary</span><span class="sxs-lookup"><span data-stu-id="abb74-121">-Primary</span></span>
<span data-ttu-id="abb74-122">Wskazuje, czy interfejsy sieciowe utworzone na podstawie konfiguracji interfejsu sieciowego będą podstawowym centrum informacyjnym (Network Information Center) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="abb74-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="abb74-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="abb74-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="abb74-124">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="abb74-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="abb74-125">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="abb74-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abb74-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="abb74-126">-Confirm</span></span>
<span data-ttu-id="abb74-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abb74-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abb74-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abb74-128">-WhatIf</span></span>
<span data-ttu-id="abb74-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="abb74-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="abb74-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="abb74-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abb74-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abb74-131">CommonParameters</span></span>
<span data-ttu-id="abb74-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="abb74-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abb74-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="abb74-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abb74-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="abb74-134">INPUTS</span></span>

### <span data-ttu-id="abb74-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="abb74-135">None</span></span>
<span data-ttu-id="abb74-136">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="abb74-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="abb74-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="abb74-137">OUTPUTS</span></span>

###  
<span data-ttu-id="abb74-138">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="abb74-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="abb74-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="abb74-139">NOTES</span></span>

## <span data-ttu-id="abb74-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="abb74-140">RELATED LINKS</span></span>

[<span data-ttu-id="abb74-141">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="abb74-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
