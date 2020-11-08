---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 37C788AC-B369-432B-8276-27FFB0B4CF10
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d2913877a9f68621bb5c1c930443a46e91e5935
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061861"
---
# <span data-ttu-id="5da2b-101">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="5da2b-101">Get-WAPackVMTemplate</span></span>

## <span data-ttu-id="5da2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5da2b-102">SYNOPSIS</span></span>
<span data-ttu-id="5da2b-103">Pobiera szablony maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5da2b-103">Gets virtual machine templates.</span></span>

## <span data-ttu-id="5da2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5da2b-104">SYNTAX</span></span>

### <span data-ttu-id="5da2b-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5da2b-105">Empty (Default)</span></span>
```
Get-WAPackVMTemplate [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5da2b-106">FromId</span><span class="sxs-lookup"><span data-stu-id="5da2b-106">FromId</span></span>
```
Get-WAPackVMTemplate [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5da2b-107">Odname</span><span class="sxs-lookup"><span data-stu-id="5da2b-107">FromName</span></span>
```
Get-WAPackVMTemplate [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5da2b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5da2b-108">DESCRIPTION</span></span>
<span data-ttu-id="5da2b-109">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="5da2b-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="5da2b-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="5da2b-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5da2b-111">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5da2b-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5da2b-112">Polecenie cmdlet **Get-WAPackVMTemplate** pobiera szablony maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5da2b-112">The **Get-WAPackVMTemplate** cmdlet gets virtual machine templates.</span></span>

## <span data-ttu-id="5da2b-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5da2b-113">EXAMPLES</span></span>

### <span data-ttu-id="5da2b-114">Przykład 1: uzyskiwanie szablonu maszyny wirtualnej za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="5da2b-114">Example 1: Get a virtual machine template by using a name</span></span>
```
PS C:\> Get-WAPackVMTemplate -Name "ContosoTemplate04"
```

<span data-ttu-id="5da2b-115">To polecenie pobiera szablon maszyny wirtualnej o nazwie ContosoTemplate04.</span><span class="sxs-lookup"><span data-stu-id="5da2b-115">This command gets the virtual machine template named ContosoTemplate04.</span></span>

### <span data-ttu-id="5da2b-116">Przykład 2: uzyskiwanie szablonu maszyny wirtualnej przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="5da2b-116">Example 2: Get a virtual machine template by using an ID</span></span>
```
PS C:\> Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="5da2b-117">To polecenie pobiera szablon maszyny wirtualnej o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="5da2b-117">This command gets the virtual machine template that has the specified ID.</span></span>

### <span data-ttu-id="5da2b-118">Przykład 3: pobieranie wszystkich szablonów maszyn wirtualnych</span><span class="sxs-lookup"><span data-stu-id="5da2b-118">Example 3: Get all virtual machine templates</span></span>
```
PS C:\> Get-WAPackVMTemplate
```

<span data-ttu-id="5da2b-119">To polecenie pobiera wszystkie szablony maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5da2b-119">This command gets all the virtual machine templates.</span></span>

## <span data-ttu-id="5da2b-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5da2b-120">PARAMETERS</span></span>

### <span data-ttu-id="5da2b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="5da2b-121">-ID</span></span>
<span data-ttu-id="5da2b-122">Określa unikatowy identyfikator szablonu.</span><span class="sxs-lookup"><span data-stu-id="5da2b-122">Specifies the unique ID of a template.</span></span>

```yaml
Type: Guid
Parameter Sets: FromId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da2b-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5da2b-123">-Name</span></span>
<span data-ttu-id="5da2b-124">Określa nazwę szablonu.</span><span class="sxs-lookup"><span data-stu-id="5da2b-124">Specifies the name of a template.</span></span>

```yaml
Type: String
Parameter Sets: FromName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da2b-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="5da2b-125">-Profile</span></span>
<span data-ttu-id="5da2b-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da2b-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5da2b-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5da2b-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5da2b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da2b-128">CommonParameters</span></span>
<span data-ttu-id="5da2b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da2b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da2b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da2b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da2b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5da2b-131">INPUTS</span></span>

## <span data-ttu-id="5da2b-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5da2b-132">OUTPUTS</span></span>

## <span data-ttu-id="5da2b-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5da2b-133">NOTES</span></span>

## <span data-ttu-id="5da2b-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5da2b-134">RELATED LINKS</span></span>

[<span data-ttu-id="5da2b-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="5da2b-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


