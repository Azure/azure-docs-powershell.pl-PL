---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220541"
---
# <span data-ttu-id="6a22b-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="6a22b-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="6a22b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a22b-102">SYNOPSIS</span></span>
<span data-ttu-id="6a22b-103">Tworzy nowy IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="6a22b-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="6a22b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a22b-104">SYNTAX</span></span>

### <span data-ttu-id="6a22b-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="6a22b-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="6a22b-106">Opis</span><span class="sxs-lookup"><span data-stu-id="6a22b-106">DESCRIPTION</span></span>
<span data-ttu-id="6a22b-107">**Nowy — AzIpConfigurationBgpPeeringAddressObject** tworzy obiekt IpConfigurationBgpPeeringAddressObject reprezentujący właściwość BgpPeeringAddresses w bramy sieci wirtualnej bgpsettings.</span><span class="sxs-lookup"><span data-stu-id="6a22b-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="6a22b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a22b-108">EXAMPLES</span></span>

### <span data-ttu-id="6a22b-109">1: Tworzenie AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="6a22b-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="6a22b-110">Powyższy element utworzy IpConfigurationBgpPeeringAddressObject. ten nowy obiekt będzie gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="6a22b-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="6a22b-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a22b-111">PARAMETERS</span></span>

### <span data-ttu-id="6a22b-112">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a22b-112">-Confirm</span></span>
<span data-ttu-id="6a22b-113">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a22b-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a22b-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="6a22b-114">-CustomAddress</span></span>
<span data-ttu-id="6a22b-115">Lista CustomAddress bramy sieci wirtualnej dla BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="6a22b-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a22b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a22b-116">-DefaultProfile</span></span>
<span data-ttu-id="6a22b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a22b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a22b-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6a22b-118">-IpConfigurationId</span></span>
<span data-ttu-id="6a22b-119">Brama sieci wirtualnej IpConfigurationId dla BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="6a22b-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="6a22b-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a22b-120">-WhatIf</span></span>
<span data-ttu-id="6a22b-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a22b-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a22b-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a22b-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a22b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a22b-123">CommonParameters</span></span>
<span data-ttu-id="6a22b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a22b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a22b-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a22b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a22b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a22b-126">INPUTS</span></span>

### <span data-ttu-id="6a22b-127">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6a22b-127">None</span></span>

## <span data-ttu-id="6a22b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a22b-128">OUTPUTS</span></span>

### <span data-ttu-id="6a22b-129">Microsoft. Azure. Commands. Network. models. PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="6a22b-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="6a22b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a22b-130">NOTES</span></span>

## <span data-ttu-id="6a22b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a22b-131">RELATED LINKS</span></span>
