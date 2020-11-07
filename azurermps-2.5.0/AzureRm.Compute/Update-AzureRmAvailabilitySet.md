---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f7d9181b5ec79434928fc8d291025aea9480b8e9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899354"
---
# <span data-ttu-id="de34a-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de34a-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="de34a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de34a-102">SYNOPSIS</span></span>
<span data-ttu-id="de34a-103">Umożliwia zaktualizowanie zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="de34a-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de34a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de34a-104">SYNTAX</span></span>

### <span data-ttu-id="de34a-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="de34a-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de34a-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="de34a-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de34a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de34a-107">DESCRIPTION</span></span>
<span data-ttu-id="de34a-108">Polecenie cmdlet **Update-AzureRmAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="de34a-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="de34a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de34a-109">EXAMPLES</span></span>

### <span data-ttu-id="de34a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de34a-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="de34a-111">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" do zestawu dostępności zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="de34a-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="de34a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de34a-112">PARAMETERS</span></span>

### <span data-ttu-id="de34a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de34a-113">-AsJob</span></span>
<span data-ttu-id="de34a-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="de34a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de34a-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de34a-115">-AvailabilitySet</span></span>
<span data-ttu-id="de34a-116">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="de34a-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="de34a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de34a-117">-DefaultProfile</span></span>
<span data-ttu-id="de34a-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de34a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de34a-119">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="de34a-119">-Managed</span></span>
<span data-ttu-id="de34a-120">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="de34a-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="de34a-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="de34a-121">-Sku</span></span>
<span data-ttu-id="de34a-122">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="de34a-122">The Name of Sku</span></span>

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

### <span data-ttu-id="de34a-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="de34a-123">-Confirm</span></span>
<span data-ttu-id="de34a-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de34a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de34a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de34a-125">-WhatIf</span></span>
<span data-ttu-id="de34a-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="de34a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="de34a-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="de34a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de34a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de34a-128">CommonParameters</span></span>
<span data-ttu-id="de34a-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de34a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de34a-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de34a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de34a-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de34a-131">INPUTS</span></span>

### <span data-ttu-id="de34a-132">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de34a-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="de34a-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de34a-133">OUTPUTS</span></span>

### <span data-ttu-id="de34a-134">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="de34a-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="de34a-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de34a-135">NOTES</span></span>

## <span data-ttu-id="de34a-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de34a-136">RELATED LINKS</span></span>

