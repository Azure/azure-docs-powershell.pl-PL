---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889874"
---
# <span data-ttu-id="1fa80-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="1fa80-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="1fa80-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1fa80-102">SYNOPSIS</span></span>
<span data-ttu-id="1fa80-103">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1fa80-103">Delete a quota by name.</span></span>

## <span data-ttu-id="1fa80-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1fa80-104">SYNTAX</span></span>

### <span data-ttu-id="1fa80-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1fa80-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fa80-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1fa80-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fa80-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1fa80-107">DESCRIPTION</span></span>
<span data-ttu-id="1fa80-108">Usuwanie przydziału według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1fa80-108">Delete a quota by name.</span></span>

## <span data-ttu-id="1fa80-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1fa80-109">EXAMPLES</span></span>

### <span data-ttu-id="1fa80-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="1fa80-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="1fa80-111">Usuwanie przydziału sieciowego według nazwy.</span><span class="sxs-lookup"><span data-stu-id="1fa80-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="1fa80-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="1fa80-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="1fa80-113">Usuwanie przydziału sieci za pomocą potoku.</span><span class="sxs-lookup"><span data-stu-id="1fa80-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="1fa80-114">PRZYKŁAD 3</span><span class="sxs-lookup"><span data-stu-id="1fa80-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="1fa80-115">Usuwanie przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="1fa80-115">Remove a network quota.</span></span>

## <span data-ttu-id="1fa80-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1fa80-116">PARAMETERS</span></span>

### <span data-ttu-id="1fa80-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1fa80-117">-Name</span></span>
<span data-ttu-id="1fa80-118">Nazwa zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fa80-118">Name of the resource.</span></span>

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

### <span data-ttu-id="1fa80-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1fa80-119">-Location</span></span>
<span data-ttu-id="1fa80-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fa80-120">Location of the resource.</span></span>

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

### <span data-ttu-id="1fa80-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fa80-121">-ResourceId</span></span>
<span data-ttu-id="1fa80-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1fa80-122">The resource id.</span></span>

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

### <span data-ttu-id="1fa80-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fa80-123">-AsJob</span></span>
<span data-ttu-id="1fa80-124">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="1fa80-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="1fa80-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1fa80-125">-Force</span></span>
<span data-ttu-id="1fa80-126">Parametr przełącznika dla potwierdzenia niepytania.</span><span class="sxs-lookup"><span data-stu-id="1fa80-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="1fa80-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fa80-127">-WhatIf</span></span>
<span data-ttu-id="1fa80-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fa80-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fa80-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1fa80-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fa80-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1fa80-130">-Confirm</span></span>
<span data-ttu-id="1fa80-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1fa80-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fa80-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fa80-132">CommonParameters</span></span>
<span data-ttu-id="1fa80-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fa80-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fa80-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fa80-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fa80-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1fa80-135">INPUTS</span></span>

## <span data-ttu-id="1fa80-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1fa80-136">OUTPUTS</span></span>

## <span data-ttu-id="1fa80-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1fa80-137">NOTES</span></span>

## <span data-ttu-id="1fa80-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1fa80-138">RELATED LINKS</span></span>
