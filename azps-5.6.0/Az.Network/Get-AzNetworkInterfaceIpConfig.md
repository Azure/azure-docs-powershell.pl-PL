---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 572ea4aac029068e3b7e4fbcf12f3b240129d585
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006346"
---
# <span data-ttu-id="f4ab5-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ab5-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="f4ab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ab5-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ab5-103">Pobiera konfigurację adresu IP interfejsu sieciowego dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="f4ab5-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f4ab5-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4ab5-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f4ab5-105">DESCRIPTION</span></span>
<span data-ttu-id="f4ab5-106">Polecenie **cmdlet Get-AzNetworkInterfaceIPConfig** pobiera konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="f4ab5-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f4ab5-107">EXAMPLES</span></span>

### <span data-ttu-id="f4ab5-108">1. Uzyskiwanie konfiguracji protokołu IP interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="f4ab5-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="f4ab5-109">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie mynic i przechowuje je w zmiennej $nic 1.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="f4ab5-110">Drugie polecenie pobiera konfigurację protokołu IP o nazwie ipconfig1 tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="f4ab5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f4ab5-111">PARAMETERS</span></span>

### <span data-ttu-id="f4ab5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ab5-112">-DefaultProfile</span></span>
<span data-ttu-id="f4ab5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ab5-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f4ab5-114">-Name</span></span>
<span data-ttu-id="f4ab5-115">Określa nazwę konfiguracji sieciowego adresu IP, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4ab5-116">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f4ab5-116">-NetworkInterface</span></span>
<span data-ttu-id="f4ab5-117">Określa obiekt **NetworkInterface** zawierający konfigurację adresu IP sieci, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f4ab5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ab5-118">CommonParameters</span></span>
<span data-ttu-id="f4ab5-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4ab5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ab5-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f4ab5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ab5-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ab5-121">INPUTS</span></span>

### <span data-ttu-id="f4ab5-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="f4ab5-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="f4ab5-123">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4ab5-123">OUTPUTS</span></span>

### <span data-ttu-id="f4ab5-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="f4ab5-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="f4ab5-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f4ab5-125">NOTES</span></span>
* <span data-ttu-id="f4ab5-126">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="f4ab5-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="f4ab5-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4ab5-127">RELATED LINKS</span></span>

[<span data-ttu-id="f4ab5-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ab5-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f4ab5-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ab5-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f4ab5-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ab5-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="f4ab5-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="f4ab5-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


