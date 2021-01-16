---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2aa9792c632a7e615091a69182c87bc06b565c18
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333478"
---
# <span data-ttu-id="cebe6-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cebe6-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="cebe6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cebe6-102">SYNOPSIS</span></span>
<span data-ttu-id="cebe6-103">Usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="cebe6-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="cebe6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cebe6-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cebe6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cebe6-105">DESCRIPTION</span></span>
<span data-ttu-id="cebe6-106">Polecenie cmdlet **Remove-AzNetworkInterfaceIpConfig** usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cebe6-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="cebe6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cebe6-107">EXAMPLES</span></span>

### <span data-ttu-id="cebe6-108">Przykład 1: Usuwanie konfiguracji adresów IP z interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="cebe6-108">Example 1: Delete an IP configuration from a network interface</span></span>
```powershell
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic

Set-AzNetworkInterface -NetworkInterface $nic
```

<span data-ttu-id="cebe6-109">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="cebe6-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="cebe6-110">Drugie polecenie usuwa konfigurację IP o nazwie IPConfig-1 skojarzoną z tym interfejsem sieciowym.</span><span class="sxs-lookup"><span data-stu-id="cebe6-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span> <span data-ttu-id="cebe6-111">Trzy polecenia ustawiają zmiany wprowadzone w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="cebe6-111">The third command sets changes made to the network interface.</span></span>

## <span data-ttu-id="cebe6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cebe6-112">PARAMETERS</span></span>

### <span data-ttu-id="cebe6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cebe6-113">-DefaultProfile</span></span>
<span data-ttu-id="cebe6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cebe6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cebe6-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cebe6-115">-Name</span></span>
<span data-ttu-id="cebe6-116">Określa nazwę konfiguracji IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cebe6-116">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="cebe6-117">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cebe6-117">-NetworkInterface</span></span>
<span data-ttu-id="cebe6-118">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="cebe6-118">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="cebe6-119">Ten obiekt zawiera konfigurację adresu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cebe6-119">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="cebe6-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cebe6-120">CommonParameters</span></span>
<span data-ttu-id="cebe6-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cebe6-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cebe6-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cebe6-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cebe6-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cebe6-123">INPUTS</span></span>

### <span data-ttu-id="cebe6-124">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cebe6-124">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cebe6-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cebe6-125">OUTPUTS</span></span>

### <span data-ttu-id="cebe6-126">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cebe6-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cebe6-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cebe6-127">NOTES</span></span>
* <span data-ttu-id="cebe6-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="cebe6-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cebe6-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cebe6-129">RELATED LINKS</span></span>

[<span data-ttu-id="cebe6-130">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cebe6-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cebe6-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cebe6-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cebe6-132">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cebe6-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cebe6-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cebe6-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


