---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: DF95285F-97F4-4064-8E27-EE6E93843E55
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0a14865c986bf6439df833a38f87835792a6e3c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054592"
---
# <span data-ttu-id="339a6-101">Get-AzureRemoteAppVpnDevice</span><span class="sxs-lookup"><span data-stu-id="339a6-101">Get-AzureRemoteAppVpnDevice</span></span>

## <span data-ttu-id="339a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="339a6-102">SYNOPSIS</span></span>
<span data-ttu-id="339a6-103">Pobiera informacje o urządzeniu sieci VPN.</span><span class="sxs-lookup"><span data-stu-id="339a6-103">Retrieves information about a VPN device.</span></span>

## <span data-ttu-id="339a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="339a6-104">SYNTAX</span></span>

```
Get-AzureRemoteAppVpnDevice [-VNetName] <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="339a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="339a6-105">DESCRIPTION</span></span>
<span data-ttu-id="339a6-106">Polecenie cmdlet **Get-AzureRemoteAppVpnDevice** pobiera informacje o urządzeniu wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="339a6-106">The **Get-AzureRemoteAppVpnDevice** cmdlet retrieves information about a virtual private network (VPN) device.</span></span>

## <span data-ttu-id="339a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="339a6-107">EXAMPLES</span></span>

### <span data-ttu-id="339a6-108">Przykład 1: zwracanie konfiguracji dostępnych urządzeń sieci VPN dla sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="339a6-108">Example 1: Return the available VPN device configurations for a virtual network</span></span>
```
PS C:\> Get-AzureRemoteVpnDevice -VNetName "ContosoVNet"


Name                   Platforms

----                   ---------

Cisco Systems, Inc.    {ASA 5500 Series Adaptive Security Appliances, ASR 1000 Series Aggregation Services Routers, ASR 1000 Series Aggregation Services Routers - Dynamic Routing, ISR Series Integrated Services Routers...} 

Juniper Networks, Inc. {SRX Series Routers, SRX Series Routers - Dynamic Routing, J Series Routers, J Series Routers - Dynamic Routing...} 

Microsoft Corporation  {RRAS}
```

<span data-ttu-id="339a6-109">To polecenie zwraca dostępne konfiguracje urządzeń sieci VPN dla określonej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="339a6-109">This command returns the available VPN device configurations for the specified virtual network.</span></span>

## <span data-ttu-id="339a6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="339a6-110">PARAMETERS</span></span>

### <span data-ttu-id="339a6-111">-Profile</span><span class="sxs-lookup"><span data-stu-id="339a6-111">-Profile</span></span>
<span data-ttu-id="339a6-112">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="339a6-112">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="339a6-113">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="339a6-113">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="339a6-114">-VNetName</span><span class="sxs-lookup"><span data-stu-id="339a6-114">-VNetName</span></span>
<span data-ttu-id="339a6-115">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="339a6-115">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="339a6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="339a6-116">CommonParameters</span></span>
<span data-ttu-id="339a6-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="339a6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="339a6-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="339a6-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="339a6-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="339a6-119">INPUTS</span></span>

## <span data-ttu-id="339a6-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="339a6-120">OUTPUTS</span></span>

### <span data-ttu-id="339a6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="339a6-121">System.String</span></span>

## <span data-ttu-id="339a6-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="339a6-122">NOTES</span></span>

## <span data-ttu-id="339a6-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="339a6-123">RELATED LINKS</span></span>

[<span data-ttu-id="339a6-124">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="339a6-124">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="339a6-125">Get-AzureRemoteAppVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="339a6-125">Get-AzureRemoteAppVpnDeviceConfigScript</span></span>](./Get-AzureRemoteAppVpnDeviceConfigScript.md)


