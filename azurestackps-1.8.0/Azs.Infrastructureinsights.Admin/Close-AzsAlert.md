---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889117"
---
# <span data-ttu-id="258cf-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="258cf-101">Close-AzsAlert</span></span>

## <span data-ttu-id="258cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="258cf-102">SYNOPSIS</span></span>
<span data-ttu-id="258cf-103">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="258cf-103">Closes the given alert.</span></span>

## <span data-ttu-id="258cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="258cf-104">SYNTAX</span></span>

### <span data-ttu-id="258cf-105">Zamknij (domyślne)</span><span class="sxs-lookup"><span data-stu-id="258cf-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="258cf-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="258cf-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="258cf-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="258cf-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="258cf-108">Opis</span><span class="sxs-lookup"><span data-stu-id="258cf-108">DESCRIPTION</span></span>
<span data-ttu-id="258cf-109">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="258cf-109">Closes the given alert.</span></span>

## <span data-ttu-id="258cf-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="258cf-110">EXAMPLES</span></span>

### <span data-ttu-id="258cf-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="258cf-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="258cf-112">Zamknij alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="258cf-112">Close an alert by Name.</span></span>

### <span data-ttu-id="258cf-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="258cf-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="258cf-114">Zamykanie alertu za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="258cf-114">Close an alert through piping.</span></span>

## <span data-ttu-id="258cf-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="258cf-115">PARAMETERS</span></span>

### <span data-ttu-id="258cf-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="258cf-116">-Name</span></span>
<span data-ttu-id="258cf-117">Identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="258cf-117">The alert identifier.</span></span>

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

### <span data-ttu-id="258cf-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="258cf-118">-Location</span></span>
<span data-ttu-id="258cf-119">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="258cf-119">Name of the location.</span></span>

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

### <span data-ttu-id="258cf-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="258cf-120">-ResourceGroupName</span></span>
<span data-ttu-id="258cf-121">Nazwa grupy zasobów alertu.</span><span class="sxs-lookup"><span data-stu-id="258cf-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="258cf-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="258cf-122">-InputObject</span></span>
<span data-ttu-id="258cf-123">Alert zwrócony w wyniku Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="258cf-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="258cf-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="258cf-124">-ResourceId</span></span>
<span data-ttu-id="258cf-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="258cf-125">The resource id.</span></span>

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

### <span data-ttu-id="258cf-126">-Force</span><span class="sxs-lookup"><span data-stu-id="258cf-126">-Force</span></span>
<span data-ttu-id="258cf-127">Parametr przełącznika dla potwierdzenia niepytania.</span><span class="sxs-lookup"><span data-stu-id="258cf-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="258cf-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="258cf-128">-WhatIf</span></span>
<span data-ttu-id="258cf-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="258cf-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="258cf-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="258cf-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="258cf-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="258cf-131">-Confirm</span></span>
<span data-ttu-id="258cf-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="258cf-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="258cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="258cf-133">CommonParameters</span></span>
<span data-ttu-id="258cf-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="258cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="258cf-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="258cf-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="258cf-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="258cf-136">INPUTS</span></span>

## <span data-ttu-id="258cf-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="258cf-137">OUTPUTS</span></span>

### <span data-ttu-id="258cf-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. alert</span><span class="sxs-lookup"><span data-stu-id="258cf-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="258cf-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="258cf-139">NOTES</span></span>

## <span data-ttu-id="258cf-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="258cf-140">RELATED LINKS</span></span>
