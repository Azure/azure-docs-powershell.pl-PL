---
external help file: Microsoft.Azure.Commands.LocationBasedServices.dll-Help.xml
Module Name: AzureRM.LocationBasedServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.locationbasedservices/remove-azurermlocationbasedservicesaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LocationBasedServices/Commands.LocationBasedServices/help/Remove-AzureRmLocationBasedServicesAccount.md
ms.openlocfilehash: 0496fcdba082370654b3259f101987d1a78621fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549727"
---
# <span data-ttu-id="a9d2c-101">Remove-AzureRmLocationBasedServicesAccount</span><span class="sxs-lookup"><span data-stu-id="a9d2c-101">Remove-AzureRmLocationBasedServicesAccount</span></span>

## <span data-ttu-id="a9d2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9d2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a9d2c-103">Umożliwia usunięcie konta usług opartego na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-103">Deletes a Location Based Services account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9d2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9d2c-104">SYNTAX</span></span>

### <span data-ttu-id="a9d2c-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a9d2c-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d2c-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9d2c-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-InputObject <PSLocationBasedServicesAccount>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9d2c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9d2c-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmLocationBasedServicesAccount [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9d2c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a9d2c-108">DESCRIPTION</span></span>
<span data-ttu-id="a9d2c-109">Polecenie cmdlet **Remove-AzureRmLocationBasedServicesAccount** usuwa określone konto usługi oparte na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-109">The **Remove-AzureRmLocationBasedServicesAccount** cmdlet deletes the specified Location Based Services account.</span></span>

## <span data-ttu-id="a9d2c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9d2c-110">EXAMPLES</span></span>

### <span data-ttu-id="a9d2c-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9d2c-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a9d2c-112">Umożliwia usunięcie konta Moje konto z grupy zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="a9d2c-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a9d2c-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmLocationBasedServicesAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.LocationBasedServices/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="a9d2c-114">Usuwa określone konto usługi oparte na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-114">Deletes the specified Location Based Services Account.</span></span>

## <span data-ttu-id="a9d2c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9d2c-115">PARAMETERS</span></span>

### <span data-ttu-id="a9d2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9d2c-116">-DefaultProfile</span></span>
<span data-ttu-id="a9d2c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9d2c-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a9d2c-118">-InputObject</span></span>
<span data-ttu-id="a9d2c-119">Konto usług opartych na lokalizacji potoku w usłudze [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span><span class="sxs-lookup"><span data-stu-id="a9d2c-119">Location Based Services Account piped from [Get-AzureRmLocationBasedServicesAccount](Get-AzureRmLocationBasedServicesAccount.md).</span></span>

```yaml
Type: PSLocationBasedServicesAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d2c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9d2c-120">-Name</span></span>
<span data-ttu-id="a9d2c-121">Nazwa konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-121">Location Based Services Account Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: LocationBasedServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d2c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9d2c-122">-ResourceGroupName</span></span>
<span data-ttu-id="a9d2c-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9d2c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9d2c-124">-ResourceId</span></span>
<span data-ttu-id="a9d2c-125">Identyfikator ResourceId konta usług opartych na lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-125">Location Based Services Account ResourceId.</span></span>
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

### <span data-ttu-id="a9d2c-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9d2c-126">-Confirm</span></span>
<span data-ttu-id="a9d2c-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9d2c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9d2c-128">-WhatIf</span></span>
<span data-ttu-id="a9d2c-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9d2c-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9d2c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9d2c-131">CommonParameters</span></span>
<span data-ttu-id="a9d2c-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9d2c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9d2c-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9d2c-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9d2c-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9d2c-134">INPUTS</span></span>

### <span data-ttu-id="a9d2c-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a9d2c-135">System.String</span></span>

## <span data-ttu-id="a9d2c-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9d2c-136">OUTPUTS</span></span>

### <span data-ttu-id="a9d2c-137">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9d2c-137">System.Object</span></span>

## <span data-ttu-id="a9d2c-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9d2c-138">NOTES</span></span>

## <span data-ttu-id="a9d2c-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9d2c-139">RELATED LINKS</span></span>
