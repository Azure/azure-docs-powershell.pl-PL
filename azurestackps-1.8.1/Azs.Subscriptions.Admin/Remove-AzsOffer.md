---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 74772615551979a9ab0cdba3603305489698e212
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889478"
---
# <span data-ttu-id="2c308-101">Remove-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="2c308-101">Remove-AzsOffer</span></span>

## <span data-ttu-id="2c308-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c308-102">SYNOPSIS</span></span>
<span data-ttu-id="2c308-103">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="2c308-103">Delete the specified offer.</span></span>

## <span data-ttu-id="2c308-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c308-104">SYNTAX</span></span>

### <span data-ttu-id="2c308-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2c308-105">Delete (Default)</span></span>
```
Remove-AzsOffer -Name <String> -ResourceGroupName <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c308-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2c308-106">ResourceId</span></span>
```
Remove-AzsOffer -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c308-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2c308-107">DESCRIPTION</span></span>
<span data-ttu-id="2c308-108">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="2c308-108">Delete the specified offer.</span></span>

## <span data-ttu-id="2c308-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c308-109">EXAMPLES</span></span>

### <span data-ttu-id="2c308-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2c308-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsOffer -Name offername1 -ResourceGroupName rg1
```

<span data-ttu-id="2c308-111">Usuwanie określonej oferty.</span><span class="sxs-lookup"><span data-stu-id="2c308-111">Delete the specified offer.</span></span>

## <span data-ttu-id="2c308-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c308-112">PARAMETERS</span></span>

### <span data-ttu-id="2c308-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2c308-113">-Force</span></span>
<span data-ttu-id="2c308-114">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="2c308-114">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c308-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2c308-115">-Name</span></span>
<span data-ttu-id="2c308-116">Nazwa oferty.</span><span class="sxs-lookup"><span data-stu-id="2c308-116">Name of an offer.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c308-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c308-117">-ResourceGroupName</span></span>
<span data-ttu-id="2c308-118">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="2c308-118">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c308-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c308-119">-ResourceId</span></span>
<span data-ttu-id="2c308-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2c308-120">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c308-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c308-121">-Confirm</span></span>
<span data-ttu-id="2c308-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c308-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c308-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c308-123">-WhatIf</span></span>
<span data-ttu-id="2c308-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c308-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c308-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c308-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c308-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c308-126">CommonParameters</span></span>
<span data-ttu-id="2c308-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c308-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c308-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c308-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c308-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c308-129">INPUTS</span></span>

## <span data-ttu-id="2c308-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c308-130">OUTPUTS</span></span>

## <span data-ttu-id="2c308-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c308-131">NOTES</span></span>

## <span data-ttu-id="2c308-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c308-132">RELATED LINKS</span></span>

