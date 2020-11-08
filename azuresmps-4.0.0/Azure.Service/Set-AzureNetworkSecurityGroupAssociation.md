---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 64639A35-0573-48C8-AB21-19FEB09537BA
online version: ''
schema: 2.0.0
ms.openlocfilehash: b1b251a5fef3ad91f830e18714796421d2abca7b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054724"
---
# <span data-ttu-id="2eba2-101">Set-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="2eba2-101">Set-AzureNetworkSecurityGroupAssociation</span></span>

## <span data-ttu-id="2eba2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2eba2-102">SYNOPSIS</span></span>
<span data-ttu-id="2eba2-103">Kojarzy grupę zabezpieczeń sieci z maszyną wirtualną, rolą PaaS lub kartą sieciową.</span><span class="sxs-lookup"><span data-stu-id="2eba2-103">Associates a network security group to a virtual machine, PaaS role, or network adapter.</span></span>

## <span data-ttu-id="2eba2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2eba2-104">SYNTAX</span></span>

### <span data-ttu-id="2eba2-105">AddNetworkSecurityGroupAssociationToSubnet</span><span class="sxs-lookup"><span data-stu-id="2eba2-105">AddNetworkSecurityGroupAssociationToSubnet</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VirtualNetworkName <String>
 -SubnetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2eba2-106">AddNetworkSecurityGroupAssociationToIaaSRole</span><span class="sxs-lookup"><span data-stu-id="2eba2-106">AddNetworkSecurityGroupAssociationToIaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] -VM <PersistentVMRoleContext>
 -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="2eba2-107">AddNetworkSecurityGroupAssociationToPaaSRole</span><span class="sxs-lookup"><span data-stu-id="2eba2-107">AddNetworkSecurityGroupAssociationToPaaSRole</span></span>
```
Set-AzureNetworkSecurityGroupAssociation -Name <String> [-Force] [-PassThru] [-Slot <String>]
 -RoleName <String> -ServiceName <String> [-NetworkInterfaceName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2eba2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2eba2-108">DESCRIPTION</span></span>
<span data-ttu-id="2eba2-109">Polecenie cmdlet **Set-AzureNetworkSecurityGroupAssociation** kojarzy grupę zabezpieczeń sieci z maszyną wirtualną, platformą w roli usługi (PaaS) lub kartą sieciową.</span><span class="sxs-lookup"><span data-stu-id="2eba2-109">The **Set-AzureNetworkSecurityGroupAssociation** cmdlet associates a network security group to a virtual machine, platform as a service (PaaS) role, or network adapter.</span></span>

## <span data-ttu-id="2eba2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2eba2-110">EXAMPLES</span></span>

### <span data-ttu-id="2eba2-111">Przykład 1: przypisywanie maszyny wirtualnej do grupy zabezpieczeń sieci</span><span class="sxs-lookup"><span data-stu-id="2eba2-111">Example 1: Assign a virtual machine to a network security group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Set-AzureNetworkSecurityGroupAssociation -Name "ContosoNetworkSecurityGroup"
```

<span data-ttu-id="2eba2-112">To polecenie pobiera maszynę wirtualną o nazwie ContosoVM06 dla usługi o nazwie ContosoService i przekazuje ten obiekt maszyny wirtualnej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eba2-112">This command gets a virtual machine named ContosoVM06 for the service named ContosoService, and passes that virtual machine object to the current cmdlet.</span></span>
<span data-ttu-id="2eba2-113">Bieżące polecenie cmdlet powoduje przypisanie grupie zabezpieczeń sieci o nazwie ContosoNetworkSecurityGroup do tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2eba2-113">The current cmdlet assigns the network security group named ContosoNetworkSecurityGroup to that virtual machine.</span></span>

## <span data-ttu-id="2eba2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2eba2-114">PARAMETERS</span></span>

### <span data-ttu-id="2eba2-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2eba2-115">-Force</span></span>
<span data-ttu-id="2eba2-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2eba2-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2eba2-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2eba2-117">-Name</span></span>
<span data-ttu-id="2eba2-118">Określa nazwę grupy zabezpieczeń sieci, która jest ustawiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eba2-118">Specifies the name of the network security group that this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-119">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="2eba2-119">-NetworkInterfaceName</span></span>
<span data-ttu-id="2eba2-120">Określa nazwę karty sieciowej, z którą to polecenie cmdlet będzie stosować grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2eba2-120">Specifies the name of the network adapter to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2eba2-121">-PassThru</span></span>
<span data-ttu-id="2eba2-122">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2eba2-122">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="2eba2-123">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2eba2-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2eba2-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="2eba2-124">-Profile</span></span>
<span data-ttu-id="2eba2-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eba2-125">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2eba2-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2eba2-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2eba2-127">-Rolename</span><span class="sxs-lookup"><span data-stu-id="2eba2-127">-RoleName</span></span>
<span data-ttu-id="2eba2-128">Określa nazwę roli PaaS, do której to polecenie cmdlet ma zastosowanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2eba2-128">Specifies the name of a PaaS role to which this cmdlet applies the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2eba2-129">-ServiceName</span></span>
<span data-ttu-id="2eba2-130">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="2eba2-130">Specifies the name of a cloud service.</span></span>
<span data-ttu-id="2eba2-131">Rola PaaS należy do usługi, którą określa ten parametr.</span><span class="sxs-lookup"><span data-stu-id="2eba2-131">The PaaS role belongs to the service that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole, AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="2eba2-132">-Slot</span></span>
<span data-ttu-id="2eba2-133">Określa gniazdo PaaS.</span><span class="sxs-lookup"><span data-stu-id="2eba2-133">Specifies a PaaS slot.</span></span>
<span data-ttu-id="2eba2-134">Rola PaaS, dla której to polecenie cmdlet ustawia grupę zabezpieczeń sieci, ma miejsce, w którym ten parametr określa.</span><span class="sxs-lookup"><span data-stu-id="2eba2-134">The PaaS role for which this cmdlet sets the network security group has the slot that this parameter specifies.</span></span>
<span data-ttu-id="2eba2-135">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="2eba2-135">Valid values are:</span></span> 

- <span data-ttu-id="2eba2-136">BOM</span><span class="sxs-lookup"><span data-stu-id="2eba2-136">Production</span></span>
- <span data-ttu-id="2eba2-137">Most</span><span class="sxs-lookup"><span data-stu-id="2eba2-137">Staging</span></span> 

<span data-ttu-id="2eba2-138">Wartością domyślną jest produkcja.</span><span class="sxs-lookup"><span data-stu-id="2eba2-138">The default value is Production.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-139">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="2eba2-139">-SubnetName</span></span>
<span data-ttu-id="2eba2-140">Określa nazwę podsieci, do której to polecenie cmdlet kojarzy grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2eba2-140">Specifies the name of a subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="2eba2-141">-VirtualNetworkName</span></span>
<span data-ttu-id="2eba2-142">Określa nazwę sieci wirtualnej zawierającej podsieć, do której to polecenie cmdlet kojarzy grupę zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2eba2-142">Specifies the name of a virtual network that contains the subnet to which this cmdlet associates the network security group.</span></span>

```yaml
Type: String
Parameter Sets: AddNetworkSecurityGroupAssociationToSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-143">-VM</span><span class="sxs-lookup"><span data-stu-id="2eba2-143">-VM</span></span>
<span data-ttu-id="2eba2-144">Określa maszynę wirtualną, do której to polecenie cmdlet ma zastosowanie do grupy zabezpieczeń sieci.</span><span class="sxs-lookup"><span data-stu-id="2eba2-144">Specifies the virtual machine to which this cmdlet applies the network security group.</span></span>

```yaml
Type: PersistentVMRoleContext
Parameter Sets: AddNetworkSecurityGroupAssociationToIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2eba2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eba2-145">CommonParameters</span></span>
<span data-ttu-id="2eba2-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eba2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eba2-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eba2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eba2-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2eba2-148">INPUTS</span></span>

## <span data-ttu-id="2eba2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2eba2-149">OUTPUTS</span></span>

### <span data-ttu-id="2eba2-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2eba2-150">System.Boolean</span></span>

## <span data-ttu-id="2eba2-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2eba2-151">NOTES</span></span>

## <span data-ttu-id="2eba2-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2eba2-152">RELATED LINKS</span></span>

[<span data-ttu-id="2eba2-153">Get-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="2eba2-153">Get-AzureNetworkSecurityGroupAssociation</span></span>](./Get-AzureNetworkSecurityGroupAssociation.md)

[<span data-ttu-id="2eba2-154">Remove-AzureNetworkSecurityGroupAssociation</span><span class="sxs-lookup"><span data-stu-id="2eba2-154">Remove-AzureNetworkSecurityGroupAssociation</span></span>](./Remove-AzureNetworkSecurityGroupAssociation.md)


