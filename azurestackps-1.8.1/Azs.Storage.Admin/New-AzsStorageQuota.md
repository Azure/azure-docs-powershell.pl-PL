---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4cc08220a92dce5a49544cf958db79d7243b9ebb
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889989"
---
# <span data-ttu-id="e1388-101">New-AzsStorageQuota</span><span class="sxs-lookup"><span data-stu-id="e1388-101">New-AzsStorageQuota</span></span>

## <span data-ttu-id="e1388-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1388-102">SYNOPSIS</span></span>
<span data-ttu-id="e1388-103">Utwórz nowy przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e1388-103">Create a new storage quota.</span></span>

## <span data-ttu-id="e1388-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1388-104">SYNTAX</span></span>

```
New-AzsStorageQuota [-Name] <String> [[-CapacityInGb] <Int32>] [[-NumberOfStorageAccounts] <Int32>]
 [[-Location] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1388-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1388-105">DESCRIPTION</span></span>
<span data-ttu-id="e1388-106">Utwórz nowy przydział magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e1388-106">Create a new storage quota.</span></span>

## <span data-ttu-id="e1388-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1388-107">EXAMPLES</span></span>

### <span data-ttu-id="e1388-108">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="e1388-108">EXAMPLE 1</span></span>
```
New-AzsStorageQuota -CapacityInGb 1000 -NumberOfStorageAccounts 100 -Name 'TestCreateStorageQuota'
```

<span data-ttu-id="e1388-109">Utwórz nowy przydział magazynowania z określonymi wartościami.</span><span class="sxs-lookup"><span data-stu-id="e1388-109">Create a new storage quota with specified values.</span></span>

## <span data-ttu-id="e1388-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1388-110">PARAMETERS</span></span>

### <span data-ttu-id="e1388-111">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1388-111">-Name</span></span>
<span data-ttu-id="e1388-112">Nazwa przydziału miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="e1388-112">The name of the storage quota.</span></span>

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

### <span data-ttu-id="e1388-113">-CapacityInGb</span><span class="sxs-lookup"><span data-stu-id="e1388-113">-CapacityInGb</span></span>
<span data-ttu-id="e1388-114">Pojemność maxium (GB).</span><span class="sxs-lookup"><span data-stu-id="e1388-114">Maxium capacity (GB).</span></span>

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

### <span data-ttu-id="e1388-115">-NumberOfStorageAccounts</span><span class="sxs-lookup"><span data-stu-id="e1388-115">-NumberOfStorageAccounts</span></span>
<span data-ttu-id="e1388-116">Łączna liczba kont magazynu.</span><span class="sxs-lookup"><span data-stu-id="e1388-116">Total number of storage accounts.</span></span>

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

### <span data-ttu-id="e1388-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e1388-117">-Location</span></span>
<span data-ttu-id="e1388-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e1388-118">Resource location.</span></span>

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

### <span data-ttu-id="e1388-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1388-119">-WhatIf</span></span>
<span data-ttu-id="e1388-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1388-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1388-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1388-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1388-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1388-122">-Confirm</span></span>
<span data-ttu-id="e1388-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1388-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1388-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1388-124">CommonParameters</span></span>
<span data-ttu-id="e1388-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1388-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1388-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1388-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1388-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1388-127">INPUTS</span></span>

## <span data-ttu-id="e1388-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1388-128">OUTPUTS</span></span>

### <span data-ttu-id="e1388-129">Microsoft. AzureStack. Management. Storage. admin. models. StorageQuota</span><span class="sxs-lookup"><span data-stu-id="e1388-129">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageQuota</span></span>

## <span data-ttu-id="e1388-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1388-130">NOTES</span></span>

## <span data-ttu-id="e1388-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1388-131">RELATED LINKS</span></span>
