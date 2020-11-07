---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 1B39809C-90DA-4ECB-B949-D4A9A54ED982
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkinterfaceipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkInterfaceIpConfig.md
ms.openlocfilehash: 5936a7e3f15919e00fa052a2950fd31e69ca32fd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890757"
---
# <span data-ttu-id="dc117-101">Get-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc117-101">Get-AzNetworkInterfaceIpConfig</span></span>

## <span data-ttu-id="dc117-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc117-102">SYNOPSIS</span></span>
<span data-ttu-id="dc117-103">Pobiera konfigurację adresu IP interfejsu sieciowego dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="dc117-103">Gets a network interface IP configuration for a network interface.</span></span>

## <span data-ttu-id="dc117-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc117-104">SYNTAX</span></span>

```
Get-AzNetworkInterfaceIpConfig [-Name <String>] -NetworkInterface <PSNetworkInterface>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc117-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc117-105">DESCRIPTION</span></span>
<span data-ttu-id="dc117-106">Polecenie cmdlet **Get-AzNetworkInterfaceIPConfig** Pobiera konfigurację adresu IP interfejsu sieciowego z interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dc117-106">The **Get-AzNetworkInterfaceIPConfig** cmdlet gets a network interface IP configuration from an Azure network interface.</span></span>

## <span data-ttu-id="dc117-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc117-107">EXAMPLES</span></span>

### <span data-ttu-id="dc117-108">1: Uzyskiwanie konfiguracji IP interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="dc117-108">1: Get an IP configuration of a network interface</span></span>
```
$nic1 = Get-AzNetworkInterface -Name mynic -ResourceGroupName $myrg
Get-AzNetworkInterfaceIpConfig -Name ipconfig1 -NetworkInterface $nic1
```

<span data-ttu-id="dc117-109">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie mynic i zapisuje go w zmiennej $nic 1.</span><span class="sxs-lookup"><span data-stu-id="dc117-109">The first command gets an existing network interface called mynic and stores it in the variable $nic1.</span></span> <span data-ttu-id="dc117-110">Drugie polecenie pobiera konfigurację IP o nazwie ipconfig1 tego interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="dc117-110">The second command gets the IP configuration called ipconfig1 of this network interface.</span></span>
    

## <span data-ttu-id="dc117-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc117-111">PARAMETERS</span></span>

### <span data-ttu-id="dc117-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc117-112">-DefaultProfile</span></span>
<span data-ttu-id="dc117-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dc117-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc117-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc117-114">-Name</span></span>
<span data-ttu-id="dc117-115">Określa nazwę konfiguracji sieci IP, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc117-115">Specifies the name of the network IP configuration that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc117-116">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dc117-116">-NetworkInterface</span></span>
<span data-ttu-id="dc117-117">Określa obiekt **NetworkInterface** , który zawiera konfigurację adresu IP sieci, która jest pobierana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc117-117">Specifies a **NetworkInterface** object that contains the network IP configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dc117-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc117-118">CommonParameters</span></span>
<span data-ttu-id="dc117-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc117-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc117-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc117-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc117-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc117-121">INPUTS</span></span>

### <span data-ttu-id="dc117-122">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="dc117-122">PSNetworkInterface</span></span>
<span data-ttu-id="dc117-123">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="dc117-123">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="dc117-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc117-124">OUTPUTS</span></span>

### <span data-ttu-id="dc117-125">Microsoft. Azure. Commands. Network. models. PSNetworkInterfaceIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="dc117-125">Microsoft.Azure.Commands.Network.Models.PSNetworkInterfaceIPConfiguration</span></span>

## <span data-ttu-id="dc117-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc117-126">NOTES</span></span>
* <span data-ttu-id="dc117-127">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, Network, Networking</span><span class="sxs-lookup"><span data-stu-id="dc117-127">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="dc117-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc117-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc117-129">Dodaj-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc117-129">Add-AzNetworkInterfaceIpConfig</span></span>](./Add-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dc117-130">Nowe — AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc117-130">New-AzNetworkInterfaceIpConfig</span></span>](./New-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dc117-131">Remove-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc117-131">Remove-AzNetworkInterfaceIpConfig</span></span>](./Remove-AzNetworkInterfaceIpConfig.md)

[<span data-ttu-id="dc117-132">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dc117-132">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)


