---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 9cbb814fde6d81449228a18913254cf807d5502c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526749"
---
# <span data-ttu-id="ccc04-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ccc04-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="ccc04-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccc04-102">SYNOPSIS</span></span>
<span data-ttu-id="ccc04-103">Usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="ccc04-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccc04-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccc04-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccc04-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ccc04-105">DESCRIPTION</span></span>
<span data-ttu-id="ccc04-106">Polecenie cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc04-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="ccc04-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccc04-107">EXAMPLES</span></span>

### <span data-ttu-id="ccc04-108">1: Usuwanie konfiguracji adresów IP z interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="ccc04-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="ccc04-109">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="ccc04-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="ccc04-110">Drugie polecenie usuwa konfigurację IP o nazwie IPConfig-1 skojarzoną z tym interfejsem sieciowym.</span><span class="sxs-lookup"><span data-stu-id="ccc04-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="ccc04-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccc04-111">PARAMETERS</span></span>

### <span data-ttu-id="ccc04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccc04-112">-DefaultProfile</span></span>
<span data-ttu-id="ccc04-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ccc04-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccc04-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ccc04-114">-Name</span></span>
<span data-ttu-id="ccc04-115">Określa nazwę konfiguracji IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ccc04-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="ccc04-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ccc04-116">-NetworkInterface</span></span>
<span data-ttu-id="ccc04-117">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="ccc04-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="ccc04-118">Ten obiekt zawiera konfigurację adresu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="ccc04-118">This object contains the network interface IP configuration to remove.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccc04-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccc04-119">CommonParameters</span></span>
<span data-ttu-id="ccc04-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccc04-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccc04-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccc04-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccc04-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccc04-122">INPUTS</span></span>

### <span data-ttu-id="ccc04-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ccc04-123">PSNetworkInterface</span></span>
<span data-ttu-id="ccc04-124">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="ccc04-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="ccc04-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccc04-125">OUTPUTS</span></span>

### <span data-ttu-id="ccc04-126">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="ccc04-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="ccc04-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccc04-127">NOTES</span></span>
* <span data-ttu-id="ccc04-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="ccc04-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ccc04-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccc04-129">RELATED LINKS</span></span>

[<span data-ttu-id="ccc04-130">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ccc04-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ccc04-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ccc04-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ccc04-132">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ccc04-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="ccc04-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="ccc04-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


