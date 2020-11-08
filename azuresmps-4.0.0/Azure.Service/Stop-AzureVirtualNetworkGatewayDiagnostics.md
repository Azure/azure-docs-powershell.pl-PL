---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9E7A170D-512A-4117-85C3-3AA4D6341C6B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 97fe847fd183caa7de281b358da579e8df4d5831
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054706"
---
# <span data-ttu-id="97b76-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="97b76-101">Stop-AzureVirtualNetworkGatewayDiagnostics</span></span>

## <span data-ttu-id="97b76-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97b76-102">SYNOPSIS</span></span>
<span data-ttu-id="97b76-103">Zatrzymuje uruchomioną sesję diagnostyczną bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97b76-103">Stops a running virtual network gateway diagnostics session.</span></span>

## <span data-ttu-id="97b76-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97b76-104">SYNTAX</span></span>

```
Stop-AzureVirtualNetworkGatewayDiagnostics -GatewayId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="97b76-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97b76-105">DESCRIPTION</span></span>
<span data-ttu-id="97b76-106">Polecenie cmdlet **stop-AzureVirtualNetworkGatewayDiagnostics** zatrzymuje uruchomioną sesję diagnostyki bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="97b76-106">The **Stop-AzureVirtualNetworkGatewayDiagnostics** cmdlet stops a running virtual network gateway diagnostics session.</span></span>
<span data-ttu-id="97b76-107">To polecenie zapisuje wyniki sesji diagnostycznej na koncie magazynu, które jest określone przez polecenie cmdlet Start-AzureVirtualNetworkGatewayDiagnostics.</span><span class="sxs-lookup"><span data-stu-id="97b76-107">This command saves the results of the diagnostics session to the storage account that the Start-AzureVirtualNetworkGatewayDiagnostics cmdlet specifies.</span></span>

## <span data-ttu-id="97b76-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97b76-108">EXAMPLES</span></span>

## <span data-ttu-id="97b76-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97b76-109">PARAMETERS</span></span>

### <span data-ttu-id="97b76-110">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="97b76-110">-GatewayId</span></span>
<span data-ttu-id="97b76-111">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="97b76-111">Specifies the ID of a gateway.</span></span>

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

### <span data-ttu-id="97b76-112">-Profile</span><span class="sxs-lookup"><span data-stu-id="97b76-112">-Profile</span></span>
<span data-ttu-id="97b76-113">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97b76-113">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="97b76-114">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="97b76-114">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97b76-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b76-115">CommonParameters</span></span>
<span data-ttu-id="97b76-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b76-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b76-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b76-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b76-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97b76-118">INPUTS</span></span>

## <span data-ttu-id="97b76-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97b76-119">OUTPUTS</span></span>

## <span data-ttu-id="97b76-120">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97b76-120">NOTES</span></span>

## <span data-ttu-id="97b76-121">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97b76-121">RELATED LINKS</span></span>

[<span data-ttu-id="97b76-122">Get-AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="97b76-122">Get-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Get-AzureVirtualNetworkGatewayDiagnostics.md)

[<span data-ttu-id="97b76-123">Start — AzureVirtualNetworkGatewayDiagnostics</span><span class="sxs-lookup"><span data-stu-id="97b76-123">Start-AzureVirtualNetworkGatewayDiagnostics</span></span>](./Start-AzureVirtualNetworkGatewayDiagnostics.md)


