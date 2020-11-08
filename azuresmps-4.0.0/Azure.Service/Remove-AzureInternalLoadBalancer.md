---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3F939FE9-5D42-4EA1-90DC-E6D60158CADE
online version: ''
schema: 2.0.0
ms.openlocfilehash: f2eb6fe50566a5de97f00876bdaa7061bbaf0587
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055441"
---
# <span data-ttu-id="41a28-101">Remove-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41a28-101">Remove-AzureInternalLoadBalancer</span></span>

## <span data-ttu-id="41a28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41a28-102">SYNOPSIS</span></span>
<span data-ttu-id="41a28-103">Umożliwia usunięcie konfiguracji wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="41a28-103">Removes an internal load balancer configuration.</span></span>

## <span data-ttu-id="41a28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41a28-104">SYNTAX</span></span>

```
Remove-AzureInternalLoadBalancer [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="41a28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41a28-105">DESCRIPTION</span></span>
<span data-ttu-id="41a28-106">Polecenie cmdlet **Remove-AzureInternalLoadBalancer** umożliwia usunięcie konfiguracji wewnętrznego modułu równoważenia obciążenia z usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="41a28-106">The **Remove-AzureInternalLoadBalancer** cmdlet removes the internal load balancer configuration from an Azure service.</span></span>
<span data-ttu-id="41a28-107">Jeśli jakiś punkt końcowy odwołuje się obecnie do wewnętrznego modułu równoważenia obciążenia, to polecenie cmdlet nie może usunąć konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="41a28-107">If any endpoint currently refers to the internal load balancer, this cmdlet cannot remove the configuration.</span></span>

## <span data-ttu-id="41a28-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41a28-108">EXAMPLES</span></span>

### <span data-ttu-id="41a28-109">Przykład 1: Usuwanie konfiguracji wewnętrznego modułu równoważenia obciążenia</span><span class="sxs-lookup"><span data-stu-id="41a28-109">Example 1: Remove an internal load balancer configuration</span></span>
```
PS C:\> Remove-AzureInternalLoadBalancer -ServiceName "ContosoService"
```

<span data-ttu-id="41a28-110">To polecenie powoduje usunięcie konfiguracji wewnętrznego modułu równoważenia obciążenia dla usługi o nazwie ContosoService.</span><span class="sxs-lookup"><span data-stu-id="41a28-110">This command removes the internal load balancer configuration for the service named ContosoService.</span></span>

## <span data-ttu-id="41a28-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41a28-111">PARAMETERS</span></span>

### <span data-ttu-id="41a28-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="41a28-112">-InformationAction</span></span>
<span data-ttu-id="41a28-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="41a28-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="41a28-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="41a28-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="41a28-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="41a28-115">Continue</span></span>
- <span data-ttu-id="41a28-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="41a28-116">Ignore</span></span>
- <span data-ttu-id="41a28-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="41a28-117">Inquire</span></span>
- <span data-ttu-id="41a28-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="41a28-118">SilentlyContinue</span></span>
- <span data-ttu-id="41a28-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="41a28-119">Stop</span></span>
- <span data-ttu-id="41a28-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="41a28-120">Suspend</span></span>

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

### <span data-ttu-id="41a28-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="41a28-121">-InformationVariable</span></span>
<span data-ttu-id="41a28-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="41a28-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="41a28-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="41a28-123">-Profile</span></span>
<span data-ttu-id="41a28-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="41a28-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="41a28-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="41a28-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="41a28-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="41a28-126">-ServiceName</span></span>
<span data-ttu-id="41a28-127">Określa nazwę usługi, z poziomu której to polecenie cmdlet powoduje usunięcie wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="41a28-127">Specifies the name of the service from which this cmdlet removes an internal load balancer.</span></span>

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

### <span data-ttu-id="41a28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a28-128">CommonParameters</span></span>
<span data-ttu-id="41a28-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a28-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a28-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a28-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41a28-131">INPUTS</span></span>

## <span data-ttu-id="41a28-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41a28-132">OUTPUTS</span></span>

### <span data-ttu-id="41a28-133">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="41a28-133">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="41a28-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41a28-134">NOTES</span></span>

## <span data-ttu-id="41a28-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41a28-135">RELATED LINKS</span></span>

[<span data-ttu-id="41a28-136">Dodaj-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41a28-136">Add-AzureInternalLoadBalancer</span></span>](./Add-AzureInternalLoadBalancer.md)

[<span data-ttu-id="41a28-137">Get-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41a28-137">Get-AzureInternalLoadBalancer</span></span>](./Get-AzureInternalLoadBalancer.md)

[<span data-ttu-id="41a28-138">Nowe — AzureInternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="41a28-138">New-AzureInternalLoadBalancerConfig</span></span>](./New-AzureInternalLoadBalancerConfig.md)

[<span data-ttu-id="41a28-139">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="41a28-139">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


