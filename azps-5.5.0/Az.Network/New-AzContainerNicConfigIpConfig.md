---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-AzContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzContainerNicConfigIpConfig.md
ms.openlocfilehash: 2e15819fe8b6b21b0f0c0751dc39736408606a7c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202842"
---
# <span data-ttu-id="d3a16-101">New-AzContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="d3a16-101">New-AzContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="d3a16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3a16-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a16-103">Tworzy obiekt konfiguracji adresu IP konfiguracji kontenera.</span><span class="sxs-lookup"><span data-stu-id="d3a16-103">Creates a container nic configuration ip configuration object.</span></span>

## <span data-ttu-id="d3a16-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3a16-104">SYNTAX</span></span>

```
New-AzContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a16-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3a16-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a16-106">Polecenie **cmdlet New-AzContainerNicConfigIpConfig** tworzy nową konfigurację ip interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d3a16-106">The **New-AzContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="d3a16-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3a16-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a16-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3a16-108">Example 1</span></span>
```powershell
$subnet = New-AzVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="d3a16-109">Pierwsze dwa polecenia tworzą i inicjują podsieci vnet oraz podsieci.</span><span class="sxs-lookup"><span data-stu-id="d3a16-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="d3a16-110">Trzecie polecenie tworzy profil konfiguracji nic ip container nic odwołujący się do utworzonej podsieci.</span><span class="sxs-lookup"><span data-stu-id="d3a16-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span> <span data-ttu-id="d3a16-111">Czwarte polecenie tworzy konfigurację kontenera interfejsu sieciowego, która dostarcza profil konfiguracji adresu IP utworzony w poprzednim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="d3a16-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="d3a16-112">Na koniec piąte polecenie tworzy profil sieciowy zainicjowany przy użyciu konfiguracji interfejsu sieciowego kontenerów przechowywanej w $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="d3a16-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="d3a16-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3a16-113">PARAMETERS</span></span>

### <span data-ttu-id="d3a16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a16-114">-DefaultProfile</span></span>
<span data-ttu-id="d3a16-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3a16-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3a16-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d3a16-116">-Name</span></span>
<span data-ttu-id="d3a16-117">Nazwa profilu konfiguracji ip interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="d3a16-117">Name of the container network interface configuration ip configuration profile.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a16-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="d3a16-118">-Subnet</span></span>
<span data-ttu-id="d3a16-119">Podsieci</span><span class="sxs-lookup"><span data-stu-id="d3a16-119">Subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a16-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="d3a16-120">-SubnetId</span></span>
<span data-ttu-id="d3a16-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="d3a16-121">SubnetId</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3a16-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3a16-122">-Confirm</span></span>
<span data-ttu-id="d3a16-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d3a16-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a16-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a16-124">-WhatIf</span></span>
<span data-ttu-id="d3a16-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3a16-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3a16-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d3a16-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a16-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a16-127">CommonParameters</span></span>
<span data-ttu-id="d3a16-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a16-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a16-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a16-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a16-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a16-130">INPUTS</span></span>

### <span data-ttu-id="d3a16-131">Brak</span><span class="sxs-lookup"><span data-stu-id="d3a16-131">None</span></span>

## <span data-ttu-id="d3a16-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3a16-132">OUTPUTS</span></span>

### <span data-ttu-id="d3a16-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3a16-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d3a16-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3a16-134">NOTES</span></span>

## <span data-ttu-id="d3a16-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3a16-135">RELATED LINKS</span></span>

[<span data-ttu-id="d3a16-136">New-AzContainerNicConfig</span><span class="sxs-lookup"><span data-stu-id="d3a16-136">New-AzContainerNicConfig</span></span>](./New-AzContainerNicConfig.md)
