---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: cbe72ac0c1b62a11b48113bd9043118f3750f37b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718591"
---
# <span data-ttu-id="e026e-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e026e-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="e026e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e026e-102">SYNOPSIS</span></span>
<span data-ttu-id="e026e-103">Usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="e026e-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e026e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e026e-104">SYNTAX</span></span>

### <span data-ttu-id="e026e-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e026e-105">ByResourceId (Default)</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e026e-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e026e-106">BySubscriptionLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e026e-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e026e-107">ByTenantLevel</span></span>
```
Remove-AzureRmResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e026e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e026e-108">DESCRIPTION</span></span>
<span data-ttu-id="e026e-109">Polecenie cmdlet **Remove-AzureRmResource** usuwa zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e026e-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="e026e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e026e-110">EXAMPLES</span></span>

### <span data-ttu-id="e026e-111">Przykład 1: usuwanie zasobu witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="e026e-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="e026e-112">To polecenie usuwa zasób witryny sieci Web o nazwie ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="e026e-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="e026e-113">W przykładzie użyto wartości zastępczej dla identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e026e-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="e026e-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="e026e-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="e026e-115">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e026e-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="e026e-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e026e-116">PARAMETERS</span></span>

### <span data-ttu-id="e026e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e026e-117">-ApiVersion</span></span>
<span data-ttu-id="e026e-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="e026e-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e026e-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="e026e-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e026e-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e026e-120">-AsJob</span></span>
<span data-ttu-id="e026e-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="e026e-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e026e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e026e-122">-DefaultProfile</span></span>
<span data-ttu-id="e026e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e026e-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e026e-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e026e-124">-ExtensionResourceName</span></span>
<span data-ttu-id="e026e-125">Określa nazwę zasobu rozszerzenia zasobu, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e026e-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e026e-126">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="e026e-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e026e-127">-ExtensionResourceType</span></span>
<span data-ttu-id="e026e-128">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e026e-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e026e-129">Określa typ zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="e026e-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="e026e-130">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e026e-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-131">-Force</span><span class="sxs-lookup"><span data-stu-id="e026e-131">-Force</span></span>
<span data-ttu-id="e026e-132">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="e026e-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e026e-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e026e-133">-ODataQuery</span></span>
<span data-ttu-id="e026e-134">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e026e-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="e026e-135">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="e026e-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e026e-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="e026e-136">-Pre</span></span>
<span data-ttu-id="e026e-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="e026e-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e026e-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e026e-138">-ResourceGroupName</span></span>
<span data-ttu-id="e026e-139">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="e026e-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e026e-140">-ResourceId</span></span>
<span data-ttu-id="e026e-141">Określa w pełni kwalifikowany identyfikator zasobu, którego usunięcie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e026e-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e026e-142">Identyfikator zawiera abonament, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e026e-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e026e-143">-ResourceName</span></span>
<span data-ttu-id="e026e-144">Określa nazwę zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e026e-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e026e-145">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e026e-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e026e-146">-ResourceType</span></span>
<span data-ttu-id="e026e-147">Określa typ zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e026e-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="e026e-148">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e026e-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e026e-149">-TenantLevel</span></span>
<span data-ttu-id="e026e-150">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="e026e-150">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e026e-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e026e-151">-Confirm</span></span>
<span data-ttu-id="e026e-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e026e-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e026e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e026e-153">-WhatIf</span></span>
<span data-ttu-id="e026e-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e026e-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e026e-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e026e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e026e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e026e-156">CommonParameters</span></span>
<span data-ttu-id="e026e-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e026e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e026e-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e026e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e026e-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e026e-159">INPUTS</span></span>

### <span data-ttu-id="e026e-160">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e026e-160">None</span></span>

## <span data-ttu-id="e026e-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e026e-161">OUTPUTS</span></span>

### <span data-ttu-id="e026e-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e026e-162">System.Boolean</span></span>

## <span data-ttu-id="e026e-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e026e-163">NOTES</span></span>

## <span data-ttu-id="e026e-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e026e-164">RELATED LINKS</span></span>

[<span data-ttu-id="e026e-165">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e026e-165">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="e026e-166">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e026e-166">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="e026e-167">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e026e-167">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="e026e-168">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e026e-168">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="e026e-169">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="e026e-169">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


