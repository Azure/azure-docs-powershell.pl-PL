---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: CFAA371E-F320-4FC3-80E0-5C857E5C0998
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0fbb80550acb0c743a3134a315f790bc25fb793a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055493"
---
# <span data-ttu-id="7784d-101">Get-AzureVNetSite</span><span class="sxs-lookup"><span data-stu-id="7784d-101">Get-AzureVNetSite</span></span>

## <span data-ttu-id="7784d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7784d-102">SYNOPSIS</span></span>
<span data-ttu-id="7784d-103">Pobiera obiekt listy z informacjami o wirtualnych sieciach Azure.</span><span class="sxs-lookup"><span data-stu-id="7784d-103">Gets a list object with information about Azure virtual networks.</span></span>

## <span data-ttu-id="7784d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7784d-104">SYNTAX</span></span>

```
Get-AzureVNetSite [[-VNetName] <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="7784d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7784d-105">DESCRIPTION</span></span>
<span data-ttu-id="7784d-106">Polecenie cmdlet **Get-AzureVNetSite** pobiera obiekt listy z informacjami o wirtualnych sieciach Azure dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7784d-106">The **Get-AzureVNetSite** cmdlet gets a list object with information about Azure virtual networks for the current subscription.</span></span>
<span data-ttu-id="7784d-107">Jeśli określisz nazwę sieci wirtualnej, zostanie zwrócona tylko informacja dla tej sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="7784d-107">If you specify a virtual network name, only information for that virtual network is returned.</span></span>

## <span data-ttu-id="7784d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7784d-108">EXAMPLES</span></span>

### <span data-ttu-id="7784d-109">Przykład 1: uzyskiwanie informacji o wszystkich sieciach wirtualnych w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7784d-109">Example 1: Get information about all virtual networks in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite
```

<span data-ttu-id="7784d-110">To polecenie pobiera informacje o wszystkich sieciach wirtualnych w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7784d-110">This command gets information about all the virtual networks in the current subscription.</span></span>

### <span data-ttu-id="7784d-111">Przykład 2: uzyskiwanie informacji o konkretnej sieci wirtualnej w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7784d-111">Example 2: Get information about a specific virtual network in the current subscription</span></span>
```
PS C:\> Get-AzureVNetSite -VNetName "MyProductionNetwork"
```

<span data-ttu-id="7784d-112">To polecenie pobiera informacje tylko z sieci wirtualnej MyProductionNetwork.</span><span class="sxs-lookup"><span data-stu-id="7784d-112">This command retrieves information on the MyProductionNetwork virtual network only.</span></span>

## <span data-ttu-id="7784d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7784d-113">PARAMETERS</span></span>

### <span data-ttu-id="7784d-114">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="7784d-114">-InformationAction</span></span>
<span data-ttu-id="7784d-115">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="7784d-115">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="7784d-116">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7784d-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7784d-117">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="7784d-117">Continue</span></span>
- <span data-ttu-id="7784d-118">Ignorować</span><span class="sxs-lookup"><span data-stu-id="7784d-118">Ignore</span></span>
- <span data-ttu-id="7784d-119">Inquire</span><span class="sxs-lookup"><span data-stu-id="7784d-119">Inquire</span></span>
- <span data-ttu-id="7784d-120">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="7784d-120">SilentlyContinue</span></span>
- <span data-ttu-id="7784d-121">Przestaw</span><span class="sxs-lookup"><span data-stu-id="7784d-121">Stop</span></span>
- <span data-ttu-id="7784d-122">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="7784d-122">Suspend</span></span>

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

### <span data-ttu-id="7784d-123">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="7784d-123">-InformationVariable</span></span>
<span data-ttu-id="7784d-124">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="7784d-124">Specifies an information variable.</span></span>

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

### <span data-ttu-id="7784d-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="7784d-125">-Profile</span></span>
<span data-ttu-id="7784d-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7784d-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7784d-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7784d-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7784d-128">-VNetName</span><span class="sxs-lookup"><span data-stu-id="7784d-128">-VNetName</span></span>
<span data-ttu-id="7784d-129">Określa nazwę sieci wirtualnej, na której należy zwrócić informacje.</span><span class="sxs-lookup"><span data-stu-id="7784d-129">Specifies a virtual network name to return information about.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7784d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7784d-130">CommonParameters</span></span>
<span data-ttu-id="7784d-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7784d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7784d-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7784d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7784d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7784d-133">INPUTS</span></span>

## <span data-ttu-id="7784d-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7784d-134">OUTPUTS</span></span>

## <span data-ttu-id="7784d-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7784d-135">NOTES</span></span>

## <span data-ttu-id="7784d-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7784d-136">RELATED LINKS</span></span>

[<span data-ttu-id="7784d-137">Get-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="7784d-137">Get-AzureVNetConfig</span></span>](./Get-AzureVNetConfig.md)

[<span data-ttu-id="7784d-138">Remove-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="7784d-138">Remove-AzureVNetConfig</span></span>](./Remove-AzureVNetConfig.md)

[<span data-ttu-id="7784d-139">Set-AzureVNetConfig</span><span class="sxs-lookup"><span data-stu-id="7784d-139">Set-AzureVNetConfig</span></span>](./Set-AzureVNetConfig.md)


