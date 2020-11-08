---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 3249E908-B1D9-4707-844D-168274F1A466
online version: ''
schema: 2.0.0
ms.openlocfilehash: ae16609adf70b2e5a0edcd05c36b30860a3920cf
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054791"
---
# <span data-ttu-id="98fee-101">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="98fee-101">Set-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="98fee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98fee-102">SYNOPSIS</span></span>
<span data-ttu-id="98fee-103">Kojarzy zarezerwowany adres IP z istniejącą maszyną wirtualną lub usługą w chmurze.</span><span class="sxs-lookup"><span data-stu-id="98fee-103">Associates a reserved IP address with an existing virtual machine or cloud service.</span></span>

## <span data-ttu-id="98fee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98fee-104">SYNTAX</span></span>

```
Set-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String> [[-VirtualIPName] <String>]
 [[-Slot] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="98fee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="98fee-105">DESCRIPTION</span></span>
<span data-ttu-id="98fee-106">Polecenie cmdlet **Set-AzureReservedIPAssociation** kojarzy zarezerwowany adres IP z wirtualnym adresem IP (VIP) uruchomionej maszyny wirtualnej lub usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="98fee-106">The **Set-AzureReservedIPAssociation** cmdlet associates a reserved IP address with the Virtual IP address (VIP) of a running virtual machine or cloud service.</span></span>
<span data-ttu-id="98fee-107">Zastrzeżony adres IP nie może być używany w czasie wywoływania tego polecenia cmdlet i musi znajdować się w tym samym regionie co maszyna wirtualna lub usługa w chmurze.</span><span class="sxs-lookup"><span data-stu-id="98fee-107">The reserved IP address must not be in use at the time of invocation of this cmdlet, and must be in the same region as the virtual machine or cloud service.</span></span>

<span data-ttu-id="98fee-108">Wykonywanie operacji trwa około 30 sekund, po czym maszyna wirtualna lub usługa jest dostępna przy użyciu zastrzeżonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="98fee-108">The operation takes about 30 seconds to complete, after which the virtual machine or service is accessible using the reserved IP address.</span></span>

## <span data-ttu-id="98fee-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98fee-109">EXAMPLES</span></span>

### <span data-ttu-id="98fee-110">Przykład 1: Ustawianie zastrzeżonego skojarzenia adresów IP</span><span class="sxs-lookup"><span data-stu-id="98fee-110">Example 1: Set a reserved IP association</span></span>
```
PS C:\> Set-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="98fee-111">To polecenie powoduje przypisanie zastrzeżonego adresu IP o nazwie ResIp14 do PipTestWestEurope usługi.</span><span class="sxs-lookup"><span data-stu-id="98fee-111">This command assigns the reserved IP address named ResIp14 to the service PipTestWestEurope.</span></span>
<span data-ttu-id="98fee-112">ResIp14 jest zastrzeżonym adresem IP w regionie Europa Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="98fee-112">ResIp14 is a reserved IP in the West Europe region.</span></span>

## <span data-ttu-id="98fee-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98fee-113">PARAMETERS</span></span>

### <span data-ttu-id="98fee-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="98fee-114">-InformationAction</span></span>
<span data-ttu-id="98fee-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="98fee-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="98fee-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="98fee-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98fee-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="98fee-117">Continue</span></span>
- <span data-ttu-id="98fee-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="98fee-118">Ignore</span></span>
- <span data-ttu-id="98fee-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="98fee-119">Inquire</span></span>
- <span data-ttu-id="98fee-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="98fee-120">SilentlyContinue</span></span>
- <span data-ttu-id="98fee-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="98fee-121">Stop</span></span>
- <span data-ttu-id="98fee-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="98fee-122">Suspend</span></span>

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

### <span data-ttu-id="98fee-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="98fee-123">-InformationVariable</span></span>
<span data-ttu-id="98fee-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="98fee-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="98fee-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="98fee-125">-Profile</span></span>
<span data-ttu-id="98fee-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98fee-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98fee-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="98fee-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98fee-128">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="98fee-128">-ReservedIPName</span></span>
<span data-ttu-id="98fee-129">Określa nazwę zastrzeżonego adresu IP, który ma być skojarzony z maszyną wirtualną lub usługą.</span><span class="sxs-lookup"><span data-stu-id="98fee-129">Specifies the name of the reserved IP address to associate with a virtual machine or service.</span></span>

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

### <span data-ttu-id="98fee-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="98fee-130">-ServiceName</span></span>
<span data-ttu-id="98fee-131">Określa nazwę usługi, z którą ma być skojarzony zastrzeżony adres IP.</span><span class="sxs-lookup"><span data-stu-id="98fee-131">Specifies the name of the service that has the deployment with which to associate the reserved IP address.</span></span>

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

### <span data-ttu-id="98fee-132">-Slot</span><span class="sxs-lookup"><span data-stu-id="98fee-132">-Slot</span></span>
<span data-ttu-id="98fee-133">Określa miejsce wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="98fee-133">Specifies the deployment slot.</span></span>
<span data-ttu-id="98fee-134">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="98fee-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="98fee-135">Most</span><span class="sxs-lookup"><span data-stu-id="98fee-135">Staging</span></span>
- <span data-ttu-id="98fee-136">BOM</span><span class="sxs-lookup"><span data-stu-id="98fee-136">Production</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fee-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="98fee-137">-VirtualIPName</span></span>
<span data-ttu-id="98fee-138">Określa nazwę istniejącego VIP, które ma zostać skojarzone z zastrzeżonym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="98fee-138">Specifies the name of an existing VIP to associate with a reserved IP.</span></span>
<span data-ttu-id="98fee-139">Zobacz Add-AzureVirtualIP, aby dodać adresy VIP do usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="98fee-139">See Add-AzureVirtualIP to add VIPs to your cloud service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98fee-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98fee-140">CommonParameters</span></span>
<span data-ttu-id="98fee-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98fee-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98fee-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98fee-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98fee-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98fee-143">INPUTS</span></span>

## <span data-ttu-id="98fee-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98fee-144">OUTPUTS</span></span>

### <span data-ttu-id="98fee-145">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="98fee-145">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="98fee-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98fee-146">NOTES</span></span>

## <span data-ttu-id="98fee-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98fee-147">RELATED LINKS</span></span>

[<span data-ttu-id="98fee-148">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="98fee-148">Remove-AzureReservedIPAssociation</span></span>](./Remove-AzureReservedIPAssociation.md)


