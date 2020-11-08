---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061484"
---
# <span data-ttu-id="e47c5-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e47c5-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="e47c5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e47c5-102">SYNOPSIS</span></span>
<span data-ttu-id="e47c5-103">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e47c5-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="e47c5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e47c5-104">SYNTAX</span></span>

### <span data-ttu-id="e47c5-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e47c5-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e47c5-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e47c5-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e47c5-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="e47c5-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e47c5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e47c5-108">DESCRIPTION</span></span>
<span data-ttu-id="e47c5-109">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e47c5-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="e47c5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e47c5-110">EXAMPLES</span></span>

### <span data-ttu-id="e47c5-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="e47c5-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="e47c5-112">Zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e47c5-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="e47c5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e47c5-113">PARAMETERS</span></span>

### <span data-ttu-id="e47c5-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e47c5-114">-Name</span></span>
<span data-ttu-id="e47c5-115">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e47c5-115">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c5-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="e47c5-116">-CapacityInGb</span></span>
<span data-ttu-id="e47c5-117">Pojemność maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="e47c5-117">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c5-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e47c5-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="e47c5-119">Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e47c5-119">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c5-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e47c5-120">-Location</span></span>
<span data-ttu-id="e47c5-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e47c5-121">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e47c5-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e47c5-122">-ResourceId</span></span>
<span data-ttu-id="e47c5-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="e47c5-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e47c5-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e47c5-124">-InputObject</span></span>
<span data-ttu-id="e47c5-125">Posbbily zmodyfikowano przydział przestrzeni dyskowej zwrócony przez Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="e47c5-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

```yaml
Type: StorageQuota
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e47c5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e47c5-126">-WhatIf</span></span>
<span data-ttu-id="e47c5-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e47c5-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e47c5-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e47c5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e47c5-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e47c5-129">-Confirm</span></span>
<span data-ttu-id="e47c5-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e47c5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e47c5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47c5-131">CommonParameters</span></span>
<span data-ttu-id="e47c5-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e47c5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47c5-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e47c5-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47c5-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e47c5-134">INPUTS</span></span>

## <span data-ttu-id="e47c5-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e47c5-135">OUTPUTS</span></span>

### <span data-ttu-id="e47c5-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e47c5-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e47c5-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e47c5-137">NOTES</span></span>

## <span data-ttu-id="e47c5-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e47c5-138">RELATED LINKS</span></span>
