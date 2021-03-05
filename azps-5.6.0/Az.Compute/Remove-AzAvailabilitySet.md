---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7320B832-50FD-48AE-9089-445318F3B08A
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzAvailabilitySet.md
ms.openlocfilehash: a4b4e5048e4d11a5b376650b94520232f10b29bf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988387"
---
# <span data-ttu-id="912ee-101">Remove-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="912ee-101">Remove-AzAvailabilitySet</span></span>

## <span data-ttu-id="912ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="912ee-102">SYNOPSIS</span></span>
<span data-ttu-id="912ee-103">Usuwa zestaw dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="912ee-103">Removes an availability set from Azure.</span></span>

## <span data-ttu-id="912ee-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="912ee-104">SYNTAX</span></span>

```
Remove-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="912ee-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="912ee-105">DESCRIPTION</span></span>
<span data-ttu-id="912ee-106">Polecenie **cmdlet Remove-AzAvailabilitySet** usuwa zestaw dostępności z platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="912ee-106">The **Remove-AzAvailabilitySet** cmdlet removes an availability set from Azure.</span></span>

## <span data-ttu-id="912ee-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="912ee-107">EXAMPLES</span></span>

### <span data-ttu-id="912ee-108">Przykład 1. Usuwanie zestawu dostępności</span><span class="sxs-lookup"><span data-stu-id="912ee-108">Example 1: Remove an availability set</span></span>
```
PS C:\> Remove-AzAvailabilitySet -Name "AvailabilitySet03" -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="912ee-109">To polecenie usuwa zestaw dostępności o nazwie AvailabilitySet03 w grupie zasobów o nazwie ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="912ee-109">This command removes an availability set named AvailabilitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="912ee-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="912ee-110">PARAMETERS</span></span>

### <span data-ttu-id="912ee-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="912ee-111">-AsJob</span></span>
<span data-ttu-id="912ee-112">Uruchom polecenie cmdlet w tle i zwróć zadanie w celu śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="912ee-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="912ee-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="912ee-113">-DefaultProfile</span></span>
<span data-ttu-id="912ee-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="912ee-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912ee-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="912ee-115">-Force</span></span>
<span data-ttu-id="912ee-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="912ee-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912ee-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="912ee-117">-Name</span></span>
<span data-ttu-id="912ee-118">Nazwa zestawu dostępności.</span><span class="sxs-lookup"><span data-stu-id="912ee-118">The availability set name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="912ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="912ee-120">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="912ee-120">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="912ee-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="912ee-121">-Confirm</span></span>
<span data-ttu-id="912ee-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="912ee-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912ee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="912ee-123">-WhatIf</span></span>
<span data-ttu-id="912ee-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="912ee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="912ee-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="912ee-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="912ee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="912ee-126">CommonParameters</span></span>
<span data-ttu-id="912ee-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="912ee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="912ee-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="912ee-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="912ee-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="912ee-129">INPUTS</span></span>

### <span data-ttu-id="912ee-130">System.String</span><span class="sxs-lookup"><span data-stu-id="912ee-130">System.String</span></span>

## <span data-ttu-id="912ee-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="912ee-131">OUTPUTS</span></span>

### <span data-ttu-id="912ee-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="912ee-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="912ee-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="912ee-133">NOTES</span></span>

## <span data-ttu-id="912ee-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="912ee-134">RELATED LINKS</span></span>

[<span data-ttu-id="912ee-135">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="912ee-135">Get-AzAvailabilitySet</span></span>](./Get-AzAvailabilitySet.md)

[<span data-ttu-id="912ee-136">New-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="912ee-136">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)


