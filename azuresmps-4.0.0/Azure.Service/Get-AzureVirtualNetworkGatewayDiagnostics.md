---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: F6A89D39-18AD-4087-823C-63FA0A3690E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36c51d0ceae42aab50e2df9e0532c98dd6800747
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055486"
---
# <span data-ttu-id="46d6b-101">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="46d6b-101">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="46d6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="46d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="46d6b-103">Pobiera wyniki diagnostyki bramy sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="46d6b-103">Gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="46d6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="46d6b-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="46d6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="46d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="46d6b-106">Polecenie cmdlet **Get-AzureVirtualNetworkGatewayDiagnostics** pobiera wyniki diagnostyki bramy usługi Azure Virtual Network.</span><span class="sxs-lookup"><span data-stu-id="46d6b-106">The **Get-AzureVirtualNetworkGatewayDiagnostics** cmdlet gets the results of Azure virtual network gateway diagnostics.</span></span>

## <span data-ttu-id="46d6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="46d6b-107">EXAMPLES</span></span>

## <span data-ttu-id="46d6b-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="46d6b-108">PARAMETERS</span></span>

### <span data-ttu-id="46d6b-109">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="46d6b-109">-GatewayId</span></span>
<span data-ttu-id="46d6b-110">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="46d6b-110">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="46d6b-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="46d6b-111">-Profile</span></span>
<span data-ttu-id="46d6b-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46d6b-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="46d6b-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="46d6b-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="46d6b-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46d6b-114">CommonParameters</span></span>
<span data-ttu-id="46d6b-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46d6b-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46d6b-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46d6b-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46d6b-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46d6b-117">INPUTS</span></span>

## <span data-ttu-id="46d6b-118">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="46d6b-118">OUTPUTS</span></span>

## <span data-ttu-id="46d6b-119">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="46d6b-119">NOTES</span></span>

## <span data-ttu-id="46d6b-120">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46d6b-120">RELATED LINKS</span></span>

[<span data-ttu-id="46d6b-121">Start — AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="46d6b-121">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="46d6b-122">Zatrzymaj — AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="46d6b-122">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Stop-AzureVirtualNetworkGatewayDiagnostics.md)


