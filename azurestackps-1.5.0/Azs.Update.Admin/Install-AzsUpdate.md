---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523777"
---
# <span data-ttu-id="447b9-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="447b9-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="447b9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="447b9-102">SYNOPSIS</span></span>
<span data-ttu-id="447b9-103">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="447b9-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="447b9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="447b9-104">SYNTAX</span></span>

### <span data-ttu-id="447b9-105">Zastosuj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="447b9-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="447b9-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="447b9-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="447b9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="447b9-107">DESCRIPTION</span></span>
<span data-ttu-id="447b9-108">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="447b9-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="447b9-109">Po wywołaniu Get-AzsUpdateRun może zostać wykorzystany do zmodyfikowania postępu aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="447b9-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="447b9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="447b9-110">EXAMPLES</span></span>

### <span data-ttu-id="447b9-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="447b9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="447b9-112">Stosowanie określonej aktualizacji w lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="447b9-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="447b9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="447b9-113">PARAMETERS</span></span>

### <span data-ttu-id="447b9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="447b9-114">-AsJob</span></span>
<span data-ttu-id="447b9-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="447b9-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="447b9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="447b9-116">-Force</span></span>
<span data-ttu-id="447b9-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="447b9-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="447b9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="447b9-118">-Location</span></span>
<span data-ttu-id="447b9-119">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="447b9-119">The name of the update location.</span></span>

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

### <span data-ttu-id="447b9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="447b9-120">-Name</span></span>
<span data-ttu-id="447b9-121">Nazwa aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="447b9-121">Name of the update.</span></span>

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

### <span data-ttu-id="447b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="447b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="447b9-123">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="447b9-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="447b9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="447b9-124">-ResourceId</span></span>
<span data-ttu-id="447b9-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="447b9-125">The resource id.</span></span>

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

### <span data-ttu-id="447b9-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="447b9-126">-Confirm</span></span>
<span data-ttu-id="447b9-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="447b9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="447b9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="447b9-128">-WhatIf</span></span>
<span data-ttu-id="447b9-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="447b9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="447b9-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="447b9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="447b9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="447b9-131">CommonParameters</span></span>
<span data-ttu-id="447b9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="447b9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="447b9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="447b9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="447b9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="447b9-134">INPUTS</span></span>

## <span data-ttu-id="447b9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="447b9-135">OUTPUTS</span></span>

### <span data-ttu-id="447b9-136">Microsoft. AzureStack. Management. Update. admin. models. Update</span><span class="sxs-lookup"><span data-stu-id="447b9-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="447b9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="447b9-137">NOTES</span></span>

## <span data-ttu-id="447b9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="447b9-138">RELATED LINKS</span></span>

