---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8152cf778cabed1c4a8a346ac86b708266058fc6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189738"
---
# <span data-ttu-id="87066-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="87066-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="87066-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87066-102">SYNOPSIS</span></span>
<span data-ttu-id="87066-103">Pobiera konfigurację adresu IP interfejsu sieciowego dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="87066-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="87066-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="87066-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87066-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="87066-105">DESCRIPTION</span></span>
<span data-ttu-id="87066-106">Polecenie **cmdlet Get-AzNetworkInterfaceIPConfig** pobiera konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="87066-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="87066-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="87066-107">EXAMPLES</span></span>

### <span data-ttu-id="87066-108">1. Uzyskiwanie konfiguracji protokołu IP interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="87066-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="87066-109">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie mynic i przechowuje je w zmiennej $nic 1.</span><span class="sxs-lookup"><span data-stu-id="87066-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="87066-110">Drugie polecenie pobiera konfigurację protokołu IP o nazwie ipconfig1 tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="87066-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="87066-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87066-111">PARAMETERS</span></span>

### <span data-ttu-id="87066-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87066-112">-DefaultProfile</span></span>
<span data-ttu-id="87066-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="87066-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87066-114">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="87066-114">-Name</span></span>
<span data-ttu-id="87066-115">Określa nazwę konfiguracji sieciowego adresu IP, która otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87066-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87066-116">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87066-116">-NetworkInterface</span></span>
<span data-ttu-id="87066-117">Określa obiekt **NetworkInterface** zawierający konfigurację adresu IP sieci, do których otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87066-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="87066-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87066-118">CommonParameters</span></span>
<span data-ttu-id="87066-119">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87066-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87066-120">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="87066-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87066-121">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87066-121">INPUTS</span></span>

### <span data-ttu-id="87066-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="87066-122">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="87066-123">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="87066-123">OUTPUTS</span></span>

### <span data-ttu-id="87066-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="87066-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="87066-125">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="87066-125">NOTES</span></span>
* <span data-ttu-id="87066-126">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="87066-126">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="87066-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87066-127">RELATED LINKS</span></span>

[<span data-ttu-id="87066-128">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="87066-128">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="87066-129">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="87066-129">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="87066-130">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="87066-130">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="87066-131">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="87066-131">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


