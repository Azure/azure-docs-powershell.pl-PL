---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 1861b048a1782f8962708ae5ed2bbd16ebc178b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716667"
---
# <span data-ttu-id="c2954-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="c2954-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="c2954-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2954-102">SYNOPSIS</span></span>
<span data-ttu-id="c2954-103">Umożliwia wywołanie akcji dotyczącej zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2954-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2954-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2954-104">SYNTAX</span></span>

### <span data-ttu-id="c2954-105">Identyfikator zasobu (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c2954-105">The resource Id. (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2954-106">Zasób znajdujący się na poziomie abonamentu.</span><span class="sxs-lookup"><span data-stu-id="c2954-106">Resource that resides at the subscription level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2954-107">Zasób znajdujący się na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c2954-107">Resource that resides at the tenant level.</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2954-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c2954-108">DESCRIPTION</span></span>
<span data-ttu-id="c2954-109">Polecenie cmdlet **Invoke-AzureRmResourceAction** umożliwia wywołanie akcji dotyczącej określonego zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2954-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="c2954-110">Aby uzyskać listę obsługiwanych akcji, użyj narzędzia Eksplorator zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c2954-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="c2954-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2954-111">EXAMPLES</span></span>

## <span data-ttu-id="c2954-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2954-112">PARAMETERS</span></span>

### <span data-ttu-id="c2954-113">-Action</span><span class="sxs-lookup"><span data-stu-id="c2954-113">-Action</span></span>
<span data-ttu-id="c2954-114">Określa nazwę akcji, którą należy wywołać.</span><span class="sxs-lookup"><span data-stu-id="c2954-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2954-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c2954-115">-ApiVersion</span></span>
<span data-ttu-id="c2954-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="c2954-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="c2954-117">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="c2954-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="c2954-118">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="c2954-118">-ExtensionResourceName</span></span>
<span data-ttu-id="c2954-119">Określa nazwę zasobu rozszerzenia dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="c2954-119">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c2954-120">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="c2954-120">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="c2954-121">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="c2954-121">server name`/`database name</span></span>

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

### <span data-ttu-id="c2954-122">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="c2954-122">-ExtensionResourceType</span></span>
<span data-ttu-id="c2954-123">Określa typ zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="c2954-123">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="c2954-124">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="c2954-124">For instance:</span></span> 

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

### <span data-ttu-id="c2954-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c2954-125">-Force</span></span>
<span data-ttu-id="c2954-126">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c2954-126">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c2954-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c2954-127">-InformationAction</span></span>
<span data-ttu-id="c2954-128">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c2954-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c2954-129">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c2954-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c2954-130">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c2954-130">Continue</span></span>
- <span data-ttu-id="c2954-131">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c2954-131">Ignore</span></span>
- <span data-ttu-id="c2954-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="c2954-132">Inquire</span></span>
- <span data-ttu-id="c2954-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c2954-133">SilentlyContinue</span></span>
- <span data-ttu-id="c2954-134">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c2954-134">Stop</span></span>
- <span data-ttu-id="c2954-135">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c2954-135">Suspend</span></span>

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

### <span data-ttu-id="c2954-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c2954-136">-InformationVariable</span></span>
<span data-ttu-id="c2954-137">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c2954-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c2954-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="c2954-138">-ODataQuery</span></span>
<span data-ttu-id="c2954-139">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="c2954-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="c2954-140">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="c2954-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="c2954-141">— Parametry</span><span class="sxs-lookup"><span data-stu-id="c2954-141">-Parameters</span></span>
<span data-ttu-id="c2954-142">Określa parametry jako tabelę skrótów dla akcji, która wywołuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2954-142">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2954-143">-Pre</span><span class="sxs-lookup"><span data-stu-id="c2954-143">-Pre</span></span>
<span data-ttu-id="c2954-144">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="c2954-144">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="c2954-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2954-145">-ResourceGroupName</span></span>
<span data-ttu-id="c2954-146">Określa nazwę grupy zasobów, w której to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="c2954-146">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="c2954-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2954-147">-ResourceId</span></span>
<span data-ttu-id="c2954-148">Określa w pełni kwalifikowany identyfikator zasobu dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="c2954-148">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c2954-149">Identyfikator zawiera abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="c2954-149">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="c2954-150">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="c2954-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="c2954-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c2954-151">-ResourceName</span></span>
<span data-ttu-id="c2954-152">Określa nazwę zasobu zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="c2954-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="c2954-153">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="c2954-153">For instance, to specify a database, use the following format:</span></span> 

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

### <span data-ttu-id="c2954-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="c2954-154">-ResourceType</span></span>
<span data-ttu-id="c2954-155">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="c2954-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="c2954-156">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="c2954-156">For instance, for a database, the resource type is as follows:</span></span> 

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

### <span data-ttu-id="c2954-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="c2954-157">-TenantLevel</span></span>
<span data-ttu-id="c2954-158">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="c2954-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="c2954-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c2954-159">-Confirm</span></span>
<span data-ttu-id="c2954-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2954-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2954-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2954-161">-WhatIf</span></span>
<span data-ttu-id="c2954-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2954-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2954-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c2954-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2954-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2954-164">-DefaultProfile</span></span>
<span data-ttu-id="c2954-165">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c2954-165">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2954-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2954-166">CommonParameters</span></span>
<span data-ttu-id="c2954-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2954-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2954-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2954-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2954-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2954-169">INPUTS</span></span>

## <span data-ttu-id="c2954-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2954-170">OUTPUTS</span></span>

### <span data-ttu-id="c2954-171">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="c2954-171">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="c2954-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2954-172">NOTES</span></span>

## <span data-ttu-id="c2954-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2954-173">RELATED LINKS</span></span>

