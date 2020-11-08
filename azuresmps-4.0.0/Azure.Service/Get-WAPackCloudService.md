---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 4BAD0DDE-80D4-4A89-AFFB-78C933D2C0D5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76771d8c0e8d06cbe134e920a06be5fc1b109fe2
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061823"
---
# <span data-ttu-id="dba5a-101">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="dba5a-101">Get-WAPackCloudService</span></span>

## <span data-ttu-id="dba5a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dba5a-102">SYNOPSIS</span></span>
<span data-ttu-id="dba5a-103">Pobiera obiekty usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="dba5a-103">Gets cloud service objects.</span></span>

## <span data-ttu-id="dba5a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dba5a-104">SYNTAX</span></span>

### <span data-ttu-id="dba5a-105">Empty (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="dba5a-105">Empty (Default)</span></span>
```
Get-WAPackCloudService [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="dba5a-106">Odname</span><span class="sxs-lookup"><span data-stu-id="dba5a-106">FromName</span></span>
```
Get-WAPackCloudService [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="dba5a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dba5a-107">DESCRIPTION</span></span>
<span data-ttu-id="dba5a-108">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="dba5a-108">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="dba5a-109">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="dba5a-109">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="dba5a-110">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="dba5a-110">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="dba5a-111">Polecenie cmdlet **Get-WAPackCloudService** Pobiera obiekty usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="dba5a-111">The **Get-WAPackCloudService** cmdlet gets cloud service objects.</span></span>

## <span data-ttu-id="dba5a-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dba5a-112">EXAMPLES</span></span>

## <span data-ttu-id="dba5a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dba5a-113">PARAMETERS</span></span>

### <span data-ttu-id="dba5a-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dba5a-114">-Name</span></span>
<span data-ttu-id="dba5a-115">Określa nazwę usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="dba5a-115">Specifies the name of a cloud service.</span></span>

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

### <span data-ttu-id="dba5a-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="dba5a-116">-Profile</span></span>
<span data-ttu-id="dba5a-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba5a-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="dba5a-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="dba5a-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="dba5a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba5a-119">CommonParameters</span></span>
<span data-ttu-id="dba5a-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba5a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba5a-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba5a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba5a-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dba5a-122">INPUTS</span></span>

## <span data-ttu-id="dba5a-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dba5a-123">OUTPUTS</span></span>

## <span data-ttu-id="dba5a-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dba5a-124">NOTES</span></span>

## <span data-ttu-id="dba5a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dba5a-125">RELATED LINKS</span></span>

[<span data-ttu-id="dba5a-126">Nowe — WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="dba5a-126">New-WAPackCloudService</span></span>](./New-WAPackCloudService.md)

[<span data-ttu-id="dba5a-127">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="dba5a-127">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


