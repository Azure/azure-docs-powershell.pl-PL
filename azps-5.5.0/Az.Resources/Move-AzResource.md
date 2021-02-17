---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: d14d591ffdc0e20934a0cf758407dc2b4e6e152c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192754"
---
# <span data-ttu-id="adfe8-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="adfe8-101">Move-AzResource</span></span>

## <span data-ttu-id="adfe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adfe8-102">SYNOPSIS</span></span>
<span data-ttu-id="adfe8-103">Przenosi zasób do innej grupy zasobów lub innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="adfe8-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="adfe8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="adfe8-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adfe8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="adfe8-105">DESCRIPTION</span></span>
<span data-ttu-id="adfe8-106">Polecenie **cmdlet Move-AzResource** przenosi istniejące zasoby do innej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="adfe8-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="adfe8-107">Ta grupa zasobów może mieć inną subskrypcję.</span><span class="sxs-lookup"><span data-stu-id="adfe8-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="adfe8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="adfe8-108">EXAMPLES</span></span>

### <span data-ttu-id="adfe8-109">Przykład 1. Przenoszenie zasobu do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="adfe8-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="adfe8-110">Pierwsze polecenie pobiera zasób o nazwie ContosoStorageAccount przy użyciu polecenia cmdlet Get-AzResource, a następnie przechowuje ten zasób w $Resource zmienną.</span><span class="sxs-lookup"><span data-stu-id="adfe8-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="adfe8-111">Drugie polecenie przenosi ten zasób do grupy zasobów o nazwie Grupa Zasobów14.</span><span class="sxs-lookup"><span data-stu-id="adfe8-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="adfe8-112">To polecenie identyfikuje zasób do przeniesienia przy użyciu właściwości **Identyfikator** Zasobu $Resource.</span><span class="sxs-lookup"><span data-stu-id="adfe8-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="adfe8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="adfe8-113">PARAMETERS</span></span>

### <span data-ttu-id="adfe8-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="adfe8-114">-ApiVersion</span></span>
<span data-ttu-id="adfe8-115">Określa wersję interfejsu API dostawcy zasobów do użycia.</span><span class="sxs-lookup"><span data-stu-id="adfe8-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="adfe8-116">Jeśli nie określisz wersji, to polecenie cmdlet użyje najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="adfe8-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfe8-117">-DefaultProfile</span></span>
<span data-ttu-id="adfe8-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="adfe8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adfe8-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfe8-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="adfe8-120">Określa nazwę grupy zasobów, do której to polecenie cmdlet przenosi zasoby.</span><span class="sxs-lookup"><span data-stu-id="adfe8-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe8-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="adfe8-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="adfe8-122">Określa identyfikator subskrypcji, do której to polecenie cmdlet przenosi zasoby.</span><span class="sxs-lookup"><span data-stu-id="adfe8-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adfe8-123">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="adfe8-123">-Force</span></span>
<span data-ttu-id="adfe8-124">Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="adfe8-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="adfe8-125">— Przed</span><span class="sxs-lookup"><span data-stu-id="adfe8-125">-Pre</span></span>
<span data-ttu-id="adfe8-126">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="adfe8-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="adfe8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="adfe8-127">-ResourceId</span></span>
<span data-ttu-id="adfe8-128">Określa tablicę identyfikatorów zasobów przeniesionych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adfe8-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="adfe8-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="adfe8-129">-Confirm</span></span>
<span data-ttu-id="adfe8-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="adfe8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adfe8-131">-WhatIf</span></span>
<span data-ttu-id="adfe8-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adfe8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="adfe8-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="adfe8-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="adfe8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfe8-134">CommonParameters</span></span>
<span data-ttu-id="adfe8-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adfe8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfe8-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="adfe8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfe8-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adfe8-137">INPUTS</span></span>

### <span data-ttu-id="adfe8-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="adfe8-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="adfe8-139">System.String[]</span><span class="sxs-lookup"><span data-stu-id="adfe8-139">System.String[]</span></span>

## <span data-ttu-id="adfe8-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="adfe8-140">OUTPUTS</span></span>

### <span data-ttu-id="adfe8-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="adfe8-141">System.Boolean</span></span>

## <span data-ttu-id="adfe8-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="adfe8-142">NOTES</span></span>

## <span data-ttu-id="adfe8-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="adfe8-143">RELATED LINKS</span></span>

[<span data-ttu-id="adfe8-144">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="adfe8-144">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="adfe8-145">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="adfe8-145">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="adfe8-146">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="adfe8-146">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="adfe8-147">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="adfe8-147">Set-AzResource</span></span>](./Set-AzResource.md)


