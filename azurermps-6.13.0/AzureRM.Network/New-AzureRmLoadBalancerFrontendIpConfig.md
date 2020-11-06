---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 77dbd80f03cb26adbb68e320d761200cd9ee7bc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545064"
---
# <span data-ttu-id="2c220-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c220-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="2c220-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c220-102">SYNOPSIS</span></span>
<span data-ttu-id="2c220-103">Tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2c220-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c220-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c220-104">SYNTAX</span></span>

### <span data-ttu-id="2c220-105">SetByResourceSubnet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2c220-105">SetByResourceSubnet (Default)</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c220-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="2c220-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-Zone <System.Collections.Generic.List`1[System.String]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c220-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c220-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c220-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c220-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c220-109">Opis</span><span class="sxs-lookup"><span data-stu-id="2c220-109">DESCRIPTION</span></span>
<span data-ttu-id="2c220-110">Polecenie cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** tworzy konfigurację frontonu IP dla modułu równoważenia obciążenia platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2c220-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="2c220-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c220-111">EXAMPLES</span></span>

### <span data-ttu-id="2c220-112">Przykład 1. Tworzenie zewnętrznej konfiguracji adresów IP dla modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="2c220-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="2c220-113">Pierwsze polecenie tworzy dynamiczny publiczny adres IP o nazwie MyPublicIP w grupie zasób o nazwie moja grupa, a następnie zapisuje go w zmiennej $publicip.</span><span class="sxs-lookup"><span data-stu-id="2c220-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="2c220-114">Drugie polecenie tworzy konfigurację adresu IP frontonu o nazwie FrontendIpConfig01 przy użyciu publicznego adresu IP w $publicip.</span><span class="sxs-lookup"><span data-stu-id="2c220-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="2c220-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c220-115">PARAMETERS</span></span>

### <span data-ttu-id="2c220-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c220-116">-DefaultProfile</span></span>
<span data-ttu-id="2c220-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c220-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c220-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c220-118">-Name</span></span>
<span data-ttu-id="2c220-119">Określa konfigurację adresu IP frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c220-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2c220-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c220-120">-PrivateIpAddress</span></span>
<span data-ttu-id="2c220-121">Określa prywatny adres IP modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="2c220-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="2c220-122">Ten parametr należy określić tylko wtedy, gdy jest określany również parametr *Subnet* .</span><span class="sxs-lookup"><span data-stu-id="2c220-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c220-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c220-123">-PublicIpAddress</span></span>
<span data-ttu-id="2c220-124">Określa obiekt **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="2c220-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c220-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="2c220-125">-PublicIpAddressId</span></span>
<span data-ttu-id="2c220-126">Określa identyfikator obiektu **PublicIpAddress** , który ma zostać skojarzony z konfiguracją adresu IP frontonu.</span><span class="sxs-lookup"><span data-stu-id="2c220-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c220-127">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="2c220-127">-Subnet</span></span>
<span data-ttu-id="2c220-128">Określa obiekt **podsieci** , w którym ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="2c220-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c220-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="2c220-129">-SubnetId</span></span>
<span data-ttu-id="2c220-130">Określa identyfikator podsieci, w której ma zostać utworzona konfiguracja frontonu IP.</span><span class="sxs-lookup"><span data-stu-id="2c220-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c220-131">-Zone</span><span class="sxs-lookup"><span data-stu-id="2c220-131">-Zone</span></span>
<span data-ttu-id="2c220-132">Lista stref dostępności oznaczająca adres IP przydzielony dla zasobu musi pochodzić od.</span><span class="sxs-lookup"><span data-stu-id="2c220-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="2c220-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c220-133">-Confirm</span></span>
<span data-ttu-id="2c220-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c220-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c220-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c220-135">-WhatIf</span></span>
<span data-ttu-id="2c220-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c220-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c220-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c220-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c220-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c220-138">CommonParameters</span></span>
<span data-ttu-id="2c220-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c220-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c220-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c220-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c220-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c220-141">INPUTS</span></span>

### <span data-ttu-id="2c220-142">System. Collections. Generic. list \` 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2c220-142">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2c220-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c220-143">OUTPUTS</span></span>

### <span data-ttu-id="2c220-144">Microsoft. Azure. Commands. Network. models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c220-144">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="2c220-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c220-145">NOTES</span></span>

## <span data-ttu-id="2c220-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c220-146">RELATED LINKS</span></span>

[<span data-ttu-id="2c220-147">Dodaj-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c220-147">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2c220-148">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c220-148">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2c220-149">Nowe — AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="2c220-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="2c220-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c220-150">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="2c220-151">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="2c220-151">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


