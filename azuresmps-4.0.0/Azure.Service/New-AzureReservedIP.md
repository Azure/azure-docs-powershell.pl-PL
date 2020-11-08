---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 9C22F5D7-1FD0-4699-83D7-1D72C5234DEF
online version: ''
schema: 2.0.0
ms.openlocfilehash: d09173c43de9c01056055f714217db5eb4c58225
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054959"
---
# <span data-ttu-id="87715-101">New-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="87715-101">New-AzureReservedIP</span></span>

## <span data-ttu-id="87715-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87715-102">SYNOPSIS</span></span>
<span data-ttu-id="87715-103">Tworzy zastrzeżony adres IP.</span><span class="sxs-lookup"><span data-stu-id="87715-103">Creates a reserved IP address.</span></span>

## <span data-ttu-id="87715-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87715-104">SYNTAX</span></span>

### <span data-ttu-id="87715-105">CreateNewReservedIP (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87715-105">CreateNewReservedIP (Default)</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="87715-106">CreateInUseReservedIPUsingSlot</span><span class="sxs-lookup"><span data-stu-id="87715-106">CreateInUseReservedIPUsingSlot</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="87715-107">CreateInUseReservedIP</span><span class="sxs-lookup"><span data-stu-id="87715-107">CreateInUseReservedIP</span></span>
```
New-AzureReservedIP [-ReservedIPName] <String> [[-Label] <String>] [-Location] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="87715-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87715-108">DESCRIPTION</span></span>
<span data-ttu-id="87715-109">Polecenie cmdlet **New-AzureReservedIP** tworzy zastrzeżony adres IP.</span><span class="sxs-lookup"><span data-stu-id="87715-109">The **New-AzureReservedIP** cmdlet creates a reserved IP address.</span></span>

## <span data-ttu-id="87715-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87715-110">EXAMPLES</span></span>

### <span data-ttu-id="87715-111">Przykład 1. Tworzenie nowego zastrzeżonego adresu IP</span><span class="sxs-lookup"><span data-stu-id="87715-111">Example 1: Create a new reserved IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName $Name -Label $Label -Location $Location
```

<span data-ttu-id="87715-112">To polecenie tworzy nowy zastrzeżony adres IP w subskrypcji, którego można użyć do tworzenia usług chmury obejmujących sieci Web, pracowników i maszyny wirtualne.</span><span class="sxs-lookup"><span data-stu-id="87715-112">This command creates a new reserved IP address in the subscription, which can be used for creating cloud services that include Web, Worker, and Virtual Machines.</span></span>

### <span data-ttu-id="87715-113">Przykład 2: Tworzenie zastrzeżonego adresu IP na podstawie istniejącego adresu IP</span><span class="sxs-lookup"><span data-stu-id="87715-113">Example 2: Create a reserved IP based on an existing IP</span></span>
```
PS C:\> New-AzureReservedIP -ReservedIPName resip14 -Location "West Europe" -ServiceName piptestwesteurope
```

<span data-ttu-id="87715-114">To polecenie tworzy istniejący wirtualny adres IP w określonej usłudze.</span><span class="sxs-lookup"><span data-stu-id="87715-114">This command creates an existing VIP (Virtual IP) on the specified service.</span></span>

## <span data-ttu-id="87715-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87715-115">PARAMETERS</span></span>

### <span data-ttu-id="87715-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="87715-116">-InformationAction</span></span>
<span data-ttu-id="87715-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="87715-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="87715-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="87715-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="87715-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="87715-119">Continue</span></span>
- <span data-ttu-id="87715-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="87715-120">Ignore</span></span>
- <span data-ttu-id="87715-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="87715-121">Inquire</span></span>
- <span data-ttu-id="87715-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="87715-122">SilentlyContinue</span></span>
- <span data-ttu-id="87715-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="87715-123">Stop</span></span>
- <span data-ttu-id="87715-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="87715-124">Suspend</span></span>

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

### <span data-ttu-id="87715-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="87715-125">-InformationVariable</span></span>
<span data-ttu-id="87715-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="87715-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="87715-127">-Label</span><span class="sxs-lookup"><span data-stu-id="87715-127">-Label</span></span>
<span data-ttu-id="87715-128">Określa etykietę zastrzeżonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="87715-128">Specifies a label for the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87715-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="87715-129">-Location</span></span>
<span data-ttu-id="87715-130">Określa lokalizację, w której ma zostać utworzony zastrzeżony adres IP.</span><span class="sxs-lookup"><span data-stu-id="87715-130">Specifies a location at which to create the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87715-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="87715-131">-Profile</span></span>
<span data-ttu-id="87715-132">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="87715-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="87715-133">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="87715-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="87715-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="87715-134">-ReservedIPName</span></span>
<span data-ttu-id="87715-135">Określa nazwę zastrzeżonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="87715-135">Specifies the reserved IP address name.</span></span>

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

### <span data-ttu-id="87715-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="87715-136">-ServiceName</span></span>
<span data-ttu-id="87715-137">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="87715-137">Specifies a service name.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87715-138">-Slot</span><span class="sxs-lookup"><span data-stu-id="87715-138">-Slot</span></span>
<span data-ttu-id="87715-139">Określa miejsce wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="87715-139">Specifies the deployment slot.</span></span>
<span data-ttu-id="87715-140">Dopuszczalne wartości tego parametru to: przemieszczanie, produkcja.</span><span class="sxs-lookup"><span data-stu-id="87715-140">The acceptable values for this parameter are: Staging, Production.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87715-141">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="87715-141">-VirtualIPName</span></span>
<span data-ttu-id="87715-142">Określa, że w tym poleceniu cmdlet jest używany parametr **VirtualIPName** w celu zarezerwowania istniejącego wirtualnego adresu IP (VIP) we wdrożeniu.</span><span class="sxs-lookup"><span data-stu-id="87715-142">Specifies that this cmdlet uses the **VirtualIPName** parameter to reserve an existing virtual IP address (VIP) in your deployment.</span></span>
<span data-ttu-id="87715-143">Jeśli ten parametr nie jest określony, polecenie cmdlet rezerwuje nowy wirtualny adres IP.</span><span class="sxs-lookup"><span data-stu-id="87715-143">If this parameter is not specified, this cmdlet reserves a new VIP.</span></span>

```yaml
Type: String
Parameter Sets: CreateInUseReservedIP
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87715-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87715-144">CommonParameters</span></span>
<span data-ttu-id="87715-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87715-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87715-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87715-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87715-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87715-147">INPUTS</span></span>

## <span data-ttu-id="87715-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87715-148">OUTPUTS</span></span>

## <span data-ttu-id="87715-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87715-149">NOTES</span></span>

## <span data-ttu-id="87715-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87715-150">RELATED LINKS</span></span>

[<span data-ttu-id="87715-151">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="87715-151">Get-AzureReservedIP</span></span>](./Get-AzureReservedIP.md)

[<span data-ttu-id="87715-152">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="87715-152">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


