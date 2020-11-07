---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/invoke-azurermresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Invoke-AzureRmResourceAction.md
ms.openlocfilehash: 7f2aa8299e3e4dcbdc6d326dfedf76092a65f351
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717703"
---
# <span data-ttu-id="3807c-101">Invoke-AzureRmResourceAction</span><span class="sxs-lookup"><span data-stu-id="3807c-101">Invoke-AzureRmResourceAction</span></span>

## <span data-ttu-id="3807c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3807c-102">SYNOPSIS</span></span>
<span data-ttu-id="3807c-103">Umożliwia wywołanie akcji dotyczącej zasobu.</span><span class="sxs-lookup"><span data-stu-id="3807c-103">Invokes an action on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3807c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3807c-104">SYNTAX</span></span>

### <span data-ttu-id="3807c-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3807c-105">ByResourceId (Default)</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String>
 [-ODataQuery <String>] [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3807c-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="3807c-106">BySubscriptionLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3807c-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="3807c-107">ByTenantLevel</span></span>
```
Invoke-AzureRmResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3807c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3807c-108">DESCRIPTION</span></span>
<span data-ttu-id="3807c-109">Polecenie cmdlet **Invoke-AzureRmResourceAction** umożliwia wywołanie akcji dotyczącej określonego zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3807c-109">The **Invoke-AzureRmResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>

<span data-ttu-id="3807c-110">Aby uzyskać listę obsługiwanych akcji, użyj narzędzia Eksplorator zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="3807c-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="3807c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3807c-111">EXAMPLES</span></span>

## <span data-ttu-id="3807c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3807c-112">PARAMETERS</span></span>

### <span data-ttu-id="3807c-113">-Action</span><span class="sxs-lookup"><span data-stu-id="3807c-113">-Action</span></span>
<span data-ttu-id="3807c-114">Określa nazwę akcji, którą należy wywołać.</span><span class="sxs-lookup"><span data-stu-id="3807c-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3807c-115">-ApiVersion</span></span>
<span data-ttu-id="3807c-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="3807c-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3807c-117">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="3807c-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3807c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3807c-118">-DefaultProfile</span></span>
<span data-ttu-id="3807c-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="3807c-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3807c-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="3807c-120">-ExtensionResourceName</span></span>
<span data-ttu-id="3807c-121">Określa nazwę zasobu rozszerzenia dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="3807c-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="3807c-122">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="3807c-122">For instance, to specify a database, use the following format:</span></span> 

<span data-ttu-id="3807c-123">`/`Nazwa bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="3807c-123">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="3807c-124">-ExtensionResourceType</span></span>
<span data-ttu-id="3807c-125">Określa typ zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="3807c-125">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="3807c-126">Na przykład:</span><span class="sxs-lookup"><span data-stu-id="3807c-126">For instance:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3807c-127">-Force</span></span>
<span data-ttu-id="3807c-128">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="3807c-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3807c-129">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3807c-129">-InformationAction</span></span>
<span data-ttu-id="3807c-130">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="3807c-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3807c-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="3807c-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3807c-132">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="3807c-132">Continue</span></span>
- <span data-ttu-id="3807c-133">Ignorować</span><span class="sxs-lookup"><span data-stu-id="3807c-133">Ignore</span></span>
- <span data-ttu-id="3807c-134">Inquire</span><span class="sxs-lookup"><span data-stu-id="3807c-134">Inquire</span></span>
- <span data-ttu-id="3807c-135">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3807c-135">SilentlyContinue</span></span>
- <span data-ttu-id="3807c-136">Przestaw</span><span class="sxs-lookup"><span data-stu-id="3807c-136">Stop</span></span>
- <span data-ttu-id="3807c-137">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="3807c-137">Suspend</span></span>

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

### <span data-ttu-id="3807c-138">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3807c-138">-InformationVariable</span></span>
<span data-ttu-id="3807c-139">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="3807c-139">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3807c-140">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="3807c-140">-ODataQuery</span></span>
<span data-ttu-id="3807c-141">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="3807c-141">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="3807c-142">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="3807c-142">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="3807c-143">— Parametry</span><span class="sxs-lookup"><span data-stu-id="3807c-143">-Parameters</span></span>
<span data-ttu-id="3807c-144">Określa parametry jako tabelę skrótów dla akcji, która wywołuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3807c-144">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-145">-Pre</span><span class="sxs-lookup"><span data-stu-id="3807c-145">-Pre</span></span>
<span data-ttu-id="3807c-146">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="3807c-146">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3807c-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3807c-147">-ResourceGroupName</span></span>
<span data-ttu-id="3807c-148">Określa nazwę grupy zasobów, w której to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="3807c-148">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3807c-149">-ResourceId</span></span>
<span data-ttu-id="3807c-150">Określa w pełni kwalifikowany identyfikator zasobu dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="3807c-150">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="3807c-151">Identyfikator zawiera abonament, tak jak w poniższym przykładzie:</span><span class="sxs-lookup"><span data-stu-id="3807c-151">The ID includes the subscription, as in the following example:</span></span> 

<span data-ttu-id="3807c-152">`/subscriptions/`Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="3807c-152">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-153">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3807c-153">-ResourceName</span></span>
<span data-ttu-id="3807c-154">Określa nazwę zasobu zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="3807c-154">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="3807c-155">Aby na przykład określić bazę danych, użyj następującego formatu:</span><span class="sxs-lookup"><span data-stu-id="3807c-155">For instance, to specify a database, use the following format:</span></span> 

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3807c-156">-ResourceType</span></span>
<span data-ttu-id="3807c-157">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="3807c-157">Specifies the type of the resource.</span></span>
<span data-ttu-id="3807c-158">Na przykład w przypadku bazy danych typ zasobu jest następujący:</span><span class="sxs-lookup"><span data-stu-id="3807c-158">For instance, for a database, the resource type is as follows:</span></span> 

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-159">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="3807c-159">-TenantLevel</span></span>
<span data-ttu-id="3807c-160">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="3807c-160">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3807c-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3807c-161">-Confirm</span></span>
<span data-ttu-id="3807c-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3807c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3807c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3807c-163">-WhatIf</span></span>
<span data-ttu-id="3807c-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3807c-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3807c-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3807c-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3807c-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3807c-166">CommonParameters</span></span>
<span data-ttu-id="3807c-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3807c-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3807c-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3807c-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3807c-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3807c-169">INPUTS</span></span>

### <span data-ttu-id="3807c-170">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="3807c-170">None</span></span>
<span data-ttu-id="3807c-171">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="3807c-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3807c-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3807c-172">OUTPUTS</span></span>

### <span data-ttu-id="3807c-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3807c-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3807c-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3807c-174">NOTES</span></span>

## <span data-ttu-id="3807c-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3807c-175">RELATED LINKS</span></span>
