---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 4E059EF1-740C-4AEB-AF41-BF6003BE15F2
online version: ''
schema: 2.0.0
ms.openlocfilehash: a52f2585771ec10d6acf52b14c88bd1ed0af0427
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054902"
---
# <span data-ttu-id="e461f-101">Test-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="e461f-101">Test-AzureStaticVNetIP</span></span>

## <span data-ttu-id="e461f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e461f-102">SYNOPSIS</span></span>
<span data-ttu-id="e461f-103">Sprawdza dostępność statycznego adresu IP sieci wirtualnej i pobiera listę sugestii, jeśli poszukiwany adres jest niedostępny.</span><span class="sxs-lookup"><span data-stu-id="e461f-103">Tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="e461f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e461f-104">SYNTAX</span></span>

```
Test-AzureStaticVNetIP [-VNetName] <String> [-IPAddress] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e461f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e461f-105">DESCRIPTION</span></span>
<span data-ttu-id="e461f-106">Polecenie cmdlet **test-AzureStaticVNetIP** sprawdza dostępność statycznego adresu IP sieci wirtualnej i pobiera listę sugestii, jeśli poszukiwany adres jest niedostępny.</span><span class="sxs-lookup"><span data-stu-id="e461f-106">The **Test-AzureStaticVNetIP** cmdlet tests the availability of a static virtual network IP address, and gets a list of suggestions if the queried address is not available.</span></span>

## <span data-ttu-id="e461f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e461f-107">EXAMPLES</span></span>

### <span data-ttu-id="e461f-108">1:1</span><span class="sxs-lookup"><span data-stu-id="e461f-108">1:</span></span>
```

```

## <span data-ttu-id="e461f-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e461f-109">PARAMETERS</span></span>

### <span data-ttu-id="e461f-110">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e461f-110">-InformationAction</span></span>
<span data-ttu-id="e461f-111">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e461f-111">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e461f-112">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e461f-112">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e461f-113">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e461f-113">Continue</span></span>
- <span data-ttu-id="e461f-114">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e461f-114">Ignore</span></span>
- <span data-ttu-id="e461f-115">Inquire</span><span class="sxs-lookup"><span data-stu-id="e461f-115">Inquire</span></span>
- <span data-ttu-id="e461f-116">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e461f-116">SilentlyContinue</span></span>
- <span data-ttu-id="e461f-117">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e461f-117">Stop</span></span>
- <span data-ttu-id="e461f-118">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e461f-118">Suspend</span></span>

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

### <span data-ttu-id="e461f-119">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e461f-119">-InformationVariable</span></span>
<span data-ttu-id="e461f-120">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e461f-120">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e461f-121">-Adres_IP</span><span class="sxs-lookup"><span data-stu-id="e461f-121">-IPAddress</span></span>
<span data-ttu-id="e461f-122">Określa statyczny adres IP sieci wirtualnej do zbadania.</span><span class="sxs-lookup"><span data-stu-id="e461f-122">Specifies the static virtual network IP address to query.</span></span>

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

### <span data-ttu-id="e461f-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="e461f-123">-Profile</span></span>
<span data-ttu-id="e461f-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e461f-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e461f-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e461f-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e461f-126">-VNetName</span><span class="sxs-lookup"><span data-stu-id="e461f-126">-VNetName</span></span>
<span data-ttu-id="e461f-127">Określa nazwę sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e461f-127">Specifies the Name of the virtual network.</span></span>

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

### <span data-ttu-id="e461f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e461f-128">CommonParameters</span></span>
<span data-ttu-id="e461f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e461f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e461f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e461f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e461f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e461f-131">INPUTS</span></span>

## <span data-ttu-id="e461f-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e461f-132">OUTPUTS</span></span>

## <span data-ttu-id="e461f-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e461f-133">NOTES</span></span>

## <span data-ttu-id="e461f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e461f-134">RELATED LINKS</span></span>

[<span data-ttu-id="e461f-135">Get-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="e461f-135">Get-AzureStaticVNetIP</span></span>](./Get-AzureStaticVNetIP.md)

[<span data-ttu-id="e461f-136">Set-AzureStaticVNetIP</span><span class="sxs-lookup"><span data-stu-id="e461f-136">Set-AzureStaticVNetIP</span></span>](./Set-AzureStaticVNetIP.md)


