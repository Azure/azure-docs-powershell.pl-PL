---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 425008DB-9761-42F1-8D6D-F35757A3CA6C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37aa0718c4faa637b16ccde61f5e5b241bb9aa92
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055481"
---
# <span data-ttu-id="0db9e-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0db9e-101">Get-AzureVirtualNetworkGatewayIPsecParameters</span></span>

## <span data-ttu-id="0db9e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0db9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0db9e-103">Pobiera parametry protokołu IPsec dla bramy sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0db9e-103">Gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="0db9e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0db9e-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayIPsecParameters -GatewayId <String> -ConnectedEntityId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0db9e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0db9e-105">DESCRIPTION</span></span>
<span data-ttu-id="0db9e-106">Polecenie cmdlet **Get-AzureVirtualNetworkGatewayIPsecParameters** pobiera parametry protokołu IPSec dla bramy wirtualnej sieci Azure.</span><span class="sxs-lookup"><span data-stu-id="0db9e-106">The **Get-AzureVirtualNetworkGatewayIPsecParameters** cmdlet gets the IPsec parameters for an Azure virtual network gateway.</span></span>

## <span data-ttu-id="0db9e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0db9e-107">EXAMPLES</span></span>

## <span data-ttu-id="0db9e-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0db9e-108">PARAMETERS</span></span>

### <span data-ttu-id="0db9e-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="0db9e-109">-ConnectedEntityId</span></span>
<span data-ttu-id="0db9e-110">Określa identyfikator połączonej entitiy.</span><span class="sxs-lookup"><span data-stu-id="0db9e-110">Specifies the ID of a connected entitiy.</span></span>

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

### <span data-ttu-id="0db9e-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="0db9e-111">-GatewayId</span></span>
<span data-ttu-id="0db9e-112">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="0db9e-112">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="0db9e-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="0db9e-113">-Profile</span></span>
<span data-ttu-id="0db9e-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0db9e-114">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="0db9e-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0db9e-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0db9e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db9e-116">CommonParameters</span></span>
<span data-ttu-id="0db9e-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0db9e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db9e-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db9e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db9e-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0db9e-119">INPUTS</span></span>

## <span data-ttu-id="0db9e-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0db9e-120">OUTPUTS</span></span>

## <span data-ttu-id="0db9e-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0db9e-121">NOTES</span></span>

## <span data-ttu-id="0db9e-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0db9e-122">RELATED LINKS</span></span>

[<span data-ttu-id="0db9e-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="0db9e-123">Set-AzureVirtualNetworkGatewayIPsecParameters</span></span>](./Set-AzureVirtualNetworkGatewayIPsecParameters.md)


