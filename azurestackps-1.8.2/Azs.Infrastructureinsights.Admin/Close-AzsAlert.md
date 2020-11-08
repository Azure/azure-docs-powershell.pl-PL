---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 14885871139eaed1c901312b9540a90d385795e5
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055888"
---
# <span data-ttu-id="c1898-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="c1898-101">Close-AzsAlert</span></span>

## <span data-ttu-id="c1898-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c1898-102">SYNOPSIS</span></span>
<span data-ttu-id="c1898-103">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="c1898-103">Closes the given alert.</span></span>

## <span data-ttu-id="c1898-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c1898-104">SYNTAX</span></span>

### <span data-ttu-id="c1898-105">Zamknij (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c1898-105">Close (Default)</span></span>
```
Close-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c1898-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1898-106">InputObject</span></span>
```
Close-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1898-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c1898-107">ResourceId</span></span>
```
Close-AzsAlert -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1898-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c1898-108">DESCRIPTION</span></span>
<span data-ttu-id="c1898-109">Zamyka dany alert.</span><span class="sxs-lookup"><span data-stu-id="c1898-109">Closes the given alert.</span></span>

## <span data-ttu-id="c1898-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c1898-110">EXAMPLES</span></span>

### <span data-ttu-id="c1898-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="c1898-111">EXAMPLE 1</span></span>
```
Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="c1898-112">Zamknij alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="c1898-112">Close an alert by Name.</span></span>

### <span data-ttu-id="c1898-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="c1898-113">EXAMPLE 2</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="c1898-114">Zamykanie alertu za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="c1898-114">Close an alert through piping.</span></span>

## <span data-ttu-id="c1898-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1898-115">PARAMETERS</span></span>

### <span data-ttu-id="c1898-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c1898-116">-Name</span></span>
<span data-ttu-id="c1898-117">Identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="c1898-117">The alert identifier.</span></span>

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

### <span data-ttu-id="c1898-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c1898-118">-Location</span></span>
<span data-ttu-id="c1898-119">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c1898-119">Name of the location.</span></span>

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

### <span data-ttu-id="c1898-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1898-120">-ResourceGroupName</span></span>
<span data-ttu-id="c1898-121">Nazwa grupy zasobów alertu.</span><span class="sxs-lookup"><span data-stu-id="c1898-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="c1898-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1898-122">-InputObject</span></span>
<span data-ttu-id="c1898-123">Alert zwrócony w wyniku Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="c1898-123">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="c1898-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1898-124">-ResourceId</span></span>
<span data-ttu-id="c1898-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c1898-125">The resource id.</span></span>

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

### <span data-ttu-id="c1898-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c1898-126">-Force</span></span>
<span data-ttu-id="c1898-127">Parametr przełącznika dla potwierdzenia niepytania.</span><span class="sxs-lookup"><span data-stu-id="c1898-127">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="c1898-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1898-128">-WhatIf</span></span>
<span data-ttu-id="c1898-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1898-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1898-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c1898-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1898-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1898-131">-Confirm</span></span>
<span data-ttu-id="c1898-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1898-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1898-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1898-133">CommonParameters</span></span>
<span data-ttu-id="c1898-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1898-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1898-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1898-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1898-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1898-136">INPUTS</span></span>

## <span data-ttu-id="c1898-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c1898-137">OUTPUTS</span></span>

### <span data-ttu-id="c1898-138">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. alert</span><span class="sxs-lookup"><span data-stu-id="c1898-138">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="c1898-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c1898-139">NOTES</span></span>

## <span data-ttu-id="c1898-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1898-140">RELATED LINKS</span></span>
