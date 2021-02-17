---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: edd98f284aa5bba6bba39c149d20a713b388bf4d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192251"
---
# <span data-ttu-id="56bc1-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="56bc1-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="56bc1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56bc1-102">SYNOPSIS</span></span>
<span data-ttu-id="56bc1-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="56bc1-103">Gets the account.</span></span>

## <span data-ttu-id="56bc1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="56bc1-104">SYNTAX</span></span>

### <span data-ttu-id="56bc1-105">ResourceGroupParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="56bc1-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56bc1-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56bc1-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56bc1-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56bc1-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56bc1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="56bc1-108">DESCRIPTION</span></span>
<span data-ttu-id="56bc1-109">Polecenie Get-AzMapsAccount cmdlet uzyskuje aprowizowane konto usługi Azure Maps według grupy zasobów i nazwy lub identyfikatora zasobu. Ponadto może zwrócić listę wszystkich kont w grupie zasobów lub wszystkich kont usługi Azure Maps dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56bc1-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="56bc1-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="56bc1-110">EXAMPLES</span></span>

### <span data-ttu-id="56bc1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="56bc1-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="56bc1-112">Pobiera konto o nazwie MyAccount w grupie zasobów MyResourceGroup, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="56bc1-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="56bc1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="56bc1-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="56bc1-114">Pobiera wszystkie konta usługi Azure Maps w grupie zasobów MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="56bc1-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="56bc1-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="56bc1-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="56bc1-116">Pobiera wszystkie konta usługi Azure Maps w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="56bc1-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="56bc1-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="56bc1-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="56bc1-118">Pobiera konto mapy określone przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="56bc1-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="56bc1-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56bc1-119">PARAMETERS</span></span>

### <span data-ttu-id="56bc1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56bc1-120">-DefaultProfile</span></span>
<span data-ttu-id="56bc1-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="56bc1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56bc1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="56bc1-122">-Name</span></span>
<span data-ttu-id="56bc1-123">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="56bc1-123">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bc1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56bc1-124">-ResourceGroupName</span></span>
<span data-ttu-id="56bc1-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="56bc1-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bc1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56bc1-126">-ResourceId</span></span>
<span data-ttu-id="56bc1-127">Mapuj konto ResourceId.</span><span class="sxs-lookup"><span data-stu-id="56bc1-127">Maps Account ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56bc1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56bc1-128">CommonParameters</span></span>
<span data-ttu-id="56bc1-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56bc1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56bc1-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56bc1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56bc1-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56bc1-131">INPUTS</span></span>

### <span data-ttu-id="56bc1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="56bc1-132">System.String</span></span>

## <span data-ttu-id="56bc1-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56bc1-133">OUTPUTS</span></span>

### <span data-ttu-id="56bc1-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="56bc1-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="56bc1-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="56bc1-135">NOTES</span></span>

## <span data-ttu-id="56bc1-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56bc1-136">RELATED LINKS</span></span>
