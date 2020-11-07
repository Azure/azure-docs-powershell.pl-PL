---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0983e05a36de72148571ccbbc7f1454343ad393a
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889990"
---
# <span data-ttu-id="45d54-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="45d54-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="45d54-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45d54-102">SYNOPSIS</span></span>
<span data-ttu-id="45d54-103">Usuwanie istniejącego przydziału</span><span class="sxs-lookup"><span data-stu-id="45d54-103">Delete an existing quota</span></span>

## <span data-ttu-id="45d54-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45d54-104">SYNTAX</span></span>

### <span data-ttu-id="45d54-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="45d54-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45d54-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="45d54-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45d54-107">Opis</span><span class="sxs-lookup"><span data-stu-id="45d54-107">DESCRIPTION</span></span>
<span data-ttu-id="45d54-108">Usuwanie istniejącego przydziału</span><span class="sxs-lookup"><span data-stu-id="45d54-108">Delete an existing quota</span></span>

## <span data-ttu-id="45d54-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45d54-109">EXAMPLES</span></span>

### <span data-ttu-id="45d54-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="45d54-110">EXAMPLE 1</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="45d54-111">Usuń przydział magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="45d54-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="45d54-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="45d54-112">EXAMPLE 2</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="45d54-113">Usuwanie przydziału miejsca do magazynowania według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="45d54-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="45d54-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45d54-114">PARAMETERS</span></span>

### <span data-ttu-id="45d54-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45d54-115">-Name</span></span>
<span data-ttu-id="45d54-116">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="45d54-116">The name of the storage quota.</span></span>

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

### <span data-ttu-id="45d54-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="45d54-117">-Location</span></span>
<span data-ttu-id="45d54-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="45d54-118">Resource location.</span></span>

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

### <span data-ttu-id="45d54-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45d54-119">-ResourceId</span></span>
<span data-ttu-id="45d54-120">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="45d54-120">The resource id.</span></span>

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

### <span data-ttu-id="45d54-121">-Force</span><span class="sxs-lookup"><span data-stu-id="45d54-121">-Force</span></span>
<span data-ttu-id="45d54-122">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="45d54-122">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="45d54-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45d54-123">-WhatIf</span></span>
<span data-ttu-id="45d54-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45d54-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45d54-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="45d54-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45d54-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="45d54-126">-Confirm</span></span>
<span data-ttu-id="45d54-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45d54-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45d54-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d54-128">CommonParameters</span></span>
<span data-ttu-id="45d54-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45d54-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d54-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d54-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d54-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45d54-131">INPUTS</span></span>

## <span data-ttu-id="45d54-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45d54-132">OUTPUTS</span></span>

## <span data-ttu-id="45d54-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45d54-133">NOTES</span></span>

## <span data-ttu-id="45d54-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45d54-134">RELATED LINKS</span></span>
