---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710686"
---
# <span data-ttu-id="7cb1f-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="7cb1f-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="7cb1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cb1f-102">SYNOPSIS</span></span>
<span data-ttu-id="7cb1f-103">Uruchamianie kolekcji garbage dla usuniętych obiektów magazynu.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="7cb1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cb1f-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cb1f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7cb1f-105">DESCRIPTION</span></span>
<span data-ttu-id="7cb1f-106">Uruchamianie kolekcji garbage dla usuniętych obiektów magazynu.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="7cb1f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cb1f-107">EXAMPLES</span></span>

### <span data-ttu-id="7cb1f-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="7cb1f-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="7cb1f-109">Uruchamianie kolekcji garbage.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-109">Start garbage collection.</span></span>

## <span data-ttu-id="7cb1f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cb1f-110">PARAMETERS</span></span>

### <span data-ttu-id="7cb1f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cb1f-111">-AsJob</span></span>
<span data-ttu-id="7cb1f-112">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="7cb1f-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="7cb1f-113">-FarmName</span></span>
<span data-ttu-id="7cb1f-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cb1f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7cb1f-115">-Force</span></span>
<span data-ttu-id="7cb1f-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7cb1f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cb1f-117">-ResourceGroupName</span></span>
<span data-ttu-id="7cb1f-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-118">Resource group name.</span></span>

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

### <span data-ttu-id="7cb1f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cb1f-119">-Confirm</span></span>
<span data-ttu-id="7cb1f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cb1f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cb1f-121">-WhatIf</span></span>
<span data-ttu-id="7cb1f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7cb1f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cb1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cb1f-124">CommonParameters</span></span>
<span data-ttu-id="7cb1f-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cb1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cb1f-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7cb1f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cb1f-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cb1f-127">INPUTS</span></span>

## <span data-ttu-id="7cb1f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cb1f-128">OUTPUTS</span></span>

## <span data-ttu-id="7cb1f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cb1f-129">NOTES</span></span>

## <span data-ttu-id="7cb1f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cb1f-130">RELATED LINKS</span></span>

