---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/get-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Get-AzMapsAccount.md
ms.openlocfilehash: 7ea94e2e7e4c3e54d67beef367dffee001e94652
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704888"
---
# <span data-ttu-id="8fb43-101">Get-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="8fb43-101">Get-AzMapsAccount</span></span>

## <span data-ttu-id="8fb43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8fb43-102">SYNOPSIS</span></span>
<span data-ttu-id="8fb43-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="8fb43-103">Gets the account.</span></span>

## <span data-ttu-id="8fb43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8fb43-104">SYNTAX</span></span>

### <span data-ttu-id="8fb43-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8fb43-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fb43-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb43-106">AccountNameParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8fb43-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fb43-107">ResourceIdParameterSet</span></span>
```
Get-AzMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fb43-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8fb43-108">DESCRIPTION</span></span>
<span data-ttu-id="8fb43-109">Polecenie cmdlet Get-AzMapsAccount powoduje odinicjowanie obsługi administracyjnie konta usługi Azure Maps według grupy zasobów i nazwy lub identyfikatora zasobu. Ponadto może zwrócić listę wszystkich kont z listy zasobów lub wszystkich kont usługi Azure Maps dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8fb43-109">The Get-AzMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="8fb43-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8fb43-110">EXAMPLES</span></span>

### <span data-ttu-id="8fb43-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8fb43-111">Example 1</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="8fb43-112">Pobiera konto o nazwie Moje konto w grupie zasobu moja grupa zasobów, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="8fb43-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="8fb43-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8fb43-113">Example 2</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="8fb43-114">Pobiera wszystkie konta usługi Azure Maps z grupy zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="8fb43-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="8fb43-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8fb43-115">Example 3</span></span>
```powershell
PS C:\> Get-AzMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="8fb43-116">Pobiera wszystkie konta usługi Azure Maps w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8fb43-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="8fb43-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8fb43-117">Example 4</span></span>
```powershell
PS C:\> Get-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="8fb43-118">Pobiera konto map określone przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8fb43-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="8fb43-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8fb43-119">PARAMETERS</span></span>

### <span data-ttu-id="8fb43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fb43-120">-DefaultProfile</span></span>
<span data-ttu-id="8fb43-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8fb43-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fb43-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8fb43-122">-Name</span></span>
<span data-ttu-id="8fb43-123">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="8fb43-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="8fb43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fb43-124">-ResourceGroupName</span></span>
<span data-ttu-id="8fb43-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8fb43-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="8fb43-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fb43-126">-ResourceId</span></span>
<span data-ttu-id="8fb43-127">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="8fb43-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="8fb43-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fb43-128">CommonParameters</span></span>
<span data-ttu-id="8fb43-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fb43-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fb43-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fb43-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fb43-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8fb43-131">INPUTS</span></span>

### <span data-ttu-id="8fb43-132">System. String</span><span class="sxs-lookup"><span data-stu-id="8fb43-132">System.String</span></span>

## <span data-ttu-id="8fb43-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8fb43-133">OUTPUTS</span></span>

### <span data-ttu-id="8fb43-134">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="8fb43-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="8fb43-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8fb43-135">NOTES</span></span>

## <span data-ttu-id="8fb43-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8fb43-136">RELATED LINKS</span></span>
