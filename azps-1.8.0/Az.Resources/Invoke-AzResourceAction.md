---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708375"
---
# <span data-ttu-id="2bf69-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="2bf69-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="2bf69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2bf69-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf69-103">Umożliwia wywołanie akcji dotyczącej zasobu.</span><span class="sxs-lookup"><span data-stu-id="2bf69-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="2bf69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2bf69-104">SYNTAX</span></span>

### <span data-ttu-id="2bf69-105">ByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2bf69-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2bf69-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="2bf69-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2bf69-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="2bf69-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bf69-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2bf69-108">DESCRIPTION</span></span>
<span data-ttu-id="2bf69-109">Polecenie cmdlet **Invoke-AzResourceAction** umożliwia wywołanie akcji dotyczącej określonego zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf69-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="2bf69-110">Aby uzyskać listę obsługiwanych akcji, użyj narzędzia Eksplorator zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf69-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="2bf69-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2bf69-111">EXAMPLES</span></span>

## <span data-ttu-id="2bf69-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2bf69-112">PARAMETERS</span></span>

### <span data-ttu-id="2bf69-113">-Action</span><span class="sxs-lookup"><span data-stu-id="2bf69-113">-Action</span></span>
<span data-ttu-id="2bf69-114">Określa nazwę akcji, którą należy wywołać.</span><span class="sxs-lookup"><span data-stu-id="2bf69-114">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="2bf69-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2bf69-115">-ApiVersion</span></span>
<span data-ttu-id="2bf69-116">Określa wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="2bf69-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="2bf69-117">Jeśli nie określisz wersji, to polecenie cmdlet będzie korzystać z najnowszej dostępnej wersji.</span><span class="sxs-lookup"><span data-stu-id="2bf69-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="2bf69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf69-118">-DefaultProfile</span></span>
<span data-ttu-id="2bf69-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2bf69-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2bf69-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="2bf69-120">-ExtensionResourceName</span></span>
<span data-ttu-id="2bf69-121">Określa nazwę zasobu rozszerzenia dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="2bf69-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="2bf69-122">Aby na przykład określić bazę danych, użyj następującego formatu: nazwa `/` bazy danych nazwy serwera</span><span class="sxs-lookup"><span data-stu-id="2bf69-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="2bf69-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="2bf69-123">-ExtensionResourceType</span></span>
<span data-ttu-id="2bf69-124">Określa typ zasobu rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="2bf69-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="2bf69-125">Na przykład: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="2bf69-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="2bf69-126">-Force</span><span class="sxs-lookup"><span data-stu-id="2bf69-126">-Force</span></span>
<span data-ttu-id="2bf69-127">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2bf69-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2bf69-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="2bf69-128">-ODataQuery</span></span>
<span data-ttu-id="2bf69-129">Określa filtr stylu protokołu OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="2bf69-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="2bf69-130">To polecenie cmdlet dołącza tę wartość do żądania oprócz innych filtrów.</span><span class="sxs-lookup"><span data-stu-id="2bf69-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="2bf69-131">— Parametry</span><span class="sxs-lookup"><span data-stu-id="2bf69-131">-Parameters</span></span>
<span data-ttu-id="2bf69-132">Określa parametry jako tabelę skrótów dla akcji, która wywołuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf69-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="2bf69-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="2bf69-133">-Pre</span></span>
<span data-ttu-id="2bf69-134">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="2bf69-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="2bf69-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2bf69-135">-ResourceGroupName</span></span>
<span data-ttu-id="2bf69-136">Określa nazwę grupy zasobów, w której to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="2bf69-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="2bf69-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2bf69-137">-ResourceId</span></span>
<span data-ttu-id="2bf69-138">Określa w pełni kwalifikowany identyfikator zasobu dla zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="2bf69-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="2bf69-139">Identyfikator zawiera abonament, tak jak w poniższym przykładzie: `/subscriptions/` Identyfikator subskrypcji`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="2bf69-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="2bf69-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="2bf69-140">-ResourceName</span></span>
<span data-ttu-id="2bf69-141">Określa nazwę zasobu zasobu, dla którego to polecenie cmdlet wywoła akcję.</span><span class="sxs-lookup"><span data-stu-id="2bf69-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="2bf69-142">Aby na przykład określić bazę danych, użyj następującego formatu: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="2bf69-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="2bf69-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="2bf69-143">-ResourceType</span></span>
<span data-ttu-id="2bf69-144">Określa typ zasobu.</span><span class="sxs-lookup"><span data-stu-id="2bf69-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="2bf69-145">Na przykład w przypadku bazy danych typ zasobu jest następujący: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="2bf69-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="2bf69-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="2bf69-146">-TenantLevel</span></span>
<span data-ttu-id="2bf69-147">Wskazuje, że ten aplet polecenia działa na poziomie dzierżawy.</span><span class="sxs-lookup"><span data-stu-id="2bf69-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="2bf69-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2bf69-148">-Confirm</span></span>
<span data-ttu-id="2bf69-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf69-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bf69-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bf69-150">-WhatIf</span></span>
<span data-ttu-id="2bf69-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bf69-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2bf69-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2bf69-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bf69-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf69-153">CommonParameters</span></span>
<span data-ttu-id="2bf69-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf69-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf69-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bf69-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf69-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bf69-156">INPUTS</span></span>

### <span data-ttu-id="2bf69-157">System. String</span><span class="sxs-lookup"><span data-stu-id="2bf69-157">System.String</span></span>

## <span data-ttu-id="2bf69-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2bf69-158">OUTPUTS</span></span>

### <span data-ttu-id="2bf69-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="2bf69-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="2bf69-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2bf69-160">NOTES</span></span>

## <span data-ttu-id="2bf69-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bf69-161">RELATED LINKS</span></span>
