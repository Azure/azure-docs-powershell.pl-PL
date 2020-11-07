---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResource.md
ms.openlocfilehash: ef81674d75ee2f5f79988875e70764df91d23d2c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "93719701"
---
# <span data-ttu-id="c837d-101">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="c837d-101">Remove-AzResource</span></span>

## <span data-ttu-id="c837d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c837d-102">SYNOPSIS</span></span>
<span data-ttu-id="c837d-103">Usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="c837d-103">Removes a resource.</span></span>

## <span data-ttu-id="c837d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c837d-104">SYNTAX</span></span>

### <span data-ttu-id="c837d-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c837d-105">ByResourceId (Default)</span></span>
```
Remove-AzResource [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c837d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="c837d-106">BySubscriptionLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c837d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="c837d-107">ByTenantLevel</span></span>
```
Remove-AzResource [-AsJob] -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c837d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c837d-108">DESCRIPTION</span></span>
<span data-ttu-id="c837d-109">Polecenie cmdlet **Remove-AzResource** usuwa zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c837d-109">The **Remove-AzResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="c837d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c837d-110">EXAMPLES</span></span>

### <span data-ttu-id="c837d-111">Przykład 1: usuwanie zasobu witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="c837d-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="c837d-112">To polecenie usuwa zasób witryny sieci Web o nazwie ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="c837d-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="c837d-113">W przykładzie użyto wartości zastępczej dla identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c837d-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="c837d-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="c837d-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c837d-115">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c837d-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="c837d-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c837d-116">PARAMETERS</span></span>

### <span data-ttu-id="c837d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c837d-117">-ApiVersion</span></span>
<span data-ttu-id="c837d-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c837d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c837d-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="c837d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c837d-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c837d-120">-AsJob</span></span>
<span data-ttu-id="c837d-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="c837d-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c837d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c837d-122">-DefaultProfile</span></span>
<span data-ttu-id="c837d-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c837d-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c837d-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c837d-124">-ExtensionResourceName</span></span>
<span data-ttu-id="c837d-125">Określa nazwę zasobu rozszerzenia zasobu, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c837d-125">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c837d-126">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="c837d-126">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="c837d-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c837d-127">-ExtensionResourceType</span></span>
<span data-ttu-id="c837d-128">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c837d-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="c837d-129">Określa typ zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="c837d-129">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="c837d-130">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c837d-130">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c837d-131">-Force</span><span class="sxs-lookup"><span data-stu-id="c837d-131">-Force</span></span>
<span data-ttu-id="c837d-132">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c837d-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c837d-133">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c837d-133">-ODataQuery</span></span>
<span data-ttu-id="c837d-134">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="c837d-134">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c837d-135">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="c837d-135">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c837d-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="c837d-136">-Pre</span></span>
<span data-ttu-id="c837d-137">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c837d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c837d-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c837d-138">-ResourceGroupName</span></span>
<span data-ttu-id="c837d-139">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="c837d-139">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

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

### <span data-ttu-id="c837d-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c837d-140">-ResourceId</span></span>
<span data-ttu-id="c837d-141">Określa w pełni kwalifikowany identyfikator zasobu, którego usunięcie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c837d-141">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c837d-142">Identyfikator zawiera abonament, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c837d-142">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c837d-143">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c837d-143">-ResourceName</span></span>
<span data-ttu-id="c837d-144">Określa nazwę zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c837d-144">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c837d-145">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c837d-145">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c837d-146">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c837d-146">-ResourceType</span></span>
<span data-ttu-id="c837d-147">Określa typ zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c837d-147">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="c837d-148">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="c837d-148">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="c837d-149">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c837d-149">-TenantLevel</span></span>
<span data-ttu-id="c837d-150">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c837d-150">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c837d-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c837d-151">-Confirm</span></span>
<span data-ttu-id="c837d-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c837d-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c837d-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c837d-153">-WhatIf</span></span>
<span data-ttu-id="c837d-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c837d-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c837d-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c837d-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c837d-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c837d-156">CommonParameters</span></span>
<span data-ttu-id="c837d-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c837d-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c837d-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c837d-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c837d-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c837d-159">INPUTS</span></span>

### <span data-ttu-id="c837d-160">System. String</span><span class="sxs-lookup"><span data-stu-id="c837d-160">System.String</span></span>

## <span data-ttu-id="c837d-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c837d-161">OUTPUTS</span></span>

### <span data-ttu-id="c837d-162">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c837d-162">System.Boolean</span></span>

## <span data-ttu-id="c837d-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c837d-163">NOTES</span></span>

## <span data-ttu-id="c837d-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c837d-164">RELATED LINKS</span></span>

[<span data-ttu-id="c837d-165">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="c837d-165">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="c837d-166">Przenieś — AzResource</span><span class="sxs-lookup"><span data-stu-id="c837d-166">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="c837d-167">Nowe — AzResource</span><span class="sxs-lookup"><span data-stu-id="c837d-167">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="c837d-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="c837d-168">Set-AzResource</span></span>](./Set-AzResource.md)

