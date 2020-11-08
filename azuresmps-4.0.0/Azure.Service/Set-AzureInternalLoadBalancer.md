---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C6D23ECB-C06E-4EB7-8096-33787E39694D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 66f6bac80b219a2b3629b399bb568140a5cef217
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054920"
---
# <span data-ttu-id="7b017-101">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b017-101">Set-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="7b017-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b017-102">SYNOPSIS</span></span>
<span data-ttu-id="7b017-103">Modyfikuje konfigurację wewnętrznego modułu równoważenia obciążenia w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="7b017-103">Modifies an internal load balancer configuration in an Azure service.</span></span>

## <span data-ttu-id="7b017-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b017-104">SYNTAX</span></span>

### <span data-ttu-id="7b017-105">ServiceAndSlot (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b017-105">ServiceAndSlot (Default)</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b017-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="7b017-106">SubnetNameOnly</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="7b017-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="7b017-107">SubnetNameAndIP</span></span>
```
Set-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7b017-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7b017-108">DESCRIPTION</span></span>
<span data-ttu-id="7b017-109">Polecenie cmdlet **Set-AzureInternalLoadBalancer** modyfikuje konfigurację wewnętrznego modułu równoważenia obciążenia w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="7b017-109">The **Set-AzureInternalLoadBalancer** cmdlet modifies an internal load balancer configuration in an Azure service.</span></span>
<span data-ttu-id="7b017-110">W przypadku sieci wirtualnej możesz określić podsieć lub adres IP wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7b017-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="7b017-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b017-111">EXAMPLES</span></span>

### <span data-ttu-id="7b017-112">1:1</span><span class="sxs-lookup"><span data-stu-id="7b017-112">1:</span></span>
```

```

## <span data-ttu-id="7b017-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b017-113">PARAMETERS</span></span>

### <span data-ttu-id="7b017-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7b017-114">-InformationAction</span></span>
<span data-ttu-id="7b017-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7b017-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7b017-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7b017-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7b017-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="7b017-117">Continue</span></span>
- <span data-ttu-id="7b017-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="7b017-118">Ignore</span></span>
- <span data-ttu-id="7b017-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="7b017-119">Inquire</span></span>
- <span data-ttu-id="7b017-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7b017-120">SilentlyContinue</span></span>
- <span data-ttu-id="7b017-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="7b017-121">Stop</span></span>
- <span data-ttu-id="7b017-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="7b017-122">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b017-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7b017-123">-InformationVariable</span></span>
<span data-ttu-id="7b017-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="7b017-124">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b017-125">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="7b017-125">-InternalLoadBalancerName</span></span>
<span data-ttu-id="7b017-126">Określa nazwę wewnętrznego modułu równoważenia obciążenia, które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b017-126">Specifies the name of the internal load balancer that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b017-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="7b017-127">-Profile</span></span>
<span data-ttu-id="7b017-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b017-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7b017-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7b017-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7b017-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7b017-130">-ServiceName</span></span>
<span data-ttu-id="7b017-131">Określa nazwę usługi, w której to polecenie cmdlet modyfikuje wewnętrzny moduł równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7b017-131">Specifies the name of the service in which this cmdlet modifies an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b017-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="7b017-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="7b017-133">Określa adres IP sieci wirtualnej dla wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7b017-133">Specifies the virtual network IP address for an internal load balancer.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b017-134">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="7b017-134">-SubnetName</span></span>
<span data-ttu-id="7b017-135">Określa nazwę podsieci dla wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="7b017-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7b017-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b017-136">CommonParameters</span></span>
<span data-ttu-id="7b017-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b017-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b017-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b017-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b017-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b017-139">INPUTS</span></span>

## <span data-ttu-id="7b017-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b017-140">OUTPUTS</span></span>

## <span data-ttu-id="7b017-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b017-141">NOTES</span></span>

## <span data-ttu-id="7b017-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b017-142">RELATED LINKS</span></span>

[<span data-ttu-id="7b017-143">Dodaj-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b017-143">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="7b017-144">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b017-144">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="7b017-145">Nowe — AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="7b017-145">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="7b017-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="7b017-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)


