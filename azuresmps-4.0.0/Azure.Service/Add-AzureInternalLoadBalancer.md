---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4A0442F9-F420-4A26-9127-4C875090CC12
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0e2709ce2939cb45200e758563e917675894e443
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054690"
---
# <span data-ttu-id="56b92-101">Add-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56b92-101">Add-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="56b92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56b92-102">SYNOPSIS</span></span>
<span data-ttu-id="56b92-103">Umożliwia dodanie wewnętrznego modułu równoważenia obciążenia do usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="56b92-103">Adds an internal load balancer to an Azure service.</span></span>

## <span data-ttu-id="56b92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56b92-104">SYNTAX</span></span>

### <span data-ttu-id="56b92-105">ServiceAndSlot (domyślny)</span><span class="sxs-lookup"><span data-stu-id="56b92-105">ServiceAndSlot (Default)</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="56b92-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="56b92-106">SubnetNameOnly</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="56b92-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="56b92-107">SubnetNameAndIP</span></span>
```
Add-AzureInternalLoadBalancer [-InternalLoadBalancerName] <String> [-ServiceName] <String>
 [-SubnetName] <String> [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="56b92-108">Opis</span><span class="sxs-lookup"><span data-stu-id="56b92-108">DESCRIPTION</span></span>
<span data-ttu-id="56b92-109">Polecenie cmdlet **Add-AzureInternalLoadBalancer** umożliwia dodanie wewnętrznej konfiguracji modułu równoważenia obciążenia do usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="56b92-109">The **Add-AzureInternalLoadBalancer** cmdlet adds an internal load balancer configuration to an Azure service.</span></span>
<span data-ttu-id="56b92-110">W przypadku sieci wirtualnej możesz określić podsieć lub adres IP wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="56b92-110">For a virtual network, you can specify a subnet or the IP address of the internal load balancer.</span></span>

## <span data-ttu-id="56b92-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56b92-111">EXAMPLES</span></span>

### <span data-ttu-id="56b92-112">Przykład 1: Dodawanie wewnętrznego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="56b92-112">Example 1: Add an internal load balancer</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB"
```

<span data-ttu-id="56b92-113">To polecenie umożliwia dodanie wewnętrznego modułu równoważenia obciążenia o nazwie ContosoILB do usługi o nazwie ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="56b92-113">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>

### <span data-ttu-id="56b92-114">Przykład 2: Dodawanie wewnętrznego modułu równoważenia obciążenia dla określonej podsieci</span><span class="sxs-lookup"><span data-stu-id="56b92-114">Example 2: Add an internal load balancer for a specified subnet</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="56b92-115">To polecenie umożliwia dodanie wewnętrznego modułu równoważenia obciążenia o nazwie ContosoILB do usługi o nazwie ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="56b92-115">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="56b92-116">Polecenie określa podsieć o nazwie FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="56b92-116">The command specifies the subnet named FrontEndSubnet.</span></span>

### <span data-ttu-id="56b92-117">Przykład 3: Dodawanie wewnętrznego modułu równoważenia obciążenia dla określonej podsieci i adresu</span><span class="sxs-lookup"><span data-stu-id="56b92-117">Example 3: Add an internal load balancer for a specified subnet and address</span></span>
```
PS C:\> Add-AzureInternalLoadBalancer -ServiceName "ContosoWebsite01" -InternalLoadBalancerName "ContosoILB" -SubnetName "FrontEndSubnet" -StaticVNetIPAddress 192.168.4.7
```

<span data-ttu-id="56b92-118">To polecenie umożliwia dodanie wewnętrznego modułu równoważenia obciążenia o nazwie ContosoILB do usługi o nazwie ContosoWebsite01.</span><span class="sxs-lookup"><span data-stu-id="56b92-118">This command adds an internal load balancer named ContosoILB to the service named ContosoWebsite01.</span></span>
<span data-ttu-id="56b92-119">Polecenie określa podsieć o nazwie FrontEndSubnet oraz adres statyczny sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="56b92-119">The command specifies the subnet named FrontEndSubnet and the static address of the virtual network.</span></span>

## <span data-ttu-id="56b92-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56b92-120">PARAMETERS</span></span>

### <span data-ttu-id="56b92-121">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="56b92-121">-InformationAction</span></span>
<span data-ttu-id="56b92-122">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="56b92-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="56b92-123">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="56b92-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="56b92-124">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="56b92-124">Continue</span></span>
- <span data-ttu-id="56b92-125">Ignorować</span><span class="sxs-lookup"><span data-stu-id="56b92-125">Ignore</span></span>
- <span data-ttu-id="56b92-126">Inquire</span><span class="sxs-lookup"><span data-stu-id="56b92-126">Inquire</span></span>
- <span data-ttu-id="56b92-127">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="56b92-127">SilentlyContinue</span></span>
- <span data-ttu-id="56b92-128">Przestaw</span><span class="sxs-lookup"><span data-stu-id="56b92-128">Stop</span></span>
- <span data-ttu-id="56b92-129">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="56b92-129">Suspend</span></span>

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

### <span data-ttu-id="56b92-130">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="56b92-130">-InformationVariable</span></span>
<span data-ttu-id="56b92-131">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="56b92-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="56b92-132">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="56b92-132">-InternalLoadBalancerName</span></span>
<span data-ttu-id="56b92-133">Określa nazwę wewnętrznego modułu równoważenia obciążenia, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b92-133">Specifies the name of the internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="56b92-134">-Profile</span><span class="sxs-lookup"><span data-stu-id="56b92-134">-Profile</span></span>
<span data-ttu-id="56b92-135">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b92-135">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="56b92-136">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="56b92-136">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="56b92-137">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="56b92-137">-ServiceName</span></span>
<span data-ttu-id="56b92-138">Określa nazwę usługi, do której to polecenie cmdlet umożliwia dodanie wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="56b92-138">Specifies the name of the service to which this cmdlet adds an internal load balancer.</span></span>

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

### <span data-ttu-id="56b92-139">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="56b92-139">-StaticVNetIPAddress</span></span>
<span data-ttu-id="56b92-140">Określa adres IP sieci wirtualnej dla wewnętrznego modułu równoważenia obciążenia, który jest dodawany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b92-140">Specifies the virtual network IP address for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="56b92-141">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="56b92-141">-SubnetName</span></span>
<span data-ttu-id="56b92-142">Określa nazwę podsieci dla wewnętrznego modułu równoważenia obciążenia, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56b92-142">Specifies the name of the subnet for an internal load balancer that this cmdlet adds.</span></span>

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

### <span data-ttu-id="56b92-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56b92-143">CommonParameters</span></span>
<span data-ttu-id="56b92-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56b92-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56b92-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56b92-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56b92-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56b92-146">INPUTS</span></span>

## <span data-ttu-id="56b92-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56b92-147">OUTPUTS</span></span>

### <span data-ttu-id="56b92-148">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="56b92-148">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="56b92-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56b92-149">NOTES</span></span>

## <span data-ttu-id="56b92-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56b92-150">RELATED LINKS</span></span>

[<span data-ttu-id="56b92-151">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56b92-151">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="56b92-152">Nowe — AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="56b92-152">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="56b92-153">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56b92-153">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="56b92-154">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="56b92-154">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


