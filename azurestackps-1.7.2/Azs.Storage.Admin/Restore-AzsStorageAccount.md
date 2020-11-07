---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888029"
---
# <span data-ttu-id="ba26c-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ba26c-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="ba26c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ba26c-102">SYNOPSIS</span></span>
<span data-ttu-id="ba26c-103">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba26c-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="ba26c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ba26c-104">SYNTAX</span></span>

### <span data-ttu-id="ba26c-105">Usuwanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ba26c-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ba26c-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ba26c-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba26c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ba26c-107">DESCRIPTION</span></span>
<span data-ttu-id="ba26c-108">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba26c-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="ba26c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ba26c-109">EXAMPLES</span></span>

### <span data-ttu-id="ba26c-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ba26c-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="ba26c-111">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="ba26c-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="ba26c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ba26c-112">PARAMETERS</span></span>

### <span data-ttu-id="ba26c-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="ba26c-113">-FarmName</span></span>
<span data-ttu-id="ba26c-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="ba26c-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba26c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ba26c-115">-Force</span></span>
<span data-ttu-id="ba26c-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba26c-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="ba26c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ba26c-117">-Name</span></span>
<span data-ttu-id="ba26c-118">Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="ba26c-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba26c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba26c-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba26c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ba26c-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba26c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ba26c-121">-ResourceId</span></span>
<span data-ttu-id="ba26c-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ba26c-122">The resource id.</span></span>

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

### <span data-ttu-id="ba26c-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba26c-123">-Confirm</span></span>
<span data-ttu-id="ba26c-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba26c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba26c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba26c-125">-WhatIf</span></span>
<span data-ttu-id="ba26c-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba26c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba26c-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ba26c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba26c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba26c-128">CommonParameters</span></span>
<span data-ttu-id="ba26c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba26c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba26c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba26c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba26c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba26c-131">INPUTS</span></span>

## <span data-ttu-id="ba26c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ba26c-132">OUTPUTS</span></span>

## <span data-ttu-id="ba26c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ba26c-133">NOTES</span></span>

## <span data-ttu-id="ba26c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba26c-134">RELATED LINKS</span></span>

