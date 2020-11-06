---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/new-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/New-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 739ce121e26f1010c5c13ff3330dadffa02053af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528126"
---
# <span data-ttu-id="0eb62-101">New-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0eb62-101">New-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="0eb62-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0eb62-102">SYNOPSIS</span></span>
<span data-ttu-id="0eb62-103">Umożliwia utworzenie konta usług opartego na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0eb62-103">Creates a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0eb62-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0eb62-104">SYNTAX</span></span>

```
New-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String> [-SkuName] <String>
 [-Tag <Hashtable[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0eb62-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0eb62-105">DESCRIPTION</span></span>
<span data-ttu-id="0eb62-106">Polecenie cmdlet **New-AzureRmLocationBasedServicesAccount** umożliwia utworzenie konta usług opartego na lokalizacji przy użyciu określonej jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="0eb62-106">The **New-AzureRmLocationBasedServicesAccount** cmdlet creates a Location Based Services account with the specified SKU.</span></span>

## <span data-ttu-id="0eb62-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0eb62-107">EXAMPLES</span></span>

### <span data-ttu-id="0eb62-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0eb62-108">Example 1</span></span>
```
PS C:\> New-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount -SkuName S0 -Tags @{Name="test";Value="true"}

Notice
By creating a Location Based Account, you are consenting to the terms of use (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): y

ResourceGroupName AccountName Id
----------------- ----------- --
MyResourceGroup   MyAccount   /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount
```

<span data-ttu-id="0eb62-109">Tworzy nowe konto usług opartych na lokalizacji o nazwie Moje konto w grupie zasobu moja grupa zasobów z S0ą SKU i znacznikiem.</span><span class="sxs-lookup"><span data-stu-id="0eb62-109">Creates a new Location Based Services account named MyAccount in the resource group MyResourceGroup with the SKU S0 and a tag.</span></span>

## <span data-ttu-id="0eb62-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0eb62-110">PARAMETERS</span></span>

### <span data-ttu-id="0eb62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0eb62-111">-DefaultProfile</span></span>
<span data-ttu-id="0eb62-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0eb62-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0eb62-113">-Force</span><span class="sxs-lookup"><span data-stu-id="0eb62-113">-Force</span></span>
<span data-ttu-id="0eb62-114">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0eb62-114">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb62-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0eb62-115">-Name</span></span>
<span data-ttu-id="0eb62-116">Nazwa konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0eb62-116">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb62-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0eb62-117">-ResourceGroupName</span></span>
<span data-ttu-id="0eb62-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="0eb62-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb62-119">-SkuName</span><span class="sxs-lookup"><span data-stu-id="0eb62-119">-SkuName</span></span>
<span data-ttu-id="0eb62-120">Nazwa SKU konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0eb62-120">Location Based Services Account Sku Name.</span></span>

<span data-ttu-id="0eb62-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0eb62-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0eb62-122">S0</span><span class="sxs-lookup"><span data-stu-id="0eb62-122">S0</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: S0

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0eb62-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="0eb62-123">-Tag</span></span>
<span data-ttu-id="0eb62-124">Znaczniki kont usług na podstawie lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="0eb62-124">Location Based Services Account Tags.</span></span>

```yaml
Type: Hashtable[]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0eb62-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0eb62-125">-Confirm</span></span>
<span data-ttu-id="0eb62-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb62-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0eb62-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0eb62-127">-WhatIf</span></span>
<span data-ttu-id="0eb62-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0eb62-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0eb62-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0eb62-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0eb62-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0eb62-130">CommonParameters</span></span>
<span data-ttu-id="0eb62-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0eb62-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0eb62-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0eb62-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0eb62-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0eb62-133">INPUTS</span></span>

### <span data-ttu-id="0eb62-134">System. String</span><span class="sxs-lookup"><span data-stu-id="0eb62-134">System.String</span></span>

## <span data-ttu-id="0eb62-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0eb62-135">OUTPUTS</span></span>

### <span data-ttu-id="0eb62-136">Microsoft. Azure. Commands. LocationBasedServices. models. PSLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="0eb62-136">Microsoft.Azure.Commands.LocationBasedServices.Models.PSLocationBasedServicesAccount</span></span>

## <span data-ttu-id="0eb62-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0eb62-137">NOTES</span></span>

<span data-ttu-id="0eb62-138">Tworzenie konta usług opartych na lokalizacji wymaga wyświetlenia monitu o zaakceptowanie warunków (zobacz https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/) .</span><span class="sxs-lookup"><span data-stu-id="0eb62-138">Creating a Location Based Services account requires answering a prompt to accept terms (see https://azure.microsoft.com/en-us/support/legal/preview-supplemental-terms/).</span></span>  <span data-ttu-id="0eb62-139">Parametru-Force można użyć w celu wskazania akceptacji warunków.</span><span class="sxs-lookup"><span data-stu-id="0eb62-139">The -Force parameter can be used to indicate acceptance of the terms.</span></span>

## <span data-ttu-id="0eb62-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0eb62-140">RELATED LINKS</span></span>
