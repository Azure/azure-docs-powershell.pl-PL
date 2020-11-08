---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055897"
---
# <span data-ttu-id="9af35-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="9af35-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="9af35-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9af35-102">SYNOPSIS</span></span>
<span data-ttu-id="9af35-103">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9af35-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="9af35-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9af35-104">SYNTAX</span></span>

### <span data-ttu-id="9af35-105">Zastosuj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9af35-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9af35-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9af35-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9af35-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9af35-107">DESCRIPTION</span></span>
<span data-ttu-id="9af35-108">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9af35-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="9af35-109">Po wywołaniu Get-AzsUpdateRun może zostać wykorzystany do zmodyfikowania postępu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9af35-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="9af35-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9af35-110">EXAMPLES</span></span>

### <span data-ttu-id="9af35-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="9af35-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="9af35-112">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9af35-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="9af35-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9af35-113">PARAMETERS</span></span>

### <span data-ttu-id="9af35-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9af35-114">-Name</span></span>
<span data-ttu-id="9af35-115">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9af35-115">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af35-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9af35-116">-ResourceGroupName</span></span>
<span data-ttu-id="9af35-117">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="9af35-117">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af35-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9af35-118">-Location</span></span>
<span data-ttu-id="9af35-119">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="9af35-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9af35-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9af35-120">-AsJob</span></span>
<span data-ttu-id="9af35-121">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="9af35-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9af35-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9af35-122">-ResourceId</span></span>
<span data-ttu-id="9af35-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9af35-123">The resource id.</span></span>

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

### <span data-ttu-id="9af35-124">-Force</span><span class="sxs-lookup"><span data-stu-id="9af35-124">-Force</span></span>
<span data-ttu-id="9af35-125">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="9af35-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="9af35-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9af35-126">-WhatIf</span></span>
<span data-ttu-id="9af35-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9af35-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9af35-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9af35-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9af35-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9af35-129">-Confirm</span></span>
<span data-ttu-id="9af35-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9af35-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9af35-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9af35-131">CommonParameters</span></span>
<span data-ttu-id="9af35-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9af35-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9af35-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9af35-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9af35-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9af35-134">INPUTS</span></span>

## <span data-ttu-id="9af35-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9af35-135">OUTPUTS</span></span>

### <span data-ttu-id="9af35-136">Microsoft. AzureStack. Management. Update. admin. models. Update</span><span class="sxs-lookup"><span data-stu-id="9af35-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="9af35-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9af35-137">NOTES</span></span>

## <span data-ttu-id="9af35-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9af35-138">RELATED LINKS</span></span>
