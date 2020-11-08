---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: A6964C80-1991-46FC-84C8-5B00616386BE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9e43f841fea77626c18edbda541fa011e95faceb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055102"
---
# <span data-ttu-id="1d265-101">Remove-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="1d265-101">Remove-AzureReservedIPAssociation</span></span>

## <span data-ttu-id="1d265-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d265-102">SYNOPSIS</span></span>
<span data-ttu-id="1d265-103">Usuwa skojarzenie z zastrzeżonego adresu IP do maszyny wirtualnej lub usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="1d265-103">Removes the association from the reserved IP address to the VM or cloud service.</span></span>

## <span data-ttu-id="1d265-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d265-104">SYNTAX</span></span>

```
Remove-AzureReservedIPAssociation [-ReservedIPName] <String> [-ServiceName] <String>
 [[-VirtualIPName] <String>] [[-Slot] <String>] [-Force] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1d265-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d265-105">DESCRIPTION</span></span>
<span data-ttu-id="1d265-106">Polecenie cmdlet **Remove-AzureReservedIPAssociation** umożliwia powiązanie zastrzeżonego adresu IP z maszyny wirtualnej (VM) lub usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="1d265-106">The **Remove-AzureReservedIPAssociation** cmdlet disassociates a reserved IP address from a virtual machine (VM) or Cloud Service.</span></span>
<span data-ttu-id="1d265-107">Gdy operacja zostanie ukończona, zastrzeżony adres IP jest bezpłatny i maszyna wirtualna/VIP pobiera dynamiczny publiczny adres IP ze spisu Azure Inventory.</span><span class="sxs-lookup"><span data-stu-id="1d265-107">When the operation completes, the reserved IP address is free and the VM/VIP gets a dynamic public IP Address from the Azure Inventory.</span></span>

## <span data-ttu-id="1d265-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d265-108">EXAMPLES</span></span>

### <span data-ttu-id="1d265-109">Przykład 1: usuwanie zastrzeżonego skojarzenia adresów IP</span><span class="sxs-lookup"><span data-stu-id="1d265-109">Example 1: Remove a reserved IP association</span></span>
```
PS C:\> Remove-AzureReservedIPAssociation -ReservedIPName "ResIp14" -ServiceName "PipTestWestEurope"
```

<span data-ttu-id="1d265-110">To polecenie powoduje skojarzenie zastrzeżonego adresu IP o nazwie ResIp14 z usługą o nazwie PipTestWestEurope.</span><span class="sxs-lookup"><span data-stu-id="1d265-110">This command disassociates the reserved IP address named ResIp14 from the service named PipTestWestEurope.</span></span>
<span data-ttu-id="1d265-111">PipTestWestEurope zostanie przypisany nowy dynamiczny adres VIP.</span><span class="sxs-lookup"><span data-stu-id="1d265-111">PipTestWestEurope will be assigned a new dynamic VIP.</span></span>

## <span data-ttu-id="1d265-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d265-112">PARAMETERS</span></span>

### <span data-ttu-id="1d265-113">-Force</span><span class="sxs-lookup"><span data-stu-id="1d265-113">-Force</span></span>
<span data-ttu-id="1d265-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1d265-114">Forces the command to run without asking for user confirmation.</span></span>

<span data-ttu-id="1d265-115">Ta flaga służy do pomijania komunikatów ostrzegawczych podczas usuwania zarezerwowanych skojarzeń adresów IP.</span><span class="sxs-lookup"><span data-stu-id="1d265-115">Use this flag to bypass warning messages when removing the reserved IP association.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d265-116">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1d265-116">-InformationAction</span></span>
<span data-ttu-id="1d265-117">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1d265-117">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1d265-118">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1d265-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d265-119">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1d265-119">Continue</span></span>
- <span data-ttu-id="1d265-120">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1d265-120">Ignore</span></span>
- <span data-ttu-id="1d265-121">Inquire</span><span class="sxs-lookup"><span data-stu-id="1d265-121">Inquire</span></span>
- <span data-ttu-id="1d265-122">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1d265-122">SilentlyContinue</span></span>
- <span data-ttu-id="1d265-123">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1d265-123">Stop</span></span>
- <span data-ttu-id="1d265-124">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1d265-124">Suspend</span></span>

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

### <span data-ttu-id="1d265-125">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1d265-125">-InformationVariable</span></span>
<span data-ttu-id="1d265-126">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1d265-126">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1d265-127">-Profile</span><span class="sxs-lookup"><span data-stu-id="1d265-127">-Profile</span></span>
<span data-ttu-id="1d265-128">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d265-128">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1d265-129">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1d265-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1d265-130">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="1d265-130">-ReservedIPName</span></span>
<span data-ttu-id="1d265-131">Określa nazwę zastrzeżonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="1d265-131">Specifies the name of the reserved IP address.</span></span>

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

### <span data-ttu-id="1d265-132">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1d265-132">-ServiceName</span></span>
<span data-ttu-id="1d265-133">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="1d265-133">Specifies the  name of the service.</span></span>

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

### <span data-ttu-id="1d265-134">-Slot</span><span class="sxs-lookup"><span data-stu-id="1d265-134">-Slot</span></span>
<span data-ttu-id="1d265-135">Określa środowisko wdrażania.</span><span class="sxs-lookup"><span data-stu-id="1d265-135">Specifies the deployment environment.</span></span>
<span data-ttu-id="1d265-136">Dopuszczalne wartości tego parametru to: produkcja, etapy.</span><span class="sxs-lookup"><span data-stu-id="1d265-136">The acceptable values for this parameter are: Production, Staging.</span></span>

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

### <span data-ttu-id="1d265-137">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="1d265-137">-VirtualIPName</span></span>
<span data-ttu-id="1d265-138">Określa wirtualny adres IP, z którego ma zostać usunięte powiązanie z usługą lub maszyną wirtualną.</span><span class="sxs-lookup"><span data-stu-id="1d265-138">Specifies a virtual IP address from which to remove the association with a service or VM.</span></span>

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

### <span data-ttu-id="1d265-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d265-139">CommonParameters</span></span>
<span data-ttu-id="1d265-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d265-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d265-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d265-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d265-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d265-142">INPUTS</span></span>

## <span data-ttu-id="1d265-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d265-143">OUTPUTS</span></span>

### <span data-ttu-id="1d265-144">Microsoft. platformy windowsazure. Commands. Utilities. Common. ManagementOperationContext</span><span class="sxs-lookup"><span data-stu-id="1d265-144">Microsoft.WindowsAzure.Commands.Utilities.Common.ManagementOperationContext</span></span>

## <span data-ttu-id="1d265-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d265-145">NOTES</span></span>

## <span data-ttu-id="1d265-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d265-146">RELATED LINKS</span></span>

[<span data-ttu-id="1d265-147">Set-AzureReservedIPAssociation</span><span class="sxs-lookup"><span data-stu-id="1d265-147">Set-AzureReservedIPAssociation</span></span>](./Set-AzureReservedIPAssociation.md)


