---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 502b7b7c97752758003c1a7f0ad007e3e6cf67e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980369"
---
# <span data-ttu-id="a1888-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a1888-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="a1888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1888-102">SYNOPSIS</span></span>
<span data-ttu-id="a1888-103">Usuwanie konta funkcji anchors przestrzennych</span><span class="sxs-lookup"><span data-stu-id="a1888-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="a1888-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1888-104">SYNTAX</span></span>

### <span data-ttu-id="a1888-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a1888-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1888-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1888-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1888-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="a1888-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1888-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1888-108">DESCRIPTION</span></span>
<span data-ttu-id="a1888-109">Usuń określone konto zakotwiczeń przestrzennych z określonej grupy subskrypcji i zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1888-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="a1888-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1888-110">EXAMPLES</span></span>

### <span data-ttu-id="a1888-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1888-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="a1888-112">Usuń "przykład" konta zakotwiczeń przestrzennych z bieżącej subskrypcji i grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="a1888-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="a1888-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1888-113">PARAMETERS</span></span>

### <span data-ttu-id="a1888-114">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1888-114">-Confirm</span></span>
<span data-ttu-id="a1888-115">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1888-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1888-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1888-116">-DefaultProfile</span></span>
<span data-ttu-id="a1888-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1888-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1888-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a1888-118">-InputObject</span></span>
<span data-ttu-id="a1888-119">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="a1888-119">The custom domain object.</span></span>

```yaml
Type: PSSpatialAnchorsAccount
Parameter Sets: PipelineParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1888-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a1888-120">-Name</span></span>
<span data-ttu-id="a1888-121">Spatial Anchors Account Name.</span><span class="sxs-lookup"><span data-stu-id="a1888-121">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1888-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a1888-122">-PassThru</span></span>
<span data-ttu-id="a1888-123">Zwracanie obiektu, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="a1888-123">Return object if specified.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1888-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1888-124">-ResourceGroupName</span></span>
<span data-ttu-id="a1888-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a1888-125">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: DefaultParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1888-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a1888-126">-ResourceId</span></span>
<span data-ttu-id="a1888-127">Identyfikator zasobu konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="a1888-127">Resource ID of Spatial Anchors Account.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1888-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1888-128">-WhatIf</span></span>
<span data-ttu-id="a1888-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1888-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1888-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1888-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1888-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1888-131">CommonParameters</span></span>
<span data-ttu-id="a1888-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1888-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a1888-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1888-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1888-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1888-134">INPUTS</span></span>

### <span data-ttu-id="a1888-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a1888-135">System.String</span></span>

### <span data-ttu-id="a1888-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="a1888-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="a1888-137">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="a1888-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a1888-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1888-138">OUTPUTS</span></span>

### <span data-ttu-id="a1888-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a1888-139">System.Boolean</span></span>

## <span data-ttu-id="a1888-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1888-140">NOTES</span></span>

## <span data-ttu-id="a1888-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1888-141">RELATED LINKS</span></span>
