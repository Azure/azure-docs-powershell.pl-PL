---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 57d7037f6deb669531bb03c3bf4f2e504586f832
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872192"
---
# <span data-ttu-id="705d9-101">New-AzsAddonPlanDefinitionObject</span><span class="sxs-lookup"><span data-stu-id="705d9-101">New-AzsAddonPlanDefinitionObject</span></span>

## <span data-ttu-id="705d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="705d9-102">SYNOPSIS</span></span>
<span data-ttu-id="705d9-103">Zawiera nazwę żądanego planu, który ma zostać połączony lub odłączony od oferty.</span><span class="sxs-lookup"><span data-stu-id="705d9-103">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="705d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="705d9-104">SYNTAX</span></span>

```
New-AzsAddonPlanDefinitionObject [[-PlanId] <String>] [[-MaxAcquisitionCount] <Int64>] [<CommonParameters>]
```

## <span data-ttu-id="705d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="705d9-105">DESCRIPTION</span></span>
<span data-ttu-id="705d9-106">Zawiera nazwę żądanego planu, który ma zostać połączony lub odłączony od oferty.</span><span class="sxs-lookup"><span data-stu-id="705d9-106">Contains the name of the desired plan to be linked or unlinked from an offer.</span></span>

## <span data-ttu-id="705d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="705d9-107">EXAMPLES</span></span>

### <span data-ttu-id="705d9-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="705d9-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsAddonPlanDefinitionObject -PlanId $planIdentifier -MaxAcquisitionCount 500
```

<span data-ttu-id="705d9-109">Utwórz nowy obiekt definicji planu dla określonego planu z limitem nabycia 500.</span><span class="sxs-lookup"><span data-stu-id="705d9-109">Create a new plan definition object for the specified plan with the acquisition limit of 500.</span></span>

## <span data-ttu-id="705d9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="705d9-110">PARAMETERS</span></span>

### <span data-ttu-id="705d9-111">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="705d9-111">-MaxAcquisitionCount</span></span>
<span data-ttu-id="705d9-112">Maksymalna liczba wystąpień, które można nabyć w ramach pojedynczego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="705d9-112">Maximum number of instances that can be acquired by a single subscription.</span></span>
<span data-ttu-id="705d9-113">Jeśli argument nie zostanie określony, przyjmowana jest wartość 1.</span><span class="sxs-lookup"><span data-stu-id="705d9-113">If not specified, the assumed value is 1.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705d9-114">-PlanId</span><span class="sxs-lookup"><span data-stu-id="705d9-114">-PlanId</span></span>
<span data-ttu-id="705d9-115">Identyfikator planu.</span><span class="sxs-lookup"><span data-stu-id="705d9-115">Plan identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="705d9-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="705d9-116">CommonParameters</span></span>
<span data-ttu-id="705d9-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="705d9-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="705d9-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="705d9-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="705d9-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="705d9-119">INPUTS</span></span>

## <span data-ttu-id="705d9-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="705d9-120">OUTPUTS</span></span>

## <span data-ttu-id="705d9-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="705d9-121">NOTES</span></span>

## <span data-ttu-id="705d9-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="705d9-122">RELATED LINKS</span></span>

