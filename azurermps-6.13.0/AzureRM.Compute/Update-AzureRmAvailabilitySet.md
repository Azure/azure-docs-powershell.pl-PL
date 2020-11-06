---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/update-azurermavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: 3e28cacc8dc6a27f20a93beb3e48ddcc0d0697cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548816"
---
# <span data-ttu-id="c0dcf-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0dcf-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="c0dcf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0dcf-102">SYNOPSIS</span></span>
<span data-ttu-id="c0dcf-103">Umożliwia zaktualizowanie zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0dcf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0dcf-104">SYNTAX</span></span>

### <span data-ttu-id="c0dcf-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0dcf-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0dcf-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="c0dcf-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0dcf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0dcf-107">DESCRIPTION</span></span>
<span data-ttu-id="c0dcf-108">Polecenie cmdlet **Update-AzureRmAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="c0dcf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0dcf-109">EXAMPLES</span></span>

### <span data-ttu-id="c0dcf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c0dcf-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="c0dcf-111">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" do zestawu dostępności zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="c0dcf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0dcf-112">PARAMETERS</span></span>

### <span data-ttu-id="c0dcf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0dcf-113">-AsJob</span></span>
<span data-ttu-id="c0dcf-114">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-115">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0dcf-115">-AvailabilitySet</span></span>
<span data-ttu-id="c0dcf-116">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-116">Specifies the availability set object to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0dcf-117">-DefaultProfile</span></span>
<span data-ttu-id="c0dcf-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-119">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="c0dcf-119">-Managed</span></span>
<span data-ttu-id="c0dcf-120">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="c0dcf-120">Managed Availability Set</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ManagedParamterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="c0dcf-121">-Sku</span></span>
<span data-ttu-id="c0dcf-122">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="c0dcf-122">The Name of Sku</span></span>

```yaml
Type: System.String
Parameter Sets: SkuParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="c0dcf-123">-Tag</span></span>
<span data-ttu-id="c0dcf-124">Pary klucz-wartość w formie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-124">Key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0dcf-125">-Confirm</span></span>
<span data-ttu-id="c0dcf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0dcf-127">-WhatIf</span></span>
<span data-ttu-id="c0dcf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c0dcf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0dcf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0dcf-130">CommonParameters</span></span>
<span data-ttu-id="c0dcf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0dcf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0dcf-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0dcf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0dcf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0dcf-133">INPUTS</span></span>

### <span data-ttu-id="c0dcf-134">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0dcf-134">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c0dcf-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0dcf-135">OUTPUTS</span></span>

### <span data-ttu-id="c0dcf-136">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="c0dcf-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="c0dcf-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0dcf-137">NOTES</span></span>

## <span data-ttu-id="c0dcf-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0dcf-138">RELATED LINKS</span></span>
