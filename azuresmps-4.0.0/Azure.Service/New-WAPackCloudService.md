---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA2E37AB-F137-4A62-9ABC-90565305A23B
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6d1bbac3db6f69f5cdda14870de20eee7f8170b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061827"
---
# <span data-ttu-id="78f28-101">New-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="78f28-101">New-WAPackCloudService</span></span>

## <span data-ttu-id="78f28-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="78f28-102">SYNOPSIS</span></span>
<span data-ttu-id="78f28-103">Tworzy usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="78f28-103">Creates a cloud service.</span></span>

## <span data-ttu-id="78f28-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="78f28-104">SYNTAX</span></span>

```
New-WAPackCloudService -Name <String> -Label <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="78f28-105">Opis</span><span class="sxs-lookup"><span data-stu-id="78f28-105">DESCRIPTION</span></span>
<span data-ttu-id="78f28-106">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="78f28-106">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="78f28-107">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="78f28-107">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="78f28-108">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="78f28-108">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="78f28-109">Polecenie cmdlet **New-WAPackCloudService** tworzy usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="78f28-109">The **New-WAPackCloudService** cmdlet creates a cloud service.</span></span>

## <span data-ttu-id="78f28-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="78f28-110">EXAMPLES</span></span>

### <span data-ttu-id="78f28-111">Przykład 1. Tworzenie usługi w chmurze</span><span class="sxs-lookup"><span data-stu-id="78f28-111">Example 1: Create a cloud service</span></span>
```
PS C:\> New-WAPackCloudService -Name "ContosoCloudService01" -Label "A label"
```

<span data-ttu-id="78f28-112">Polecenie tworzy usługę w chmurze o nazwie ContosoCloudService01 z etykietą.</span><span class="sxs-lookup"><span data-stu-id="78f28-112">The command creates a cloud service named ContosoCloudService01 with a label.</span></span>

## <span data-ttu-id="78f28-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="78f28-113">PARAMETERS</span></span>

### <span data-ttu-id="78f28-114">-Label</span><span class="sxs-lookup"><span data-stu-id="78f28-114">-Label</span></span>
<span data-ttu-id="78f28-115">Określa etykietę dla usługi w chmurze.</span><span class="sxs-lookup"><span data-stu-id="78f28-115">Specifies a label for the cloud service.</span></span>

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

### <span data-ttu-id="78f28-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="78f28-116">-Name</span></span>
<span data-ttu-id="78f28-117">Określa nazwę CloudService.</span><span class="sxs-lookup"><span data-stu-id="78f28-117">Specifies a name for the cloudservice.</span></span>

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

### <span data-ttu-id="78f28-118">-Profile</span><span class="sxs-lookup"><span data-stu-id="78f28-118">-Profile</span></span>
<span data-ttu-id="78f28-119">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78f28-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="78f28-120">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="78f28-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="78f28-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f28-121">CommonParameters</span></span>
<span data-ttu-id="78f28-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f28-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f28-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f28-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f28-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="78f28-124">INPUTS</span></span>

## <span data-ttu-id="78f28-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="78f28-125">OUTPUTS</span></span>

## <span data-ttu-id="78f28-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="78f28-126">NOTES</span></span>

## <span data-ttu-id="78f28-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="78f28-127">RELATED LINKS</span></span>

[<span data-ttu-id="78f28-128">Get-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="78f28-128">Get-WAPackCloudService</span></span>](./Get-WAPackCloudService.md)

[<span data-ttu-id="78f28-129">Remove-WAPackCloudService</span><span class="sxs-lookup"><span data-stu-id="78f28-129">Remove-WAPackCloudService</span></span>](./Remove-WAPackCloudService.md)


