---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 88AB3621-7C80-41BA-BE49-4F8F9C46BCF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fb0fa13cb5ea155b945505fd3f99c28494c5dc0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055489"
---
# <span data-ttu-id="34263-101">Get-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34263-101">Get-AzureVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="34263-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="34263-102">SYNOPSIS</span></span>
<span data-ttu-id="34263-103">Pobiera połączenie bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="34263-103">Gets a virtual network gateway connection.</span></span>

## <span data-ttu-id="34263-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="34263-104">SYNTAX</span></span>

```
Get-AzureVirtualNetworkGatewayConnection [-GatewayId <String>] [-ConnectedEntityId <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="34263-105">Opis</span><span class="sxs-lookup"><span data-stu-id="34263-105">DESCRIPTION</span></span>
<span data-ttu-id="34263-106">Polecenie cmdlet **Get-AzureVirtualNetworkGatewayConnection** umożliwia połączenie bramy sieci wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="34263-106">The **Get-AzureVirtualNetworkGatewayConnection** cmdlet gets an Azure virtual network gateway connection.</span></span>

## <span data-ttu-id="34263-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="34263-107">EXAMPLES</span></span>

## <span data-ttu-id="34263-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="34263-108">PARAMETERS</span></span>

### <span data-ttu-id="34263-109">-ConnectedEntityId</span><span class="sxs-lookup"><span data-stu-id="34263-109">-ConnectedEntityId</span></span>
<span data-ttu-id="34263-110">Określa identyfikator połączonej jednostki.</span><span class="sxs-lookup"><span data-stu-id="34263-110">Specifies the ID of a connected entity.</span></span>

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

### <span data-ttu-id="34263-111">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="34263-111">-GatewayId</span></span>
<span data-ttu-id="34263-112">Określa identyfikator bramy.</span><span class="sxs-lookup"><span data-stu-id="34263-112">Specifies the ID of the gateway.</span></span>

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

### <span data-ttu-id="34263-113">-Profile</span><span class="sxs-lookup"><span data-stu-id="34263-113">-Profile</span></span>
<span data-ttu-id="34263-114">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="34263-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="34263-115">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="34263-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="34263-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34263-116">CommonParameters</span></span>
<span data-ttu-id="34263-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34263-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34263-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34263-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34263-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="34263-119">INPUTS</span></span>

## <span data-ttu-id="34263-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="34263-120">OUTPUTS</span></span>

## <span data-ttu-id="34263-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="34263-121">NOTES</span></span>

## <span data-ttu-id="34263-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="34263-122">RELATED LINKS</span></span>

[<span data-ttu-id="34263-123">Nowe — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34263-123">New-AzureVirtualNetworkGatewayConnection</span></span>](./New-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="34263-124">Remove-AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34263-124">Remove-AzureVirtualNetworkGatewayConnection</span></span>](./Remove-AzureVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="34263-125">Resetowanie — AzureVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="34263-125">Reset-AzureVirtualNetworkGatewayConnection</span></span>](./Reset-AzureVirtualNetworkGatewayConnection.md)
