---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmAvailabilitySet.md
ms.openlocfilehash: c7b33e3f2afd013b6fd54f6d425c0aa1d0d08bd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553960"
---
# <span data-ttu-id="6c567-101">Update-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c567-101">Update-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="6c567-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6c567-102">SYNOPSIS</span></span>
<span data-ttu-id="6c567-103">Umożliwia zaktualizowanie zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="6c567-103">Updates an availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c567-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6c567-104">SYNTAX</span></span>

### <span data-ttu-id="6c567-105">SkuParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c567-105">SkuParameterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Sku] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c567-106">ManagedParamterSet</span><span class="sxs-lookup"><span data-stu-id="6c567-106">ManagedParamterSet</span></span>
```
Update-AzureRmAvailabilitySet [-AvailabilitySet] <PSAvailabilitySet> [-Managed]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c567-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6c567-107">DESCRIPTION</span></span>
<span data-ttu-id="6c567-108">Polecenie cmdlet **Update-AzureRmAvailabilitySet** aktualizuje zestaw dostępności.</span><span class="sxs-lookup"><span data-stu-id="6c567-108">The **Update-AzureRmAvailabilitySet** cmdlet updates an availability set.</span></span>

## <span data-ttu-id="6c567-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6c567-109">EXAMPLES</span></span>

### <span data-ttu-id="6c567-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c567-110">Example 1</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName 'ResourceGroup01' -Name 'AvSet01' | Update-AzureRmAvailabilitySet -Managed;
```

<span data-ttu-id="6c567-111">To polecenie aktualizuje zestaw dostępności o nazwie "AvSet01" w grupie zasobów o nazwie "ResourceGroup01" do zestawu dostępności zarządzanej.</span><span class="sxs-lookup"><span data-stu-id="6c567-111">This command updates the availability set named 'AvSet01' in the resource group named 'ResourceGroup01' to a managed availability set.</span></span>

## <span data-ttu-id="6c567-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6c567-112">PARAMETERS</span></span>

### <span data-ttu-id="6c567-113">-AvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c567-113">-AvailabilitySet</span></span>
<span data-ttu-id="6c567-114">Określa obiekt zestawu dostępności do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="6c567-114">Specifies the availability set object to be updated.</span></span>

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

### <span data-ttu-id="6c567-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c567-115">-DefaultProfile</span></span>
<span data-ttu-id="6c567-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c567-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c567-117">-Zarządzany</span><span class="sxs-lookup"><span data-stu-id="6c567-117">-Managed</span></span>
<span data-ttu-id="6c567-118">Zarządzany zestaw dostępności</span><span class="sxs-lookup"><span data-stu-id="6c567-118">Managed Availability Set</span></span>

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

### <span data-ttu-id="6c567-119">-SKU</span><span class="sxs-lookup"><span data-stu-id="6c567-119">-Sku</span></span>
<span data-ttu-id="6c567-120">Nazwa SKU</span><span class="sxs-lookup"><span data-stu-id="6c567-120">The Name of Sku</span></span>

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

### <span data-ttu-id="6c567-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6c567-121">-Confirm</span></span>
<span data-ttu-id="6c567-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c567-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c567-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c567-123">-WhatIf</span></span>
<span data-ttu-id="6c567-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6c567-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6c567-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6c567-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c567-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c567-126">CommonParameters</span></span>
<span data-ttu-id="6c567-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c567-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c567-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c567-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c567-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c567-129">INPUTS</span></span>

### <span data-ttu-id="6c567-130">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c567-130">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="6c567-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6c567-131">OUTPUTS</span></span>

### <span data-ttu-id="6c567-132">Microsoft. Azure. Commands. COMPUTE. models. PSAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="6c567-132">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="6c567-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6c567-133">NOTES</span></span>

## <span data-ttu-id="6c567-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c567-134">RELATED LINKS</span></span>

