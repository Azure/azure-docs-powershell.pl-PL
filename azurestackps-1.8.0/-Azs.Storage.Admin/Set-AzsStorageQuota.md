---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2eec56d9fc157da994521a5b258cd28132344c52
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889078"
---
# <span data-ttu-id="409ad-101">Set-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="409ad-101">Set-AzsStorageQuota</span></span>

## <span data-ttu-id="409ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="409ad-102">SYNOPSIS</span></span>
<span data-ttu-id="409ad-103">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="409ad-103">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="409ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="409ad-104">SYNTAX</span></span>

### <span data-ttu-id="409ad-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="409ad-105">Update (Default)</span></span>
```
Set-AzsStorageQuota -Name <String> [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>]
 [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409ad-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="409ad-106">ResourceId</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -ResourceId <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409ad-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="409ad-107">InputObject</span></span>
```
Set-AzsStorageQuota [-CapacityInGb <Int32>] [-NumberOfStorageAccounts <Int32>] -InputObject <StorageQuota>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="409ad-108">Opis</span><span class="sxs-lookup"><span data-stu-id="409ad-108">DESCRIPTION</span></span>
<span data-ttu-id="409ad-109">Utwórz lub zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="409ad-109">Create or update an existing storage quota.</span></span>

## <span data-ttu-id="409ad-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="409ad-110">EXAMPLES</span></span>

### <span data-ttu-id="409ad-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="409ad-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsStorageQuota -Name 'TestUpdateStorageQuota' -CapacityInGb 123 -NumberOfStorageAccounts 10
```

<span data-ttu-id="409ad-112">Zaktualizuj istniejący przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="409ad-112">Update an existing storage quota.</span></span>

## <span data-ttu-id="409ad-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="409ad-113">PARAMETERS</span></span>

### <span data-ttu-id="409ad-114">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="409ad-114">-CapacityInGb</span></span>
<span data-ttu-id="409ad-115">Pojemność maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="409ad-115">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="409ad-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="409ad-116">-InputObject</span></span>
<span data-ttu-id="409ad-117">Posbbily zmodyfikowano przydział przestrzeni dyskowej zwrócony przez Get-AzsStorageQuota.</span><span class="sxs-lookup"><span data-stu-id="409ad-117">Posbbily modified storage quota returned by Get-AzsStorageQuota.</span></span>

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

### <span data-ttu-id="409ad-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="409ad-118">-Location</span></span>
<span data-ttu-id="409ad-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="409ad-119">Resource location.</span></span>

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

### <span data-ttu-id="409ad-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="409ad-120">-Name</span></span>
<span data-ttu-id="409ad-121">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="409ad-121">The name of the storage quota.</span></span>

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

### <span data-ttu-id="409ad-122">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="409ad-122">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="409ad-123">Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="409ad-123">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="409ad-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="409ad-124">-ResourceId</span></span>
<span data-ttu-id="409ad-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="409ad-125">The resource id.</span></span>

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

### <span data-ttu-id="409ad-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="409ad-126">-Confirm</span></span>
<span data-ttu-id="409ad-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="409ad-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="409ad-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="409ad-128">-WhatIf</span></span>
<span data-ttu-id="409ad-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="409ad-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="409ad-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="409ad-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="409ad-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409ad-131">CommonParameters</span></span>
<span data-ttu-id="409ad-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409ad-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409ad-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="409ad-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409ad-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="409ad-134">INPUTS</span></span>

## <span data-ttu-id="409ad-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="409ad-135">OUTPUTS</span></span>

### <span data-ttu-id="409ad-136">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="409ad-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="409ad-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="409ad-137">NOTES</span></span>

## <span data-ttu-id="409ad-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="409ad-138">RELATED LINKS</span></span>

