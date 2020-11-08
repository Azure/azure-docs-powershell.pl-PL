---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MixedReality.dll-Help.xml
Module Name: Az.MixedReality
online version: https://docs.microsoft.com/en-us/powershell/module/az.mixedreality/get-azspatialanchorsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MixedReality/MixedReality/help/Get-AzSpatialAnchorsAccount.md
ms.openlocfilehash: 2497b41399c79297726bc82e3232934cbd6768d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233086"
---
# <span data-ttu-id="62dae-101">Get-AzSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="62dae-101">Get-AzSpatialAnchorsAccount</span></span>

## <span data-ttu-id="62dae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62dae-102">SYNOPSIS</span></span>
<span data-ttu-id="62dae-103">Uzyskiwanie konta zakotwiczeń przestrzennych</span><span class="sxs-lookup"><span data-stu-id="62dae-103">Get Spatial Anchors Account</span></span>

## <span data-ttu-id="62dae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62dae-104">SYNTAX</span></span>

### <span data-ttu-id="62dae-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="62dae-105">ListParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62dae-106">GetParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="62dae-106">GetParameterSet (Default)</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62dae-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62dae-107">ResourceIdParameterSet</span></span>
```
Get-AzSpatialAnchorsAccount -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62dae-108">Opis</span><span class="sxs-lookup"><span data-stu-id="62dae-108">DESCRIPTION</span></span>
<span data-ttu-id="62dae-109">Uzyskiwanie lub wyświetlanie listy kont zakotwiczeń przestrzennych w niektórych abonamentach i grupach zasobów.</span><span class="sxs-lookup"><span data-stu-id="62dae-109">Get or list Spatial Anchors Account(s) in certain Subscription and Resource Group.</span></span>

## <span data-ttu-id="62dae-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62dae-110">EXAMPLES</span></span>

### <span data-ttu-id="62dae-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62dae-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : 2f7443d0-2c2b-4514-9b29-a78072a1556f
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/2f7443d0-2c2b-4514-9b29-a78072a1556f/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/demo
Name                : demo
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts

ResourceGroupName   : rg1
AccountId           : ed3273ce-1eeb-42c7-b3b8-fb9896b9801c
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/ed3273ce-1eeb-42c7-b3b8-fb9896b9801c/
AccountDomain       : mixedreality.azure.com
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/foobar
Name                : foobar
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="62dae-112">Lista wszystkich kont zakotwiczenia przestrzennego w grupie zasób "RG1".</span><span class="sxs-lookup"><span data-stu-id="62dae-112">List all Spatial Anchors Account in Resource Group "rg1".</span></span> 

### <span data-ttu-id="62dae-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="62dae-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSpatialAnchorsAccount -ResourceGroup rg1 -Name example

ResourceGroupName   : rg1
AccountId           : 5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef
AccountEndpoint     : https://mrc-anchor-prod.trafficmanager.net/Accounts/5f70bc31-a5da-4dd7-b5ec-ccdf806ff0ef/
AccountDomain       : mrc-anchor-prod.trafficmanager.net
Tags                : {}
Location            : eastus2
Id                  : /subscriptions/10438cf7-a794-4c7b-ad4c-5ddc1313ba7d/resourceGroups/rg1/providers/Microsoft.MixedReality/SpatialAnchorsAccounts/example
Name                : example
Type                : Microsoft.MixedReality/SpatialAnchorsAccounts
```

<span data-ttu-id="62dae-114">Pobierz konto zakotwiczeń przestrzennych "przykład" w grupie zasobów "RG1".</span><span class="sxs-lookup"><span data-stu-id="62dae-114">Get Spatial Anchors Account "example" in Resource Group "rg1".</span></span> 

## <span data-ttu-id="62dae-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62dae-115">PARAMETERS</span></span>

### <span data-ttu-id="62dae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62dae-116">-DefaultProfile</span></span>
<span data-ttu-id="62dae-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="62dae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62dae-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62dae-118">-Name</span></span>
<span data-ttu-id="62dae-119">Nazwa konta kotwicy przestrzennych.</span><span class="sxs-lookup"><span data-stu-id="62dae-119">Spatial Anchors Account Name.</span></span>

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: SpatialAnchorsAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dae-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62dae-120">-ResourceGroupName</span></span>
<span data-ttu-id="62dae-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62dae-121">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListParameterSet
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetParameterSet
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62dae-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62dae-122">-ResourceId</span></span>
<span data-ttu-id="62dae-123">Identyfikator zasobu konta zakotwiczenia przestrzennego.</span><span class="sxs-lookup"><span data-stu-id="62dae-123">Resource ID of Spatial Anchors Account.</span></span>

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

### <span data-ttu-id="62dae-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62dae-124">CommonParameters</span></span>
<span data-ttu-id="62dae-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62dae-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="62dae-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62dae-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62dae-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62dae-127">INPUTS</span></span>

### <span data-ttu-id="62dae-128">System. String</span><span class="sxs-lookup"><span data-stu-id="62dae-128">System.String</span></span>

## <span data-ttu-id="62dae-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62dae-129">OUTPUTS</span></span>

### <span data-ttu-id="62dae-130">Microsoft. Azure. Commands. MixedReality. SpatialAnchorsAccount. PSSpatialAnchorsAccount</span><span class="sxs-lookup"><span data-stu-id="62dae-130">Microsoft.Azure.Commands.MixedReality.SpatialAnchorsAccount.PSSpatialAnchorsAccount</span></span>

## <span data-ttu-id="62dae-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62dae-131">NOTES</span></span>

## <span data-ttu-id="62dae-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62dae-132">RELATED LINKS</span></span>
