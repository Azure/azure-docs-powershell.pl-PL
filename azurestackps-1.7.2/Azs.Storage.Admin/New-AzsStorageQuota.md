---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 143f368b73aac490242e42f21ed76ee76ab012dc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888034"
---
# <span data-ttu-id="3e79a-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="3e79a-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="3e79a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e79a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e79a-103">Utwórz nowy przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3e79a-103">Create a new storage quota.</span></span>

## <span data-ttu-id="3e79a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e79a-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e79a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e79a-105">DESCRIPTION</span></span>
<span data-ttu-id="3e79a-106">Utwórz nowy przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3e79a-106">Create a new storage quota.</span></span>

## <span data-ttu-id="3e79a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e79a-107">EXAMPLES</span></span>

### <span data-ttu-id="3e79a-108">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3e79a-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="3e79a-109">Utwórz nowy przydział magazynowania z określonymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="3e79a-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="3e79a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e79a-110">PARAMETERS</span></span>

### <span data-ttu-id="3e79a-111">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="3e79a-111">-CapacityInGb</span></span>
<span data-ttu-id="3e79a-112">Pojemność maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="3e79a-112">Maxium capacity (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 500
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e79a-113">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e79a-113">-Location</span></span>
<span data-ttu-id="3e79a-114">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3e79a-114">Resource location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e79a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e79a-115">-Name</span></span>
<span data-ttu-id="3e79a-116">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="3e79a-116">The name of the storage quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e79a-117">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="3e79a-117">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="3e79a-118">Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="3e79a-118">Total number of storage accounts.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: 20
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e79a-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e79a-119">-Confirm</span></span>
<span data-ttu-id="3e79a-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e79a-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e79a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e79a-121">-WhatIf</span></span>
<span data-ttu-id="3e79a-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e79a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e79a-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e79a-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e79a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e79a-124">CommonParameters</span></span>
<span data-ttu-id="3e79a-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e79a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e79a-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e79a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e79a-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e79a-127">INPUTS</span></span>

## <span data-ttu-id="3e79a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e79a-128">OUTPUTS</span></span>

### <span data-ttu-id="3e79a-129">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="3e79a-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="3e79a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e79a-130">NOTES</span></span>

## <span data-ttu-id="3e79a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e79a-131">RELATED LINKS</span></span>

