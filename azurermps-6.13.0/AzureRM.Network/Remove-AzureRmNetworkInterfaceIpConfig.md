---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: c912d32c39380ee3d653fa228632a4d01f0e3049
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545039"
---
# <span data-ttu-id="cfb70-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfb70-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="cfb70-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cfb70-102">SYNOPSIS</span></span>
<span data-ttu-id="cfb70-103">Usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="cfb70-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfb70-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cfb70-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfb70-105">Opis</span><span class="sxs-lookup"><span data-stu-id="cfb70-105">DESCRIPTION</span></span>
<span data-ttu-id="cfb70-106">Polecenie cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb70-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="cfb70-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cfb70-107">EXAMPLES</span></span>

### <span data-ttu-id="cfb70-108">1: Usuwanie konfiguracji adresów IP z interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="cfb70-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="cfb70-109">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="cfb70-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="cfb70-110">Drugie polecenie usuwa konfigurację IP o nazwie IPConfig-1 skojarzoną z tym interfejsem sieciowym.</span><span class="sxs-lookup"><span data-stu-id="cfb70-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="cfb70-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cfb70-111">PARAMETERS</span></span>

### <span data-ttu-id="cfb70-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfb70-112">-DefaultProfile</span></span>
<span data-ttu-id="cfb70-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cfb70-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfb70-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cfb70-114">-Name</span></span>
<span data-ttu-id="cfb70-115">Określa nazwę konfiguracji IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cfb70-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="cfb70-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cfb70-116">-NetworkInterface</span></span>
<span data-ttu-id="cfb70-117">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="cfb70-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="cfb70-118">Ten obiekt zawiera konfigurację adresu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="cfb70-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="cfb70-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfb70-119">CommonParameters</span></span>
<span data-ttu-id="cfb70-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfb70-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfb70-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfb70-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfb70-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cfb70-122">INPUTS</span></span>

### <span data-ttu-id="cfb70-123">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cfb70-123">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>
<span data-ttu-id="cfb70-124">Parametry: NetworkInterface (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cfb70-124">Parameters: NetworkInterface (ByValue)</span></span>

## <span data-ttu-id="cfb70-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cfb70-125">OUTPUTS</span></span>

### <span data-ttu-id="cfb70-126">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="cfb70-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="cfb70-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cfb70-127">NOTES</span></span>
* <span data-ttu-id="cfb70-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="cfb70-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cfb70-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cfb70-129">RELATED LINKS</span></span>

[<span data-ttu-id="cfb70-130">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfb70-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cfb70-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfb70-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cfb70-132">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfb70-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="cfb70-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="cfb70-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


