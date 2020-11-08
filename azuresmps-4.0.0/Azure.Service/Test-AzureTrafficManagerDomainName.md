---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 92E2409B-14BC-428F-8BAF-60D8DAFA5F57
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1adaafdfdd4331bbba86530eb532964430ed7c69
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054901"
---
# <span data-ttu-id="bc31e-101">Test-AzureTrafficManagerDomainName</span><span class="sxs-lookup"><span data-stu-id="bc31e-101">Test-AzureTrafficManagerDomainName</span></span>

## <span data-ttu-id="bc31e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bc31e-102">SYNOPSIS</span></span>
<span data-ttu-id="bc31e-103">Sprawdza, czy nazwa domeny jest dostępna jako profil w usłudze Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bc31e-103">Checks whether a domain name is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="bc31e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bc31e-104">SYNTAX</span></span>

```
Test-AzureTrafficManagerDomainName -DomainName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="bc31e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bc31e-105">DESCRIPTION</span></span>
<span data-ttu-id="bc31e-106">Polecenie cmdlet **test-AzureTrafficManagerDomainName** sprawdza, czy nazwa domeny jest dostępna jako profil usługi Microsoft Azure Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bc31e-106">The **Test-AzureTrafficManagerDomainName** cmdlet checks whether a domain name is available as a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bc31e-107">Jeśli nazwa domeny jest dostępna, to polecenie cmdlet zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="bc31e-107">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="bc31e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bc31e-108">EXAMPLES</span></span>

### <span data-ttu-id="bc31e-109">Przykład 1. Sprawdź, czy nazwa domeny jest dostępna</span><span class="sxs-lookup"><span data-stu-id="bc31e-109">Example 1: Check whether a domain name is available</span></span>
```
PS C:\>Test-AzureTrafficManagerDomainName -DomainName "ContosoApp.trafficmanager.net"
$True
```

<span data-ttu-id="bc31e-110">To polecenie sprawdza, czy nazwa domeny ContosoApp.trafficmanager.net jest dostępna jako profil usługi Traffic Manager.</span><span class="sxs-lookup"><span data-stu-id="bc31e-110">This command checks whether the domain name ContosoApp.trafficmanager.net is available as a Traffic Manager profile.</span></span>

## <span data-ttu-id="bc31e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bc31e-111">PARAMETERS</span></span>

### <span data-ttu-id="bc31e-112">-NazwaDomeny</span><span class="sxs-lookup"><span data-stu-id="bc31e-112">-DomainName</span></span>
<span data-ttu-id="bc31e-113">Określa nazwę domeny do sprawdzenia.</span><span class="sxs-lookup"><span data-stu-id="bc31e-113">Specifies the domain name to test.</span></span>
<span data-ttu-id="bc31e-114">Musisz podać następujący ciąg:</span><span class="sxs-lookup"><span data-stu-id="bc31e-114">You must include the following string:</span></span> 

<span data-ttu-id="bc31e-115">. trafficmanager.net</span><span class="sxs-lookup"><span data-stu-id="bc31e-115">.trafficmanager.net</span></span>

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

### <span data-ttu-id="bc31e-116">-Profile</span><span class="sxs-lookup"><span data-stu-id="bc31e-116">-Profile</span></span>
<span data-ttu-id="bc31e-117">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc31e-117">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="bc31e-118">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="bc31e-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="bc31e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc31e-119">CommonParameters</span></span>
<span data-ttu-id="bc31e-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc31e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc31e-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc31e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc31e-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bc31e-122">INPUTS</span></span>

## <span data-ttu-id="bc31e-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bc31e-123">OUTPUTS</span></span>

### <span data-ttu-id="bc31e-124">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bc31e-124">System.Boolean</span></span>
<span data-ttu-id="bc31e-125">To polecenie cmdlet generuje $True lub $False.</span><span class="sxs-lookup"><span data-stu-id="bc31e-125">This cmdlet generates $True or $False.</span></span>
<span data-ttu-id="bc31e-126">Jeśli nazwa domeny jest dostępna, to polecenie cmdlet zwraca wartość $True.</span><span class="sxs-lookup"><span data-stu-id="bc31e-126">If the domain name is available, this cmdlet returns a value of $True.</span></span>

## <span data-ttu-id="bc31e-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bc31e-127">NOTES</span></span>

## <span data-ttu-id="bc31e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bc31e-128">RELATED LINKS</span></span>

