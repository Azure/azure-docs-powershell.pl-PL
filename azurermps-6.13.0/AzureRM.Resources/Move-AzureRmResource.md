---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: e1a1e96dbee53dddf0731252329525620cc4933d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548579"
---
# <span data-ttu-id="bee74-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bee74-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="bee74-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bee74-102">SYNOPSIS</span></span>
<span data-ttu-id="bee74-103">Przenoszenie zasobu do innej grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="bee74-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bee74-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bee74-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bee74-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bee74-105">DESCRIPTION</span></span>
<span data-ttu-id="bee74-106">Polecenie cmdlet **Move-AzureRmResource** przenosi istniejące zasoby do innej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee74-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="bee74-107">Ta grupa zasobów może być w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="bee74-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="bee74-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bee74-108">EXAMPLES</span></span>

### <span data-ttu-id="bee74-109">Przykład 1. Przenoszenie zasobu do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bee74-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="bee74-110">Pierwsze polecenie uzyskuje zasób o nazwie ContosoStorageAccount przy użyciu polecenia cmdlet Get-AzureRmResource, a następnie przechowuje ten zasób w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="bee74-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>
<span data-ttu-id="bee74-111">Drugie polecenie przeniesie zasób do grupy zasobów o nazwie ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="bee74-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="bee74-112">To polecenie identyfikuje zasób do przeniesienia przy użyciu właściwości **ResourceId** $Resource.</span><span class="sxs-lookup"><span data-stu-id="bee74-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="bee74-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bee74-113">PARAMETERS</span></span>

### <span data-ttu-id="bee74-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bee74-114">-ApiVersion</span></span>
<span data-ttu-id="bee74-115">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="bee74-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bee74-116">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="bee74-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="bee74-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bee74-117">-DefaultProfile</span></span>
<span data-ttu-id="bee74-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="bee74-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bee74-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bee74-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="bee74-120">Określa nazwę grupy zasobów, do której to polecenie cmdlet powoduje przeniesienie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee74-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

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

### <span data-ttu-id="bee74-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bee74-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="bee74-122">Określa identyfikator subskrypcji, do której to polecenie cmdlet powoduje przeniesienie zasobów.</span><span class="sxs-lookup"><span data-stu-id="bee74-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

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

### <span data-ttu-id="bee74-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bee74-123">-Force</span></span>
<span data-ttu-id="bee74-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bee74-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bee74-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="bee74-125">-InformationAction</span></span>
<span data-ttu-id="bee74-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="bee74-126">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="bee74-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="bee74-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="bee74-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="bee74-128">Continue</span></span>
- <span data-ttu-id="bee74-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="bee74-129">Ignore</span></span>
- <span data-ttu-id="bee74-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="bee74-130">Inquire</span></span>
- <span data-ttu-id="bee74-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="bee74-131">SilentlyContinue</span></span>
- <span data-ttu-id="bee74-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="bee74-132">Stop</span></span>
- <span data-ttu-id="bee74-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="bee74-133">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee74-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="bee74-134">-InformationVariable</span></span>
<span data-ttu-id="bee74-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="bee74-135">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bee74-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="bee74-136">-Pre</span></span>
<span data-ttu-id="bee74-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="bee74-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="bee74-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bee74-138">-ResourceId</span></span>
<span data-ttu-id="bee74-139">Określa tablicę identyfikatorów zasobów przenoszonych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee74-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

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

### <span data-ttu-id="bee74-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bee74-140">-Confirm</span></span>
<span data-ttu-id="bee74-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee74-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bee74-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bee74-142">-WhatIf</span></span>
<span data-ttu-id="bee74-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bee74-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bee74-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bee74-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bee74-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bee74-145">CommonParameters</span></span>
<span data-ttu-id="bee74-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bee74-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bee74-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bee74-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bee74-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bee74-148">INPUTS</span></span>

## <span data-ttu-id="bee74-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bee74-149">OUTPUTS</span></span>

## <span data-ttu-id="bee74-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bee74-150">NOTES</span></span>

## <span data-ttu-id="bee74-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bee74-151">RELATED LINKS</span></span>

[<span data-ttu-id="bee74-152">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bee74-152">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="bee74-153">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bee74-153">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="bee74-154">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bee74-154">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="bee74-155">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bee74-155">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="bee74-156">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="bee74-156">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


