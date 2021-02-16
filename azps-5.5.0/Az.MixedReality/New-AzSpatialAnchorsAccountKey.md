---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 35c00fca10223a22d586efba8961dd9cab6b0faf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185018"
---
# <span data-ttu-id="ece70-101">New-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ece70-101">New-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="ece70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece70-102">SYNOPSIS</span></span>
<span data-ttu-id="ece70-103">Klucz ponownego generowania konta zakotwiczeń przestrzennych</span><span class="sxs-lookup"><span data-stu-id="ece70-103">Regenerate key of Spatial Anchors Account</span></span>

## <span data-ttu-id="ece70-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ece70-104">SYNTAX</span></span>

### <span data-ttu-id="ece70-105">RegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece70-105">RegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece70-106">RegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece70-106">RegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece70-107">ResourceIdRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece70-107">ResourceIdRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Primary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece70-108">ResourceIdRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece70-108">ResourceIdRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -ResourceId <String> [-Secondary] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece70-109">PipelineRegeneratePrimaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece70-109">PipelineRegeneratePrimaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Primary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ece70-110">PipelineRegenerateSecondaryKeyParameterSet</span><span class="sxs-lookup"><span data-stu-id="ece70-110">PipelineRegenerateSecondaryKeyParameterSet</span></span>
```
New-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount> -Secondary [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece70-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="ece70-111">DESCRIPTION</span></span>
<span data-ttu-id="ece70-112">Ponownie generuj klucz podstawowy lub klucz pomocniczy konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ece70-112">Regenerate primary key or secondary key of Spatial Anchors Account.</span></span>

## <span data-ttu-id="ece70-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ece70-113">EXAMPLES</span></span>

### <span data-ttu-id="ece70-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ece70-114">Example 1</span></span>
```powershell
PS C:\> New-AzSpatialAnchorsAccountKey -ResourceGroupName rg1 -Name example -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= mF8lsBeEbs51H/jLe4COW4zUiEyg9lDM1XHQ03jtxZU=
```

<span data-ttu-id="ece70-115">Ponownie generuj klucz pomocniczy konta zakotwiczeń przestrzennych w "przykładzie" w grupie zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="ece70-115">Regenerate secondary key of Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

### <span data-ttu-id="ece70-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ece70-116">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | New-AzSpatialAnchorsAccountKey -Secondary

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ece70-117">Ponownie generuj klucz pomocniczy konta zakotwiczeń przestrzennych "example" z bieżącej subskrypcji i grupy zasobów "rg1" za pomocą funkcji rurowych.</span><span class="sxs-lookup"><span data-stu-id="ece70-117">Regenerate secondary key of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="ece70-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ece70-118">PARAMETERS</span></span>

### <span data-ttu-id="ece70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece70-119">-DefaultProfile</span></span>
<span data-ttu-id="ece70-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ece70-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-121">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="ece70-121">-Force</span></span>
<span data-ttu-id="ece70-122">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ece70-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ece70-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ece70-123">-InputObject</span></span>
<span data-ttu-id="ece70-124">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="ece70-124">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineRegeneratePrimaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ece70-125">-Name</span></span>
<span data-ttu-id="ece70-126">Spatial Anchors Account Name.</span><span class="sxs-lookup"><span data-stu-id="ece70-126">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-127">— Podstawowy</span><span class="sxs-lookup"><span data-stu-id="ece70-127">-Primary</span></span>
<span data-ttu-id="ece70-128">Ponownie generuj klucz podstawowy konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ece70-128">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegeneratePrimaryKeyParameterSet, ResourceIdRegeneratePrimaryKeyParameterSet, PipelineRegeneratePrimaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece70-129">-ResourceGroupName</span></span>
<span data-ttu-id="ece70-130">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ece70-130">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: RegeneratePrimaryKeyParameterSet, RegenerateSecondaryKeyParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ece70-131">-ResourceId</span></span>
<span data-ttu-id="ece70-132">Identyfikator zasobu konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ece70-132">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdRegeneratePrimaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-133">— pomocniczy</span><span class="sxs-lookup"><span data-stu-id="ece70-133">-Secondary</span></span>
<span data-ttu-id="ece70-134">Ponownie generuj klucz podstawowy konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ece70-134">Regenerate primary key of Spatial Anchors Account.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RegenerateSecondaryKeyParameterSet, ResourceIdRegenerateSecondaryKeyParameterSet, PipelineRegenerateSecondaryKeyParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece70-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ece70-135">-Confirm</span></span>
<span data-ttu-id="ece70-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ece70-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ece70-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece70-137">-WhatIf</span></span>
<span data-ttu-id="ece70-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ece70-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ece70-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ece70-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ece70-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece70-140">CommonParameters</span></span>
<span data-ttu-id="ece70-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ece70-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ece70-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece70-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece70-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece70-143">INPUTS</span></span>

### <span data-ttu-id="ece70-144">System.String</span><span class="sxs-lookup"><span data-stu-id="ece70-144">System.String</span></span>

### <span data-ttu-id="ece70-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="ece70-145">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="ece70-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ece70-146">OUTPUTS</span></span>

### <span data-ttu-id="ece70-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ece70-147">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="ece70-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ece70-148">NOTES</span></span>

## <span data-ttu-id="ece70-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ece70-149">RELATED LINKS</span></span>
