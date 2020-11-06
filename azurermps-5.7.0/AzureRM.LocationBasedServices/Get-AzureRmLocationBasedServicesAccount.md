---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/get-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Get-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 18f492147e897b8061795434c309cc63729bec5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542543"
---
# <span data-ttu-id="8e9cd-101">Get-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e9cd-101">Get-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="8e9cd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e9cd-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9cd-103">Pobiera konto.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-103">Gets the account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e9cd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e9cd-104">SYNTAX</span></span>

### <span data-ttu-id="8e9cd-105">ResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e9cd-105">ResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmLocationBasedServicesAccount [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9cd-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9cd-106">AccountNameParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9cd-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e9cd-107">ResourceIdParameterSet</span></span>
```
Get-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9cd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8e9cd-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9cd-109">Polecenie cmdlet **Get-AzureRmLocationBasedServicesAccount** umożliwia przechowanie konta usług opartych na lokalizacji — według grup zasobów i nazw albo według identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-109">The **Get-AzureRmLocationBasedServicesAccount** cmdlet gets a provisioned Location Based Services account, either by resource group and name, or by resource id.</span></span>

<span data-ttu-id="8e9cd-110">Ponadto może zwrócić listę wszystkich kont z listy zasobów lub wszystkich kont usług opartych na lokalizacji dla bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-110">Additionally, it can return a list of all accounts in the ResourceGroup, or all Location Based Services accounts for the current subscription.</span></span>

## <span data-ttu-id="8e9cd-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e9cd-111">EXAMPLES</span></span>

### <span data-ttu-id="8e9cd-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8e9cd-112">Example 1</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="8e9cd-113">Pobiera konto o nazwie Moje konto w grupie zasobu moja grupa zasobów, jeśli istnieje.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-113">Gets the account named MyAccount in the resource group MyResourceGroup, if it exists.</span></span>

### <span data-ttu-id="8e9cd-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8e9cd-114">Example 2</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="8e9cd-115">Pobiera wszystkie konta usług opartych na lokalizacji w grupie moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-115">Gets all Location Based Services accounts in the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="8e9cd-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8e9cd-116">Example 3</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount

ResourceGroupName   AccountName            Id
-----------------   -----------            --
[...]
MyResourceGroup     MyAccount              /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
[...]
```

<span data-ttu-id="8e9cd-117">Pobiera wszystkie konta usług opartych na lokalizacji w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-117">Gets all Location Based Services accounts in the current subscription.</span></span>

### <span data-ttu-id="8e9cd-118">Przykład 4</span><span class="sxs-lookup"><span data-stu-id="8e9cd-118">Example 4</span></span>
```
PS C:\> Get-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="8e9cd-119">Pobiera konto usługi oparte na lokalizacji określone przez identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-119">Gets the Location Based Services account specified by the Resource Id.</span></span>

## <span data-ttu-id="8e9cd-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e9cd-120">PARAMETERS</span></span>

### <span data-ttu-id="8e9cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9cd-121">-DefaultProfile</span></span>
<span data-ttu-id="8e9cd-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cd-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8e9cd-123">-Name</span></span>
<span data-ttu-id="8e9cd-124">Nazwa konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-124">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="8e9cd-126">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e9cd-127">-ResourceId</span></span>
<span data-ttu-id="8e9cd-128">Identyfikator ResourceId konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-128">Location Based Services Account ResourceId.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9cd-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9cd-129">CommonParameters</span></span>
<span data-ttu-id="8e9cd-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9cd-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9cd-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9cd-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e9cd-132">INPUTS</span></span>

### <span data-ttu-id="8e9cd-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8e9cd-133">System.String</span></span>

## <span data-ttu-id="8e9cd-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e9cd-134">OUTPUTS</span></span>

### <span data-ttu-id="8e9cd-135">Microsoft. Azure. Commands. LocationBasedServices. models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="8e9cd-135">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>
<span data-ttu-id="8e9cd-136">To polecenie cmdlet zwraca obiekt **PSLocationBasedServicesAccount** .</span><span class="sxs-lookup"><span data-stu-id="8e9cd-136">This cmdlet returns a **PSLocationBasedServicesAccount** object.</span></span>
<span data-ttu-id="8e9cd-137">Możesz zmodyfikować ten obiekt, a następnie zastosować zmiany przy użyciu polecenia **Set-AzureRmLocationBasedServices**.</span><span class="sxs-lookup"><span data-stu-id="8e9cd-137">You can modify this object, and then apply changes by using **Set-AzureRmLocationBasedServices**.</span></span>

## <span data-ttu-id="8e9cd-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e9cd-138">NOTES</span></span>

## <span data-ttu-id="8e9cd-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e9cd-139">RELATED LINKS</span></span>
