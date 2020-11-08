---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: 81bce36cb1b8cd4737141e58ad3e220199e726cf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064414"
---
# <span data-ttu-id="ed466-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="ed466-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="ed466-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed466-102">SYNOPSIS</span></span>
<span data-ttu-id="ed466-103">Uzyskiwanie kluczy konta kotwicy przestrzennych</span><span class="sxs-lookup"><span data-stu-id="ed466-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="ed466-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed466-104">SYNTAX</span></span>

### <span data-ttu-id="ed466-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed466-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed466-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed466-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed466-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed466-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed466-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ed466-108">DESCRIPTION</span></span>
<span data-ttu-id="ed466-109">Uzyskiwanie kluczy deweloperskich konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ed466-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="ed466-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed466-110">EXAMPLES</span></span>

### <span data-ttu-id="ed466-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed466-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ed466-112">Pobierz klawisze deweloperskie z kontami zakotwiczeń przestrzennych "przykład" z bieżącego abonamentu i grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="ed466-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="ed466-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed466-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="ed466-114">Pobierz klawisze deweloperskie z kontami zakotwiczeń przestrzennych "przykład" z bieżącego abonamentu i grupy zasobów "RG1" z potokiem.</span><span class="sxs-lookup"><span data-stu-id="ed466-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="ed466-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed466-115">PARAMETERS</span></span>

### <span data-ttu-id="ed466-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed466-116">-DefaultProfile</span></span>
<span data-ttu-id="ed466-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed466-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed466-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ed466-118">-InputObject</span></span>
<span data-ttu-id="ed466-119">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="ed466-119">The custom domain object.</span></span>

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

### <span data-ttu-id="ed466-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed466-120">-Name</span></span>
<span data-ttu-id="ed466-121">Nazwa konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="ed466-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="ed466-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed466-122">-ResourceGroupName</span></span>
<span data-ttu-id="ed466-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed466-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ed466-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed466-124">-ResourceId</span></span>
<span data-ttu-id="ed466-125">Identyfikator zasobu konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="ed466-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="ed466-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed466-126">CommonParameters</span></span>
<span data-ttu-id="ed466-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed466-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ed466-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed466-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed466-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed466-129">INPUTS</span></span>

### <span data-ttu-id="ed466-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ed466-130">System.String</span></span>

### <span data-ttu-id="ed466-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="ed466-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="ed466-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed466-132">OUTPUTS</span></span>

### <span data-ttu-id="ed466-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ed466-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSAccountKeys</span></span>

## <span data-ttu-id="ed466-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed466-134">NOTES</span></span>

## <span data-ttu-id="ed466-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed466-135">RELATED LINKS</span></span>
