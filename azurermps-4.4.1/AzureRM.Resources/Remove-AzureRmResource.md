---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A262DFD1-8B90-462C-A4E2-ABA0F51173FA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmResource.md
ms.openlocfilehash: 92d6fc81536568b2654fb72a1d6462830c05923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549871"
---
# <span data-ttu-id="010a3-101">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="010a3-101">Remove-AzureRmResource</span></span>

## <span data-ttu-id="010a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="010a3-102">SYNOPSIS</span></span>
<span data-ttu-id="010a3-103">Usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="010a3-103">Removes a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="010a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="010a3-104">SYNTAX</span></span>

### <span data-ttu-id="010a3-105">Identyfikator zasobu (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="010a3-105">The resource Id. (Default)</span></span>
```
Remove-AzureRmResource -ResourceId <String> [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="010a3-106">Zasób znajdujący się na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="010a3-106">Resource that resides at the subscription level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="010a3-107">Zasób znajdujący się na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="010a3-107">Resource that resides at the tenant level.</span></span>
```
Remove-AzureRmResource -ResourceName <String> -ResourceType <String> [-ExtensionResourceName <String>]
 [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="010a3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="010a3-108">DESCRIPTION</span></span>
<span data-ttu-id="010a3-109">Polecenie cmdlet **Remove-AzureRmResource** usuwa zasób platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="010a3-109">The **Remove-AzureRmResource** cmdlet removes an Azure resource.</span></span>

## <span data-ttu-id="010a3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="010a3-110">EXAMPLES</span></span>

### <span data-ttu-id="010a3-111">Przykład 1: usuwanie zasobu witryny sieci Web</span><span class="sxs-lookup"><span data-stu-id="010a3-111">Example 1: Remove a website resource</span></span>
```
PS C:\>Remove-AzureRmResource -ResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup11/providers/Microsoft.Web/sites/ContosoSite" -Force
```

<span data-ttu-id="010a3-112">To polecenie usuwa zasób witryny sieci Web o nazwie ContosoSite.</span><span class="sxs-lookup"><span data-stu-id="010a3-112">This command removes the website resource named ContosoSite.</span></span>
<span data-ttu-id="010a3-113">W przykładzie użyto wartości zastępczej dla identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="010a3-113">The example uses a placeholder value for the subscription ID.</span></span>
<span data-ttu-id="010a3-114">Polecenie określa parametr *Force* .</span><span class="sxs-lookup"><span data-stu-id="010a3-114">The command specifies the *Force* parameter.</span></span>
<span data-ttu-id="010a3-115">W związku z tym nie jest wyświetlany monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="010a3-115">Therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="010a3-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="010a3-116">PARAMETERS</span></span>

### <span data-ttu-id="010a3-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="010a3-117">-ApiVersion</span></span>
<span data-ttu-id="010a3-118">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="010a3-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="010a3-119">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="010a3-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="010a3-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="010a3-120">-ExtensionResourceName</span></span>
<span data-ttu-id="010a3-121">Określa nazwę zasobu rozszerzenia zasobu, który jest usuwany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a3-121">Specifies the name of an extension resource of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="010a3-122">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="010a3-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="010a3-123">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="010a3-123">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="010a3-124">-ExtensionResourceType</span></span>
<span data-ttu-id="010a3-125">Określa typ zasobu dla zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="010a3-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="010a3-126">Określa typ zasobu rozszerzenia dla zasobu.</span><span class="sxs-lookup"><span data-stu-id="010a3-126">Specifies the extension resource type for the resource.</span></span>
<span data-ttu-id="010a3-127">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="010a3-127">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-128">-Force</span><span class="sxs-lookup"><span data-stu-id="010a3-128">-Force</span></span>
<span data-ttu-id="010a3-129">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="010a3-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="010a3-130">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="010a3-130">-ODataQuery</span></span>
<span data-ttu-id="010a3-131">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="010a3-131">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="010a3-132">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="010a3-132">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="010a3-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="010a3-133">-Pre</span></span>
<span data-ttu-id="010a3-134">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="010a3-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="010a3-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="010a3-135">-ResourceGroupName</span></span>
<span data-ttu-id="010a3-136">Określa nazwę grupy zasobów, z której to polecenie cmdlet usuwa zasób.</span><span class="sxs-lookup"><span data-stu-id="010a3-136">Specifies the name of the resource group from which this cmdlet removes a resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="010a3-137">-ResourceId</span></span>
<span data-ttu-id="010a3-138">Określa w pełni kwalifikowany identyfikator zasobu, którego usunięcie to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a3-138">Specifies the fully qualified resource ID of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="010a3-139">Identyfikator zawiera abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="010a3-139">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="010a3-140">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="010a3-140">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-141">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="010a3-141">-ResourceName</span></span>
<span data-ttu-id="010a3-142">Określa nazwę zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a3-142">Specifies the name of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="010a3-143">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="010a3-143">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-144">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="010a3-144">-ResourceType</span></span>
<span data-ttu-id="010a3-145">Określa typ zasobu usuniętego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a3-145">Specifies the type of the resource that this cmdlet removes.</span></span>
<span data-ttu-id="010a3-146">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="010a3-146">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-147">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="010a3-147">-TenantLevel</span></span>
<span data-ttu-id="010a3-148">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="010a3-148">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010a3-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="010a3-149">-Confirm</span></span>
<span data-ttu-id="010a3-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="010a3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="010a3-151">-WhatIf</span></span>
<span data-ttu-id="010a3-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="010a3-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="010a3-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="010a3-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="010a3-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010a3-154">-DefaultProfile</span></span>
<span data-ttu-id="010a3-155">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="010a3-155">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="010a3-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010a3-156">CommonParameters</span></span>
<span data-ttu-id="010a3-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="010a3-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010a3-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010a3-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010a3-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="010a3-159">INPUTS</span></span>

## <span data-ttu-id="010a3-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="010a3-160">OUTPUTS</span></span>

### <span data-ttu-id="010a3-161">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="010a3-161">System.Boolean</span></span>

## <span data-ttu-id="010a3-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="010a3-162">NOTES</span></span>

## <span data-ttu-id="010a3-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="010a3-163">RELATED LINKS</span></span>

[<span data-ttu-id="010a3-164">Znajdź-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="010a3-164">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="010a3-165">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="010a3-165">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="010a3-166">Przenieś — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="010a3-166">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="010a3-167">Nowe — AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="010a3-167">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="010a3-168">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="010a3-168">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)


