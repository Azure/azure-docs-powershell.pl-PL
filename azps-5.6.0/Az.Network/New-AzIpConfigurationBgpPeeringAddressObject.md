---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: ba713650670abdeb9c64242109b30f47d99724f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001105"
---
# <span data-ttu-id="e2b09-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="e2b09-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="e2b09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2b09-102">SYNOPSIS</span></span>
<span data-ttu-id="e2b09-103">tworzy nową konfigurację IpconfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="e2b09-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="e2b09-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e2b09-104">SYNTAX</span></span>

### <span data-ttu-id="e2b09-105">Domyślne (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e2b09-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="e2b09-106">OPIS</span><span class="sxs-lookup"><span data-stu-id="e2b09-106">DESCRIPTION</span></span>
<span data-ttu-id="e2b09-107">**New-AzIpConfigurationBgpPeeringAddressObject** tworzy obiekt IpConfigurationBgpPeeringAddressObject, który reprezentuje właściwość BgpPeeringAddresses w twoich bgpsettings bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e2b09-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="e2b09-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e2b09-108">EXAMPLES</span></span>

### <span data-ttu-id="e2b09-109">1. Tworzenie elementu AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="e2b09-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="e2b09-110">Powyższe spowoduje utworzenie obiektu IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="e2b09-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="e2b09-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e2b09-111">PARAMETERS</span></span>

### <span data-ttu-id="e2b09-112">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e2b09-112">-Confirm</span></span>
<span data-ttu-id="e2b09-113">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e2b09-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2b09-114">- CustomAddress</span><span class="sxs-lookup"><span data-stu-id="e2b09-114">-CustomAddress</span></span>
<span data-ttu-id="e2b09-115">Lista customAddress bramy sieci wirtualnej dla adresów BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="e2b09-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="e2b09-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2b09-116">-DefaultProfile</span></span>
<span data-ttu-id="e2b09-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2b09-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2b09-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="e2b09-118">-IpConfigurationId</span></span>
<span data-ttu-id="e2b09-119">Wirtualna brama sieciowa IpConfigurationId for BgpPeeringAddresses.</span><span class="sxs-lookup"><span data-stu-id="e2b09-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="e2b09-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2b09-120">-WhatIf</span></span>
<span data-ttu-id="e2b09-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2b09-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2b09-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e2b09-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2b09-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2b09-123">CommonParameters</span></span>
<span data-ttu-id="e2b09-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2b09-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2b09-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2b09-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2b09-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2b09-126">INPUTS</span></span>

### <span data-ttu-id="e2b09-127">Brak</span><span class="sxs-lookup"><span data-stu-id="e2b09-127">None</span></span>

## <span data-ttu-id="e2b09-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2b09-128">OUTPUTS</span></span>

### <span data-ttu-id="e2b09-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="e2b09-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="e2b09-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e2b09-130">NOTES</span></span>

## <span data-ttu-id="e2b09-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2b09-131">RELATED LINKS</span></span>
