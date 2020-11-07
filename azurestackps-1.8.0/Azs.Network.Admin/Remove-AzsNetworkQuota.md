---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889294"
---
# <span data-ttu-id="226f0-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="226f0-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="226f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="226f0-102">SYNOPSIS</span></span>
<span data-ttu-id="226f0-103">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="226f0-103">Delete a quota by name.</span></span>

## <span data-ttu-id="226f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="226f0-104">SYNTAX</span></span>

### <span data-ttu-id="226f0-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="226f0-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="226f0-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="226f0-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="226f0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="226f0-107">DESCRIPTION</span></span>
<span data-ttu-id="226f0-108">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="226f0-108">Delete a quota by name.</span></span>

## <span data-ttu-id="226f0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="226f0-109">EXAMPLES</span></span>

### <span data-ttu-id="226f0-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="226f0-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="226f0-111">Usuwanie przydziału sieciowego według nazwy.</span><span class="sxs-lookup"><span data-stu-id="226f0-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="226f0-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="226f0-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="226f0-113">Usuwanie przydziału sieci za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="226f0-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="226f0-114">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="226f0-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="226f0-115">Usuwanie przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="226f0-115">Remove a network quota.</span></span>

## <span data-ttu-id="226f0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="226f0-116">PARAMETERS</span></span>

### <span data-ttu-id="226f0-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="226f0-117">-Name</span></span>
<span data-ttu-id="226f0-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="226f0-118">Name of the resource.</span></span>

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

### <span data-ttu-id="226f0-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="226f0-119">-Location</span></span>
<span data-ttu-id="226f0-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="226f0-120">Location of the resource.</span></span>

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

### <span data-ttu-id="226f0-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="226f0-121">-ResourceId</span></span>
<span data-ttu-id="226f0-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="226f0-122">The resource id.</span></span>

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

### <span data-ttu-id="226f0-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="226f0-123">-AsJob</span></span>
<span data-ttu-id="226f0-124">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="226f0-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="226f0-125">-Force</span><span class="sxs-lookup"><span data-stu-id="226f0-125">-Force</span></span>
<span data-ttu-id="226f0-126">Parametr przełącznika dla potwierdzenia niepytania.</span><span class="sxs-lookup"><span data-stu-id="226f0-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="226f0-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="226f0-127">-WhatIf</span></span>
<span data-ttu-id="226f0-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="226f0-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="226f0-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="226f0-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="226f0-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="226f0-130">-Confirm</span></span>
<span data-ttu-id="226f0-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="226f0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="226f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="226f0-132">CommonParameters</span></span>
<span data-ttu-id="226f0-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="226f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="226f0-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="226f0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="226f0-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="226f0-135">INPUTS</span></span>

## <span data-ttu-id="226f0-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="226f0-136">OUTPUTS</span></span>

## <span data-ttu-id="226f0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="226f0-137">NOTES</span></span>

## <span data-ttu-id="226f0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="226f0-138">RELATED LINKS</span></span>
