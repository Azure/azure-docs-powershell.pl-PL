---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 7e460c866912387b05a55b6fd228c65ef9b68348
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525254"
---
# <span data-ttu-id="06e0d-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06e0d-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="06e0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="06e0d-103">Umożliwia zaktualizowanie zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="06e0d-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06e0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06e0d-104">SYNTAX</span></span>

### <span data-ttu-id="06e0d-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="06e0d-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="06e0d-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="06e0d-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="06e0d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="06e0d-107">DESCRIPTION</span></span>
<span data-ttu-id="06e0d-108">Polecenie cmdlet **Update-AzureRmAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="06e0d-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="06e0d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06e0d-109">EXAMPLES</span></span>

### <span data-ttu-id="06e0d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06e0d-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="06e0d-111">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" do zestawu dostępności zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="06e0d-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="06e0d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06e0d-112">PARAMETERS</span></span>

### <span data-ttu-id="06e0d-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06e0d-113">-AvailabilitySet</span></span>
<span data-ttu-id="06e0d-114">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="06e0d-114">Specifies the availability set object to be updated.</span></span>

```yaml
Type: PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06e0d-115">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="06e0d-115">-Managed</span></span>
<span data-ttu-id="06e0d-116">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="06e0d-116">Managed Availability Set</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e0d-117">-SKU</span><span class="sxs-lookup"><span data-stu-id="06e0d-117">-Sku</span></span>
<span data-ttu-id="06e0d-118">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="06e0d-118">The Name of Sku</span></span>

```yaml
Type: String
Parameter Sets: SkuParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06e0d-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06e0d-119">-Confirm</span></span>
<span data-ttu-id="06e0d-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e0d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06e0d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06e0d-121">-WhatIf</span></span>
<span data-ttu-id="06e0d-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06e0d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06e0d-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="06e0d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06e0d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06e0d-124">CommonParameters</span></span>
<span data-ttu-id="06e0d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06e0d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06e0d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06e0d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06e0d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06e0d-127">INPUTS</span></span>

### <span data-ttu-id="06e0d-128">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06e0d-128">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="06e0d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06e0d-129">OUTPUTS</span></span>

### <span data-ttu-id="06e0d-130">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="06e0d-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="06e0d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06e0d-131">NOTES</span></span>

## <span data-ttu-id="06e0d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06e0d-132">RELATED LINKS</span></span>

