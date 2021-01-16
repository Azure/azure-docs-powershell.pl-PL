---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380037"
---
# <span data-ttu-id="c11cb-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c11cb-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="c11cb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c11cb-102">SYNOPSIS</span></span>
<span data-ttu-id="c11cb-103">Pobiera konfigurację adresu IP interfejsu sieciowego dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c11cb-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="c11cb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c11cb-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c11cb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c11cb-105">DESCRIPTION</span></span>
<span data-ttu-id="c11cb-106">Polecenie cmdlet **Get-AzNetworkInterfaceIPConfig** Pobiera konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c11cb-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="c11cb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c11cb-107">EXAMPLES</span></span>

### <span data-ttu-id="c11cb-108">1: Uzyskiwanie konfiguracji IP interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="c11cb-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="c11cb-109">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic 1.</span><span class="sxs-lookup"><span data-stu-id="c11cb-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="c11cb-110">Drugie polecenie pobiera konfigurację IP o nazwie ipconfig1 tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c11cb-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="c11cb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c11cb-111">PARAMETERS</span></span>

### <span data-ttu-id="c11cb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c11cb-112">-DefaultProfile</span></span>
<span data-ttu-id="c11cb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c11cb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c11cb-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c11cb-114">-Name</span></span>
<span data-ttu-id="c11cb-115">Określa nazwę konfiguracji sieci IP, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c11cb-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c11cb-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c11cb-116">-NetworkInterface</span></span>
<span data-ttu-id="c11cb-117">Określa obiekt **NetworkInterface** , który zawiera konfigurację adresu IP sieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c11cb-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c11cb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c11cb-118">CommonParameters</span></span>
<span data-ttu-id="c11cb-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c11cb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c11cb-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c11cb-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c11cb-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c11cb-121">INPUTS</span></span>

### <span data-ttu-id="c11cb-122">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c11cb-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c11cb-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c11cb-123">OUTPUTS</span></span>

### <span data-ttu-id="c11cb-124">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="c11cb-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="c11cb-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c11cb-125">NOTES</span></span>
* <span data-ttu-id="c11cb-126">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="c11cb-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c11cb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c11cb-127">RELATED LINKS</span></span>

[<span data-ttu-id="c11cb-128">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c11cb-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c11cb-129">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c11cb-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c11cb-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c11cb-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c11cb-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c11cb-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


