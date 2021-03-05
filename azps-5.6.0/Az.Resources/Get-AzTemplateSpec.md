---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960113"
---
# <span data-ttu-id="e0185-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e0185-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="e0185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0185-102">SYNOPSIS</span></span>
<span data-ttu-id="e0185-103">Pobiera lub wyświetla specyfikacje szablonu</span><span class="sxs-lookup"><span data-stu-id="e0185-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="e0185-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0185-104">SYNTAX</span></span>

### <span data-ttu-id="e0185-105">ListTemplateSpecsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e0185-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e0185-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0185-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e0185-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e0185-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0185-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0185-108">DESCRIPTION</span></span>
<span data-ttu-id="e0185-109">To polecenie cmdlet służy do listy specyfikacji szablonów w grupie subskrypcji/zasobów lub do uzyskania określonej specyfikacji szablonu według nazwy lub identyfikatora. W przypadku uzyskiwania określonej specyfikacji szablonu według nazwy/identyfikatora można opcjonalnie pobrać określoną wersję, określając nazwę wersji za pomocą **parametru -Version.**</span><span class="sxs-lookup"><span data-stu-id="e0185-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="e0185-110">W **przypadku korzystania z** wersji -Version w ciągu \* będą obecne tylko szczegóły określonej *wersji. Wersje* zwróconego obiektu Spec szablonu.</span><span class="sxs-lookup"><span data-stu-id="e0185-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="e0185-111">Jeśli podczas pobierania specyfikacji szablonu według nazwy/identyfikatora nie określono konkretnej wersji, wszystkie wersje będą obecne w pliku \**. Właściwość* Versions zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="e0185-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="e0185-112">**Uwaga:** gdy podano wszystkie specyfikacje szablonów w ramach subskrypcji lub grupy zasobów, każda zwrócona specyfikacja szablonu jest *". Właściwość Versions"* będzie mieć wartość *null.*</span><span class="sxs-lookup"><span data-stu-id="e0185-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="e0185-113">Informacje o wersji są uwzględniane tylko wtedy, gdy zostaną podane parametry -Name lub -ResourceId (np.: żądasz określonej specyfikacji/wersji szablonu).</span><span class="sxs-lookup"><span data-stu-id="e0185-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="e0185-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0185-114">EXAMPLES</span></span>

### <span data-ttu-id="e0185-115">Przykład 1. Specyfikacja szablonu listy w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e0185-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="e0185-116">Zawiera listę wszystkich specyfikacji szablonów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0185-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="e0185-117">Przykład 2. Specyfikacja szablonu listy w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="e0185-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="e0185-118">Wyświetla listę wszystkich specyfikacji szablonów w grupie zasobów "myRG" bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0185-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="e0185-119">Przykład 3. Uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według nazwy</span><span class="sxs-lookup"><span data-stu-id="e0185-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="e0185-120">Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e0185-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="e0185-121">**Uwaga:** Wszystkie wersje specyfikacji szablonów będą dostępne w "*. Właściwość Versions*" obiektu zwracanego.</span><span class="sxs-lookup"><span data-stu-id="e0185-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="e0185-122">Przykład 4. Uzyskiwanie specyfikacji szablonu (konkretnej wersji) według nazwy</span><span class="sxs-lookup"><span data-stu-id="e0185-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="e0185-123">Pobiera informacje o wersji "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="e0185-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="e0185-124">**Uwaga:** *". Właściwość Versions"* zwróconego obiektu będzie zawierać tylko określoną żądaną wersję.</span><span class="sxs-lookup"><span data-stu-id="e0185-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="e0185-125">Przykład 5. Uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e0185-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="e0185-126">Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0185-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="e0185-127">**Uwaga:** Wszystkie wersje specyfikacji szablonów będą dostępne w "*. Właściwość Versions*" obiektu zwracanego.</span><span class="sxs-lookup"><span data-stu-id="e0185-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="e0185-128">Przykład 6. Uzyskiwanie specyfikacji szablonu (określonej wersji) według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="e0185-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="e0185-129">Pobiera informacje o wersji "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e0185-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="e0185-130">**Uwaga:** *". Właściwość Versions"* zwróconego obiektu będzie zawierać tylko określoną żądaną wersję.</span><span class="sxs-lookup"><span data-stu-id="e0185-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="e0185-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0185-131">PARAMETERS</span></span>

### <span data-ttu-id="e0185-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0185-132">-DefaultProfile</span></span>
<span data-ttu-id="e0185-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e0185-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0185-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="e0185-134">-Name</span></span>
<span data-ttu-id="e0185-135">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="e0185-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0185-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0185-136">-ResourceGroupName</span></span>
<span data-ttu-id="e0185-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0185-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0185-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0185-138">-ResourceId</span></span>
<span data-ttu-id="e0185-139">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="e0185-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0185-140">— Wersja</span><span class="sxs-lookup"><span data-stu-id="e0185-140">-Version</span></span>
<span data-ttu-id="e0185-141">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="e0185-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0185-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0185-142">CommonParameters</span></span>
<span data-ttu-id="e0185-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0185-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0185-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0185-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0185-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0185-145">INPUTS</span></span>

### <span data-ttu-id="e0185-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e0185-146">System.String</span></span>

## <span data-ttu-id="e0185-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0185-147">OUTPUTS</span></span>

### <span data-ttu-id="e0185-148">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e0185-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="e0185-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0185-149">NOTES</span></span>

## <span data-ttu-id="e0185-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0185-150">RELATED LINKS</span></span>
