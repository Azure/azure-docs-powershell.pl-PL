---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: eac8a985cfcb531247fcf2617fee86da92ea0112
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554274"
---
# <span data-ttu-id="e2ecd-101">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2ecd-101">Get-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e2ecd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e2ecd-102">SYNOPSIS</span></span>
<span data-ttu-id="e2ecd-103">Pobiera konfigurację adresu IP interfejsu sieciowego dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-103">Gets a network interface IP configuration for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e2ecd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e2ecd-104">SYNTAX</span></span>

```
Get-AzureRmNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e2ecd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e2ecd-105">DESCRIPTION</span></span>
<span data-ttu-id="e2ecd-106">Polecenie cmdlet **Get-AzureRmNetworkInterfaceIPConfig** Pobiera konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-106">The **Get-AzureRmNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="e2ecd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e2ecd-107">EXAMPLES</span></span>

### <span data-ttu-id="e2ecd-108">1: Uzyskiwanie konfiguracji IP interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="e2ecd-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzureRmNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="e2ecd-109">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic 1.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="e2ecd-110">Drugie polecenie pobiera konfigurację IP o nazwie ipconfig1 tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="e2ecd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e2ecd-111">PARAMETERS</span></span>

### <span data-ttu-id="e2ecd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2ecd-112">-DefaultProfile</span></span>
<span data-ttu-id="e2ecd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e2ecd-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e2ecd-114">-Name</span></span>
<span data-ttu-id="e2ecd-115">Określa nazwę konfiguracji sieci IP, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2ecd-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2ecd-116">-NetworkInterface</span></span>
<span data-ttu-id="e2ecd-117">Określa obiekt **NetworkInterface** , który zawiera konfigurację adresu IP sieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="e2ecd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2ecd-118">CommonParameters</span></span>
<span data-ttu-id="e2ecd-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2ecd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2ecd-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2ecd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2ecd-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e2ecd-121">INPUTS</span></span>

### <span data-ttu-id="e2ecd-122">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e2ecd-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="e2ecd-123">Parametry: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e2ecd-123">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="e2ecd-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e2ecd-124">OUTPUTS</span></span>

### <span data-ttu-id="e2ecd-125">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="e2ecd-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="e2ecd-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e2ecd-126">NOTES</span></span>
* <span data-ttu-id="e2ecd-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="e2ecd-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e2ecd-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e2ecd-128">RELATED LINKS</span></span>

[<span data-ttu-id="e2ecd-129">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2ecd-129">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e2ecd-130">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2ecd-130">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e2ecd-131">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2ecd-131">Remove-AzureRmNetworkInterfaceIpConfig</span></span>](./Remove-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e2ecd-132">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e2ecd-132">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)

