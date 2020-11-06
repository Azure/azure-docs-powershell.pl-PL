---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-AzureRmNetworkProfileContainerNicconfigipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmContainerNicConfigIpConfig.md
ms.openlocfilehash: 0a2157d006277aa491281c51f1c3b7a910b8a5c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547475"
---
# <span data-ttu-id="34ff8-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span><span class="sxs-lookup"><span data-stu-id="34ff8-101">New-AzureRmNetworkProfileContainerNicConfigIpConfig</span></span>

## <span data-ttu-id="34ff8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="34ff8-103">Umożliwia utworzenie obiektu konfiguracji IP konfiguracji interfejsu karty sieciowej kontenera.</span><span class="sxs-lookup"><span data-stu-id="34ff8-103">Creates a container nic configuration ip configuration object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34ff8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34ff8-104">SYNTAX</span></span>

```
New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name <String> -Subnet <PSSubnet> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34ff8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="34ff8-106">Polecenie cmdlet **New-AzureRmNetworkProfileContainerNicConfigIpConfig** tworzy nową konfigurację adresu IP konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="34ff8-106">The **New-AzureRmNetworkProfileContainerNicConfigIpConfig** cmdlet creates a new container network interface configuration ip configuration.</span></span> 

## <span data-ttu-id="34ff8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34ff8-107">EXAMPLES</span></span>

### <span data-ttu-id="34ff8-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="34ff8-108">Example 1</span></span>
```powershell
$subnet = New-AzureRmVirtualNetworkSubnetConfig -Name subnet -AddressPrefix 10.0.1.0/24

$vnet = New-AzureRmVirtualNetwork -Name vnet -ResourceGroupName rg1 -Location "West US" -AddressPrefix 10.0.0.0/16 -Subnet $subnet

$containerNicConfigIpConfig = New-AzureRmNetworkProfileContainerNicConfigIpConfig -Name ipconfigprofile1 -Subnet $vnet.Subnets[0]

$containerNicConfig = New-AzureRmNetworkProfileContainerNicConfig -Name cnic -IpConfiguration containerNicConfigIpConfig

$networkProfile = New-AzureRmNetworkProfile -Name np1 -Location "West US" -ResourceGroupName rg1 -ContainerNetworkInterfaceConfiguration $containerNicConfig
```

<span data-ttu-id="34ff8-109">Pierwsze dwa polecenia tworzą i inicjują sieć VNET oraz podsieć.</span><span class="sxs-lookup"><span data-stu-id="34ff8-109">The first two commands create and initialize a vnet and a subnet.</span></span> <span data-ttu-id="34ff8-110">W trzecim poleceniu jest tworzony profil konfiguracji IP kontenera, który odwołuje się do utworzonej podsieci.</span><span class="sxs-lookup"><span data-stu-id="34ff8-110">The third command creates a container nic ip configuration profile referencing the created subnet.</span></span>  <span data-ttu-id="34ff8-111">Czwarte polecenie tworzy konfigurację interfejsu sieciowego kontenera dostarczającego profil konfiguracji IP utworzony w poprzednim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="34ff8-111">The fourth command creates a container network interface configuration supplying the ip configuration profile created in the previous command.</span></span> <span data-ttu-id="34ff8-112">Wreszcie, piąte polecenie tworzy profil sieciowy zainicjowany z konfiguracją interfejsu sieciowego kontenera przechowywaną w $containerNicConfig.</span><span class="sxs-lookup"><span data-stu-id="34ff8-112">Finally, the fifth command creates a network profile initialized with the container network interface configuration stored in $containerNicConfig.</span></span>

## <span data-ttu-id="34ff8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34ff8-113">PARAMETERS</span></span>

### <span data-ttu-id="34ff8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34ff8-114">-DefaultProfile</span></span>
<span data-ttu-id="34ff8-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="34ff8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34ff8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="34ff8-116">-Name</span></span>
<span data-ttu-id="34ff8-117">Nazwa profilu konfiguracji protokołu IP konfiguracji interfejsu sieciowego kontenera.</span><span class="sxs-lookup"><span data-stu-id="34ff8-117">Name of the container network interface configuration ip configuration profile.</span></span>

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

### <span data-ttu-id="34ff8-118">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="34ff8-118">-Subnet</span></span>
<span data-ttu-id="34ff8-119">Żąda</span><span class="sxs-lookup"><span data-stu-id="34ff8-119">Subnet</span></span>

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

### <span data-ttu-id="34ff8-120">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="34ff8-120">-SubnetId</span></span>
<span data-ttu-id="34ff8-121">SubnetId</span><span class="sxs-lookup"><span data-stu-id="34ff8-121">SubnetId</span></span>

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

### <span data-ttu-id="34ff8-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="34ff8-122">-Confirm</span></span>
<span data-ttu-id="34ff8-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ff8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34ff8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34ff8-124">-WhatIf</span></span>
<span data-ttu-id="34ff8-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34ff8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34ff8-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="34ff8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34ff8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34ff8-127">CommonParameters</span></span>
<span data-ttu-id="34ff8-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34ff8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34ff8-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34ff8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34ff8-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34ff8-130">INPUTS</span></span>

### <span data-ttu-id="34ff8-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="34ff8-131">None</span></span>

## <span data-ttu-id="34ff8-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34ff8-132">OUTPUTS</span></span>

### <span data-ttu-id="34ff8-133">Microsoft. Azure. Commands. Network. models. PSContainerNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="34ff8-133">Microsoft.Azure.Commands.Network.Models.PSContainerNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="34ff8-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34ff8-134">NOTES</span></span>

## <span data-ttu-id="34ff8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34ff8-135">RELATED LINKS</span></span>
