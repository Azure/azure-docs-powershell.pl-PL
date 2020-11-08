---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 94D20309-5F72-4BE5-A150-2D6DD754286A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a9d793bb9bc8d96150b812474bed9f8997adbe1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055070"
---
# <span data-ttu-id="da8d2-101">Remove-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="da8d2-101">Remove-AzureStaticVNetIP</span></span>

## <span data-ttu-id="da8d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="da8d2-102">SYNOPSIS</span></span>
<span data-ttu-id="da8d2-103">Usuwa informacje o statycznym adresie IP sieci wirtualnej z obiektu maszyny wirtualnej (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="da8d2-103">Removes the static virtual network IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="da8d2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="da8d2-104">SYNTAX</span></span>

```
Remove-AzureStaticVNetIP -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="da8d2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="da8d2-105">DESCRIPTION</span></span>
<span data-ttu-id="da8d2-106">Polecenie cmdlet **Remove-AzureStaticVNetIP** usuwa informacje o adresie IP statycznej sieci wirtualnej (wirtualnej) z obiektu maszyny wirtualnej (jeśli istnieje).</span><span class="sxs-lookup"><span data-stu-id="da8d2-106">The **Remove-AzureStaticVNetIP** cmdlet removes the static virtual network (VNet) IP address information from a virtual machine object, if any.</span></span>

## <span data-ttu-id="da8d2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="da8d2-107">EXAMPLES</span></span>

### <span data-ttu-id="da8d2-108">1:1</span><span class="sxs-lookup"><span data-stu-id="da8d2-108">1:</span></span>
```

```

## <span data-ttu-id="da8d2-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="da8d2-109">PARAMETERS</span></span>

### <span data-ttu-id="da8d2-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="da8d2-110">-InformationAction</span></span>
<span data-ttu-id="da8d2-111">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="da8d2-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="da8d2-112">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="da8d2-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="da8d2-113">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="da8d2-113">Continue</span></span>
- <span data-ttu-id="da8d2-114">Ignorować</span><span class="sxs-lookup"><span data-stu-id="da8d2-114">Ignore</span></span>
- <span data-ttu-id="da8d2-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="da8d2-115">Inquire</span></span>
- <span data-ttu-id="da8d2-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="da8d2-116">SilentlyContinue</span></span>
- <span data-ttu-id="da8d2-117">Przestaw</span><span class="sxs-lookup"><span data-stu-id="da8d2-117">Stop</span></span>
- <span data-ttu-id="da8d2-118">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="da8d2-118">Suspend</span></span>

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

### <span data-ttu-id="da8d2-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="da8d2-119">-InformationVariable</span></span>
<span data-ttu-id="da8d2-120">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="da8d2-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="da8d2-121">-Profile</span><span class="sxs-lookup"><span data-stu-id="da8d2-121">-Profile</span></span>
<span data-ttu-id="da8d2-122">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da8d2-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="da8d2-123">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="da8d2-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="da8d2-124">-VM</span><span class="sxs-lookup"><span data-stu-id="da8d2-124">-VM</span></span>
<span data-ttu-id="da8d2-125">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="da8d2-125">Specifies a persistent virtual machine object.</span></span>

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

### <span data-ttu-id="da8d2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da8d2-126">CommonParameters</span></span>
<span data-ttu-id="da8d2-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da8d2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da8d2-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da8d2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da8d2-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da8d2-129">INPUTS</span></span>

## <span data-ttu-id="da8d2-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="da8d2-130">OUTPUTS</span></span>

## <span data-ttu-id="da8d2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="da8d2-131">NOTES</span></span>

## <span data-ttu-id="da8d2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da8d2-132">RELATED LINKS</span></span>

[<span data-ttu-id="da8d2-133">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="da8d2-133">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="da8d2-134">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="da8d2-134">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


