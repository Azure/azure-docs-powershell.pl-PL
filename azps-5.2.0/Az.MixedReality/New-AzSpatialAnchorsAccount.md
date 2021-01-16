---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 0b61764d358cc234f66dc8bb24249ca93a4e9919
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344878"
---
# <span data-ttu-id="d961c-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d961c-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d961c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d961c-102">SYNOPSIS</span></span>
<span data-ttu-id="d961c-103">Tworzenie konta kotwicy przestrzennych</span><span class="sxs-lookup"><span data-stu-id="d961c-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="d961c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d961c-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d961c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d961c-105">DESCRIPTION</span></span>
<span data-ttu-id="d961c-106">Utwórz nowe konto zakotwiczeń przestrzennych w pewnych abonamentach, grupach zasobów i regionach.</span><span class="sxs-lookup"><span data-stu-id="d961c-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="d961c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d961c-107">EXAMPLES</span></span>

### <span data-ttu-id="d961c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d961c-108">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSpatialAnchorsAccount -ResourceGroup rg1 -Name example -Location centralus

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : centralus
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="d961c-109">Utwórz nowe konto zakotwiczeń przestrzennych "przykład" w bieżącym Abonamentzie, grupie zasobów "RG1" i centrali my.</span><span class="sxs-lookup"><span data-stu-id="d961c-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="d961c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d961c-110">PARAMETERS</span></span>

### <span data-ttu-id="d961c-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d961c-111">-Confirm</span></span>
<span data-ttu-id="d961c-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d961c-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d961c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d961c-113">-DefaultProfile</span></span>
<span data-ttu-id="d961c-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d961c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d961c-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d961c-115">-Location</span></span>
<span data-ttu-id="d961c-116">Lokalizacja konta w zakotwiczeniu przestrzennym.</span><span class="sxs-lookup"><span data-stu-id="d961c-116">Spatial Anchors Account Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d961c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d961c-117">-Name</span></span>
<span data-ttu-id="d961c-118">Nazwa konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="d961c-118">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d961c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d961c-119">-ResourceGroupName</span></span>
<span data-ttu-id="d961c-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d961c-120">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d961c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d961c-121">-WhatIf</span></span>
<span data-ttu-id="d961c-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d961c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d961c-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d961c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d961c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d961c-124">CommonParameters</span></span>
<span data-ttu-id="d961c-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d961c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d961c-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d961c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d961c-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d961c-127">INPUTS</span></span>

### <span data-ttu-id="d961c-128">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d961c-128">None</span></span>

## <span data-ttu-id="d961c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d961c-129">OUTPUTS</span></span>

### <span data-ttu-id="d961c-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="d961c-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="d961c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d961c-131">NOTES</span></span>

## <span data-ttu-id="d961c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d961c-132">RELATED LINKS</span></span>
