---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ab432625ab6af4a8fbd23895cb82e1d9f83954c8
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889766"
---
# <span data-ttu-id="e81be-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="e81be-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="e81be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e81be-102">SYNOPSIS</span></span>
<span data-ttu-id="e81be-103">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e81be-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="e81be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e81be-104">SYNTAX</span></span>

### <span data-ttu-id="e81be-105">Zastosuj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e81be-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e81be-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e81be-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e81be-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e81be-107">DESCRIPTION</span></span>
<span data-ttu-id="e81be-108">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e81be-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="e81be-109">Po wywołaniu Get-AzsUpdateRun może zostać wykorzystany do zmodyfikowania postępu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e81be-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="e81be-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e81be-110">EXAMPLES</span></span>

### <span data-ttu-id="e81be-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="e81be-111">EXAMPLE 1</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="e81be-112">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e81be-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="e81be-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e81be-113">PARAMETERS</span></span>

### <span data-ttu-id="e81be-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e81be-114">-Name</span></span>
<span data-ttu-id="e81be-115">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e81be-115">Name of the update.</span></span>

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

### <span data-ttu-id="e81be-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e81be-116">-ResourceGroupName</span></span>
<span data-ttu-id="e81be-117">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="e81be-117">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="e81be-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e81be-118">-Location</span></span>
<span data-ttu-id="e81be-119">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="e81be-119">The name of the update location.</span></span>

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

### <span data-ttu-id="e81be-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e81be-120">-AsJob</span></span>
<span data-ttu-id="e81be-121">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="e81be-121">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e81be-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e81be-122">-ResourceId</span></span>
<span data-ttu-id="e81be-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e81be-123">The resource id.</span></span>

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

### <span data-ttu-id="e81be-124">-Force</span><span class="sxs-lookup"><span data-stu-id="e81be-124">-Force</span></span>
<span data-ttu-id="e81be-125">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="e81be-125">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="e81be-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e81be-126">-WhatIf</span></span>
<span data-ttu-id="e81be-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81be-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e81be-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e81be-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e81be-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e81be-129">-Confirm</span></span>
<span data-ttu-id="e81be-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e81be-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e81be-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e81be-131">CommonParameters</span></span>
<span data-ttu-id="e81be-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e81be-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e81be-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e81be-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e81be-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e81be-134">INPUTS</span></span>

## <span data-ttu-id="e81be-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e81be-135">OUTPUTS</span></span>

### <span data-ttu-id="e81be-136">Microsoft. AzureStack. Management. Update. admin. models. Update</span><span class="sxs-lookup"><span data-stu-id="e81be-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="e81be-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e81be-137">NOTES</span></span>

## <span data-ttu-id="e81be-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e81be-138">RELATED LINKS</span></span>
