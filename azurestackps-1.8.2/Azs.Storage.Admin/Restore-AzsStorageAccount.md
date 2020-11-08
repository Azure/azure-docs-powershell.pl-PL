---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055873"
---
# <span data-ttu-id="8262c-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8262c-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="8262c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8262c-102">SYNOPSIS</span></span>
<span data-ttu-id="8262c-103">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8262c-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8262c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8262c-104">SYNTAX</span></span>

### <span data-ttu-id="8262c-105">Usuwanie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="8262c-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8262c-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8262c-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8262c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8262c-107">DESCRIPTION</span></span>
<span data-ttu-id="8262c-108">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8262c-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8262c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8262c-109">EXAMPLES</span></span>

### <span data-ttu-id="8262c-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="8262c-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="8262c-111">Usuwanie usuniętego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="8262c-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="8262c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8262c-112">PARAMETERS</span></span>

### <span data-ttu-id="8262c-113">-Farmname</span><span class="sxs-lookup"><span data-stu-id="8262c-113">-FarmName</span></span>
<span data-ttu-id="8262c-114">Identyfikator farmy.</span><span class="sxs-lookup"><span data-stu-id="8262c-114">Farm Id.</span></span>

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

### <span data-ttu-id="8262c-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8262c-115">-Name</span></span>
<span data-ttu-id="8262c-116">Identyfikator konta magazynu wewnętrznego, który nie jest widoczny dla dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="8262c-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="8262c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8262c-117">-ResourceGroupName</span></span>
<span data-ttu-id="8262c-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8262c-118">Resource group name.</span></span>

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

### <span data-ttu-id="8262c-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8262c-119">-ResourceId</span></span>
<span data-ttu-id="8262c-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8262c-120">The resource id.</span></span>

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

### <span data-ttu-id="8262c-121">-Force</span><span class="sxs-lookup"><span data-stu-id="8262c-121">-Force</span></span>
<span data-ttu-id="8262c-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8262c-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8262c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8262c-123">-WhatIf</span></span>
<span data-ttu-id="8262c-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8262c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8262c-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8262c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8262c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8262c-126">-Confirm</span></span>
<span data-ttu-id="8262c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8262c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8262c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8262c-128">CommonParameters</span></span>
<span data-ttu-id="8262c-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8262c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8262c-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8262c-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8262c-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8262c-131">INPUTS</span></span>

## <span data-ttu-id="8262c-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8262c-132">OUTPUTS</span></span>

## <span data-ttu-id="8262c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8262c-133">NOTES</span></span>

## <span data-ttu-id="8262c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8262c-134">RELATED LINKS</span></span>
