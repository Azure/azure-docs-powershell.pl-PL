---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 60BED40A-EEA4-4667-93E9-8A9B35037726
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/move-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Move-AzureRmResource.md
ms.openlocfilehash: 4562c217a771f53995a531a3ca72066da672a144
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549575"
---
# <span data-ttu-id="a93ac-101">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a93ac-101">Move-AzureRmResource</span></span>

## <span data-ttu-id="a93ac-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a93ac-102">SYNOPSIS</span></span>
<span data-ttu-id="a93ac-103">Przenoszenie zasobu do innej grupy zasobów lub abonamentu.</span><span class="sxs-lookup"><span data-stu-id="a93ac-103">Moves a resource to a different resource group or subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a93ac-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a93ac-104">SYNTAX</span></span>

```
Move-AzureRmResource -DestinationResourceGroupName <String> [-DestinationSubscriptionId <Guid>]
 -ResourceId <String[]> [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a93ac-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a93ac-105">DESCRIPTION</span></span>
<span data-ttu-id="a93ac-106">Polecenie cmdlet **Move-AzureRmResource** przenosi istniejące zasoby do innej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a93ac-106">The **Move-AzureRmResource** cmdlet moves existing resources to a different resource group.</span></span>
<span data-ttu-id="a93ac-107">Ta grupa zasobów może być w innej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a93ac-107">That resource group can be in a different subscription.</span></span>

## <span data-ttu-id="a93ac-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a93ac-108">EXAMPLES</span></span>

### <span data-ttu-id="a93ac-109">Przykład 1. Przenoszenie zasobu do grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a93ac-109">Example 1: Move a resource to a resource group</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "Microsoft.ClassicCompute/storageAccounts" -ResourceName "ContosoStorageAccount"
PS C:\> Move-AzureRmResource -ResourceId $Resource.ResourceId -DestinationResourceGroupName "ResourceGroup14"
```

<span data-ttu-id="a93ac-110">Pierwsze polecenie uzyskuje zasób o nazwie ContosoStorageAccount przy użyciu polecenia cmdlet Get-AzureRmResource, a następnie przechowuje ten zasób w zmiennej $Resource.</span><span class="sxs-lookup"><span data-stu-id="a93ac-110">The first command gets a resource named ContosoStorageAccount by using the Get-AzureRmResource cmdlet, and then stores that resource in the $Resource variable.</span></span>

<span data-ttu-id="a93ac-111">Drugie polecenie przeniesie zasób do grupy zasobów o nazwie ResourceGroup14.</span><span class="sxs-lookup"><span data-stu-id="a93ac-111">The second command moves that resource into the resource group named ResourceGroup14.</span></span>
<span data-ttu-id="a93ac-112">To polecenie identyfikuje zasób do przeniesienia przy użyciu właściwości **ResourceId** $Resource.</span><span class="sxs-lookup"><span data-stu-id="a93ac-112">The command identifies the resource to move by using the **ResourceId** property of $Resource.</span></span>

## <span data-ttu-id="a93ac-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a93ac-113">PARAMETERS</span></span>

### <span data-ttu-id="a93ac-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a93ac-114">-ApiVersion</span></span>
<span data-ttu-id="a93ac-115">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="a93ac-115">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="a93ac-116">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="a93ac-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a93ac-117">-DefaultProfile</span></span>
<span data-ttu-id="a93ac-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a93ac-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a93ac-119">-DestinationResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a93ac-119">-DestinationResourceGroupName</span></span>
<span data-ttu-id="a93ac-120">Określa nazwę grupy zasobów, do której to polecenie cmdlet powoduje przeniesienie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a93ac-120">Specifies the name of the resource group into which this cmdlet moves resources.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-121">-DestinationSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a93ac-121">-DestinationSubscriptionId</span></span>
<span data-ttu-id="a93ac-122">Określa identyfikator subskrypcji, do której to polecenie cmdlet powoduje przeniesienie zasobów.</span><span class="sxs-lookup"><span data-stu-id="a93ac-122">Specifies the ID of the subscription into which this cmdlet moves resources .</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: Id, SubscriptionId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a93ac-123">-Force</span></span>
<span data-ttu-id="a93ac-124">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a93ac-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a93ac-125">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a93ac-125">-InformationAction</span></span>
<span data-ttu-id="a93ac-126">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="a93ac-126">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a93ac-127">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="a93ac-127">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a93ac-128">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="a93ac-128">Continue</span></span>
- <span data-ttu-id="a93ac-129">Ignorować</span><span class="sxs-lookup"><span data-stu-id="a93ac-129">Ignore</span></span>
- <span data-ttu-id="a93ac-130">Inquire</span><span class="sxs-lookup"><span data-stu-id="a93ac-130">Inquire</span></span>
- <span data-ttu-id="a93ac-131">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a93ac-131">SilentlyContinue</span></span>
- <span data-ttu-id="a93ac-132">Przestaw</span><span class="sxs-lookup"><span data-stu-id="a93ac-132">Stop</span></span>
- <span data-ttu-id="a93ac-133">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="a93ac-133">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-134">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a93ac-134">-InformationVariable</span></span>
<span data-ttu-id="a93ac-135">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="a93ac-135">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="a93ac-136">-Pre</span></span>
<span data-ttu-id="a93ac-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="a93ac-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a93ac-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a93ac-138">-ResourceId</span></span>
<span data-ttu-id="a93ac-139">Określa tablicę identyfikatorów zasobów przenoszonych przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93ac-139">Specifies an array of IDs of the resources that this cmdlet moves.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a93ac-140">-Confirm</span></span>
<span data-ttu-id="a93ac-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93ac-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a93ac-142">-WhatIf</span></span>
<span data-ttu-id="a93ac-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a93ac-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a93ac-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a93ac-144">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a93ac-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a93ac-145">CommonParameters</span></span>
<span data-ttu-id="a93ac-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a93ac-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a93ac-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a93ac-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a93ac-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a93ac-148">INPUTS</span></span>

### <span data-ttu-id="a93ac-149">String []</span><span class="sxs-lookup"><span data-stu-id="a93ac-149">String[]</span></span>
<span data-ttu-id="a93ac-150">Parametr "ResourceId" akceptuje wartość typu "String []" z procesu</span><span class="sxs-lookup"><span data-stu-id="a93ac-150">Parameter 'ResourceId' accepts value of type 'String[]' from the pipeline</span></span>

## <span data-ttu-id="a93ac-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a93ac-151">OUTPUTS</span></span>

### <span data-ttu-id="a93ac-152">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a93ac-152">System.Boolean</span></span>

## <span data-ttu-id="a93ac-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a93ac-153">NOTES</span></span>

## <span data-ttu-id="a93ac-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a93ac-154">RELATED LINKS</span></span>

[<span data-ttu-id="a93ac-155">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a93ac-155">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="a93ac-156">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a93ac-156">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="a93ac-157">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a93ac-157">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="a93ac-158">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a93ac-158">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="a93ac-159">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="a93ac-159">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


