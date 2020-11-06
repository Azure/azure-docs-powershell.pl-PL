---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f7f40982a4c7d24e02e7e365163cc6250ff8791
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523894"
---
# <span data-ttu-id="523c8-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="523c8-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="523c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="523c8-102">SYNOPSIS</span></span>
<span data-ttu-id="523c8-103">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="523c8-103">Delete a quota by name.</span></span>

## <span data-ttu-id="523c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="523c8-104">SYNTAX</span></span>

### <span data-ttu-id="523c8-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="523c8-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="523c8-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="523c8-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="523c8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="523c8-107">DESCRIPTION</span></span>
<span data-ttu-id="523c8-108">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="523c8-108">Delete a quota by name.</span></span>

## <span data-ttu-id="523c8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="523c8-109">EXAMPLES</span></span>

### <span data-ttu-id="523c8-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="523c8-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="523c8-111">Usuwanie przydziału sieciowego według nazwy.</span><span class="sxs-lookup"><span data-stu-id="523c8-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="523c8-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="523c8-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="523c8-113">Usuwanie przydziału sieci za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="523c8-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="523c8-114">--------------------------PRZYKŁAD 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="523c8-114">-------------------------- EXAMPLE 3 --------------------------</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="523c8-115">Usuwanie przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="523c8-115">Remove a network quota.</span></span>

## <span data-ttu-id="523c8-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="523c8-116">PARAMETERS</span></span>

### <span data-ttu-id="523c8-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="523c8-117">-AsJob</span></span>
<span data-ttu-id="523c8-118">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="523c8-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="523c8-119">-Force</span><span class="sxs-lookup"><span data-stu-id="523c8-119">-Force</span></span>
<span data-ttu-id="523c8-120">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="523c8-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="523c8-121">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="523c8-121">-Location</span></span>
<span data-ttu-id="523c8-122">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="523c8-122">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="523c8-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="523c8-123">-Name</span></span>
<span data-ttu-id="523c8-124">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="523c8-124">Name of the resource.</span></span>

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

### <span data-ttu-id="523c8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="523c8-125">-ResourceId</span></span>
<span data-ttu-id="523c8-126">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="523c8-126">The resource id.</span></span>

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

### <span data-ttu-id="523c8-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="523c8-127">-Confirm</span></span>
<span data-ttu-id="523c8-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="523c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="523c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="523c8-129">-WhatIf</span></span>
<span data-ttu-id="523c8-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="523c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="523c8-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="523c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="523c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="523c8-132">CommonParameters</span></span>
<span data-ttu-id="523c8-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="523c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="523c8-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="523c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="523c8-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="523c8-135">INPUTS</span></span>

## <span data-ttu-id="523c8-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="523c8-136">OUTPUTS</span></span>

## <span data-ttu-id="523c8-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="523c8-137">NOTES</span></span>

## <span data-ttu-id="523c8-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="523c8-138">RELATED LINKS</span></span>

