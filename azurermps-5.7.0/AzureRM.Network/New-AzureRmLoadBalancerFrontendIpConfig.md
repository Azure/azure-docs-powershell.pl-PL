---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: b05804bb5af2513e6a54026c7b989662212ba350
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717482"
---
# <span data-ttu-id="4839b-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4839b-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="4839b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4839b-102">SYNOPSIS</span></span>
<span data-ttu-id="4839b-103">Tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4839b-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4839b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4839b-104">SYNTAX</span></span>

### <span data-ttu-id="4839b-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="4839b-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4839b-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="4839b-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4839b-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4839b-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4839b-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4839b-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4839b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4839b-109">DESCRIPTION</span></span>
<span data-ttu-id="4839b-110">Polecenie cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4839b-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="4839b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4839b-111">EXAMPLES</span></span>

### <span data-ttu-id="4839b-112">Przykład 1. Tworzenie zewnętrznej konfiguracji adresów IP dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="4839b-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="4839b-113">Pierwsze polecenie tworzy dynamiczny publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="4839b-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="4839b-114">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip.</span><span class="sxs-lookup"><span data-stu-id="4839b-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="4839b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4839b-115">PARAMETERS</span></span>

### <span data-ttu-id="4839b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4839b-116">-DefaultProfile</span></span>
<span data-ttu-id="4839b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4839b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4839b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4839b-118">-Name</span></span>
<span data-ttu-id="4839b-119">Określa konfigurację adresu IP frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4839b-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4839b-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="4839b-120">-PrivateIpAddress</span></span>
<span data-ttu-id="4839b-121">Określa prywatny adres IP modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="4839b-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="4839b-122">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="4839b-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4839b-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4839b-123">-PublicIpAddress</span></span>
<span data-ttu-id="4839b-124">Określa obiekt **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="4839b-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4839b-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="4839b-125">-PublicIpAddressId</span></span>
<span data-ttu-id="4839b-126">Określa identyfikator obiektu **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="4839b-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4839b-127">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="4839b-127">-Subnet</span></span>
<span data-ttu-id="4839b-128">Określa obiekt **podsieci** , w którym ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="4839b-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4839b-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4839b-129">-SubnetId</span></span>
<span data-ttu-id="4839b-130">Określa identyfikator podsieci, w której ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="4839b-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4839b-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="4839b-131">-Zone</span></span>
<span data-ttu-id="4839b-132">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="4839b-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4839b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4839b-133">CommonParameters</span></span>
<span data-ttu-id="4839b-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4839b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4839b-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4839b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4839b-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4839b-136">INPUTS</span></span>

### <span data-ttu-id="4839b-137">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="4839b-137">None</span></span>
<span data-ttu-id="4839b-138">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="4839b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4839b-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4839b-139">OUTPUTS</span></span>

### <span data-ttu-id="4839b-140">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="4839b-140">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="4839b-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4839b-141">NOTES</span></span>

## <span data-ttu-id="4839b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4839b-142">RELATED LINKS</span></span>

[<span data-ttu-id="4839b-143">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4839b-143">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4839b-144">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4839b-144">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4839b-145">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="4839b-145">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="4839b-146">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4839b-146">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="4839b-147">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="4839b-147">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


