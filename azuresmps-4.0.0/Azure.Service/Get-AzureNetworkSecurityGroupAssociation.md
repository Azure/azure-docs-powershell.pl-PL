---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055548"
---
# <span data-ttu-id="399b3-101">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="399b3-101">Get-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="399b3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="399b3-102">SYNOPSIS</span></span>
<span data-ttu-id="399b3-103">Pobiera grupę zabezpieczeń sieci dla maszyny wirtualnej, karty sieciowej lub roli PaaS.</span><span class="sxs-lookup"><span data-stu-id="399b3-103">Gets a network security group for a virtual machine, network adapter, or PaaS role.</span></span>

## <span data-ttu-id="399b3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="399b3-104">SYNTAX</span></span>

### <span data-ttu-id="399b3-105">GetNetworkSecurityGroupAssociationForSubnet</span><span class="sxs-lookup"><span data-stu-id="399b3-105">GetNetworkSecurityGroupAssociationForSubnet</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="399b3-106">GetNetworkSecurityGroupAssociationForIaaSRole</span><span class="sxs-lookup"><span data-stu-id="399b3-106">GetNetworkSecurityGroupAssociationForIaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="399b3-107">GetNetworkSecurityGroupAssociationForPaaSRole</span><span class="sxs-lookup"><span data-stu-id="399b3-107">GetNetworkSecurityGroupAssociationForPaaSRole</span></span>
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="399b3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="399b3-108">DESCRIPTION</span></span>
<span data-ttu-id="399b3-109">Polecenie cmdlet **Get-AzureNetworkSecurityGroupAssociation** pobiera grupę zabezpieczeń sieci dla maszyny wirtualnej, karty sieciowej lub platformy jako rolę usługi (PaaS).</span><span class="sxs-lookup"><span data-stu-id="399b3-109">The **Get-AzureNetworkSecurityGroupAssociation** cmdlet gets the network security group for a virtual machine, network adapter, or platform as a service (PaaS) role.</span></span>

## <span data-ttu-id="399b3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="399b3-110">EXAMPLES</span></span>

### <span data-ttu-id="399b3-111">Przykład 1: Uzyskiwanie grupy zabezpieczeń sieci dla maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="399b3-111">Example 1: Get the network security group for a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

<span data-ttu-id="399b3-112">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="399b3-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="399b3-113">Bieżące polecenie cmdlet pobiera grupę zabezpieczeń sieci skojarzoną z tą maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="399b3-113">The current cmdlet gets the network security group associated to that virtual machine.</span></span>

## <span data-ttu-id="399b3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="399b3-114">PARAMETERS</span></span>

### <span data-ttu-id="399b3-115">— Szczegółowe informacje</span><span class="sxs-lookup"><span data-stu-id="399b3-115">-Detailed</span></span>
<span data-ttu-id="399b3-116">Wskazuje, że ten aplet polecenia zwraca szczegóły grupy zabezpieczeń sieci skojarzonej z maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="399b3-116">Indicates that this cmdlet returns details of the network security group that is associated to the virtual machine.</span></span>
<span data-ttu-id="399b3-117">Dane te obejmują lokalizację i reguły.</span><span class="sxs-lookup"><span data-stu-id="399b3-117">These details include location and rules.</span></span>

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

### <span data-ttu-id="399b3-118">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="399b3-118">-NetworkInterfaceName</span></span>
<span data-ttu-id="399b3-119">Określa nazwę karty sieciowej, dla której to polecenie cmdlet pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="399b3-119">Specifies the name of the network adapter for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="399b3-120">-Profile</span></span>
<span data-ttu-id="399b3-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="399b3-121">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="399b3-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="399b3-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-123">-Rolename</span><span class="sxs-lookup"><span data-stu-id="399b3-123">-RoleName</span></span>
<span data-ttu-id="399b3-124">Określa nazwę roli PaaS, dla której to polecenie cmdlet pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="399b3-124">Specifies the name of a PaaS role for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="399b3-125">-ServiceName</span></span>
<span data-ttu-id="399b3-126">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="399b3-126">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="399b3-127">Rola PaaS należy do usługi, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="399b3-127">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-128">-Slot</span><span class="sxs-lookup"><span data-stu-id="399b3-128">-Slot</span></span>
<span data-ttu-id="399b3-129">Określa gniazdo PaaS.</span><span class="sxs-lookup"><span data-stu-id="399b3-129">Specifies a PaaS slot.</span></span>
<span data-ttu-id="399b3-130">Rola PaaS, dla której to polecenie cmdlet pobiera grupę zabezpieczeń sieci, ma miejsce, w którym ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="399b3-130">The PaaS role for which this cmdlet gets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="399b3-131">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="399b3-131">Valid values are:</span></span> 

- <span data-ttu-id="399b3-132">BOM</span><span class="sxs-lookup"><span data-stu-id="399b3-132">Production</span></span>
- <span data-ttu-id="399b3-133">Most</span><span class="sxs-lookup"><span data-stu-id="399b3-133">Staging</span></span> 

<span data-ttu-id="399b3-134">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="399b3-134">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-135">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="399b3-135">-SubnetName</span></span>
<span data-ttu-id="399b3-136">Określa nazwę podsieci, dla której to polecenie cmdlet pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="399b3-136">Specifies the name of a subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-137">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="399b3-137">-VirtualNetworkName</span></span>
<span data-ttu-id="399b3-138">Określa nazwę sieci wirtualnej zawierającej podsieć, dla której to polecenie cmdlet pobiera grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="399b3-138">Specifies the name of a virtual network that contains the subnet for which this cmdlet gets the network security group.</span></span>

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-139">-VM</span><span class="sxs-lookup"><span data-stu-id="399b3-139">-VM</span></span>
<span data-ttu-id="399b3-140">Określa maszynę wirtualną, do której to polecenie cmdlet ma zastosowanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="399b3-140">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="399b3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="399b3-141">CommonParameters</span></span>
<span data-ttu-id="399b3-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="399b3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="399b3-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="399b3-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="399b3-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="399b3-144">INPUTS</span></span>

## <span data-ttu-id="399b3-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="399b3-145">OUTPUTS</span></span>

### <span data-ttu-id="399b3-146">Microsoft. platformy windowsazure. Commands. servicemanagement. Network. NetworkSecurityGroup. model. INetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="399b3-146">Microsoft.WindowsAzure.Commands.ServiceManagement.Network.NetworkSecurityGroup.Model.INetworkSecurityGroup</span></span>

## <span data-ttu-id="399b3-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="399b3-147">NOTES</span></span>

## <span data-ttu-id="399b3-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="399b3-148">RELATED LINKS</span></span>

[<span data-ttu-id="399b3-149">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="399b3-149">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="399b3-150">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="399b3-150">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)


