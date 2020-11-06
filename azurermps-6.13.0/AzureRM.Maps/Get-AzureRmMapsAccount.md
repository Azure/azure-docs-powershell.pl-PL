---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/get-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Get-AzureRmMapsAccount.md
ms.openlocfilehash: 68ccff91f6e233862ba1ee5aa94a3a3d0d8422b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552736"
---
# <span data-ttu-id="87cf2-101">Get-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="87cf2-101">Get-AzureRmMapsAccount</span></span>

## <span data-ttu-id="87cf2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="87cf2-102">SYNOPSIS</span></span>
<span data-ttu-id="87cf2-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="87cf2-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="87cf2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="87cf2-104">SYNTAX</span></span>

### <span data-ttu-id="87cf2-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="87cf2-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmMapsAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87cf2-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="87cf2-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87cf2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87cf2-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmMapsAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87cf2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="87cf2-108">DESCRIPTION</span></span>
<span data-ttu-id="87cf2-109">Polecenie cmdlet Get-AzureRmMapsAccount powoduje odinicjowanie obsługi administracyjnie konta usługi Azure Maps według grupy zasobów i nazwy lub identyfikatora zasobu. Ponadto może zwrócić listę wszystkich kont z listy zasobów lub wszystkich kont usługi Azure Maps dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87cf2-109">The Get-AzureRmMapsAccount cmdlet gets a provisioned Azure Maps account, either by resource group and name, or by resource id. Additionally, it can return a list of all accounts in the ResourceGroup, or all Azure Maps accounts for the current subscription.</span></span>

## <span data-ttu-id="87cf2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="87cf2-110">EXAMPLES</span></span>

### <span data-ttu-id="87cf2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="87cf2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="87cf2-112">Pobiera konto o nazwie Moje konto w grupie zasobu moja grupa zasobów, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="87cf2-112">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="87cf2-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="87cf2-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="87cf2-114">Pobiera wszystkie konta usługi Azure Maps z grupy zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="87cf2-114">Gets all Azure Maps accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="87cf2-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="87cf2-115">Example 3</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
[...]
```

<span data-ttu-id="87cf2-116">Pobiera wszystkie konta usługi Azure Maps w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="87cf2-116">Gets all Azure Maps accounts in the current subscription.</span></span>

### <span data-ttu-id="87cf2-117">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="87cf2-117">Example 4</span></span>
```powershell
PS C:\> Get-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount
```

<span data-ttu-id="87cf2-118">Pobiera konto map określone przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="87cf2-118">Gets the Maps account specified by the Resource Id.</span></span>

## <span data-ttu-id="87cf2-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="87cf2-119">PARAMETERS</span></span>

### <span data-ttu-id="87cf2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87cf2-120">-DefaultProfile</span></span>
<span data-ttu-id="87cf2-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="87cf2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87cf2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="87cf2-122">-Name</span></span>
<span data-ttu-id="87cf2-123">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="87cf2-123">Maps Account Name.</span></span>

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

### <span data-ttu-id="87cf2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87cf2-124">-ResourceGroupName</span></span>
<span data-ttu-id="87cf2-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="87cf2-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="87cf2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87cf2-126">-ResourceId</span></span>
<span data-ttu-id="87cf2-127">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="87cf2-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="87cf2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87cf2-128">CommonParameters</span></span>
<span data-ttu-id="87cf2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87cf2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87cf2-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87cf2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87cf2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="87cf2-131">INPUTS</span></span>

### <span data-ttu-id="87cf2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="87cf2-132">System.String</span></span>

## <span data-ttu-id="87cf2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="87cf2-133">OUTPUTS</span></span>

### <span data-ttu-id="87cf2-134">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="87cf2-134">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="87cf2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="87cf2-135">NOTES</span></span>

## <span data-ttu-id="87cf2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="87cf2-136">RELATED LINKS</span></span>
