---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ce97fe1fc7e21f166b1bb86db52bc8ad6e29e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523365"
---
# <span data-ttu-id="088d6-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="088d6-101">Close-AzsAlert</span></span>

## <span data-ttu-id="088d6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="088d6-102">SYNOPSIS</span></span>
<span data-ttu-id="088d6-103">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="088d6-103">Closes the given alert.</span></span>

## <span data-ttu-id="088d6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="088d6-104">SYNTAX</span></span>

### <span data-ttu-id="088d6-105">Zamknij (domyślne)</span><span class="sxs-lookup"><span data-stu-id="088d6-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="088d6-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="088d6-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="088d6-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="088d6-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="088d6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="088d6-108">DESCRIPTION</span></span>
<span data-ttu-id="088d6-109">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="088d6-109">Closes the given alert.</span></span>

## <span data-ttu-id="088d6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="088d6-110">EXAMPLES</span></span>

### <span data-ttu-id="088d6-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="088d6-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="088d6-112">Zamknij alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="088d6-112">Close an alert by Name.</span></span>

### <span data-ttu-id="088d6-113">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="088d6-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="088d6-114">Zamykanie alertu za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="088d6-114">Close an alert through piping.</span></span>

## <span data-ttu-id="088d6-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="088d6-115">PARAMETERS</span></span>

### <span data-ttu-id="088d6-116">-Force</span><span class="sxs-lookup"><span data-stu-id="088d6-116">-Force</span></span>
<span data-ttu-id="088d6-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="088d6-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="088d6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="088d6-118">-InputObject</span></span>
<span data-ttu-id="088d6-119">Alert zwrócony w wyniku Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="088d6-119">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="088d6-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="088d6-120">-Location</span></span>
<span data-ttu-id="088d6-121">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="088d6-121">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="088d6-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="088d6-122">-Name</span></span>
<span data-ttu-id="088d6-123">Identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="088d6-123">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="088d6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="088d6-124">-ResourceGroupName</span></span>
<span data-ttu-id="088d6-125">Nazwa grupy zasobów, w której znajduje się dany zasób.</span><span class="sxs-lookup"><span data-stu-id="088d6-125">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Close
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="088d6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="088d6-126">-ResourceId</span></span>
<span data-ttu-id="088d6-127">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="088d6-127">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="088d6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="088d6-128">-Confirm</span></span>
<span data-ttu-id="088d6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="088d6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="088d6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="088d6-130">-WhatIf</span></span>
<span data-ttu-id="088d6-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="088d6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="088d6-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="088d6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="088d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="088d6-133">CommonParameters</span></span>
<span data-ttu-id="088d6-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="088d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="088d6-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="088d6-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="088d6-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="088d6-136">INPUTS</span></span>

## <span data-ttu-id="088d6-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="088d6-137">OUTPUTS</span></span>

### <span data-ttu-id="088d6-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. alert</span><span class="sxs-lookup"><span data-stu-id="088d6-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="088d6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="088d6-139">NOTES</span></span>

## <span data-ttu-id="088d6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="088d6-140">RELATED LINKS</span></span>

