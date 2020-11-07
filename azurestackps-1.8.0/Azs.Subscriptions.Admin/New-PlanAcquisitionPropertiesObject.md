---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889213"
---
# <span data-ttu-id="1ac55-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="1ac55-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="1ac55-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1ac55-102">SYNOPSIS</span></span>
<span data-ttu-id="1ac55-103">Przedstawia przejęcie planu dodatków dla abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1ac55-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="1ac55-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1ac55-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ac55-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1ac55-105">DESCRIPTION</span></span>
<span data-ttu-id="1ac55-106">Przedstawia przejęcie planu dodatków dla abonamentu.</span><span class="sxs-lookup"><span data-stu-id="1ac55-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="1ac55-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1ac55-107">EXAMPLES</span></span>

### <span data-ttu-id="1ac55-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1ac55-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1ac55-109">{{Dodaj opis przykładu}}</span><span class="sxs-lookup"><span data-stu-id="1ac55-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1ac55-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1ac55-110">PARAMETERS</span></span>

### <span data-ttu-id="1ac55-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="1ac55-111">-AcquisitionId</span></span>
<span data-ttu-id="1ac55-112">Identyfikator nabycia.</span><span class="sxs-lookup"><span data-stu-id="1ac55-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac55-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="1ac55-113">-AcquisitionTime</span></span>
<span data-ttu-id="1ac55-114">Czas pobierania.</span><span class="sxs-lookup"><span data-stu-id="1ac55-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac55-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="1ac55-115">-ExternalReferenceId</span></span>
<span data-ttu-id="1ac55-116">Zewnętrzny identyfikator odwołania.</span><span class="sxs-lookup"><span data-stu-id="1ac55-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac55-117">-ID</span><span class="sxs-lookup"><span data-stu-id="1ac55-117">-Id</span></span>
<span data-ttu-id="1ac55-118">Identyfikator w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1ac55-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac55-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="1ac55-119">-PlanId</span></span>
<span data-ttu-id="1ac55-120">Identyfikator planu w kontekście subskrypcji dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="1ac55-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1ac55-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="1ac55-121">-ProvisioningState</span></span>
<span data-ttu-id="1ac55-122">Stan aprowizacji.</span><span class="sxs-lookup"><span data-stu-id="1ac55-122">State of the provisioning.</span></span>

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

### <span data-ttu-id="1ac55-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ac55-123">CommonParameters</span></span>
<span data-ttu-id="1ac55-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ac55-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ac55-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1ac55-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ac55-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1ac55-126">INPUTS</span></span>

## <span data-ttu-id="1ac55-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1ac55-127">OUTPUTS</span></span>

## <span data-ttu-id="1ac55-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1ac55-128">NOTES</span></span>

## <span data-ttu-id="1ac55-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1ac55-129">RELATED LINKS</span></span>

