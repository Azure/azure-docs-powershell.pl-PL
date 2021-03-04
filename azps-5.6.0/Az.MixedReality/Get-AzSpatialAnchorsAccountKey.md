---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 351b7a2412a861fcebc456d165e9fc4eddea5122
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957066"
---
# <span data-ttu-id="ca48a-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ca48a-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="ca48a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca48a-102">SYNOPSIS</span></span>
<span data-ttu-id="ca48a-103">Uzyskiwanie kluczy konta funkcji Anchors przestrzennych</span><span class="sxs-lookup"><span data-stu-id="ca48a-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="ca48a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ca48a-104">SYNTAX</span></span>

### <span data-ttu-id="ca48a-105">DefaultParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ca48a-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca48a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca48a-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca48a-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca48a-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca48a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ca48a-108">DESCRIPTION</span></span>
<span data-ttu-id="ca48a-109">Uzyskaj klucze dewelopera dla konta anchors przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ca48a-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="ca48a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ca48a-110">EXAMPLES</span></span>

### <span data-ttu-id="ca48a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ca48a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ca48a-112">Uzyskiwanie kluczy dewelopera "przykładu" konta funkcji anchors przestrzennych z bieżącej subskrypcji i grupy zasobów "rg1".</span><span class="sxs-lookup"><span data-stu-id="ca48a-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="ca48a-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ca48a-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ca48a-114">Uzyskiwanie kluczy dewelopera "przykładu" konta usługi Spatial Anchors z bieżącej subskrypcji i grupy zasobów "rg1" za pomocą funkcji rurowych.</span><span class="sxs-lookup"><span data-stu-id="ca48a-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="ca48a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca48a-115">PARAMETERS</span></span>

### <span data-ttu-id="ca48a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca48a-116">-DefaultProfile</span></span>
<span data-ttu-id="ca48a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ca48a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca48a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca48a-118">-InputObject</span></span>
<span data-ttu-id="ca48a-119">Obiekt domeny niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="ca48a-119">The custom domain object.</span></span>

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

### <span data-ttu-id="ca48a-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ca48a-120">-Name</span></span>
<span data-ttu-id="ca48a-121">Spatial Anchors Account Name.</span><span class="sxs-lookup"><span data-stu-id="ca48a-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="ca48a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca48a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca48a-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca48a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ca48a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca48a-124">-ResourceId</span></span>
<span data-ttu-id="ca48a-125">Identyfikator zasobu konta zakotwiczeń przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ca48a-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ca48a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca48a-126">CommonParameters</span></span>
<span data-ttu-id="ca48a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca48a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ca48a-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca48a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca48a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca48a-129">INPUTS</span></span>

### <span data-ttu-id="ca48a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ca48a-130">System.String</span></span>

### <span data-ttu-id="ca48a-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="ca48a-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="ca48a-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca48a-132">OUTPUTS</span></span>

### <span data-ttu-id="ca48a-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ca48a-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="ca48a-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ca48a-134">NOTES</span></span>

## <span data-ttu-id="ca48a-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca48a-135">RELATED LINKS</span></span>
