---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C01AFE1-65E7-4C5F-B3ED-8FCD9C4D20FC
online version: ''
schema: 2.0.0
ms.openlocfilehash: a42ffe7ded2eb47638dd961ae79b10dd21cf08ad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054880"
---
# <span data-ttu-id="a9fdf-101">New-AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="a9fdf-101">New-AzureInternalLoadBalancerConfig</span></span>

## <span data-ttu-id="a9fdf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9fdf-102">SYNOPSIS</span></span>
<span data-ttu-id="a9fdf-103">Umożliwia utworzenie wewnętrznej konfiguracji modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-103">Creates an internal load balancer configuration.</span></span>

## <span data-ttu-id="a9fdf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9fdf-104">SYNTAX</span></span>

### <span data-ttu-id="a9fdf-105">ServiceAndSlot (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9fdf-105">ServiceAndSlot (Default)</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a9fdf-106">SubnetNameOnly</span><span class="sxs-lookup"><span data-stu-id="a9fdf-106">SubnetNameOnly</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9fdf-107">SubnetNameAndIP</span><span class="sxs-lookup"><span data-stu-id="a9fdf-107">SubnetNameAndIP</span></span>
```
New-AzureInternalLoadBalancerConfig [-InternalLoadBalancerName] <String> [-SubnetName] <String>
 [-StaticVNetIPAddress] <IPAddress> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a9fdf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9fdf-108">DESCRIPTION</span></span>
<span data-ttu-id="a9fdf-109">Polecenie cmdlet **New-AzureInternalLoadBalancerConfig** tworzy obiekt **InternalLoadBalancerConfig** .</span><span class="sxs-lookup"><span data-stu-id="a9fdf-109">The **New-AzureInternalLoadBalancerConfig** cmdlet creates an **InternalLoadBalancerConfig** object.</span></span>
<span data-ttu-id="a9fdf-110">Możesz użyć konfiguracji wewnętrznego modułu równoważenia obciążenia podczas tworzenia wdrożenia maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-110">You can use an internal load balancer configuration when you create an Azure virtual machine deployment.</span></span>

## <span data-ttu-id="a9fdf-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9fdf-111">EXAMPLES</span></span>

### <span data-ttu-id="a9fdf-112">Przykład 1. Tworzenie wewnętrznej konfiguracji modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="a9fdf-112">Example 1: Create an internal load balancer configuration</span></span>
```
PS C:\> $IlbConfig = New-AzureInternalLoadBalancerConfig -InternalLoadBalancerName "Contoso" -SubnetName "FrontEndSubnet"
```

<span data-ttu-id="a9fdf-113">To polecenie tworzy wewnętrzną konfigurację modułu równoważenia obciążenia dla podsieci o nazwie FrontEndSubnet.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-113">This command creates an internal load balancer configuration for the subnet named FrontEndSubnet.</span></span>
<span data-ttu-id="a9fdf-114">Polecenie zapisuje konfigurację w zmiennej $IlbConfig, która ma być używana do wdrożenia maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-114">The command stores the configuration in the $IlbConfig variable for you to use for a virtual machine deployment.</span></span>

## <span data-ttu-id="a9fdf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9fdf-115">PARAMETERS</span></span>

### <span data-ttu-id="a9fdf-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a9fdf-116">-InformationAction</span></span>
<span data-ttu-id="a9fdf-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a9fdf-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a9fdf-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a9fdf-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="a9fdf-119">Continue</span></span>
- <span data-ttu-id="a9fdf-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="a9fdf-120">Ignore</span></span>
- <span data-ttu-id="a9fdf-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="a9fdf-121">Inquire</span></span>
- <span data-ttu-id="a9fdf-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a9fdf-122">SilentlyContinue</span></span>
- <span data-ttu-id="a9fdf-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="a9fdf-123">Stop</span></span>
- <span data-ttu-id="a9fdf-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="a9fdf-124">Suspend</span></span>

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

### <span data-ttu-id="a9fdf-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a9fdf-125">-InformationVariable</span></span>
<span data-ttu-id="a9fdf-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a9fdf-127">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a9fdf-127">-InternalLoadBalancerName</span></span>
<span data-ttu-id="a9fdf-128">Określa nazwę wewnętrznego modułu równoważenia obciążenia, które obejmuje ten aplet polecenia w konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-128">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="a9fdf-129">-Profile</span><span class="sxs-lookup"><span data-stu-id="a9fdf-129">-Profile</span></span>
<span data-ttu-id="a9fdf-130">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a9fdf-131">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a9fdf-132">-StaticVNetIPAddress</span><span class="sxs-lookup"><span data-stu-id="a9fdf-132">-StaticVNetIPAddress</span></span>
<span data-ttu-id="a9fdf-133">Określa adres IP sieci wirtualnej dla wewnętrznego modułu równoważenia obciążenia, który obejmuje to polecenie cmdlet w konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-133">Specifies the virtual network IP address for an internal load balancer that this cmdlet includes in the configuration.</span></span>

```yaml
Type: IPAddress
Parameter Sets: SubnetNameAndIP
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fdf-134">-Subnetname</span><span class="sxs-lookup"><span data-stu-id="a9fdf-134">-SubnetName</span></span>
<span data-ttu-id="a9fdf-135">Określa nazwę podsieci dla wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-135">Specifies the name of the subnet for an internal load balancer.</span></span>

```yaml
Type: String
Parameter Sets: SubnetNameOnly, SubnetNameAndIP
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9fdf-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9fdf-136">CommonParameters</span></span>
<span data-ttu-id="a9fdf-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9fdf-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9fdf-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9fdf-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9fdf-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9fdf-139">INPUTS</span></span>

## <span data-ttu-id="a9fdf-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9fdf-140">OUTPUTS</span></span>

### <span data-ttu-id="a9fdf-141">Microsoft. platformy windowsazure. Commands. servicemanagement. model. InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="a9fdf-141">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerConfig</span></span>

## <span data-ttu-id="a9fdf-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9fdf-142">NOTES</span></span>

## <span data-ttu-id="a9fdf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9fdf-143">RELATED LINKS</span></span>

[<span data-ttu-id="a9fdf-144">Dodaj-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fdf-144">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="a9fdf-145">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fdf-145">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="a9fdf-146">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fdf-146">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="a9fdf-147">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a9fdf-147">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


