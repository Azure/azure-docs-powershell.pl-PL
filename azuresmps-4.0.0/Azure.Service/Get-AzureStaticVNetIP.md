---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 12BF47AA-9E82-425E-A1EB-BAD64D800943
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3be6496993ed6de248103b9a222df4cbe15ed2ff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055523"
---
# <span data-ttu-id="0551d-101">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="0551d-101">Get-AzureStaticVNetIP</span></span>

## <span data-ttu-id="0551d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0551d-102">SYNOPSIS</span></span>
<span data-ttu-id="0551d-103">Pobiera z obiektu maszyny wirtualnej informacje o statycznym adresie IP VNet (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="0551d-103">Gets the static VNet IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="0551d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0551d-104">SYNTAX</span></span>

```
Get-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="0551d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0551d-105">DESCRIPTION</span></span>
<span data-ttu-id="0551d-106">Polecenie cmdlet **Get-AzureStaticVNetIP** pobiera informacje o adresie IP statycznej sieci wirtualnej (wirtualnej) z obiektu maszyny wirtualnej (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="0551d-106">The **Get-AzureStaticVNetIP** cmdlet gets the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="0551d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0551d-107">EXAMPLES</span></span>

### <span data-ttu-id="0551d-108">1:1</span><span class="sxs-lookup"><span data-stu-id="0551d-108">1:</span></span>
```

```

## <span data-ttu-id="0551d-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0551d-109">PARAMETERS</span></span>

### <span data-ttu-id="0551d-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="0551d-110">-InformationAction</span></span>
<span data-ttu-id="0551d-111">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="0551d-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="0551d-112">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0551d-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0551d-113">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="0551d-113">Continue</span></span>
- <span data-ttu-id="0551d-114">Ignorować</span><span class="sxs-lookup"><span data-stu-id="0551d-114">Ignore</span></span>
- <span data-ttu-id="0551d-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="0551d-115">Inquire</span></span>
- <span data-ttu-id="0551d-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="0551d-116">SilentlyContinue</span></span>
- <span data-ttu-id="0551d-117">Przestaw</span><span class="sxs-lookup"><span data-stu-id="0551d-117">Stop</span></span>
- <span data-ttu-id="0551d-118">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="0551d-118">Suspend</span></span>

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

### <span data-ttu-id="0551d-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="0551d-119">-InformationVariable</span></span>
<span data-ttu-id="0551d-120">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="0551d-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="0551d-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="0551d-121">-Profile</span></span>
<span data-ttu-id="0551d-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0551d-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0551d-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="0551d-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0551d-124">-VM</span><span class="sxs-lookup"><span data-stu-id="0551d-124">-VM</span></span>
<span data-ttu-id="0551d-125">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0551d-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="0551d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0551d-126">CommonParameters</span></span>
<span data-ttu-id="0551d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0551d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0551d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0551d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0551d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0551d-129">INPUTS</span></span>

## <span data-ttu-id="0551d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0551d-130">OUTPUTS</span></span>

## <span data-ttu-id="0551d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0551d-131">NOTES</span></span>

## <span data-ttu-id="0551d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0551d-132">RELATED LINKS</span></span>

[<span data-ttu-id="0551d-133">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="0551d-133">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


