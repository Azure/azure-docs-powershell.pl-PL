---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/remove-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Remove-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 5ba079a17dcfb0a263766237adbbec9beb4cc64c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053301"
---
# <span data-ttu-id="8a5a6-101">Remove-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="8a5a6-101">Remove-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="8a5a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8a5a6-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5a6-103">Usuwanie konta kotwicy przestrzennych</span><span class="sxs-lookup"><span data-stu-id="8a5a6-103">Delete Spatial Anchors Account</span></span>

## <span data-ttu-id="8a5a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8a5a6-104">SYNTAX</span></span>

### <span data-ttu-id="8a5a6-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8a5a6-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5a6-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5a6-106">ResourceIdParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a5a6-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a5a6-107">PipelineParameterSet</span></span>
```
Remove-AzSpatialAnchorsAccount -InputObject <PSSpatialAnchorsAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a5a6-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8a5a6-108">DESCRIPTION</span></span>
<span data-ttu-id="8a5a6-109">Usuwanie określonych kont zakotwiczeń przestrzennych z określonych subskrypcji i grup zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-109">Delete specified Spatial Anchors Account from certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="8a5a6-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8a5a6-110">EXAMPLES</span></span>

### <span data-ttu-id="8a5a6-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a5a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example
```

<span data-ttu-id="8a5a6-112">Usuń konto zakotwiczeń przestrzennych "przykład" z bieżącego abonamentu i grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="8a5a6-112">Delete Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="8a5a6-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8a5a6-113">PARAMETERS</span></span>

### <span data-ttu-id="8a5a6-114">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a5a6-114">-Confirm</span></span>
<span data-ttu-id="8a5a6-115">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a5a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5a6-116">-DefaultProfile</span></span>
<span data-ttu-id="8a5a6-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a5a6-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8a5a6-118">-InputObject</span></span>
<span data-ttu-id="8a5a6-119">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-119">The custom domain object.</span></span>

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

### <span data-ttu-id="8a5a6-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8a5a6-120">-Name</span></span>
<span data-ttu-id="8a5a6-121">Nazwa konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="8a5a6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a5a6-122">-PassThru</span></span>
<span data-ttu-id="8a5a6-123">Zwraca obiekt, jeśli jest określony.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-123">Return object if specified.</span></span>

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

### <span data-ttu-id="8a5a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a5a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="8a5a6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8a5a6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a5a6-126">-ResourceId</span></span>
<span data-ttu-id="8a5a6-127">Identyfikator zasobu konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-127">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="8a5a6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a5a6-128">-WhatIf</span></span>
<span data-ttu-id="8a5a6-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a5a6-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a5a6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5a6-131">CommonParameters</span></span>
<span data-ttu-id="8a5a6-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5a6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8a5a6-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a5a6-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5a6-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a5a6-134">INPUTS</span></span>

### <span data-ttu-id="8a5a6-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8a5a6-135">System.String</span></span>

### <span data-ttu-id="8a5a6-136">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="8a5a6-136">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

### <span data-ttu-id="8a5a6-137">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8a5a6-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8a5a6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8a5a6-138">OUTPUTS</span></span>

### <span data-ttu-id="8a5a6-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8a5a6-139">System.Boolean</span></span>

## <span data-ttu-id="8a5a6-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8a5a6-140">NOTES</span></span>

## <span data-ttu-id="8a5a6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a5a6-141">RELATED LINKS</span></span>
