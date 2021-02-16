---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Maps.dll-Help.xml
Module Name: Az.Maps
online version: https://docs.microsoft.com/en-us/powershell/module/az.maps/remove-azmapsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Maps/Maps/help/Remove-AzMapsAccount.md
ms.openlocfilehash: b84a5d6cbbf090243a63ad9919a3fbb1977d77f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100241266"
---
# <span data-ttu-id="22484-101">Remove-AzMapsAccount</span><span class="sxs-lookup"><span data-stu-id="22484-101">Remove-AzMapsAccount</span></span>

## <span data-ttu-id="22484-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22484-102">SYNOPSIS</span></span>
<span data-ttu-id="22484-103">Usuwa konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="22484-103">Deletes an Azure Maps account.</span></span>

## <span data-ttu-id="22484-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="22484-104">SYNTAX</span></span>

### <span data-ttu-id="22484-105">NameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="22484-105">NameParameterSet (Default)</span></span>
```
Remove-AzMapsAccount [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22484-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22484-106">InputObjectParameterSet</span></span>
```
Remove-AzMapsAccount [-InputObject <PSMapsAccount>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22484-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22484-107">ResourceIdParameterSet</span></span>
```
Remove-AzMapsAccount [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22484-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="22484-108">DESCRIPTION</span></span>
<span data-ttu-id="22484-109">Polecenie Remove-AzMapsAccount cmdlet usuwa określone konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="22484-109">The Remove-AzMapsAccount cmdlet deletes the specified Azure Maps account.</span></span>

## <span data-ttu-id="22484-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="22484-110">EXAMPLES</span></span>

### <span data-ttu-id="22484-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="22484-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzMapsAccount -ResourceGroupName MyResourceGroup -Name MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="22484-112">Usuwa konto MyAccount z grupy zasobów MyResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22484-112">Deletes the account MyAccount from the resource group MyResourceGroup.</span></span>

### <span data-ttu-id="22484-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="22484-113">Example 2</span></span>
```
PS C:\> Remove-AzMapsAccount -ResourceId /subscriptions/21a9967a-e8a9-4656-a70b-96ff1c4d05a0/resourceGroups/MyResourceGroup/providers/Microsoft.Maps/accounts/MyAccount

Confirm
Are you sure you want to perform this action?
Performing the operation "Deleting account MyAccount." on target "MyAccount".
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="22484-114">Usuwa określone konto usługi Azure Maps.</span><span class="sxs-lookup"><span data-stu-id="22484-114">Deletes the specified Azure Maps Account.</span></span>

## <span data-ttu-id="22484-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="22484-115">PARAMETERS</span></span>

### <span data-ttu-id="22484-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22484-116">-DefaultProfile</span></span>
<span data-ttu-id="22484-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="22484-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22484-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22484-118">-InputObject</span></span>
<span data-ttu-id="22484-119">Konto mapy potokowo z Get-AzMapsAccount.</span><span class="sxs-lookup"><span data-stu-id="22484-119">Maps Account piped from Get-AzMapsAccount.</span></span>

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

### <span data-ttu-id="22484-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="22484-120">-Name</span></span>
<span data-ttu-id="22484-121">Nazwa konta mapy.</span><span class="sxs-lookup"><span data-stu-id="22484-121">Maps Account Name.</span></span>

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

### <span data-ttu-id="22484-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22484-122">-PassThru</span></span>
<span data-ttu-id="22484-123">Sprawdź, czy określone konto zostało pomyślnie usunięte.</span><span class="sxs-lookup"><span data-stu-id="22484-123">Return whether the specified account was successfully deleted or not.</span></span>

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

### <span data-ttu-id="22484-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22484-124">-ResourceGroupName</span></span>
<span data-ttu-id="22484-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22484-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="22484-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22484-126">-ResourceId</span></span>
<span data-ttu-id="22484-127">Konto mapy ResourceId.</span><span class="sxs-lookup"><span data-stu-id="22484-127">Maps Account ResourceId.</span></span>

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

### <span data-ttu-id="22484-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="22484-128">-Confirm</span></span>
<span data-ttu-id="22484-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="22484-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22484-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22484-130">-WhatIf</span></span>
<span data-ttu-id="22484-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22484-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22484-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="22484-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22484-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22484-133">CommonParameters</span></span>
<span data-ttu-id="22484-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22484-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22484-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22484-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22484-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22484-136">INPUTS</span></span>

### <span data-ttu-id="22484-137">System.String</span><span class="sxs-lookup"><span data-stu-id="22484-137">System.String</span></span>

### <span data-ttu-id="22484-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span><span class="sxs-lookup"><span data-stu-id="22484-138">Microsoft.Azure.Commands.Maps.Models.PSMapsAccount</span></span>

## <span data-ttu-id="22484-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22484-139">OUTPUTS</span></span>

### <span data-ttu-id="22484-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="22484-140">System.Boolean</span></span>

## <span data-ttu-id="22484-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="22484-141">NOTES</span></span>

## <span data-ttu-id="22484-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22484-142">RELATED LINKS</span></span>
