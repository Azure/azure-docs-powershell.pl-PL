---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054960"
---
# <span data-ttu-id="5ae73-101">New-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5ae73-101">New-AzureRemoteAppVNet</span></span>

## <span data-ttu-id="5ae73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ae73-102">SYNOPSIS</span></span>
<span data-ttu-id="5ae73-103">Tworzy sieć wirtualną funkcji Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5ae73-103">Creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="5ae73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ae73-104">SYNTAX</span></span>

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5ae73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ae73-105">DESCRIPTION</span></span>
<span data-ttu-id="5ae73-106">Polecenie cmdlet **New-AzureRemoteAppVNet** umożliwia utworzenie wirtualnej sieci usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5ae73-106">The **New-AzureRemoteAppVNet** cmdlet creates an Azure RemoteApp virtual network.</span></span>

## <span data-ttu-id="5ae73-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ae73-107">EXAMPLES</span></span>

### <span data-ttu-id="5ae73-108">Przykład 1. Tworzenie sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5ae73-108">Example 1: Create a virtual network</span></span>
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

<span data-ttu-id="5ae73-109">To polecenie tworzy sieć wirtualną o nazwie ContosoVNet.</span><span class="sxs-lookup"><span data-stu-id="5ae73-109">This command creates a virtual network named ContosoVNet.</span></span>

<span data-ttu-id="5ae73-110">Aby ustalić stan operacji, użyj polecenia cmdlet **Get-AzureRemoteAppOperationResult** z identyfikatorem śledzenia, który jest zwracany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ae73-110">To determine the status of the operation, use the **Get-AzureRemoteAppOperationResult** cmdlet with the tracking ID that this cmdlet returns.</span></span>

## <span data-ttu-id="5ae73-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ae73-111">PARAMETERS</span></span>

### <span data-ttu-id="5ae73-112">-DnsServerIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ae73-112">-DnsServerIpAddress</span></span>
<span data-ttu-id="5ae73-113">Określa tablicę adresów IPv4 serwerów DNS.</span><span class="sxs-lookup"><span data-stu-id="5ae73-113">Specifies an array of the IPv4 addresses of the DNS servers.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae73-114">-Gatewaytype</span><span class="sxs-lookup"><span data-stu-id="5ae73-114">-GatewayType</span></span>
<span data-ttu-id="5ae73-115">Określa typ routingu bramy, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="5ae73-115">Specifies the type of gateway routing to use.</span></span>
<span data-ttu-id="5ae73-116">Dopuszczalne wartości tego parametru to: StaticRouting lub DynamicRouting.</span><span class="sxs-lookup"><span data-stu-id="5ae73-116">The acceptable values for this parameter are:  StaticRouting or DynamicRouting.</span></span>

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae73-117">-LocalNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="5ae73-117">-LocalNetworkAddressSpace</span></span>
<span data-ttu-id="5ae73-118">Określa tablicę ciągów określającą przestrzeń adresową sieci lokalnej w notacji CIDR (Classless subdomain Routing).</span><span class="sxs-lookup"><span data-stu-id="5ae73-118">Specifies an array of strings that specify the local network address space, in Classless Interdomain Routing (CIDR) notation.</span></span>
<span data-ttu-id="5ae73-119">Ta przestrzeń adresowa nie może zachodzić na przestrzeń adresową sieci wirtualnej określaną przez parametr *VirtualNetworkAddressSpace* .</span><span class="sxs-lookup"><span data-stu-id="5ae73-119">This address space must not overlap with the virtual network address space that the *VirtualNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae73-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5ae73-120">-Location</span></span>
<span data-ttu-id="5ae73-121">Określa lokalizację, w której ma zostać utworzona sieć wirtualna.</span><span class="sxs-lookup"><span data-stu-id="5ae73-121">Specifies the location in which to create the virtual network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae73-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="5ae73-122">-Profile</span></span>
<span data-ttu-id="5ae73-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ae73-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5ae73-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5ae73-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5ae73-125">-VirtualNetworkAddressSpace</span><span class="sxs-lookup"><span data-stu-id="5ae73-125">-VirtualNetworkAddressSpace</span></span>
<span data-ttu-id="5ae73-126">Określa tablicę ciągów określającą przestrzeń adresową sieci wirtualnej w notacji CIDR.</span><span class="sxs-lookup"><span data-stu-id="5ae73-126">Specifies an array of string that specify the virtual network address space in CIDR notation.</span></span>
<span data-ttu-id="5ae73-127">Ten parametr musi znajdować się w zakresie prywatnego adresu IP i nie może się pokrywać z przestrzenią adresową sieci lokalnej określającej parametr *LocalNetworkAddressSpace* .</span><span class="sxs-lookup"><span data-stu-id="5ae73-127">This must be in the private IP address range and cannot overlap with the local network address space that the *LocalNetworkAddressSpace* parameter specifies.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5ae73-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="5ae73-128">-VNetName</span></span>
<span data-ttu-id="5ae73-129">Określa nazwę sieci wirtualnej usługi Azure RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="5ae73-129">Specifies the name of the Azure RemoteApp virtual network.</span></span>

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

### <span data-ttu-id="5ae73-130">-VpnDeviceIpAddress</span><span class="sxs-lookup"><span data-stu-id="5ae73-130">-VpnDeviceIpAddress</span></span>
<span data-ttu-id="5ae73-131">Określa adres urządzenia wirtualnej sieci prywatnej (VPN).</span><span class="sxs-lookup"><span data-stu-id="5ae73-131">Specifies the address of the virtual private network (VPN) device.</span></span>
<span data-ttu-id="5ae73-132">To musi być adres publiczny.</span><span class="sxs-lookup"><span data-stu-id="5ae73-132">This must be a public-facing address.</span></span>

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

### <span data-ttu-id="5ae73-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ae73-133">CommonParameters</span></span>
<span data-ttu-id="5ae73-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ae73-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ae73-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ae73-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ae73-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ae73-136">INPUTS</span></span>

## <span data-ttu-id="5ae73-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ae73-137">OUTPUTS</span></span>

## <span data-ttu-id="5ae73-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ae73-138">NOTES</span></span>

## <span data-ttu-id="5ae73-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ae73-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ae73-140">Get-AzureRemoteAppOperationResult</span><span class="sxs-lookup"><span data-stu-id="5ae73-140">Get-AzureRemoteAppOperationResult</span></span>](./Get-AzureRemoteAppOperationResult.md)

[<span data-ttu-id="5ae73-141">Get-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5ae73-141">Get-AzureRemoteAppVNet</span></span>](./Get-AzureRemoteAppVNet.md)

[<span data-ttu-id="5ae73-142">Remove-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5ae73-142">Remove-AzureRemoteAppVNet</span></span>](./Remove-AzureRemoteAppVNet.md)

[<span data-ttu-id="5ae73-143">Set-AzureRemoteAppVNet</span><span class="sxs-lookup"><span data-stu-id="5ae73-143">Set-AzureRemoteAppVNet</span></span>](./Set-AzureRemoteAppVNet.md)


