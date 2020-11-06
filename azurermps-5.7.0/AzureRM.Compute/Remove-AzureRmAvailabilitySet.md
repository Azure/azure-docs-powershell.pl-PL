---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmAvailabilitySet.md
ms.openlocfilehash: 467b430232805da132b568918ac0a1ed7b6db5c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526942"
---
# <span data-ttu-id="a9a3b-101">Remove-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9a3b-101">Remove-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="a9a3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9a3b-102">SYNOPSIS</span></span>
<span data-ttu-id="a9a3b-103">Usuwa zestaw dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-103">Removes an availability set from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9a3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9a3b-104">SYNTAX</span></span>

```
Remove-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a9a3b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9a3b-105">DESCRIPTION</span></span>
<span data-ttu-id="a9a3b-106">Polecenie cmdlet **Remove-AzureRmAvailabilitySet** umożliwia usunięcie zestawu dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-106">The **Remove-AzureRmAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="a9a3b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9a3b-107">EXAMPLES</span></span>

### <span data-ttu-id="a9a3b-108">Przykład 1: usuwanie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="a9a3b-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzureRmAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="a9a3b-109">To polecenie usuwa zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="a9a3b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9a3b-110">PARAMETERS</span></span>

### <span data-ttu-id="a9a3b-111">-Force</span><span class="sxs-lookup"><span data-stu-id="a9a3b-111">-Force</span></span>
<span data-ttu-id="a9a3b-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a3b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9a3b-113">-Name</span></span>
<span data-ttu-id="a9a3b-114">Nazwa zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-114">The availability set name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a3b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9a3b-115">-ResourceGroupName</span></span>
<span data-ttu-id="a9a3b-116">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-116">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9a3b-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9a3b-117">-Confirm</span></span>
<span data-ttu-id="a9a3b-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a3b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9a3b-119">-WhatIf</span></span>
<span data-ttu-id="a9a3b-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a9a3b-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9a3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9a3b-122">CommonParameters</span></span>
<span data-ttu-id="a9a3b-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9a3b-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9a3b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9a3b-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9a3b-125">INPUTS</span></span>

### <span data-ttu-id="a9a3b-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a9a3b-126">None</span></span>
<span data-ttu-id="a9a3b-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a9a3b-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9a3b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9a3b-128">OUTPUTS</span></span>

## <span data-ttu-id="a9a3b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9a3b-129">NOTES</span></span>

## <span data-ttu-id="a9a3b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9a3b-130">RELATED LINKS</span></span>

[<span data-ttu-id="a9a3b-131">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9a3b-131">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="a9a3b-132">Nowe — AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="a9a3b-132">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)


