---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccountKey.md
ms.openlocfilehash: ec84b4def7b1dfd19b2c85c71dc6562fa4cae763
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704854"
---
# <span data-ttu-id="f9497-101">Get-AzSpatialAnchorsAccountKey</span><span class="sxs-lookup"><span data-stu-id="f9497-101">Get-AzSpatialAnchorsAccountKey</span></span>

## <span data-ttu-id="f9497-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f9497-102">SYNOPSIS</span></span>
<span data-ttu-id="f9497-103">Uzyskiwanie kluczy konta kotwicy przestrzennych</span><span class="sxs-lookup"><span data-stu-id="f9497-103">Get keys of Spatial Anchors Account</span></span>

## <span data-ttu-id="f9497-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f9497-104">SYNTAX</span></span>

### <span data-ttu-id="f9497-105">DefaultParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f9497-105">DefaultParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9497-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9497-106">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9497-107">PipelineParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9497-107">PipelineParameterSet</span></span>
```
Get-AzSpatialAnchorsAccountKey -InputObject <PSSpatialAnchorsAccount>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9497-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f9497-108">DESCRIPTION</span></span>
<span data-ttu-id="f9497-109">Uzyskiwanie kluczy deweloperskich konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="f9497-109">Get developer keys of Spatial Anchors Account.</span></span>

## <span data-ttu-id="f9497-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f9497-110">EXAMPLES</span></span>

### <span data-ttu-id="f9497-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f9497-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccountKey -ResourceGroup rg1 -Name example

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="f9497-112">Pobierz klawisze deweloperskie z kontami zakotwiczeń przestrzennych "przykład" z bieżącego abonamentu i grupy zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="f9497-112">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1".</span></span>

### <span data-ttu-id="f9497-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f9497-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example | Get-AzSpatialAnchorsAccountKey 

PrimaryKey                                   SecondaryKey
----------                                   ------------
QTwT6LpnD6NuUfgfkCKFBmf89xWJ7tDC0Yx0yxxaejs= BGOP2NZN5ThHbDFKzW+FISSgxnnBqCPKpTsixAxkvXk=
```

<span data-ttu-id="f9497-114">Pobierz klawisze deweloperskie z kontami zakotwiczeń przestrzennych "przykład" z bieżącego abonamentu i grupy zasobów "RG1" z potokiem.</span><span class="sxs-lookup"><span data-stu-id="f9497-114">Get developer keys of Spatial Anchors Account "example" from current Subscription and Resource Group "rg1" with piping.</span></span>

## <span data-ttu-id="f9497-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f9497-115">PARAMETERS</span></span>

### <span data-ttu-id="f9497-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9497-116">-DefaultProfile</span></span>
<span data-ttu-id="f9497-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f9497-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9497-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f9497-118">-InputObject</span></span>
<span data-ttu-id="f9497-119">Niestandardowy obiekt domeny.</span><span class="sxs-lookup"><span data-stu-id="f9497-119">The custom domain object.</span></span>

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

### <span data-ttu-id="f9497-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f9497-120">-Name</span></span>
<span data-ttu-id="f9497-121">Nazwa konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="f9497-121">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="f9497-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9497-122">-ResourceGroupName</span></span>
<span data-ttu-id="f9497-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f9497-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f9497-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f9497-124">-ResourceId</span></span>
<span data-ttu-id="f9497-125">Identyfikator zasobu konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="f9497-125">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="f9497-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9497-126">CommonParameters</span></span>
<span data-ttu-id="f9497-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9497-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f9497-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9497-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9497-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f9497-129">INPUTS</span></span>

### <span data-ttu-id="f9497-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f9497-130">System.String</span></span>

### <span data-ttu-id="f9497-131">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f9497-131">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f9497-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f9497-132">OUTPUTS</span></span>

### <span data-ttu-id="f9497-133">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccountKeys</span><span class="sxs-lookup"><span data-stu-id="f9497-133">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccountKeys</span></span>

## <span data-ttu-id="f9497-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f9497-134">NOTES</span></span>

## <span data-ttu-id="f9497-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f9497-135">RELATED LINKS</span></span>
