---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 015C7DB7-2B08-4033-9B6E-1738D4DDACDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 2ccb5f7117df8f959698c894915cedd3a5d4c7e2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890278"
---
# <span data-ttu-id="d10cd-101">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d10cd-101">Remove-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="d10cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d10cd-102">SYNOPSIS</span></span>
<span data-ttu-id="d10cd-103">Usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="d10cd-103">Removes a network interface IP configuration from a network interface.</span></span>

## <span data-ttu-id="d10cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d10cd-104">SYNTAX</span></span>

```
Remove-AzNetworkInterfaceIpConfig -Name <String> -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d10cd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d10cd-105">DESCRIPTION</span></span>
<span data-ttu-id="d10cd-106">Polecenie cmdlet **Remove-AzNetworkInterfaceIpConfig** usuwa konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d10cd-106">The **Remove-AzNetworkInterfaceIpConfig** cmdlet removes a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="d10cd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d10cd-107">EXAMPLES</span></span>

### <span data-ttu-id="d10cd-108">1: Usuwanie konfiguracji adresów IP z interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="d10cd-108">1: Delete an IP configuration from a network interface</span></span>
```
$nic = Get-AzNetworkInterface -Name mynic -ResourceGroupName myrg

Remove-AzNetworkInterfaceIpConfig -Name IPConfig-1 -NetworkInterface $nic
```

<span data-ttu-id="d10cd-109">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="d10cd-109">The first command gets a network interface called mynic and stores it in the variable $nic.</span></span> <span data-ttu-id="d10cd-110">Drugie polecenie usuwa konfigurację IP o nazwie IPConfig-1 skojarzoną z tym interfejsem sieciowym.</span><span class="sxs-lookup"><span data-stu-id="d10cd-110">The second command removes the IP configuration called IPConfig-1 associated with this network interface.</span></span>

## <span data-ttu-id="d10cd-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d10cd-111">PARAMETERS</span></span>

### <span data-ttu-id="d10cd-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10cd-112">-DefaultProfile</span></span>
<span data-ttu-id="d10cd-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d10cd-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d10cd-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d10cd-114">-Name</span></span>
<span data-ttu-id="d10cd-115">Określa nazwę konfiguracji IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d10cd-115">Specifies the name of the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="d10cd-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d10cd-116">-NetworkInterface</span></span>
<span data-ttu-id="d10cd-117">Określa obiekt **NetworkInterface** .</span><span class="sxs-lookup"><span data-stu-id="d10cd-117">Specifies a **NetworkInterface** object.</span></span>
<span data-ttu-id="d10cd-118">Ten obiekt zawiera konfigurację adresu IP interfejsu sieciowego do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="d10cd-118">This object contains the network interface IP configuration to remove.</span></span>

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

### <span data-ttu-id="d10cd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10cd-119">CommonParameters</span></span>
<span data-ttu-id="d10cd-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10cd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10cd-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10cd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10cd-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d10cd-122">INPUTS</span></span>

### <span data-ttu-id="d10cd-123">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d10cd-123">PSNetworkInterface</span></span>
<span data-ttu-id="d10cd-124">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="d10cd-124">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="d10cd-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d10cd-125">OUTPUTS</span></span>

### <span data-ttu-id="d10cd-126">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="d10cd-126">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="d10cd-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d10cd-127">NOTES</span></span>
* <span data-ttu-id="d10cd-128">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="d10cd-128">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="d10cd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d10cd-129">RELATED LINKS</span></span>

[<span data-ttu-id="d10cd-130">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d10cd-130">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d10cd-131">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d10cd-131">Get-AzNetworkInterfaceIpConfig</span></span>](./Get-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d10cd-132">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d10cd-132">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="d10cd-133">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="d10cd-133">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


