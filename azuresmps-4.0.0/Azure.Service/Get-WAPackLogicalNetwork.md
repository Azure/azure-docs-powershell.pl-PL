---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7D51BE56-C0A2-4A32-BB7F-8FA9CC67F8F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 986d4998119c4ede1780fa35ad6baadce4574a81
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061824"
---
# <span data-ttu-id="98866-101">Get-WAPackLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="98866-101">Get-WAPackLogicalNetwork</span></span>

## <span data-ttu-id="98866-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98866-102">SYNOPSIS</span></span>
<span data-ttu-id="98866-103">Pobiera logiczne obiekty sieciowe.</span><span class="sxs-lookup"><span data-stu-id="98866-103">Gets logical network objects.</span></span>

## <span data-ttu-id="98866-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98866-104">SYNTAX</span></span>

### <span data-ttu-id="98866-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="98866-105">Empty (Default)</span></span>
```
Get-WAPackLogicalNetwork [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="98866-106">Odname</span><span class="sxs-lookup"><span data-stu-id="98866-106">FromName</span></span>
```
Get-WAPackLogicalNetwork [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="98866-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98866-107">DESCRIPTION</span></span>
<span data-ttu-id="98866-108">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="98866-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="98866-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="98866-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="98866-110">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="98866-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="98866-111">Polecenie cmdlet **Get-WAPackLogicalNetwork** pobiera logiczne obiekty sieciowe.</span><span class="sxs-lookup"><span data-stu-id="98866-111">The **Get-WAPackLogicalNetwork** cmdlet gets logical network objects.</span></span>

## <span data-ttu-id="98866-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98866-112">EXAMPLES</span></span>

### <span data-ttu-id="98866-113">Przykład 1: uzyskiwanie sieci logicznej przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="98866-113">Example 1: Get a logical network by using a name</span></span>
```
PS C:\> Get-WAPackLogicalNetwork -Name "ContosoLogicalNetwork01"
```

<span data-ttu-id="98866-114">To polecenie uzyskuje sieć logiczną o nazwie ContosoLogicalNetwork01.</span><span class="sxs-lookup"><span data-stu-id="98866-114">This command gets a logical network named ContosoLogicalNetwork01.</span></span>

### <span data-ttu-id="98866-115">Przykład 2: pobieranie wszystkich sieci logicznych</span><span class="sxs-lookup"><span data-stu-id="98866-115">Example 2: Get all logical networks</span></span>
```
PS C:\> Get-WAPackLogicalNetwork
```

<span data-ttu-id="98866-116">To polecenie pobiera wszystkie sieci logiczne.</span><span class="sxs-lookup"><span data-stu-id="98866-116">This command gets all logical networks.</span></span>

## <span data-ttu-id="98866-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98866-117">PARAMETERS</span></span>

### <span data-ttu-id="98866-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98866-118">-Name</span></span>
<span data-ttu-id="98866-119">Określa nazwę sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="98866-119">Specifies the name of a logical network.</span></span>

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

### <span data-ttu-id="98866-120">-Profile</span><span class="sxs-lookup"><span data-stu-id="98866-120">-Profile</span></span>
<span data-ttu-id="98866-121">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98866-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="98866-122">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="98866-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="98866-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98866-123">CommonParameters</span></span>
<span data-ttu-id="98866-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98866-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98866-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98866-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98866-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98866-126">INPUTS</span></span>

## <span data-ttu-id="98866-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98866-127">OUTPUTS</span></span>

## <span data-ttu-id="98866-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98866-128">NOTES</span></span>

## <span data-ttu-id="98866-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98866-129">RELATED LINKS</span></span>

