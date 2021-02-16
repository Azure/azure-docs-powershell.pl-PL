---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194074"
---
# <span data-ttu-id="44339-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="44339-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="44339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44339-102">SYNOPSIS</span></span>
<span data-ttu-id="44339-103">Uzyskiwanie kluczy konta funkcji Anchors przestrzennych</span><span class="sxs-lookup"><span data-stu-id="44339-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="44339-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44339-104">SYNTAX</span></span>

### <span data-ttu-id="44339-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="44339-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44339-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44339-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="44339-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="44339-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="44339-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="44339-108">DESCRIPTION</span></span>
<span data-ttu-id="44339-109">Uzyskaj klucze dewelopera dla konta anchors przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="44339-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="44339-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44339-110">EXAMPLES</span></span>

### <span data-ttu-id="44339-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44339-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="44339-112">Uzyskiwanie kluczy dewelopera "przykładu" konta funkcji anchors przestrzennych z bieżącej subskrypcji i grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="44339-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="44339-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="44339-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="44339-114">Uzyskiwanie kluczy dewelopera "przykładu" konta usługi Spatial Anchors z bieżącej grupy subskrypcji i grupy zasobów "rg1" za pomocą funkcji pipingu.</span><span class="sxs-lookup"><span data-stu-id="44339-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="44339-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44339-115">PARAMETERS</span></span>

### <span data-ttu-id="44339-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44339-116">-DefaultProfile</span></span>
<span data-ttu-id="44339-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44339-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44339-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44339-118">-InputObject</span></span>
<span data-ttu-id="44339-119">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="44339-119">The custom domain object.</span></span>

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

### <span data-ttu-id="44339-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44339-120">-Name</span></span>
<span data-ttu-id="44339-121">Spatial Anchors Account Name.</span><span class="sxs-lookup"><span data-stu-id="44339-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="44339-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44339-122">-ResourceGroupName</span></span>
<span data-ttu-id="44339-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="44339-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="44339-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44339-124">-ResourceId</span></span>
<span data-ttu-id="44339-125">Identyfikator zasobu konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="44339-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="44339-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44339-126">CommonParameters</span></span>
<span data-ttu-id="44339-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44339-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="44339-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44339-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44339-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44339-129">INPUTS</span></span>

### <span data-ttu-id="44339-130">System.String</span><span class="sxs-lookup"><span data-stu-id="44339-130">System.String</span></span>

### <span data-ttu-id="44339-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="44339-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="44339-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44339-132">OUTPUTS</span></span>

### <span data-ttu-id="44339-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="44339-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="44339-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44339-134">NOTES</span></span>

## <span data-ttu-id="44339-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44339-135">RELATED LINKS</span></span>
