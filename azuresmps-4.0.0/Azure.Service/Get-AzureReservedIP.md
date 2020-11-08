---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: C0EEC51F-F8AB-4A6C-8F99-2B2DFFE9BB26
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9b5f4d5319e705c4f0481edcb5a44a579f4ff01d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054584"
---
# <span data-ttu-id="1829b-101">Get-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="1829b-101">Get-AzureReservedIP</span></span>

## <span data-ttu-id="1829b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1829b-102">SYNOPSIS</span></span>
<span data-ttu-id="1829b-103">Pobiera zastrzeżony adres IP według jego nazwy lub listę wszystkich zarezerwowanych adresów IP w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1829b-103">Gets a reserved IP address by its name or lists all the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="1829b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1829b-104">SYNTAX</span></span>

```
Get-AzureReservedIP [[-ReservedIPName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1829b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1829b-105">DESCRIPTION</span></span>
<span data-ttu-id="1829b-106">Polecenie cmdlet **Get-AzureReservedIP** pobiera zastrzeżony adres IP według jego nazwy lub zawiera listę wszystkich zarezerwowanych adresów IP w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1829b-106">The **Get-AzureReservedIP** cmdlet gets a reserved IP address by its name or lists all of the reserved IP addresses in the subscription.</span></span>

## <span data-ttu-id="1829b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1829b-107">EXAMPLES</span></span>

### <span data-ttu-id="1829b-108">Przykład 1: pobieranie wszystkich zastrzeżonych adresów IP</span><span class="sxs-lookup"><span data-stu-id="1829b-108">Example 1: Get all reserved IP addresses</span></span>
```
PS C:\> Get-AzureReservedIP
```

<span data-ttu-id="1829b-109">To polecenie pobiera wszystkie zastrzeżone adresy IP.</span><span class="sxs-lookup"><span data-stu-id="1829b-109">This command gets all reserved IP addresses.</span></span>

### <span data-ttu-id="1829b-110">Przykład 2: uzyskiwanie zastrzeżonego adresu IP o określonej nazwie</span><span class="sxs-lookup"><span data-stu-id="1829b-110">Example 2: Get a reserved IP address with a specified name</span></span>
```
PS C:\> Get-AzureReservedIP -ReservedIPName $IpName
```

<span data-ttu-id="1829b-111">To polecenie pobiera zastrzeżony adres IP o nazwie określonej przez zmienną $IpName.</span><span class="sxs-lookup"><span data-stu-id="1829b-111">This command gets the reserved IP address that has the name specified by the $IpName variable.</span></span>

## <span data-ttu-id="1829b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1829b-112">PARAMETERS</span></span>

### <span data-ttu-id="1829b-113">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1829b-113">-InformationAction</span></span>
<span data-ttu-id="1829b-114">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="1829b-114">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="1829b-115">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="1829b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1829b-116">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="1829b-116">Continue</span></span>
- <span data-ttu-id="1829b-117">Ignorować</span><span class="sxs-lookup"><span data-stu-id="1829b-117">Ignore</span></span>
- <span data-ttu-id="1829b-118">Inquire</span><span class="sxs-lookup"><span data-stu-id="1829b-118">Inquire</span></span>
- <span data-ttu-id="1829b-119">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="1829b-119">SilentlyContinue</span></span>
- <span data-ttu-id="1829b-120">Przestaw</span><span class="sxs-lookup"><span data-stu-id="1829b-120">Stop</span></span>
- <span data-ttu-id="1829b-121">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="1829b-121">Suspend</span></span>

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

### <span data-ttu-id="1829b-122">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1829b-122">-InformationVariable</span></span>
<span data-ttu-id="1829b-123">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="1829b-123">Specifies an information variable.</span></span>

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

### <span data-ttu-id="1829b-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="1829b-124">-Profile</span></span>
<span data-ttu-id="1829b-125">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1829b-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1829b-126">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="1829b-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1829b-127">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="1829b-127">-ReservedIPName</span></span>
<span data-ttu-id="1829b-128">Określa zastrzeżoną nazwę IP.</span><span class="sxs-lookup"><span data-stu-id="1829b-128">Specifies the reserved IP name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1829b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1829b-129">CommonParameters</span></span>
<span data-ttu-id="1829b-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1829b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1829b-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1829b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1829b-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1829b-132">INPUTS</span></span>

## <span data-ttu-id="1829b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1829b-133">OUTPUTS</span></span>

## <span data-ttu-id="1829b-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1829b-134">NOTES</span></span>

## <span data-ttu-id="1829b-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1829b-135">RELATED LINKS</span></span>

[<span data-ttu-id="1829b-136">Nowe — AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="1829b-136">New-AzureReservedIP</span></span>](./New-AzureReservedIP.md)

[<span data-ttu-id="1829b-137">Remove-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="1829b-137">Remove-AzureReservedIP</span></span>](./Remove-AzureReservedIP.md)


