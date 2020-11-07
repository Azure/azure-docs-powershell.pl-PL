---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523597"
---
# <span data-ttu-id="dce87-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="dce87-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="dce87-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dce87-102">SYNOPSIS</span></span>
<span data-ttu-id="dce87-103">Naprawia podany alert.</span><span class="sxs-lookup"><span data-stu-id="dce87-103">Repairs the given alert.</span></span>

## <span data-ttu-id="dce87-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dce87-104">SYNTAX</span></span>

### <span data-ttu-id="dce87-105">Naprawianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dce87-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dce87-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="dce87-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dce87-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dce87-107">DESCRIPTION</span></span>
<span data-ttu-id="dce87-108">Naprawia podany alert.</span><span class="sxs-lookup"><span data-stu-id="dce87-108">Repairs the given alert.</span></span>

## <span data-ttu-id="dce87-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dce87-109">EXAMPLES</span></span>

### <span data-ttu-id="dce87-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="dce87-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="dce87-111">Naprawianie alertu według nazwy.</span><span class="sxs-lookup"><span data-stu-id="dce87-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="dce87-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="dce87-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="dce87-113">Naprawianie alertu za pośrednictwem połączenia rurowego.</span><span class="sxs-lookup"><span data-stu-id="dce87-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="dce87-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dce87-114">PARAMETERS</span></span>

### <span data-ttu-id="dce87-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dce87-115">-Force</span></span>
<span data-ttu-id="dce87-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dce87-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dce87-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dce87-117">-InputObject</span></span>
<span data-ttu-id="dce87-118">Alert zwrócony w wyniku Get-AzsAlert.</span><span class="sxs-lookup"><span data-stu-id="dce87-118">An alert returned from Get-AzsAlert.</span></span>

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

### <span data-ttu-id="dce87-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dce87-119">-Location</span></span>
<span data-ttu-id="dce87-120">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dce87-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce87-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dce87-121">-Name</span></span>
<span data-ttu-id="dce87-122">Identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="dce87-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce87-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dce87-123">-ResourceGroupName</span></span>
<span data-ttu-id="dce87-124">Nazwa grupy zasobów, w której znajduje się dany zasób.</span><span class="sxs-lookup"><span data-stu-id="dce87-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dce87-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dce87-125">-Confirm</span></span>
<span data-ttu-id="dce87-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dce87-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dce87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dce87-127">-WhatIf</span></span>
<span data-ttu-id="dce87-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dce87-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dce87-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dce87-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dce87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dce87-130">CommonParameters</span></span>
<span data-ttu-id="dce87-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dce87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dce87-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dce87-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dce87-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dce87-133">INPUTS</span></span>

## <span data-ttu-id="dce87-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dce87-134">OUTPUTS</span></span>

## <span data-ttu-id="dce87-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dce87-135">NOTES</span></span>

## <span data-ttu-id="dce87-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dce87-136">RELATED LINKS</span></span>
