---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: CB2936E4-E403-44B3-9CB8-617308E54C50
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9059e5bad8441f25846cf98a12c5e8dada2e814a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061867"
---
# <span data-ttu-id="54609-101">New-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="54609-101">New-WAPackVNet</span></span>

## <span data-ttu-id="54609-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="54609-102">SYNOPSIS</span></span>
<span data-ttu-id="54609-103">Tworzy wirtualną sieć.</span><span class="sxs-lookup"><span data-stu-id="54609-103">Creates a virtualized network.</span></span>

## <span data-ttu-id="54609-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="54609-104">SYNTAX</span></span>

```
New-WAPackVNet -LogicalNetwork <LogicalNetwork> -Name <String> [-Description <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="54609-105">Opis</span><span class="sxs-lookup"><span data-stu-id="54609-105">DESCRIPTION</span></span>
<span data-ttu-id="54609-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="54609-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="54609-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="54609-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="54609-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="54609-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="54609-109">Polecenie cmdlet **New-WAPackVNet** tworzy wirtualną sieć.</span><span class="sxs-lookup"><span data-stu-id="54609-109">The **New-WAPackVNet** cmdlet creates a virtualized network.</span></span>

## <span data-ttu-id="54609-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="54609-110">EXAMPLES</span></span>

### <span data-ttu-id="54609-111">Przykład 1. Tworzenie sieci zwirtualizowanej</span><span class="sxs-lookup"><span data-stu-id="54609-111">Example 1: Create a virtualized network</span></span>
```
PS C:\> $LogicalNetwork = Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
PS C:\> New-WAPackVNet -LogicalNetwork $LogicalNetwork -Name "ContosoVNett01" -Description "A description"
```

<span data-ttu-id="54609-112">Pierwsze polecenie najpierw pobiera sieć logiczną, do której chcemy dodać nową wirtualną sieć.</span><span class="sxs-lookup"><span data-stu-id="54609-112">The first command first retrieves the logical network to which we want to add a new virtualized network.</span></span>
<span data-ttu-id="54609-113">Ta sieć logiczna nosi nazwę ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="54609-113">This logical network is named ContosoLogicalNetwork01.</span></span>

<span data-ttu-id="54609-114">Drugie i ostatnie polecenie tworzy wirtualną sieć przy użyciu poprzedniej pobranej sieci logicznej, nazwy (ContosoVNett01) i opisu (opisu).</span><span class="sxs-lookup"><span data-stu-id="54609-114">The second and last command creates a virtualized network using the previously retrieved logical network, a name (ContosoVNett01) and a description (A description).</span></span>

## <span data-ttu-id="54609-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="54609-115">PARAMETERS</span></span>

### <span data-ttu-id="54609-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="54609-116">-Description</span></span>
<span data-ttu-id="54609-117">Określa opis wirtualnej sieci.</span><span class="sxs-lookup"><span data-stu-id="54609-117">Specifies a description for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54609-118">-LogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="54609-118">-LogicalNetwork</span></span>
<span data-ttu-id="54609-119">Określa LogicalNetworką skojarzoną z wirtualną siecią.</span><span class="sxs-lookup"><span data-stu-id="54609-119">Specifies a LogicalNetwork associated with the virtualized network.</span></span>

```yaml
Type: LogicalNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54609-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="54609-120">-Name</span></span>
<span data-ttu-id="54609-121">Określa nazwę wirtualnej sieci.</span><span class="sxs-lookup"><span data-stu-id="54609-121">Specifies a name for the virtualized network.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54609-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="54609-122">-Profile</span></span>
<span data-ttu-id="54609-123">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54609-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="54609-124">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="54609-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="54609-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54609-125">CommonParameters</span></span>
<span data-ttu-id="54609-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54609-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54609-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54609-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54609-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="54609-128">INPUTS</span></span>

## <span data-ttu-id="54609-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="54609-129">OUTPUTS</span></span>

## <span data-ttu-id="54609-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="54609-130">NOTES</span></span>

## <span data-ttu-id="54609-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="54609-131">RELATED LINKS</span></span>

[<span data-ttu-id="54609-132">Get-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="54609-132">Get-WAPackVNet</span></span>](./Get-WAPackVNet.md)

[<span data-ttu-id="54609-133">Remove-WAPackVNet</span><span class="sxs-lookup"><span data-stu-id="54609-133">Remove-WAPackVNet</span></span>](./Remove-WAPackVNet.md)


