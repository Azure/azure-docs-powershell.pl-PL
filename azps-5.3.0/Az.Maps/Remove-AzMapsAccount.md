---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499717"
---
# <span data-ttu-id="7b8be-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="7b8be-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="7b8be-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b8be-102">SYNOPSIS</span></span>
<span data-ttu-id="7b8be-103">Usuwa konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7b8be-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="7b8be-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b8be-104">SYNTAX</span></span>

### <span data-ttu-id="7b8be-105">NameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b8be-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b8be-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8be-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7b8be-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b8be-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b8be-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7b8be-108">DESCRIPTION</span></span>
<span data-ttu-id="7b8be-109">Polecenie cmdlet Remove-AzMapsAccount powoduje usunięcie określonego konta usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7b8be-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="7b8be-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b8be-110">EXAMPLES</span></span>

### <span data-ttu-id="7b8be-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b8be-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7b8be-112">Umożliwia usunięcie konta Moje konto z grupy zasobu moja grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b8be-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="7b8be-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7b8be-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="7b8be-114">Usuwa określone konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="7b8be-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="7b8be-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b8be-115">PARAMETERS</span></span>

### <span data-ttu-id="7b8be-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b8be-116">-DefaultProfile</span></span>
<span data-ttu-id="7b8be-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b8be-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b8be-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7b8be-118">-InputObject</span></span>
<span data-ttu-id="7b8be-119">Konto mapy potoku w usłudze Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="7b8be-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="7b8be-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b8be-120">-Name</span></span>
<span data-ttu-id="7b8be-121">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="7b8be-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="7b8be-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b8be-122">-PassThru</span></span>
<span data-ttu-id="7b8be-123">Zwraca, czy określone konto zostało pomyślnie usunięte.</span><span class="sxs-lookup"><span data-stu-id="7b8be-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="7b8be-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b8be-124">-ResourceGroupName</span></span>
<span data-ttu-id="7b8be-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b8be-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b8be-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b8be-126">-ResourceId</span></span>
<span data-ttu-id="7b8be-127">Mapowanie ResourceId konta.</span><span class="sxs-lookup"><span data-stu-id="7b8be-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="7b8be-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7b8be-128">-Confirm</span></span>
<span data-ttu-id="7b8be-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b8be-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b8be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b8be-130">-WhatIf</span></span>
<span data-ttu-id="7b8be-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b8be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b8be-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7b8be-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b8be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b8be-133">CommonParameters</span></span>
<span data-ttu-id="7b8be-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b8be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b8be-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b8be-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b8be-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b8be-136">INPUTS</span></span>

### <span data-ttu-id="7b8be-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7b8be-137">System.String</span></span>

### <span data-ttu-id="7b8be-138">Microsoft. Azure. Commands. Maps. modele. PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="7b8be-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="7b8be-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b8be-139">OUTPUTS</span></span>

### <span data-ttu-id="7b8be-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7b8be-140">System.Boolean</span></span>

## <span data-ttu-id="7b8be-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b8be-141">NOTES</span></span>

## <span data-ttu-id="7b8be-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b8be-142">RELATED LINKS</span></span>
