---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E6E40D1B-A5BC-4B38-9D22-F06A8E4DABDF
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1360f45b751088bd899282cee2e64ce965d11fb
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061822"
---
# <span data-ttu-id="e19ad-101">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="e19ad-101">Get-WAPackVMOSDisk</span></span>

## <span data-ttu-id="e19ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e19ad-102">SYNOPSIS</span></span>
<span data-ttu-id="e19ad-103">Pobiera obiekty dyskowe systemu operacyjnego dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e19ad-103">Gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="e19ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e19ad-104">SYNTAX</span></span>

### <span data-ttu-id="e19ad-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e19ad-105">Empty (Default)</span></span>
```
Get-WAPackVMOSDisk [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e19ad-106">FromId</span><span class="sxs-lookup"><span data-stu-id="e19ad-106">FromId</span></span>
```
Get-WAPackVMOSDisk [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="e19ad-107">Odname</span><span class="sxs-lookup"><span data-stu-id="e19ad-107">FromName</span></span>
```
Get-WAPackVMOSDisk [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="e19ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e19ad-108">DESCRIPTION</span></span>
<span data-ttu-id="e19ad-109">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="e19ad-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="e19ad-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="e19ad-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="e19ad-111">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="e19ad-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="e19ad-112">Polecenie cmdlet **Get-WAPackVMOSDisk** Pobiera obiekty dysku systemu operacyjnego dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="e19ad-112">The **Get-WAPackVMOSDisk** cmdlet gets operating system disk objects for virtual machines.</span></span>

## <span data-ttu-id="e19ad-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e19ad-113">EXAMPLES</span></span>

### <span data-ttu-id="e19ad-114">Przykład 1: uzyskiwanie dysku z systemem operacyjnym przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="e19ad-114">Example 1: Get an operating system disk by using a name</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Name "ContosoOSDisk"
```

<span data-ttu-id="e19ad-115">To polecenie uzyskuje dysk z systemem operacyjnym o nazwie ContosoOSDisk.</span><span class="sxs-lookup"><span data-stu-id="e19ad-115">This command gets an operating system disk named ContosoOSDisk.</span></span>

### <span data-ttu-id="e19ad-116">Przykład 2: uzyskiwanie dysku z systemem operacyjnym przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="e19ad-116">Example 2: Get an operating system disk by using an ID</span></span>
```
PS C:\> Get-WAPackVMOSDisk -Id 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="e19ad-117">To polecenie pobiera dysk z systemem operacyjnym o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="e19ad-117">This command gets the operating system disk that has the specified ID.</span></span>

### <span data-ttu-id="e19ad-118">Przykład 3: uzyskiwanie wszystkich dysków z systemem operacyjnym</span><span class="sxs-lookup"><span data-stu-id="e19ad-118">Example 3: Get all operating system disks</span></span>
```
PS C:\> Get-WAPackVMOSDisk
```

<span data-ttu-id="e19ad-119">To polecenie pobiera wszystkie dyski z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="e19ad-119">This command gets all operating system disks.</span></span>

## <span data-ttu-id="e19ad-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e19ad-120">PARAMETERS</span></span>

### <span data-ttu-id="e19ad-121">-ID</span><span class="sxs-lookup"><span data-stu-id="e19ad-121">-ID</span></span>
<span data-ttu-id="e19ad-122">Określa unikatowy identyfikator dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e19ad-122">Specifies the unique ID of an operating system disk.</span></span>

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

### <span data-ttu-id="e19ad-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e19ad-123">-Name</span></span>
<span data-ttu-id="e19ad-124">Określa nazwę dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="e19ad-124">Specifies the name of an operating system disk.</span></span>

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

### <span data-ttu-id="e19ad-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="e19ad-125">-Profile</span></span>
<span data-ttu-id="e19ad-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e19ad-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e19ad-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e19ad-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="e19ad-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e19ad-128">CommonParameters</span></span>
<span data-ttu-id="e19ad-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e19ad-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e19ad-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e19ad-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e19ad-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e19ad-131">INPUTS</span></span>

## <span data-ttu-id="e19ad-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e19ad-132">OUTPUTS</span></span>

## <span data-ttu-id="e19ad-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e19ad-133">NOTES</span></span>

## <span data-ttu-id="e19ad-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e19ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="e19ad-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="e19ad-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


