---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: abeeabcc3930a2f18822dbf3d9986e17fbc01c88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993644"
---
# <span data-ttu-id="e5ff6-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5ff6-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="e5ff6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5ff6-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ff6-103">Usuwa konfigurację protokołu IP interfejsu sieciowego z interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="e5ff6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e5ff6-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5ff6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e5ff6-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ff6-106">Polecenie **cmdlet Remove-AzNetworkInterfaceIpConfig** usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="e5ff6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e5ff6-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ff6-108">Przykład 1. Usuwanie konfiguracji protokołu IP z interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="e5ff6-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="e5ff6-109">Pierwsze polecenie otrzymuje interfejs sieciowy o nazwie mynic i przechowuje je w zmiennym $nic.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="e5ff6-110">Drugie polecenie usuwa konfigurację protokołu IP o nazwie IPConfig-1 skojarzoną z tym interfejsem sieciowym.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="e5ff6-111">Trzecie polecenie ustawia zmiany wprowadzone w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="e5ff6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e5ff6-112">PARAMETERS</span></span>

### <span data-ttu-id="e5ff6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ff6-113">-DefaultProfile</span></span>
<span data-ttu-id="e5ff6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e5ff6-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e5ff6-115">-Name</span></span>
<span data-ttu-id="e5ff6-116">Określa nazwę konfiguracji protokołu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="e5ff6-117">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e5ff6-117">-NetworkInterface</span></span>
<span data-ttu-id="e5ff6-118">Określa **obiekt NetworkInterface.**</span><span class="sxs-lookup"><span data-stu-id="e5ff6-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="e5ff6-119">Ten obiekt zawiera konfigurację adresu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="e5ff6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ff6-120">CommonParameters</span></span>
<span data-ttu-id="e5ff6-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ff6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ff6-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ff6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ff6-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5ff6-123">INPUTS</span></span>

### <span data-ttu-id="e5ff6-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e5ff6-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e5ff6-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5ff6-125">OUTPUTS</span></span>

### <span data-ttu-id="e5ff6-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e5ff6-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="e5ff6-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e5ff6-127">NOTES</span></span>
* <span data-ttu-id="e5ff6-128">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="e5ff6-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="e5ff6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5ff6-129">RELATED LINKS</span></span>

[<span data-ttu-id="e5ff6-130">Add-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5ff6-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e5ff6-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5ff6-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e5ff6-132">New-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5ff6-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="e5ff6-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="e5ff6-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


