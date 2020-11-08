---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 1D433BD2-4604-474B-A2DA-BC80EE935E5C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ffbe5ae961c1733be68c902a9657b200cba0a5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054579"
---
# <span data-ttu-id="db74b-101">Get-AzureSBNamespace</span><span class="sxs-lookup"><span data-stu-id="db74b-101">Get-AzureSBNamespace</span></span>

## <span data-ttu-id="db74b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db74b-102">SYNOPSIS</span></span>
<span data-ttu-id="db74b-103">Pobiera obszar nazw.</span><span class="sxs-lookup"><span data-stu-id="db74b-103">Gets the namespace.</span></span>


## <span data-ttu-id="db74b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db74b-104">SYNTAX</span></span>

```
Get-AzureSBNamespace [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="db74b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db74b-105">DESCRIPTION</span></span>
<span data-ttu-id="db74b-106">W tym temacie opisano polecenie cmdlet w wersji 0.8.10 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="db74b-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="db74b-107">Aby uzyskać wersję używanego modułu, należy wpisać w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="db74b-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="db74b-108">Polecenie cmdlet **Get-AzureSBNamespace** zwraca obszary nazw usługi magistrali usług skojarzone z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="db74b-108">The **Get-AzureSBNamespace** cmdlet returns the Service Bus service namespaces associated with the current subscription.</span></span>

[!INCLUDE [sb-deprecation.md](../include/sb-deprecation.md)]

## <span data-ttu-id="db74b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db74b-109">EXAMPLES</span></span>

### <span data-ttu-id="db74b-110">Przykład 1: uzyskiwanie przestrzeni nazw usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="db74b-110">Example 1: Get the Service Bus namespace</span></span>
```
PS C:\> Get-AzureSBNamespace
```

<span data-ttu-id="db74b-111">W tym przykładzie są pobierane obszary nazw usługi magistrali usług skojarzone z bieżącą subskrypcją.</span><span class="sxs-lookup"><span data-stu-id="db74b-111">This example gets the Service Bus service namespaces associated with the current subscription.</span></span>

## <span data-ttu-id="db74b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db74b-112">PARAMETERS</span></span>

### <span data-ttu-id="db74b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="db74b-113">-Name</span></span>
<span data-ttu-id="db74b-114">Określa nazwę obszaru nazw magistrali usług, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="db74b-114">Specifies the name of a Service Bus namespace to look for.</span></span>

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

### <span data-ttu-id="db74b-115">-Profile</span><span class="sxs-lookup"><span data-stu-id="db74b-115">-Profile</span></span>
<span data-ttu-id="db74b-116">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db74b-116">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="db74b-117">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="db74b-117">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="db74b-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db74b-118">CommonParameters</span></span>
<span data-ttu-id="db74b-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db74b-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db74b-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db74b-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db74b-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db74b-121">INPUTS</span></span>

## <span data-ttu-id="db74b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db74b-122">OUTPUTS</span></span>

## <span data-ttu-id="db74b-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db74b-123">NOTES</span></span>

## <span data-ttu-id="db74b-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db74b-124">RELATED LINKS</span></span>

[<span data-ttu-id="db74b-125">Get-AzureSBLocation</span><span class="sxs-lookup"><span data-stu-id="db74b-125">Get-AzureSBLocation</span></span>](./Get-AzureSBLocation.md)


