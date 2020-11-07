---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710754"
---
# <span data-ttu-id="d8409-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="d8409-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="d8409-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8409-102">SYNOPSIS</span></span>
<span data-ttu-id="d8409-103">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d8409-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="d8409-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8409-104">SYNTAX</span></span>

### <span data-ttu-id="d8409-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8409-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8409-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d8409-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8409-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8409-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8409-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d8409-108">DESCRIPTION</span></span>
<span data-ttu-id="d8409-109">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d8409-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="d8409-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8409-110">EXAMPLES</span></span>

### <span data-ttu-id="d8409-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8409-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="d8409-112">Zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d8409-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="d8409-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8409-113">PARAMETERS</span></span>

### <span data-ttu-id="d8409-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="d8409-114">-CapacityInGb</span></span>
<span data-ttu-id="d8409-115">Pojemność maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="d8409-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="d8409-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8409-116">-InputObject</span></span>
<span data-ttu-id="d8409-117">Posbbily zmodyfikowano przydział przestrzeni dyskowej zwrócony przez Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="d8409-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="d8409-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d8409-118">-Location</span></span>
<span data-ttu-id="d8409-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8409-119">Resource location.</span></span>

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

### <span data-ttu-id="d8409-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d8409-120">-Name</span></span>
<span data-ttu-id="d8409-121">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="d8409-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="d8409-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="d8409-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="d8409-123">Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="d8409-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="d8409-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8409-124">-ResourceId</span></span>
<span data-ttu-id="d8409-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8409-125">The resource id.</span></span>

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

### <span data-ttu-id="d8409-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8409-126">-Confirm</span></span>
<span data-ttu-id="d8409-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8409-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8409-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8409-128">-WhatIf</span></span>
<span data-ttu-id="d8409-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8409-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8409-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8409-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8409-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8409-131">CommonParameters</span></span>
<span data-ttu-id="d8409-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8409-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8409-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8409-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8409-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8409-134">INPUTS</span></span>

## <span data-ttu-id="d8409-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8409-135">OUTPUTS</span></span>

### <span data-ttu-id="d8409-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="d8409-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="d8409-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8409-137">NOTES</span></span>

## <span data-ttu-id="d8409-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8409-138">RELATED LINKS</span></span>

