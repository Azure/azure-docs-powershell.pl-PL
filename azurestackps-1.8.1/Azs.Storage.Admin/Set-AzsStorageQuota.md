---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 641017c75243a253a6b9eb0054df7737a674f671
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889958"
---
# <span data-ttu-id="004e7-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="004e7-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="004e7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="004e7-102">SYNOPSIS</span></span>
<span data-ttu-id="004e7-103">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="004e7-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="004e7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="004e7-104">SYNTAX</span></span>

### <span data-ttu-id="004e7-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="004e7-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004e7-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="004e7-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004e7-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="004e7-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="004e7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="004e7-108">DESCRIPTION</span></span>
<span data-ttu-id="004e7-109">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="004e7-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="004e7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="004e7-110">EXAMPLES</span></span>

### <span data-ttu-id="004e7-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="004e7-111">EXAMPLE 1</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="004e7-112">Zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="004e7-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="004e7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="004e7-113">PARAMETERS</span></span>

### <span data-ttu-id="004e7-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="004e7-114">-Name</span></span>
<span data-ttu-id="004e7-115">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="004e7-115">The name of the storage quota.</span></span>

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

### <span data-ttu-id="004e7-116">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="004e7-116">-CapacityInGb</span></span>
<span data-ttu-id="004e7-117">Pojemność maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="004e7-117">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="004e7-118">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="004e7-118">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="004e7-119">Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="004e7-119">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="004e7-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="004e7-120">-Location</span></span>
<span data-ttu-id="004e7-121">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="004e7-121">Resource location.</span></span>

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

### <span data-ttu-id="004e7-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="004e7-122">-ResourceId</span></span>
<span data-ttu-id="004e7-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="004e7-123">The resource id.</span></span>

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

### <span data-ttu-id="004e7-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="004e7-124">-InputObject</span></span>
<span data-ttu-id="004e7-125">Posbbily zmodyfikowano przydział przestrzeni dyskowej zwrócony przez Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="004e7-125">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="004e7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004e7-126">-WhatIf</span></span>
<span data-ttu-id="004e7-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004e7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="004e7-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="004e7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004e7-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="004e7-129">-Confirm</span></span>
<span data-ttu-id="004e7-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="004e7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004e7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004e7-131">CommonParameters</span></span>
<span data-ttu-id="004e7-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="004e7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004e7-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="004e7-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004e7-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="004e7-134">INPUTS</span></span>

## <span data-ttu-id="004e7-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="004e7-135">OUTPUTS</span></span>

### <span data-ttu-id="004e7-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="004e7-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="004e7-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="004e7-137">NOTES</span></span>

## <span data-ttu-id="004e7-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="004e7-138">RELATED LINKS</span></span>
