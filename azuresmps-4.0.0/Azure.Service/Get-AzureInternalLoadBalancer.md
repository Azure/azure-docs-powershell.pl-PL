---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A439ADC4-991E-4860-82AA-7BED315991B9
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9f28659835fef4778eac729ccd020eb82f563bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055306"
---
# <span data-ttu-id="97b6b-101">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97b6b-101">Get-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="97b6b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="97b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="97b6b-103">Pobiera szczegóły konfiguracji wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="97b6b-103">Gets the details of the internal load balancer configuration.</span></span>

## <span data-ttu-id="97b6b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="97b6b-104">SYNTAX</span></span>

```
Get-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="97b6b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="97b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="97b6b-106">Polecenie cmdlet **Get-AzureInternalLoadBalancer** pobiera szczegóły konfiguracji wewnętrznego modułu równoważenia obciążenia dla usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="97b6b-106">The **Get-AzureInternalLoadBalancer** cmdlet gets the details of the internal load balancer configuration for an Azure service.</span></span>

## <span data-ttu-id="97b6b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="97b6b-107">EXAMPLES</span></span>

### <span data-ttu-id="97b6b-108">Przykład 1: uzyskiwanie szczegółów dotyczących wewnętrznego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="97b6b-108">Example 1: Get details for an internal load balancer</span></span>
```
PS C:\> Get-AzureService -ServiceName "ContosoService" | Get-AzureInternalLoadBalancer
```

<span data-ttu-id="97b6b-109">To polecenie uzyskuje usługę o nazwie ContosoService przy użyciu polecenia cmdlet **Get-AzureService** .</span><span class="sxs-lookup"><span data-stu-id="97b6b-109">This command gets the service named ContosoService by using the **Get-AzureService** cmdlet.</span></span>
<span data-ttu-id="97b6b-110">Polecenie przekazuje usługę do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="97b6b-110">The command passes that service to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="97b6b-111">Bieżące polecenie cmdlet pobiera szczegóły dotyczące wewnętrznego modułu równoważenia obciążenia dla tej usługi.</span><span class="sxs-lookup"><span data-stu-id="97b6b-111">The current cmdlet gets details for the internal load balancer for that service.</span></span>

## <span data-ttu-id="97b6b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="97b6b-112">PARAMETERS</span></span>

### <span data-ttu-id="97b6b-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="97b6b-113">-InformationAction</span></span>
<span data-ttu-id="97b6b-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="97b6b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="97b6b-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="97b6b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="97b6b-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="97b6b-116">Continue</span></span>
- <span data-ttu-id="97b6b-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="97b6b-117">Ignore</span></span>
- <span data-ttu-id="97b6b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="97b6b-118">Inquire</span></span>
- <span data-ttu-id="97b6b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="97b6b-119">SilentlyContinue</span></span>
- <span data-ttu-id="97b6b-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="97b6b-120">Stop</span></span>
- <span data-ttu-id="97b6b-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="97b6b-121">Suspend</span></span>

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

### <span data-ttu-id="97b6b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="97b6b-122">-InformationVariable</span></span>
<span data-ttu-id="97b6b-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="97b6b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="97b6b-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="97b6b-124">-Profile</span></span>
<span data-ttu-id="97b6b-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97b6b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="97b6b-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="97b6b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="97b6b-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="97b6b-127">-ServiceName</span></span>
<span data-ttu-id="97b6b-128">Określa nazwę usługi, dla której to polecenie cmdlet pobiera szczegóły wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="97b6b-128">Specifies the name of the service for which this cmdlet gets details for an internal load balancer.</span></span>

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

### <span data-ttu-id="97b6b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97b6b-129">CommonParameters</span></span>
<span data-ttu-id="97b6b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97b6b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97b6b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97b6b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97b6b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="97b6b-132">INPUTS</span></span>

## <span data-ttu-id="97b6b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="97b6b-133">OUTPUTS</span></span>

### <span data-ttu-id="97b6b-134">Microsoft. platformy windowsazure. Commands. servicemanagement. model. InternalLoadBalancerContext</span><span class="sxs-lookup"><span data-stu-id="97b6b-134">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.InternalLoadBalancerContext</span></span>

## <span data-ttu-id="97b6b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="97b6b-135">NOTES</span></span>

## <span data-ttu-id="97b6b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="97b6b-136">RELATED LINKS</span></span>

[<span data-ttu-id="97b6b-137">Dodaj-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97b6b-137">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="97b6b-138">Get-AzureService</span><span class="sxs-lookup"><span data-stu-id="97b6b-138">Get-AzureService</span></span>](./Get-AzureService.md)

[<span data-ttu-id="97b6b-139">Nowe — AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="97b6b-139">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="97b6b-140">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97b6b-140">Remove-AzureInternalLoadBalancer</span></span>](./Remove-AzureInternalLoadBalancer.md)

[<span data-ttu-id="97b6b-141">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="97b6b-141">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


