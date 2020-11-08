---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FBED8515-4216-4AB6-B34E-D14A6063A3A7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c2f145ec51bc6744d877661554e3d8e475d722fb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054679"
---
# <span data-ttu-id="b1068-101">Add-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="b1068-101">Add-AzureVirtualIP</span></span>

## <span data-ttu-id="b1068-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1068-102">SYNOPSIS</span></span>
<span data-ttu-id="b1068-103">Dodaje wirtualny adres IP do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="b1068-103">Adds a virtual IP to a cloud service.</span></span>

## <span data-ttu-id="b1068-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1068-104">SYNTAX</span></span>

```
Add-AzureVirtualIP [-ServiceName] <String> [-VirtualIPName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1068-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b1068-105">DESCRIPTION</span></span>
<span data-ttu-id="b1068-106">Polecenie cmdlet **Add-AzureVirtualIP** dodaje nowy wirtualny adres IP (VIP) do usługi platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b1068-106">The **Add-AzureVirtualIP** cmdlet adds a new virtual IP (VIP) to your Azure service.</span></span>
<span data-ttu-id="b1068-107">Nowy wirtualny adres IP ma nazwę, ale nie ma przydzielonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="b1068-107">The new virtual IP has a name but is not allocated an IP address.</span></span>

<span data-ttu-id="b1068-108">Adres IP jest przydzielany tylko w przypadku skojarzenia punktu końcowego z adresem VIP.</span><span class="sxs-lookup"><span data-stu-id="b1068-108">The IP address is allocated only when you associate an endpoint to the VIP.</span></span>
<span data-ttu-id="b1068-109">Aby uzyskać więcej informacji, zobacz Add-AzureEndpoint.</span><span class="sxs-lookup"><span data-stu-id="b1068-109">See Add-AzureEndpoint for more details.</span></span>

<span data-ttu-id="b1068-110">Abonament jest naliczany za dodatkowe adresy VIP tylko wtedy, gdy są skojarzone z punktem końcowym.</span><span class="sxs-lookup"><span data-stu-id="b1068-110">Your subscription is charged for extra VIPs only once they are associated with an endpoint.</span></span>

## <span data-ttu-id="b1068-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1068-111">EXAMPLES</span></span>

### <span data-ttu-id="b1068-112">Przykład 1: Dodawanie wirtualnego adresu IP do usługi</span><span class="sxs-lookup"><span data-stu-id="b1068-112">Example 1: Add a virtual IP to a service</span></span>
```
PS C:\> Add-AzureVirtualIP -VirtualIPName "Vip01" -ServiceName "ContosoService03"
OperationDescription OperationId                          OperationStatus
-------------------- -----------                          ---------------
Add-AzureVirtualIP   4bd7b638-d2e7-216f-ba38-5221233d70ce Succeeded
```

<span data-ttu-id="b1068-113">To polecenie dodaje wirtualny adres IP do usługi.</span><span class="sxs-lookup"><span data-stu-id="b1068-113">This command adds a virtual IP address to a service.</span></span>

## <span data-ttu-id="b1068-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1068-114">PARAMETERS</span></span>

### <span data-ttu-id="b1068-115">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1068-115">-InformationAction</span></span>
<span data-ttu-id="b1068-116">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="b1068-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1068-117">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b1068-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1068-118">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="b1068-118">Continue</span></span>
- <span data-ttu-id="b1068-119">Ignorować</span><span class="sxs-lookup"><span data-stu-id="b1068-119">Ignore</span></span>
- <span data-ttu-id="b1068-120">Inquire</span><span class="sxs-lookup"><span data-stu-id="b1068-120">Inquire</span></span>
- <span data-ttu-id="b1068-121">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1068-121">SilentlyContinue</span></span>
- <span data-ttu-id="b1068-122">Przestaw</span><span class="sxs-lookup"><span data-stu-id="b1068-122">Stop</span></span>
- <span data-ttu-id="b1068-123">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="b1068-123">Suspend</span></span>

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

### <span data-ttu-id="b1068-124">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1068-124">-InformationVariable</span></span>
<span data-ttu-id="b1068-125">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="b1068-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b1068-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="b1068-126">-Profile</span></span>
<span data-ttu-id="b1068-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b1068-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b1068-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="b1068-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b1068-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b1068-129">-ServiceName</span></span>
<span data-ttu-id="b1068-130">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="b1068-130">Specifies the name of the service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1068-131">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="b1068-131">-VirtualIPName</span></span>
<span data-ttu-id="b1068-132">Określa nazwę wirtualnego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="b1068-132">Specifies the name of the virtual IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1068-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1068-133">CommonParameters</span></span>
<span data-ttu-id="b1068-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1068-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1068-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1068-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1068-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1068-136">INPUTS</span></span>

## <span data-ttu-id="b1068-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1068-137">OUTPUTS</span></span>

### <span data-ttu-id="b1068-138">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="b1068-138">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="b1068-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1068-139">NOTES</span></span>

## <span data-ttu-id="b1068-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1068-140">RELATED LINKS</span></span>

[<span data-ttu-id="b1068-141">Dodaj-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="b1068-141">Add-AzureEndpoint</span></span>](./Add-AzureEndpoint.md)

[<span data-ttu-id="b1068-142">Remove-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="b1068-142">Remove-AzureVirtualIP</span></span>](./Remove-AzureVirtualIP.md)


