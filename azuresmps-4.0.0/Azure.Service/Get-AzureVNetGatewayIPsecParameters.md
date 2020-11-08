---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055242"
---
# <span data-ttu-id="90d50-101">Get-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="90d50-101">Get-AzureVNetGatewayIPsecParameters</span></span>

## <span data-ttu-id="90d50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90d50-102">SYNOPSIS</span></span>
<span data-ttu-id="90d50-103">Pobiera parametry protokołu IPsec połączenia między bramą sieci wirtualnej a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="90d50-103">Gets IPsec parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="90d50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90d50-104">SYNTAX</span></span>

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="90d50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90d50-105">DESCRIPTION</span></span>
<span data-ttu-id="90d50-106">Polecenie cmdlet **Get-AzureVNetGatewayIPsecParameters** pobiera bieżące parametry zabezpieczeń protokołu internetowego (IPSec) i IKE (Internet Key Exchange) połączenia między bramą sieci wirtualnej a lokacją sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="90d50-106">The **Get-AzureVNetGatewayIPsecParameters** cmdlet gets current Internet Protocol security (IPsec) and Internet Key Exchange (IKE) parameters for the connection between a virtual network gateway and a local network site.</span></span>

## <span data-ttu-id="90d50-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90d50-107">EXAMPLES</span></span>

## <span data-ttu-id="90d50-108">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90d50-108">PARAMETERS</span></span>

### <span data-ttu-id="90d50-109">-LocalNetworkSiteName</span><span class="sxs-lookup"><span data-stu-id="90d50-109">-LocalNetworkSiteName</span></span>
<span data-ttu-id="90d50-110">Określa nazwę lokacji sieci lokalnej łączącej się z bramą sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="90d50-110">Specifies the name of the local network site that connects to the virtual network gateway.</span></span>

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

### <span data-ttu-id="90d50-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="90d50-111">-Profile</span></span>
<span data-ttu-id="90d50-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90d50-112">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="90d50-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="90d50-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="90d50-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="90d50-114">-VNetName</span></span>
<span data-ttu-id="90d50-115">Określa sieć wirtualną, za pomocą której to polecenie cmdlet pobiera parametry protokołu IPsec dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="90d50-115">Specifies the virtual network for which this cmdlet gets IPsec parameters for the connection.</span></span>

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

### <span data-ttu-id="90d50-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90d50-116">CommonParameters</span></span>
<span data-ttu-id="90d50-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90d50-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90d50-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90d50-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90d50-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90d50-119">INPUTS</span></span>

## <span data-ttu-id="90d50-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90d50-120">OUTPUTS</span></span>

## <span data-ttu-id="90d50-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90d50-121">NOTES</span></span>

## <span data-ttu-id="90d50-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90d50-122">RELATED LINKS</span></span>

[<span data-ttu-id="90d50-123">Set-AzureVNetGatewayIPsecParameters</span><span class="sxs-lookup"><span data-stu-id="90d50-123">Set-AzureVNetGatewayIPsecParameters</span></span>](./Set-AzureVNetGatewayIPsecParameters.md)


