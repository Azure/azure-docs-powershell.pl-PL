---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/move-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Move-AzResource.md
ms.openlocfilehash: 4f21ce7a14873d201fa18f45c96d508dcd38cb8e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223643"
---
# <span data-ttu-id="65a77-101">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="65a77-101">Move-AzResource</span></span>

## <span data-ttu-id="65a77-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65a77-102">SYNOPSIS</span></span>
<span data-ttu-id="65a77-103">Przenoszenie zasobu do innej grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="65a77-103">Moves a resource to a different resource group or subscription.</span></span>

## <span data-ttu-id="65a77-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65a77-104">SYNTAX</span></span>

```
Move-AzResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="65a77-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65a77-105">DESCRIPTION</span></span>
<span data-ttu-id="65a77-106">Polecenie cmdlet **Move-AzResource** przenosi istniejące zasoby do innej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="65a77-106">The **Move-AzResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="65a77-107">Ta grupa zasobów może być w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="65a77-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="65a77-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65a77-108">EXAMPLES</span></span>

### <span data-ttu-id="65a77-109">Przykład 1. Przenoszenie zasobu do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="65a77-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="65a77-110">Pierwsze polecenie uzyskuje zasób o nazwie ContosoStorageAccount przy użyciu polecenia cmdlet Get-AzResource, a następnie przechowuje ten zasób w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="65a77-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="65a77-111">Drugie polecenie przeniesie zasób do grupy zasobów o nazwie ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="65a77-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="65a77-112">To polecenie identyfikuje zasób do przeniesienia przy użyciu właściwości **ResourceId** $Resource.</span><span class="sxs-lookup"><span data-stu-id="65a77-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="65a77-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65a77-113">PARAMETERS</span></span>

### <span data-ttu-id="65a77-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65a77-114">-ApiVersion</span></span>
<span data-ttu-id="65a77-115">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="65a77-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="65a77-116">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="65a77-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="65a77-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a77-117">-DefaultProfile</span></span>
<span data-ttu-id="65a77-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="65a77-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65a77-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a77-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="65a77-120">Określa nazwę grupy zasobów, do której to polecenie cmdlet powoduje przeniesienie zasobów.</span><span class="sxs-lookup"><span data-stu-id="65a77-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="65a77-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="65a77-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="65a77-122">Określa identyfikator subskrypcji, do której to polecenie cmdlet powoduje przeniesienie zasobów.</span><span class="sxs-lookup"><span data-stu-id="65a77-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="65a77-123">-Force</span><span class="sxs-lookup"><span data-stu-id="65a77-123">-Force</span></span>
<span data-ttu-id="65a77-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="65a77-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="65a77-125">-Pre</span><span class="sxs-lookup"><span data-stu-id="65a77-125">-Pre</span></span>
<span data-ttu-id="65a77-126">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="65a77-126">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="65a77-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="65a77-127">-ResourceId</span></span>
<span data-ttu-id="65a77-128">Określa tablicę identyfikatorów zasobów przenoszonych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a77-128">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="65a77-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65a77-129">-Confirm</span></span>
<span data-ttu-id="65a77-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a77-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a77-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a77-131">-WhatIf</span></span>
<span data-ttu-id="65a77-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a77-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a77-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65a77-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a77-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a77-134">CommonParameters</span></span>
<span data-ttu-id="65a77-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a77-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a77-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65a77-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a77-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a77-137">INPUTS</span></span>

### <span data-ttu-id="65a77-138">System. Nullable "1 [[System. GUID, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="65a77-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="65a77-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="65a77-139">System.String[]</span></span>

## <span data-ttu-id="65a77-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65a77-140">OUTPUTS</span></span>

### <span data-ttu-id="65a77-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="65a77-141">System.Boolean</span></span>

## <span data-ttu-id="65a77-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65a77-142">NOTES</span></span>

## <span data-ttu-id="65a77-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65a77-143">RELATED LINKS</span></span>

[<span data-ttu-id="65a77-144">Znajdź-AzResource</span><span class="sxs-lookup"><span data-stu-id="65a77-144">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="65a77-145">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="65a77-145">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="65a77-146">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="65a77-146">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="65a77-147">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="65a77-147">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="65a77-148">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="65a77-148">Set-AzResource</span></span>](./Set-AzResource.md)


