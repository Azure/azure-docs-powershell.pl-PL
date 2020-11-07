---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: 5a2a8157e69c1b50cc066bb24e8261c1748a6323
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93893589"
---
# <span data-ttu-id="822f0-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="822f0-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="822f0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="822f0-102">SYNOPSIS</span></span>
<span data-ttu-id="822f0-103">Usuwa zestaw dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822f0-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="822f0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="822f0-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="822f0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="822f0-105">DESCRIPTION</span></span>
<span data-ttu-id="822f0-106">Polecenie cmdlet **Remove-AzAvailabilitySet** umożliwia usunięcie zestawu dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="822f0-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="822f0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="822f0-107">EXAMPLES</span></span>

### <span data-ttu-id="822f0-108">Przykład 1: usuwanie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="822f0-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="822f0-109">To polecenie usuwa zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="822f0-109">This command removes an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="822f0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="822f0-110">PARAMETERS</span></span>

### <span data-ttu-id="822f0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="822f0-111">-AsJob</span></span>
<span data-ttu-id="822f0-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="822f0-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="822f0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822f0-113">-DefaultProfile</span></span>
<span data-ttu-id="822f0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="822f0-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822f0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="822f0-115">-Force</span></span>
<span data-ttu-id="822f0-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="822f0-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="822f0-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="822f0-117">-Name</span></span>
<span data-ttu-id="822f0-118">Nazwa zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="822f0-118">The availability set name.</span></span>

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

### <span data-ttu-id="822f0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="822f0-119">-ResourceGroupName</span></span>
<span data-ttu-id="822f0-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="822f0-120">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="822f0-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="822f0-121">-Confirm</span></span>
<span data-ttu-id="822f0-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="822f0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822f0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822f0-123">-WhatIf</span></span>
<span data-ttu-id="822f0-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="822f0-124">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="822f0-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="822f0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822f0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822f0-126">CommonParameters</span></span>
<span data-ttu-id="822f0-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822f0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822f0-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="822f0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822f0-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="822f0-129">INPUTS</span></span>

### <span data-ttu-id="822f0-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="822f0-130">None</span></span>
<span data-ttu-id="822f0-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="822f0-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="822f0-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="822f0-132">OUTPUTS</span></span>

### <span data-ttu-id="822f0-133">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="822f0-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="822f0-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="822f0-134">NOTES</span></span>

## <span data-ttu-id="822f0-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="822f0-135">RELATED LINKS</span></span>

[<span data-ttu-id="822f0-136">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="822f0-136">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="822f0-137">Nowe — AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="822f0-137">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


