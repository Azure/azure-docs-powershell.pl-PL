---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-Azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2f813b9da28ce42e9afb738af1fa0c247dffdc71
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892546"
---
# <span data-ttu-id="eeb1d-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="eeb1d-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="eeb1d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eeb1d-102">SYNOPSIS</span></span>
<span data-ttu-id="eeb1d-103">Umożliwia wywołanie akcji dotyczącej zasobu.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="eeb1d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eeb1d-104">SYNTAX</span></span>

### <span data-ttu-id="eeb1d-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eeb1d-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eeb1d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="eeb1d-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eeb1d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="eeb1d-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeb1d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="eeb1d-108">DESCRIPTION</span></span>
<span data-ttu-id="eeb1d-109">Polecenie cmdlet **Invoke-AzResourceAction** umożliwia wywołanie akcji dotyczącej określonego zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="eeb1d-110">Aby uzyskać listę obsługiwanych akcji, użyj narzędzia Eksplorator zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="eeb1d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eeb1d-111">EXAMPLES</span></span>

## <span data-ttu-id="eeb1d-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eeb1d-112">PARAMETERS</span></span>

### <span data-ttu-id="eeb1d-113">-Action</span><span class="sxs-lookup"><span data-stu-id="eeb1d-113">-Action</span></span>
<span data-ttu-id="eeb1d-114">Określa nazwę akcji, którą należy wywołać.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="eeb1d-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="eeb1d-115">-ApiVersion</span></span>
<span data-ttu-id="eeb1d-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="eeb1d-117">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="eeb1d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeb1d-118">-DefaultProfile</span></span>
<span data-ttu-id="eeb1d-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="eeb1d-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeb1d-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="eeb1d-120">-ExtensionResourceName</span></span>
<span data-ttu-id="eeb1d-121">Określa nazwę zasobu rozszerzenia dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="eeb1d-122">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="eeb1d-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="eeb1d-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="eeb1d-123">-ExtensionResourceType</span></span>
<span data-ttu-id="eeb1d-124">Określa typ zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="eeb1d-125">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="eeb1d-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="eeb1d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="eeb1d-126">-Force</span></span>
<span data-ttu-id="eeb1d-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="eeb1d-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="eeb1d-128">-InformationAction</span></span>
<span data-ttu-id="eeb1d-129">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-129">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="eeb1d-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="eeb1d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="eeb1d-131">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="eeb1d-131">Continue</span></span>
- <span data-ttu-id="eeb1d-132">Ignorować</span><span class="sxs-lookup"><span data-stu-id="eeb1d-132">Ignore</span></span>
- <span data-ttu-id="eeb1d-133">Inquire</span><span class="sxs-lookup"><span data-stu-id="eeb1d-133">Inquire</span></span>
- <span data-ttu-id="eeb1d-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="eeb1d-134">SilentlyContinue</span></span>
- <span data-ttu-id="eeb1d-135">Przestaw</span><span class="sxs-lookup"><span data-stu-id="eeb1d-135">Stop</span></span>
- <span data-ttu-id="eeb1d-136">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="eeb1d-136">Suspend</span></span>

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

### <span data-ttu-id="eeb1d-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="eeb1d-137">-InformationVariable</span></span>
<span data-ttu-id="eeb1d-138">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-138">Specifies an information variable.</span></span>

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

### <span data-ttu-id="eeb1d-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="eeb1d-139">-ODataQuery</span></span>
<span data-ttu-id="eeb1d-140">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="eeb1d-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="eeb1d-141">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="eeb1d-142">— Parametry</span><span class="sxs-lookup"><span data-stu-id="eeb1d-142">-Parameters</span></span>
<span data-ttu-id="eeb1d-143">Określa parametry jako tabelę skrótów dla akcji, która wywołuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-143">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="eeb1d-144">-Pre</span><span class="sxs-lookup"><span data-stu-id="eeb1d-144">-Pre</span></span>
<span data-ttu-id="eeb1d-145">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-145">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="eeb1d-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeb1d-146">-ResourceGroupName</span></span>
<span data-ttu-id="eeb1d-147">Określa nazwę grupy zasobów, w której to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-147">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="eeb1d-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeb1d-148">-ResourceId</span></span>
<span data-ttu-id="eeb1d-149">Określa w pełni kwalifikowany identyfikator zasobu dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-149">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="eeb1d-150">Identyfikator zawiera abonament, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="eeb1d-150">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="eeb1d-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="eeb1d-151">-ResourceName</span></span>
<span data-ttu-id="eeb1d-152">Określa nazwę zasobu zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-152">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="eeb1d-153">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="eeb1d-153">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="eeb1d-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="eeb1d-154">-ResourceType</span></span>
<span data-ttu-id="eeb1d-155">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="eeb1d-156">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="eeb1d-156">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="eeb1d-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="eeb1d-157">-TenantLevel</span></span>
<span data-ttu-id="eeb1d-158">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="eeb1d-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eeb1d-159">-Confirm</span></span>
<span data-ttu-id="eeb1d-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeb1d-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeb1d-161">-WhatIf</span></span>
<span data-ttu-id="eeb1d-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeb1d-163">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeb1d-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeb1d-164">CommonParameters</span></span>
<span data-ttu-id="eeb1d-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeb1d-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeb1d-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeb1d-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeb1d-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eeb1d-167">INPUTS</span></span>

## <span data-ttu-id="eeb1d-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eeb1d-168">OUTPUTS</span></span>

## <span data-ttu-id="eeb1d-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eeb1d-169">NOTES</span></span>

## <span data-ttu-id="eeb1d-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eeb1d-170">RELATED LINKS</span></span>
