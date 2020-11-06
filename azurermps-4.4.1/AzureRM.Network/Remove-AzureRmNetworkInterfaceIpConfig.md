---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkInterfaceIpConfig.md
ms.openlocfilehash: 8afc90c8709869a9acf3464c4ad39bdbc2b3ab5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525485"
---
# <span data-ttu-id="c72c5-101">Remove-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c72c5-101">Remove-AzureRmNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="c72c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c72c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c72c5-103">Usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="c72c5-103">Removes a network interface IP configuration from a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c72c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c72c5-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c72c5-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c72c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c72c5-106">Polecenie cmdlet **Remove-AzureRmNetworkInterfaceIpConfig** usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c72c5-106">The **Remove-AzureRmNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="c72c5-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c72c5-107">EXAMPLES</span></span>

### <span data-ttu-id="c72c5-108">1: Usuwanie konfiguracji adresów IP z interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="c72c5-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzureRmNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="c72c5-109">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="c72c5-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="c72c5-110">Drugie polecenie usuwa konfigurację IP o nazwie IPConfig-1 skojarzoną z tym interfejsem sieciowym.</span><span class="sxs-lookup"><span data-stu-id="c72c5-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="c72c5-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c72c5-111">PARAMETERS</span></span>

### <span data-ttu-id="c72c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c72c5-112">-DefaultProfile</span></span>
<span data-ttu-id="c72c5-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c72c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c72c5-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c72c5-114">-Name</span></span>
<span data-ttu-id="c72c5-115">Określa nazwę konfiguracji IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c72c5-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="c72c5-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c72c5-116">-NetworkInterface</span></span>
<span data-ttu-id="c72c5-117">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="c72c5-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="c72c5-118">Ten obiekt zawiera konfigurację adresu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="c72c5-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="c72c5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c72c5-119">CommonParameters</span></span>
<span data-ttu-id="c72c5-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c72c5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c72c5-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c72c5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c72c5-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c72c5-122">INPUTS</span></span>

### <span data-ttu-id="c72c5-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c72c5-123">PSNetworkInterface</span></span>
<span data-ttu-id="c72c5-124">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="c72c5-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="c72c5-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c72c5-125">OUTPUTS</span></span>

### <span data-ttu-id="c72c5-126">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="c72c5-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="c72c5-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c72c5-127">NOTES</span></span>
* <span data-ttu-id="c72c5-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="c72c5-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="c72c5-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c72c5-129">RELATED LINKS</span></span>

[<span data-ttu-id="c72c5-130">Dodaj-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c72c5-130">Add-AzureRmNetworkInterfaceIpConfig</span></span>](./Add-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c72c5-131">Get-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c72c5-131">Get-AzureRmNetworkInterfaceIpConfig</span></span>](./Get-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c72c5-132">Nowe — AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c72c5-132">New-AzureRmNetworkInterfaceIpConfig</span></span>](./New-AzureRmNetworkInterfaceIpConfig.md)

[<span data-ttu-id="c72c5-133">Set-AzureRmNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="c72c5-133">Set-AzureRmNetworkInterfaceIpConfig</span></span>](./Set-AzureRmNetworkInterfaceIpConfig.md)


