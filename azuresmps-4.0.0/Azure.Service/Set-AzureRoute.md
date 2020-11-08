---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A7DFF559-188D-4CF9-9315-CA327E0C5C0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: d502ba2961e5238426228e4ac58a29b922be81f3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054789"
---
# <span data-ttu-id="66b2b-101">Set-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="66b2b-101">Set-AzureRoute</span></span>

## <span data-ttu-id="66b2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="66b2b-102">SYNOPSIS</span></span>
<span data-ttu-id="66b2b-103">Tworzy trasę w tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="66b2b-103">Creates a route in a route table.</span></span>

## <span data-ttu-id="66b2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="66b2b-104">SYNTAX</span></span>

```
Set-AzureRoute -RouteName <String> -AddressPrefix <String> -NextHopType <String> [-NextHopIpAddress <String>]
 -RouteTable <IRouteTable> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="66b2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="66b2b-105">DESCRIPTION</span></span>
<span data-ttu-id="66b2b-106">Polecenie cmdlet **Set-AzureRoute** tworzy trasę w tabeli tras.</span><span class="sxs-lookup"><span data-stu-id="66b2b-106">The **Set-AzureRoute** cmdlet creates a route in a route table.</span></span>
<span data-ttu-id="66b2b-107">Nowa trasa zacznie obowiązywać prawie natychmiast na maszynach wirtualnych skojarzonych z tabelą tras.</span><span class="sxs-lookup"><span data-stu-id="66b2b-107">The new route takes effect almost immediately on the virtual machines that are associated with the route table.</span></span>

## <span data-ttu-id="66b2b-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="66b2b-108">EXAMPLES</span></span>

### <span data-ttu-id="66b2b-109">Przykład 1: Dodawanie urządzenia wirtualnego — Następna przeskokowa trasa</span><span class="sxs-lookup"><span data-stu-id="66b2b-109">Example 1: Add a virtual appliance next hop route</span></span>
```
PS C:\> New-AzureRouteTable -Name "ApplianceRouteTable" -Location "Central US" -Label "Appliance Route Table" | Set-AzureRoute -RouteName "ApplianceRoute03" -AddressPrefix "10.0.0.0/24" -NextHopType VirtualAppliance -NextHopIpAddress "10.0.1.5"

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute}                    AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="66b2b-110">To polecenie tworzy tabelę tras o nazwie ApplianceRouteTable w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="66b2b-110">This command creates a route table named ApplianceRouteTable in the specified location.</span></span>
<span data-ttu-id="66b2b-111">Polecenie przekazuje tę tabelę routingu do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b2b-111">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="66b2b-112">Bieżące polecenie cmdlet umożliwia dodanie trasy o nazwie ApplianceRoute03, która jest typu VirtualAppliance następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="66b2b-112">The current cmdlet adds a route named ApplianceRoute03, which is a VirtualAppliance next hop type.</span></span>
<span data-ttu-id="66b2b-113">Polecenie określa adres IP następnego przeskoku oraz prefiks adresu dla tej trasy.</span><span class="sxs-lookup"><span data-stu-id="66b2b-113">The command specifies the next hop IP address and the address prefix for the route.</span></span>

### <span data-ttu-id="66b2b-114">Przykład 2: Dodawanie internetowego trasy przeskoków internetowych</span><span class="sxs-lookup"><span data-stu-id="66b2b-114">Example 2: Add an Internet next hop route</span></span>
```
PS C:\> Get-AzureRouteTable -Name "ApplianceRouteTable" | Set-AzureRoute -RouteName "InternetRoute" -AddressPrefix "0.0.0.0/0" -NextHopType Internet

Routes                        Name                          Location                      Label
------                        ----                          --------                      -----
{approute, internetroute}     AppRT                         Central US                    Appliance Route Table
```

<span data-ttu-id="66b2b-115">To polecenie pobiera tabelę tras o nazwie ApplianceRouteTable.</span><span class="sxs-lookup"><span data-stu-id="66b2b-115">This command gets a route table named ApplianceRouteTable.</span></span>
<span data-ttu-id="66b2b-116">Polecenie przekazuje tę tabelę routingu do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b2b-116">The command passes that route table to the current cmdlet.</span></span>
<span data-ttu-id="66b2b-117">Bieżące polecenie cmdlet umożliwia dodanie trasy o nazwie InternetRoute, która jest internetowym typem następnego przeskoku.</span><span class="sxs-lookup"><span data-stu-id="66b2b-117">The current cmdlet adds a route named InternetRoute, which is an Internet next hop type.</span></span>
<span data-ttu-id="66b2b-118">Polecenie Określa prefiks adresu dla trasy.</span><span class="sxs-lookup"><span data-stu-id="66b2b-118">The command specifies the address prefix for the route.</span></span>

## <span data-ttu-id="66b2b-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="66b2b-119">PARAMETERS</span></span>

### <span data-ttu-id="66b2b-120">-AddressPrefix</span><span class="sxs-lookup"><span data-stu-id="66b2b-120">-AddressPrefix</span></span>
<span data-ttu-id="66b2b-121">Określa prefiks adresu dla nowej trasy.</span><span class="sxs-lookup"><span data-stu-id="66b2b-121">Specifies an address prefix for the new route.</span></span>

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

### <span data-ttu-id="66b2b-122">-NextHopIpAddress</span><span class="sxs-lookup"><span data-stu-id="66b2b-122">-NextHopIpAddress</span></span>
<span data-ttu-id="66b2b-123">Określa adres IP urządzenia, które jest następnym skokiem dla ruchu sieciowego korzystającego z tej trasy.</span><span class="sxs-lookup"><span data-stu-id="66b2b-123">Specifies the IP address of the appliance that is the next hop for traffic that uses this route.</span></span>
<span data-ttu-id="66b2b-124">Tę wartość należy określić tylko wtedy, gdy dla parametru *NextHopType* określono wartość VirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="66b2b-124">Specify this value only if you specify a value of VirtualAppliance for the *NextHopType* parameter.</span></span>

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

### <span data-ttu-id="66b2b-125">-NextHopType</span><span class="sxs-lookup"><span data-stu-id="66b2b-125">-NextHopType</span></span>
<span data-ttu-id="66b2b-126">Określa typ następnego przeskoku dla ruchu, który używa tej trasy.</span><span class="sxs-lookup"><span data-stu-id="66b2b-126">Specifies the next hop type for traffic that uses this route.</span></span>
<span data-ttu-id="66b2b-127">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="66b2b-127">Valid values are:</span></span> 

- <span data-ttu-id="66b2b-128">VPNGateway</span><span class="sxs-lookup"><span data-stu-id="66b2b-128">VPNGateway</span></span>
- <span data-ttu-id="66b2b-129">VNETLocal</span><span class="sxs-lookup"><span data-stu-id="66b2b-129">VNETLocal</span></span>
- <span data-ttu-id="66b2b-130">Internetowe</span><span class="sxs-lookup"><span data-stu-id="66b2b-130">Internet</span></span>
- <span data-ttu-id="66b2b-131">VirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="66b2b-131">VirtualAppliance</span></span>
- <span data-ttu-id="66b2b-132">Puste</span><span class="sxs-lookup"><span data-stu-id="66b2b-132">Null</span></span>

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

### <span data-ttu-id="66b2b-133">-Profile</span><span class="sxs-lookup"><span data-stu-id="66b2b-133">-Profile</span></span>
<span data-ttu-id="66b2b-134">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b2b-134">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="66b2b-135">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="66b2b-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="66b2b-136">-RouteName</span><span class="sxs-lookup"><span data-stu-id="66b2b-136">-RouteName</span></span>
<span data-ttu-id="66b2b-137">Określa nazwę nowej trasy, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66b2b-137">Specifies a name for the new route that this cmdlet adds.</span></span>

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

### <span data-ttu-id="66b2b-138">-Routeing</span><span class="sxs-lookup"><span data-stu-id="66b2b-138">-RouteTable</span></span>
<span data-ttu-id="66b2b-139">Określa tabelę tras, z którą to polecenie cmdlet dodaje nową trasę.</span><span class="sxs-lookup"><span data-stu-id="66b2b-139">Specifies the route table to which this cmdlet adds the new route.</span></span>

```yaml
Type: IRouteTable
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66b2b-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66b2b-140">CommonParameters</span></span>
<span data-ttu-id="66b2b-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66b2b-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66b2b-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66b2b-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66b2b-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66b2b-143">INPUTS</span></span>

## <span data-ttu-id="66b2b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="66b2b-144">OUTPUTS</span></span>

## <span data-ttu-id="66b2b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="66b2b-145">NOTES</span></span>

## <span data-ttu-id="66b2b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66b2b-146">RELATED LINKS</span></span>

[<span data-ttu-id="66b2b-147">Remove-AzureRoute</span><span class="sxs-lookup"><span data-stu-id="66b2b-147">Remove-AzureRoute</span></span>](./Remove-AzureRoute.md)


