---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F956CC89-A2CA-4D73-8014-C36778C51927
online version: ''
schema: 2.0.0
ms.openlocfilehash: eba992b183795d016108419834c38bcf64a82d41
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055134"
---
# <span data-ttu-id="1efd2-101">Remove-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1efd2-101">Remove-AzureAvailabilitySet</span></span>

## <span data-ttu-id="1efd2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1efd2-102">SYNOPSIS</span></span>
<span data-ttu-id="1efd2-103">Usuwa zestaw dostępności z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1efd2-103">Removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="1efd2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1efd2-104">SYNTAX</span></span>

```
Remove-AzureAvailabilitySet -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1efd2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1efd2-105">DESCRIPTION</span></span>
<span data-ttu-id="1efd2-106">Polecenie cmdlet **Remove-AzureAvailabilitySet** umożliwia usunięcie zestawu dostępności z maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1efd2-106">The **Remove-AzureAvailabilitySet** cmdlet removes an availability set from an Azure virtual machine.</span></span>

## <span data-ttu-id="1efd2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1efd2-107">EXAMPLES</span></span>

### <span data-ttu-id="1efd2-108">1:1</span><span class="sxs-lookup"><span data-stu-id="1efd2-108">1:</span></span>
```

```

## <span data-ttu-id="1efd2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1efd2-109">PARAMETERS</span></span>

### <span data-ttu-id="1efd2-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1efd2-110">-InformationAction</span></span>
<span data-ttu-id="1efd2-111">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1efd2-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1efd2-112">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1efd2-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1efd2-113">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1efd2-113">Continue</span></span>
- <span data-ttu-id="1efd2-114">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1efd2-114">Ignore</span></span>
- <span data-ttu-id="1efd2-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="1efd2-115">Inquire</span></span>
- <span data-ttu-id="1efd2-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1efd2-116">SilentlyContinue</span></span>
- <span data-ttu-id="1efd2-117">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1efd2-117">Stop</span></span>
- <span data-ttu-id="1efd2-118">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1efd2-118">Suspend</span></span>

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

### <span data-ttu-id="1efd2-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1efd2-119">-InformationVariable</span></span>
<span data-ttu-id="1efd2-120">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1efd2-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1efd2-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="1efd2-121">-Profile</span></span>
<span data-ttu-id="1efd2-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1efd2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1efd2-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1efd2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1efd2-124">-VM</span><span class="sxs-lookup"><span data-stu-id="1efd2-124">-VM</span></span>
<span data-ttu-id="1efd2-125">Określa maszynę wirtualną, z której to polecenie cmdlet usuwa zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="1efd2-125">Specifies the virtual machine from which this cmdlet removes an availability set.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1efd2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1efd2-126">CommonParameters</span></span>
<span data-ttu-id="1efd2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1efd2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1efd2-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1efd2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1efd2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1efd2-129">INPUTS</span></span>

## <span data-ttu-id="1efd2-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1efd2-130">OUTPUTS</span></span>

## <span data-ttu-id="1efd2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1efd2-131">NOTES</span></span>

## <span data-ttu-id="1efd2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1efd2-132">RELATED LINKS</span></span>

[<span data-ttu-id="1efd2-133">Set-AzureAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1efd2-133">Set-AzureAvailabilitySet</span></span>](./Set-AzureAvailabilitySet.md)


