---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 22A9B83D-789D-4722-BDD1-D8C448CFB88A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c809a49e2e8c1a534d6868c99bcc7cab1d20ccd1
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061851"
---
# <span data-ttu-id="8cf40-101">New-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="8cf40-101">New-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="8cf40-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cf40-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf40-103">Tworzy statyczną pulę adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-103">Creates a static IP address pool.</span></span>

## <span data-ttu-id="8cf40-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cf40-104">SYNTAX</span></span>

```
New-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> -IPAddressRangeStart <String>
 -IPAddressRangeEnd <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8cf40-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8cf40-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf40-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="8cf40-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8cf40-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf40-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8cf40-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8cf40-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8cf40-109">Polecenie cmdlet **New-WAPackStaticIPAddressPool** tworzy statyczną pulę adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-109">The **New-WAPackStaticIPAddressPool** cmdlet creates a static IP address pool.</span></span>

## <span data-ttu-id="8cf40-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cf40-110">EXAMPLES</span></span>

### <span data-ttu-id="8cf40-111">Przykład 1. Tworzenie puli statycznych adresów IP</span><span class="sxs-lookup"><span data-stu-id="8cf40-111">Example 1: Create a static IP address pool</span></span>
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> $VMSubnet = Get-WAPackVMSubnet -VNet $VNet -Name "ContosoVMSubnet01"
PS C:\> New-WAPackStaticIpAddressPool ?VMSubnet $VMSubnet -Name "ContosoStaticIpAddressPool01" -IPAddressRangeStart "192.168.1.0" -IPAddressRangeEnd "192.168.1.10"
```

<span data-ttu-id="8cf40-112">Pierwsze polecenie najpierw pobiera sieć maszyny wirtualnej, do której chcemy dodać pulę statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-112">The first command first retrieves the virtual machine network to which we want to add the static IP address pool.</span></span>
<span data-ttu-id="8cf40-113">Ta sieć maszyny wirtualnej nosi nazwę ContosoVNet01.</span><span class="sxs-lookup"><span data-stu-id="8cf40-113">This virtual machine network is named ContosoVNet01.</span></span>

<span data-ttu-id="8cf40-114">W drugim poleceniu jest używana uprzednio pobrana sieć maszyny wirtualnej w celu pobrania podsieci maszyny wirtualnej o nazwie ContosoVMSubnet01, do której chcemy dodać pulę statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-114">The second command uses the previously retrieved virtual machine network to get the virtual machine subnet named ContosoVMSubnet01 to which we want to add the static IP address pool.</span></span>

<span data-ttu-id="8cf40-115">Ostatnie polecenie tworzy nową statyczną pulę adresów IP z nazwą ContosoStaticIpAddressPool01 oraz początkiem zakresu od 192.168.1.0 i 192.168.1.10 końca zakresu.</span><span class="sxs-lookup"><span data-stu-id="8cf40-115">The last command creates a new static IP address pool with a name ContosoStaticIpAddressPool01 and a range start 192.168.1.0 and a range end 192.168.1.10.</span></span>

## <span data-ttu-id="8cf40-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cf40-116">PARAMETERS</span></span>

### <span data-ttu-id="8cf40-117">-IPAddressRangeEnd</span><span class="sxs-lookup"><span data-stu-id="8cf40-117">-IPAddressRangeEnd</span></span>
<span data-ttu-id="8cf40-118">Określa koniec zakresu adresów IP dla puli statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-118">Specifies an IP address range end for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf40-119">-IPAddressRangeStart</span><span class="sxs-lookup"><span data-stu-id="8cf40-119">-IPAddressRangeStart</span></span>
<span data-ttu-id="8cf40-120">Określa początek zakresu adresów IP dla puli statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-120">Specifies an IP address range start for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf40-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cf40-121">-Name</span></span>
<span data-ttu-id="8cf40-122">Określa nazwę puli statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-122">Specifies a name for the static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf40-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="8cf40-123">-Profile</span></span>
<span data-ttu-id="8cf40-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf40-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8cf40-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8cf40-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8cf40-126">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="8cf40-126">-VMSubnet</span></span>
<span data-ttu-id="8cf40-127">Określa podsieć VMSubnet skojarzoną z pulą statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="8cf40-127">Specifies a VMSubnet associated with the static IP address pool.</span></span>

```yaml
Type: VMSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf40-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf40-128">CommonParameters</span></span>
<span data-ttu-id="8cf40-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf40-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf40-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf40-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf40-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cf40-131">INPUTS</span></span>

## <span data-ttu-id="8cf40-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cf40-132">OUTPUTS</span></span>

## <span data-ttu-id="8cf40-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cf40-133">NOTES</span></span>

## <span data-ttu-id="8cf40-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cf40-134">RELATED LINKS</span></span>

[<span data-ttu-id="8cf40-135">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="8cf40-135">Get-WAPackStaticIPAddressPool</span></span>](./Get-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="8cf40-136">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="8cf40-136">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


