---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/powershell/module/az.mixedreality/new-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/New-AzSpatialAnchorsAccount.md
ms.openlocfilehash: a2a6dafe9aedfc41200e12bb3c583ad1b5fb02b6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970522"
---
# <span data-ttu-id="f1251-101">New-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f1251-101">New-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f1251-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1251-102">SYNOPSIS</span></span>
<span data-ttu-id="f1251-103">Tworzenie konta zakotwiczeń przestrzennych</span><span class="sxs-lookup"><span data-stu-id="f1251-103">Create Spatial Anchors Account</span></span>

## <span data-ttu-id="f1251-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1251-104">SYNTAX</span></span>

```
New-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1251-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1251-105">DESCRIPTION</span></span>
<span data-ttu-id="f1251-106">Utwórz nowe konto usługi Spatial Anchors w ramach określonej subskrypcji, grupy zasobów i regionu.</span><span class="sxs-lookup"><span data-stu-id="f1251-106">Create a new Spatial Anchors Account in certain Subscription, Resource Group and Region.</span></span>

## <span data-ttu-id="f1251-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1251-107">EXAMPLES</span></span>

### <span data-ttu-id="f1251-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f1251-108">Example 1</span></span>
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

<span data-ttu-id="f1251-109">Tworzenie nowego "przykładu" konta usługi Anchors przestrzennych w bieżącej subskrypcji, grupy zasobów "rg1" i środkowych Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="f1251-109">Create a new Spatial Anchors Account "example" in current Subscription, Resource Group "rg1" and Central US.</span></span>

## <span data-ttu-id="f1251-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1251-110">PARAMETERS</span></span>

### <span data-ttu-id="f1251-111">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1251-111">-Confirm</span></span>
<span data-ttu-id="f1251-112">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f1251-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1251-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1251-113">-DefaultProfile</span></span>
<span data-ttu-id="f1251-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1251-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1251-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f1251-115">-Location</span></span>
<span data-ttu-id="f1251-116">Lokalizacja konta usługi Spatial Anchors.</span><span class="sxs-lookup"><span data-stu-id="f1251-116">Spatial Anchors Account Location.</span></span>

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

### <span data-ttu-id="f1251-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f1251-117">-Name</span></span>
<span data-ttu-id="f1251-118">Spatial Anchors Account Name.</span><span class="sxs-lookup"><span data-stu-id="f1251-118">Spatial Anchors Account Name.</span></span>

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

### <span data-ttu-id="f1251-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1251-119">-ResourceGroupName</span></span>
<span data-ttu-id="f1251-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f1251-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="f1251-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1251-121">-WhatIf</span></span>
<span data-ttu-id="f1251-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1251-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1251-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f1251-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1251-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1251-124">CommonParameters</span></span>
<span data-ttu-id="f1251-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1251-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f1251-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1251-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1251-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1251-127">INPUTS</span></span>

### <span data-ttu-id="f1251-128">Brak</span><span class="sxs-lookup"><span data-stu-id="f1251-128">None</span></span>

## <span data-ttu-id="f1251-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1251-129">OUTPUTS</span></span>

### <span data-ttu-id="f1251-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="f1251-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="f1251-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1251-131">NOTES</span></span>

## <span data-ttu-id="f1251-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1251-132">RELATED LINKS</span></span>
