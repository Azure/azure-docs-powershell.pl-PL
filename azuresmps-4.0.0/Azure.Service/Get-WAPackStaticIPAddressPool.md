---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4414EA89-8573-416E-A611-DA2135E350BD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 75b216b512c364a3285df185a3365b1fc85a3d94
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061901"
---
# <span data-ttu-id="715b4-101">Get-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="715b4-101">Get-WAPackStaticIPAddressPool</span></span>

## <span data-ttu-id="715b4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="715b4-102">SYNOPSIS</span></span>
<span data-ttu-id="715b4-103">Pobiera statyczne obiekty puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="715b4-103">Gets static IP address pool objects.</span></span>

## <span data-ttu-id="715b4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="715b4-104">SYNTAX</span></span>

### <span data-ttu-id="715b4-105">FromVMSubnetObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="715b4-105">FromVMSubnetObject (Default)</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="715b4-106">Odname</span><span class="sxs-lookup"><span data-stu-id="715b4-106">FromName</span></span>
```
Get-WAPackStaticIPAddressPool -VMSubnet <VMSubnet> -Name <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="715b4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="715b4-107">DESCRIPTION</span></span>
<span data-ttu-id="715b4-108">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="715b4-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="715b4-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="715b4-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="715b4-110">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="715b4-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="715b4-111">Polecenie cmdlet **Get-WAPackStaticIPAddressPool** pobiera statyczne obiekty puli adresów IP.</span><span class="sxs-lookup"><span data-stu-id="715b4-111">The **Get-WAPackStaticIPAddressPool** cmdlet gets static IP address pool objects.</span></span>

## <span data-ttu-id="715b4-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="715b4-112">EXAMPLES</span></span>

### <span data-ttu-id="715b4-113">Przykład 1: uzyskiwanie puli statycznych adresów IP z danej podsieci VMSubnet</span><span class="sxs-lookup"><span data-stu-id="715b4-113">Example 1: Get a static IP address pool from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet -Name "ContosoStaticIPAddressPool01"
```

<span data-ttu-id="715b4-114">To polecenie pobiera statyczną pulę adresów IP o nazwie ContosoStaticIPAddressPool01 z określonej podsieci VMSubnet.</span><span class="sxs-lookup"><span data-stu-id="715b4-114">This command gets the static IP address pool named ContosoStaticIPAddressPool01 from a specified VMSubnet.</span></span>

### <span data-ttu-id="715b4-115">Przykład 2: pobieranie wszystkich pul statycznych adresów IP z danej podsieci VMSubnet</span><span class="sxs-lookup"><span data-stu-id="715b4-115">Example 2: Get all static IP address pools from a given VMSubnet</span></span>
```
PS C:\> $Subnet = Get-WAPackVMSubet -Name "ContosoVMSubnet01"
PS C:\> Get-WAPackStaticIPAddressPool -VMSubnet $Subnet
```

<span data-ttu-id="715b4-116">To polecenie pobiera wszystkie pule statyczne IP z określonego VMSubet.</span><span class="sxs-lookup"><span data-stu-id="715b4-116">This command gets all the static IP pools from a specified VMSubet.</span></span>

## <span data-ttu-id="715b4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="715b4-117">PARAMETERS</span></span>

### <span data-ttu-id="715b4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="715b4-118">-Name</span></span>
<span data-ttu-id="715b4-119">Określa nazwę puli statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="715b4-119">Specifies the name of a static IP address pool.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="715b4-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="715b4-120">-Profile</span></span>
<span data-ttu-id="715b4-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="715b4-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="715b4-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="715b4-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="715b4-123">-VMSubnet</span><span class="sxs-lookup"><span data-stu-id="715b4-123">-VMSubnet</span></span>
<span data-ttu-id="715b4-124">Określa obiekt **VMSubnet** powiązany z pulą statycznych adresów IP.</span><span class="sxs-lookup"><span data-stu-id="715b4-124">Specifies the **VMSubnet** object associated to the static IP address pool.</span></span>

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

### <span data-ttu-id="715b4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="715b4-125">CommonParameters</span></span>
<span data-ttu-id="715b4-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="715b4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="715b4-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="715b4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="715b4-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="715b4-128">INPUTS</span></span>

## <span data-ttu-id="715b4-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="715b4-129">OUTPUTS</span></span>

## <span data-ttu-id="715b4-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="715b4-130">NOTES</span></span>

## <span data-ttu-id="715b4-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="715b4-131">RELATED LINKS</span></span>

[<span data-ttu-id="715b4-132">Nowe — WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="715b4-132">New-WAPackStaticIPAddressPool</span></span>](./New-WAPackStaticIPAddressPool.md)

[<span data-ttu-id="715b4-133">Remove-WAPackStaticIPAddressPool</span><span class="sxs-lookup"><span data-stu-id="715b4-133">Remove-WAPackStaticIPAddressPool</span></span>](./Remove-WAPackStaticIPAddressPool.md)


