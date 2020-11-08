---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 48211644-1B92-443D-A992-BDF517D89341
online version: ''
schema: 2.0.0
ms.openlocfilehash: 49b4039e07cf9f393a85c9592598ad870586fd06
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061900"
---
# <span data-ttu-id="10b69-101">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="10b69-101">Get-WAPackVMSizeProfile</span></span>

## <span data-ttu-id="10b69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10b69-102">SYNOPSIS</span></span>
<span data-ttu-id="10b69-103">Pobiera obiekty profilu rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="10b69-103">Gets size profile objects.</span></span>

## <span data-ttu-id="10b69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10b69-104">SYNTAX</span></span>

### <span data-ttu-id="10b69-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="10b69-105">Empty (Default)</span></span>
```
Get-WAPackVMSizeProfile [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="10b69-106">FromId</span><span class="sxs-lookup"><span data-stu-id="10b69-106">FromId</span></span>
```
Get-WAPackVMSizeProfile [-ID <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="10b69-107">Odname</span><span class="sxs-lookup"><span data-stu-id="10b69-107">FromName</span></span>
```
Get-WAPackVMSizeProfile [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="10b69-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10b69-108">DESCRIPTION</span></span>
<span data-ttu-id="10b69-109">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="10b69-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="10b69-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="10b69-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="10b69-111">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="10b69-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="10b69-112">Polecenie cmdlet **Get-WAPackVMSizeProfile** Pobiera obiekty profilu rozmiaru dla maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="10b69-112">The **Get-WAPackVMSizeProfile** cmdlet gets size profile objects for virtual machines.</span></span>

## <span data-ttu-id="10b69-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10b69-113">EXAMPLES</span></span>

### <span data-ttu-id="10b69-114">Przykład 1: Pobieranie profilu rozmiaru za pomocą nazwy</span><span class="sxs-lookup"><span data-stu-id="10b69-114">Example 1: Get a size profile by using a name</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -Name "ContosoSizeProfile07"
```

<span data-ttu-id="10b69-115">To polecenie pobiera profil rozmiaru o nazwie ContosoSizeProfile07.</span><span class="sxs-lookup"><span data-stu-id="10b69-115">This command gets the size profile named ContosoSizeProfile07.</span></span>

### <span data-ttu-id="10b69-116">Przykład 2: Pobieranie profilu rozmiaru przy użyciu identyfikatora</span><span class="sxs-lookup"><span data-stu-id="10b69-116">Example 2: Get a size profile by using an ID</span></span>
```
PS C:\> Get-WAPackVMSizeProfile -ID 66242D17-189F-480D-87CF-8E1D749998C8
```

<span data-ttu-id="10b69-117">To polecenie pobiera profil rozmiaru o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="10b69-117">This command gets the size profile that has the specified ID.</span></span>

### <span data-ttu-id="10b69-118">Przykład 3: pobieranie wszystkich profilów rozmiaru</span><span class="sxs-lookup"><span data-stu-id="10b69-118">Example 3: Get all size profiles</span></span>
```
PS C:\> Get-WAPackVMSizeProfile
```

<span data-ttu-id="10b69-119">To polecenie pobiera wszystkie profile rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="10b69-119">This command gets all the size profiles.</span></span>

## <span data-ttu-id="10b69-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10b69-120">PARAMETERS</span></span>

### <span data-ttu-id="10b69-121">-ID</span><span class="sxs-lookup"><span data-stu-id="10b69-121">-ID</span></span>
<span data-ttu-id="10b69-122">Określa unikatowy identyfikator profilu rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="10b69-122">Specifies the unique ID of a size profile.</span></span>

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

### <span data-ttu-id="10b69-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="10b69-123">-Name</span></span>
<span data-ttu-id="10b69-124">Określa nazwę profilu rozmiaru.</span><span class="sxs-lookup"><span data-stu-id="10b69-124">Specifies the name of a size profile.</span></span>

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

### <span data-ttu-id="10b69-125">-Profile</span><span class="sxs-lookup"><span data-stu-id="10b69-125">-Profile</span></span>
<span data-ttu-id="10b69-126">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10b69-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="10b69-127">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="10b69-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="10b69-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b69-128">CommonParameters</span></span>
<span data-ttu-id="10b69-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b69-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b69-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b69-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b69-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10b69-131">INPUTS</span></span>

## <span data-ttu-id="10b69-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10b69-132">OUTPUTS</span></span>

## <span data-ttu-id="10b69-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10b69-133">NOTES</span></span>

## <span data-ttu-id="10b69-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10b69-134">RELATED LINKS</span></span>

[<span data-ttu-id="10b69-135">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="10b69-135">Get-WAPackVM</span></span>](./Get-WAPackVM.md)


