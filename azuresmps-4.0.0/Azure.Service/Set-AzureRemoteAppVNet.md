---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 97B96661-E60A-4505-AD06-D2A541DB820E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19f7b09d26df88591e03acf8b01842efdead05e2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055018"
---
# <span data-ttu-id="96bf2-101">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="96bf2-101">Set-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="96bf2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="96bf2-102">SYNOPSIS</span></span>
<span data-ttu-id="96bf2-103">Ustawia właściwości sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="96bf2-103">Sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="96bf2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="96bf2-104">SYNTAX</span></span>

```
Set-AzureRemoteAppVNet -VNetName <String> [-VirtualNetworkAddressSpace <String[]>]
 [-LocalNetworkAddressSpace <String[]>] [-DnsServerIpAddress <String[]>] [-VpnDeviceIpAddress <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="96bf2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="96bf2-105">DESCRIPTION</span></span>
<span data-ttu-id="96bf2-106">Polecenie cmdlet **Set-AzureRemoteAppVNet** ustawia właściwości sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="96bf2-106">The **Set-AzureRemoteAppVNet** cmdlet sets the properties of an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="96bf2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="96bf2-107">EXAMPLES</span></span>

### <span data-ttu-id="96bf2-108">Przykład 1: Ustawianie właściwości sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="96bf2-108">Example 1: Set the properties of a virtual network</span></span>
```
PS C:\> Set-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "131.253.33.200" -LocalNetworkAddressSpace "192.168.0.0/24" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.253.33.200"
```

<span data-ttu-id="96bf2-109">To polecenie ustawia właściwości sieci wirtualnej o nazwie ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="96bf2-109">This command sets the properties of a virtual network named ContosoVNet.</span></span>

## <span data-ttu-id="96bf2-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="96bf2-110">PARAMETERS</span></span>

### <span data-ttu-id="96bf2-111">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="96bf2-111">-DnsServerIpAddress</span></span>
<span data-ttu-id="96bf2-112">Określa adresy IPv4 serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="96bf2-112">Specifies the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96bf2-113">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="96bf2-113">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="96bf2-114">Określa przestrzeń adresową w sieci lokalnej, w notacji CIDR (Class Inter-Domain Routing).</span><span class="sxs-lookup"><span data-stu-id="96bf2-114">Specifies the local network address space, in Classes Inter-Domain Routing (CIDR) notation.</span></span>
<span data-ttu-id="96bf2-115">Ta funkcja nie może zachodzić na przestrzeń adresową sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="96bf2-115">This must not overlap the virtual network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96bf2-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="96bf2-116">-Profile</span></span>
<span data-ttu-id="96bf2-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96bf2-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="96bf2-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="96bf2-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="96bf2-119">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="96bf2-119">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="96bf2-120">Określa przestrzeń adresową sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="96bf2-120">Specifies the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="96bf2-121">Musi to być adres w prywatnym zakresie adresów IP i nie może zachodzić na przestrzeń adresową sieci lokalnej.</span><span class="sxs-lookup"><span data-stu-id="96bf2-121">This must be in the private IP address range and cannot overlap the local network address space.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96bf2-122">-VNetName</span><span class="sxs-lookup"><span data-stu-id="96bf2-122">-VNetName</span></span>
<span data-ttu-id="96bf2-123">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="96bf2-123">Specifies the name of the Azure RemoteApp virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96bf2-124">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="96bf2-124">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="96bf2-125">Określa adres urządzenia wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="96bf2-125">Specifies the address of the Virtual Private Network (VPN) device.</span></span>
<span data-ttu-id="96bf2-126">To musi być adres publiczny.</span><span class="sxs-lookup"><span data-stu-id="96bf2-126">This must be a public-facing address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96bf2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96bf2-127">CommonParameters</span></span>
<span data-ttu-id="96bf2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96bf2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96bf2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96bf2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96bf2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="96bf2-130">INPUTS</span></span>

## <span data-ttu-id="96bf2-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="96bf2-131">OUTPUTS</span></span>

## <span data-ttu-id="96bf2-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="96bf2-132">NOTES</span></span>

## <span data-ttu-id="96bf2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="96bf2-133">RELATED LINKS</span></span>

[<span data-ttu-id="96bf2-134">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="96bf2-134">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)


