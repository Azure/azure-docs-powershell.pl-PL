---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548351"
---
# <span data-ttu-id="d7569-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7569-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d7569-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7569-102">SYNOPSIS</span></span>
<span data-ttu-id="d7569-103">Dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7569-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d7569-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7569-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7569-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7569-105">DESCRIPTION</span></span>
<span data-ttu-id="d7569-106">Polecenie cmdlet **Add-AzureRmVmssNetworkInterfaceConfiguration** umożliwia dodanie konfiguracji interfejsu sieciowego do zestawu skali maszyny wirtualnej (VMSS).</span><span class="sxs-lookup"><span data-stu-id="d7569-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d7569-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7569-107">EXAMPLES</span></span>

### <span data-ttu-id="d7569-108">Przykład 1: Dodawanie konfiguracji interfejsu sieciowego do VMSS</span><span class="sxs-lookup"><span data-stu-id="d7569-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="d7569-109">To polecenie dodaje konfigurację interfejsu sieciowego do VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7569-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="d7569-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7569-110">PARAMETERS</span></span>

### <span data-ttu-id="d7569-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7569-111">-DefaultProfile</span></span>
<span data-ttu-id="d7569-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7569-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7569-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="d7569-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="d7569-114">Lista adresów IP serwerów DNS dla ustawień DNS.</span><span class="sxs-lookup"><span data-stu-id="d7569-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="d7569-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="d7569-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="d7569-116">Określa, czy interfejs sieciowy jest włączony do przyspieszania obsługi sieci.</span><span class="sxs-lookup"><span data-stu-id="d7569-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7569-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d7569-117">-Id</span></span>
<span data-ttu-id="d7569-118">Określa identyfikator zasobu maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7569-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="d7569-119">-Element IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d7569-119">-IpConfiguration</span></span>
<span data-ttu-id="d7569-120">Określa konfiguracje IP interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="d7569-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="d7569-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7569-121">-Name</span></span>
<span data-ttu-id="d7569-122">Określa nazwę konfiguracji interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="d7569-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="d7569-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d7569-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d7569-124">Identyfikator grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="d7569-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="d7569-125">-Primary</span><span class="sxs-lookup"><span data-stu-id="d7569-125">-Primary</span></span>
<span data-ttu-id="d7569-126">Wskazuje, czy interfejsy sieciowe utworzone na podstawie konfiguracji interfejsu sieciowego będą podstawowym centrum informacyjnym (Network Information Center) maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="d7569-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="d7569-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d7569-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d7569-128">Określa obiekt VMSS.</span><span class="sxs-lookup"><span data-stu-id="d7569-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="d7569-129">Aby utworzyć obiekt, możesz użyć polecenia cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="d7569-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="d7569-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7569-130">-Confirm</span></span>
<span data-ttu-id="d7569-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7569-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7569-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7569-132">-WhatIf</span></span>
<span data-ttu-id="d7569-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7569-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d7569-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7569-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7569-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7569-135">CommonParameters</span></span>
<span data-ttu-id="d7569-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7569-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7569-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7569-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7569-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7569-138">INPUTS</span></span>

## <span data-ttu-id="d7569-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7569-139">OUTPUTS</span></span>

###  
<span data-ttu-id="d7569-140">To polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="d7569-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d7569-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7569-141">NOTES</span></span>

## <span data-ttu-id="d7569-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7569-142">RELATED LINKS</span></span>

[<span data-ttu-id="d7569-143">Nowe — AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d7569-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
