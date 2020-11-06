---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 85b62b8ffbdcdcefff5bbb5c984a19ef0b7cb644
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523462"
---
# <span data-ttu-id="8efe7-101">Remove-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="8efe7-101">Remove-AzsStorageQuota</span></span>

## <span data-ttu-id="8efe7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8efe7-102">SYNOPSIS</span></span>
<span data-ttu-id="8efe7-103">Usuwanie istniejącego przydziału</span><span class="sxs-lookup"><span data-stu-id="8efe7-103">Delete an existing quota</span></span>

## <span data-ttu-id="8efe7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8efe7-104">SYNTAX</span></span>

### <span data-ttu-id="8efe7-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8efe7-105">Delete (Default)</span></span>
```
Remove-AzsStorageQuota -Name <String> [-Location <String>] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8efe7-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="8efe7-106">ResourceId</span></span>
```
Remove-AzsStorageQuota -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8efe7-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8efe7-107">DESCRIPTION</span></span>
<span data-ttu-id="8efe7-108">Usuwanie istniejącego przydziału</span><span class="sxs-lookup"><span data-stu-id="8efe7-108">Delete an existing quota</span></span>

## <span data-ttu-id="8efe7-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8efe7-109">EXAMPLES</span></span>

### <span data-ttu-id="8efe7-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8efe7-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Remove-AzsStorageQuota -Name 'TestDeleteStorageQuota'
```

<span data-ttu-id="8efe7-111">Usuń przydział magazynowania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="8efe7-111">Remove a storage quota by name.</span></span>

### <span data-ttu-id="8efe7-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="8efe7-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageQuota -Name 'testquota' | Remove-AzsStorageQuota
```

<span data-ttu-id="8efe7-113">Usuwanie przydziału miejsca do magazynowania według połączeń rurowych.</span><span class="sxs-lookup"><span data-stu-id="8efe7-113">Remove a storage quota by piping.</span></span>

## <span data-ttu-id="8efe7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8efe7-114">PARAMETERS</span></span>

### <span data-ttu-id="8efe7-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8efe7-115">-Force</span></span>
<span data-ttu-id="8efe7-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8efe7-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8efe7-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8efe7-117">-Location</span></span>
<span data-ttu-id="8efe7-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="8efe7-118">Resource location.</span></span>

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

### <span data-ttu-id="8efe7-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8efe7-119">-Name</span></span>
<span data-ttu-id="8efe7-120">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="8efe7-120">The name of the storage quota.</span></span>

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

### <span data-ttu-id="8efe7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8efe7-121">-ResourceId</span></span>
<span data-ttu-id="8efe7-122">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8efe7-122">The resource id.</span></span>

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

### <span data-ttu-id="8efe7-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8efe7-123">-Confirm</span></span>
<span data-ttu-id="8efe7-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8efe7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8efe7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8efe7-125">-WhatIf</span></span>
<span data-ttu-id="8efe7-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8efe7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8efe7-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8efe7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8efe7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8efe7-128">CommonParameters</span></span>
<span data-ttu-id="8efe7-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8efe7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8efe7-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8efe7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8efe7-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8efe7-131">INPUTS</span></span>

## <span data-ttu-id="8efe7-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8efe7-132">OUTPUTS</span></span>

## <span data-ttu-id="8efe7-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8efe7-133">NOTES</span></span>

## <span data-ttu-id="8efe7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8efe7-134">RELATED LINKS</span></span>

