---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E3E0237-8E2D-4B3A-AD0C-2121DDE1AAB6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 28259b97f382092f5e6293048c040688011cfe92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055118"
---
# <span data-ttu-id="93927-101">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="93927-101">Remove-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="93927-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93927-102">SYNOPSIS</span></span>
<span data-ttu-id="93927-103">Usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93927-103">Removes a network security group.</span></span>

## <span data-ttu-id="93927-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93927-104">SYNTAX</span></span>

### <span data-ttu-id="93927-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span><span class="sxs-lookup"><span data-stu-id="93927-105">RemoveNetworkSecurityGroupAssociationFromSubnet</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VirtualNetworkName <String> -SubnetName <String>
 [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93927-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span><span class="sxs-lookup"><span data-stu-id="93927-106">RemoveNetworkSecurityGroupAssociationFromIaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="93927-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span><span class="sxs-lookup"><span data-stu-id="93927-107">RemoveNetworkSecurityGroupAssociationFromPaaSRole</span></span>
```
Remove-AzureNetworkSecurityGroupAssociation -Name <String> [-Slot <String>] -RoleName <String>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Force] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="93927-108">Opis</span><span class="sxs-lookup"><span data-stu-id="93927-108">DESCRIPTION</span></span>
<span data-ttu-id="93927-109">Polecenie cmdlet **Remove-AzureNetworkSecurityGroupAssociation** usuwa grupę zabezpieczeń sieci z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93927-109">The **Remove-AzureNetworkSecurityGroupAssociation** cmdlet removes a network security group from a virtual machine.</span></span>

## <span data-ttu-id="93927-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93927-110">EXAMPLES</span></span>

### <span data-ttu-id="93927-111">Przykład 1: usunięcie maszyny wirtualnej w grupie zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="93927-111">Example 1: Remove a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Remove-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="93927-112">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93927-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="93927-113">Bieżące polecenie cmdlet usuwa grupę zabezpieczeń sieci o nazwie ContosoNetworkSecurityGroup z tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="93927-113">The current cmdlet removes the network security group named ContosoNetworkSecurityGroup from that virtual machine.</span></span>

## <span data-ttu-id="93927-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93927-114">PARAMETERS</span></span>

### <span data-ttu-id="93927-115">-Force</span><span class="sxs-lookup"><span data-stu-id="93927-115">-Force</span></span>
<span data-ttu-id="93927-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="93927-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93927-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93927-117">-Name</span></span>
<span data-ttu-id="93927-118">Określa nazwę grupy zabezpieczeń sieci, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="93927-118">Specifies the name of the network security group that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93927-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="93927-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="93927-120">Określa nazwę karty sieciowej, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93927-120">Specifies the name of the network adapter from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93927-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93927-121">-PassThru</span></span>
<span data-ttu-id="93927-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="93927-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="93927-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="93927-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="93927-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="93927-124">-Profile</span></span>
<span data-ttu-id="93927-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93927-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="93927-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="93927-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="93927-127">-Rolename</span><span class="sxs-lookup"><span data-stu-id="93927-127">-RoleName</span></span>
<span data-ttu-id="93927-128">Określa nazwę roli PaaS, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93927-128">Specifies the name of a PaaS role from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93927-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="93927-129">-ServiceName</span></span>
<span data-ttu-id="93927-130">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="93927-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="93927-131">Rola PaaS, za pomocą której to polecenie cmdlet usuwa grupę zabezpieczeń sieci, należy do usługi, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="93927-131">The PaaS role from which this cmdlet removes a network security group belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole, RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93927-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="93927-132">-Slot</span></span>
<span data-ttu-id="93927-133">Określa gniazdo PaaS.</span><span class="sxs-lookup"><span data-stu-id="93927-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="93927-134">Rola PaaS, za pomocą której to polecenie cmdlet usuwa grupę zabezpieczeń sieci, ma miejsce określone przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="93927-134">The PaaS role from which this cmdlet removes a network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="93927-135">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="93927-135">Valid values are:</span></span>

- <span data-ttu-id="93927-136">BOM</span><span class="sxs-lookup"><span data-stu-id="93927-136">Production</span></span>
- <span data-ttu-id="93927-137">Most</span><span class="sxs-lookup"><span data-stu-id="93927-137">Staging</span></span>

<span data-ttu-id="93927-138">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="93927-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93927-139">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="93927-139">-SubnetName</span></span>
<span data-ttu-id="93927-140">Określa nazwę podsieci, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93927-140">Specifies the name of a subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93927-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="93927-141">-VirtualNetworkName</span></span>
<span data-ttu-id="93927-142">Określa nazwę sieci wirtualnej zawierającej podsieć, z której to polecenie cmdlet usuwa grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93927-142">Specifies the name of a virtual network that contains the subnet from which this cmdlet removes the network security group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93927-143">-VM</span><span class="sxs-lookup"><span data-stu-id="93927-143">-VM</span></span>
<span data-ttu-id="93927-144">Określa maszynę wirtualną, do której to polecenie cmdlet ma zastosowanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="93927-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: RemoveNetworkSecurityGroupAssociationFromIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="93927-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93927-145">CommonParameters</span></span>
<span data-ttu-id="93927-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93927-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93927-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93927-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93927-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93927-148">INPUTS</span></span>

## <span data-ttu-id="93927-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93927-149">OUTPUTS</span></span>

### <span data-ttu-id="93927-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93927-150">System.Boolean</span></span>

## <span data-ttu-id="93927-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93927-151">NOTES</span></span>

## <span data-ttu-id="93927-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93927-152">RELATED LINKS</span></span>

[<span data-ttu-id="93927-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="93927-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="93927-154">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="93927-154">Set-AzureNetworkSecurityGroupAssociation</span></span>](./Set-AzureNetworkSecurityGroupAssociation.md)
