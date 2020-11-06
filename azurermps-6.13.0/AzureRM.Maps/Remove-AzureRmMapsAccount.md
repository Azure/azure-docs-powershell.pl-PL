---
external help file: Microsoft.Azure.Commands.Maps.dll-Help.xml
Module Name: AzureRM.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.maps/remove-azurermmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Maps/Commands.Maps/help/Remove-AzureRmMapsAccount.md
ms.openlocfilehash: 9880bf574aec57796d185742b2f33b79da8f7c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527909"
---
# <span data-ttu-id="5daa4-101">Remove-AzureRmMapsAccount</span><span class="sxs-lookup"><span data-stu-id="5daa4-101">Remove-AzureRmMapsAccount</span></span>

## <span data-ttu-id="5daa4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5daa4-102">SYNOPSIS</span></span>
<span data-ttu-id="5daa4-103">Usuwa konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="5daa4-103">Deletes an Azure Maps account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5daa4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5daa4-104">SYNTAX</span></span>

### <span data-ttu-id="5daa4-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5daa4-105">NameParameterSet (Default)</span></span>
```
Remove-AzureRmMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5daa4-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5daa4-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5daa4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5daa4-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5daa4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5daa4-108">DESCRIPTION</span></span>
<span data-ttu-id="5daa4-109">Polecenie cmdlet Remove-AzureRmMapsAccount powoduje usunięcie określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="5daa4-109">The Remove-AzureRmMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="5daa4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5daa4-110">EXAMPLES</span></span>

### <span data-ttu-id="5daa4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5daa4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="5daa4-112">Umożliwia usunięcie konta Moje konto z grupy zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5daa4-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="5daa4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5daa4-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="5daa4-114">Usuwa określone konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="5daa4-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="5daa4-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5daa4-115">PARAMETERS</span></span>

### <span data-ttu-id="5daa4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5daa4-116">-DefaultProfile</span></span>
<span data-ttu-id="5daa4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5daa4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5daa4-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5daa4-118">-InputObject</span></span>
<span data-ttu-id="5daa4-119">Konto mapy potoku w usłudze Get-AzureRmMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="5daa4-119">Maps Account piped from Get-AzureRmMapsAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Maps.Models.PSMapsAccount
Parameter Sets: InputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5daa4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5daa4-120">-Name</span></span>
<span data-ttu-id="5daa4-121">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="5daa4-121">Maps Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: MapsAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5daa4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5daa4-122">-PassThru</span></span>
<span data-ttu-id="5daa4-123">Zwraca, czy określone konto zostało pomyślnie usunięte.</span><span class="sxs-lookup"><span data-stu-id="5daa4-123">Return whether the specified account was successfully deleted or not.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5daa4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5daa4-124">-ResourceGroupName</span></span>
<span data-ttu-id="5daa4-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5daa4-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5daa4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5daa4-126">-ResourceId</span></span>
<span data-ttu-id="5daa4-127">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="5daa4-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="5daa4-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5daa4-128">-Confirm</span></span>
<span data-ttu-id="5daa4-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5daa4-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5daa4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5daa4-130">-WhatIf</span></span>
<span data-ttu-id="5daa4-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5daa4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5daa4-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5daa4-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5daa4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5daa4-133">CommonParameters</span></span>
<span data-ttu-id="5daa4-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5daa4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5daa4-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5daa4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5daa4-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5daa4-136">INPUTS</span></span>

### <span data-ttu-id="5daa4-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5daa4-137">System.String</span></span>

### <span data-ttu-id="5daa4-138">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="5daa4-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>
<span data-ttu-id="5daa4-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5daa4-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="5daa4-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5daa4-140">OUTPUTS</span></span>

### <span data-ttu-id="5daa4-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5daa4-141">System.Boolean</span></span>

## <span data-ttu-id="5daa4-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5daa4-142">NOTES</span></span>

## <span data-ttu-id="5daa4-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5daa4-143">RELATED LINKS</span></span>
