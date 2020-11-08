---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CCA6334F-A193-4506-B873-76F29980C68D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25749aca2d0fb2682404d6c4d006c8ad1b1f3c6b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055302"
---
# <span data-ttu-id="06ce0-101">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="06ce0-101">Get-AzureLocation</span></span>

## <span data-ttu-id="06ce0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="06ce0-103">Pobiera dostępne lokalizacje centrum danych dla bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06ce0-103">Gets the available data center locations for the current Azure subscription.</span></span>

## <span data-ttu-id="06ce0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06ce0-104">SYNTAX</span></span>

```
Get-AzureLocation [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="06ce0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="06ce0-106">Polecenie cmdlet **Get-AzureLocation** pobiera listę dostępnych centrów danych platformy Azure oraz ich właściwości dla bieżącej subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06ce0-106">The **Get-AzureLocation** cmdlet gets a list of the available Azure data centers and their properties for the current Azure subscription.</span></span>
<span data-ttu-id="06ce0-107">Przed uruchomieniem tego polecenia cmdlet musisz ustawić bieżącą subskrypcję za pomocą poleceń cmdlet Select-AzureSubscription i Set-AzureSubscription.</span><span class="sxs-lookup"><span data-stu-id="06ce0-107">Before you run this cmdlet, you must set your current subscription by using the Select-AzureSubscription and Set-AzureSubscription cmdlets.</span></span>

## <span data-ttu-id="06ce0-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06ce0-108">EXAMPLES</span></span>

### <span data-ttu-id="06ce0-109">Przykład 1: Pobieranie lokalizacji</span><span class="sxs-lookup"><span data-stu-id="06ce0-109">Example 1: Get locations</span></span>
```
PS C:\> Get-AzureLocation
```

<span data-ttu-id="06ce0-110">To polecenie umożliwia wyświetlenie listy dostępnych centrów danych oraz ich właściwości dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="06ce0-110">This command gets a list of available data centers, and their properties, for the current subscription.</span></span>

## <span data-ttu-id="06ce0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06ce0-111">PARAMETERS</span></span>

### <span data-ttu-id="06ce0-112">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="06ce0-112">-InformationAction</span></span>
<span data-ttu-id="06ce0-113">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="06ce0-113">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="06ce0-114">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="06ce0-114">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="06ce0-115">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="06ce0-115">Continue</span></span>
- <span data-ttu-id="06ce0-116">Ignorować</span><span class="sxs-lookup"><span data-stu-id="06ce0-116">Ignore</span></span>
- <span data-ttu-id="06ce0-117">Inquire</span><span class="sxs-lookup"><span data-stu-id="06ce0-117">Inquire</span></span>
- <span data-ttu-id="06ce0-118">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="06ce0-118">SilentlyContinue</span></span>
- <span data-ttu-id="06ce0-119">Przestaw</span><span class="sxs-lookup"><span data-stu-id="06ce0-119">Stop</span></span>
- <span data-ttu-id="06ce0-120">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="06ce0-120">Suspend</span></span>

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

### <span data-ttu-id="06ce0-121">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="06ce0-121">-InformationVariable</span></span>
<span data-ttu-id="06ce0-122">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="06ce0-122">Specifies an information variable.</span></span>

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

### <span data-ttu-id="06ce0-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="06ce0-123">-Profile</span></span>
<span data-ttu-id="06ce0-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ce0-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="06ce0-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="06ce0-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="06ce0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ce0-126">CommonParameters</span></span>
<span data-ttu-id="06ce0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ce0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ce0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06ce0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ce0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ce0-129">INPUTS</span></span>

## <span data-ttu-id="06ce0-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06ce0-130">OUTPUTS</span></span>

## <span data-ttu-id="06ce0-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06ce0-131">NOTES</span></span>

## <span data-ttu-id="06ce0-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06ce0-132">RELATED LINKS</span></span>

