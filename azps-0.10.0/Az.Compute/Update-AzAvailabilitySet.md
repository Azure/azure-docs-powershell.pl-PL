---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/update-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Update-AzAvailabilitySet.md
ms.openlocfilehash: e8bd36cd9c054d155dca034f49be8cd422a244bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891597"
---
# <span data-ttu-id="c0a8b-101">Update-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0a8b-101">Update-AzAvailabilitySet</span></span>

## <span data-ttu-id="c0a8b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0a8b-102">SYNOPSIS</span></span>
<span data-ttu-id="c0a8b-103">Umożliwia zaktualizowanie zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-103">Updates an availability set.</span></span>

## <span data-ttu-id="c0a8b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0a8b-104">SYNTAX</span></span>

### <span data-ttu-id="c0a8b-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0a8b-105">SkuParameterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0a8b-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="c0a8b-106">ManagedParamterSet</span></span>
```
Update-AzAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0a8b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0a8b-107">DESCRIPTION</span></span>
<span data-ttu-id="c0a8b-108">Polecenie cmdlet **Update-AzAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-108">The **Update-AzAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="c0a8b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0a8b-109">EXAMPLES</span></span>

### <span data-ttu-id="c0a8b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0a8b-110">Example 1</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzAvailabilitySet -Managed;
```

<span data-ttu-id="c0a8b-111">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" do zestawu dostępności zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="c0a8b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0a8b-112">PARAMETERS</span></span>

### <span data-ttu-id="c0a8b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0a8b-113">-AsJob</span></span>
<span data-ttu-id="c0a8b-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="c0a8b-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0a8b-115">-AvailabilitySet</span></span>
<span data-ttu-id="c0a8b-116">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-116">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="c0a8b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0a8b-117">-DefaultProfile</span></span>
<span data-ttu-id="c0a8b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c0a8b-119">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="c0a8b-119">-Managed</span></span>
<span data-ttu-id="c0a8b-120">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="c0a8b-120">Managed Availability Set</span></span>

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

### <span data-ttu-id="c0a8b-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="c0a8b-121">-Sku</span></span>
<span data-ttu-id="c0a8b-122">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="c0a8b-122">The Name of Sku</span></span>

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

### <span data-ttu-id="c0a8b-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0a8b-123">-Confirm</span></span>
<span data-ttu-id="c0a8b-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0a8b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0a8b-125">-WhatIf</span></span>
<span data-ttu-id="c0a8b-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0a8b-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0a8b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0a8b-128">CommonParameters</span></span>
<span data-ttu-id="c0a8b-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0a8b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0a8b-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0a8b-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0a8b-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0a8b-131">INPUTS</span></span>

### <span data-ttu-id="c0a8b-132">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0a8b-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c0a8b-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0a8b-133">OUTPUTS</span></span>

### <span data-ttu-id="c0a8b-134">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0a8b-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c0a8b-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0a8b-135">NOTES</span></span>

## <span data-ttu-id="c0a8b-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0a8b-136">RELATED LINKS</span></span>

