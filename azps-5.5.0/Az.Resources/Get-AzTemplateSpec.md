---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192778"
---
# <span data-ttu-id="91c71-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="91c71-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="91c71-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91c71-102">SYNOPSIS</span></span>
<span data-ttu-id="91c71-103">Pobiera lub wyświetla specyfikacje szablonu</span><span class="sxs-lookup"><span data-stu-id="91c71-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="91c71-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="91c71-104">SYNTAX</span></span>

### <span data-ttu-id="91c71-105">ListTemplateSpecsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="91c71-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="91c71-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c71-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="91c71-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="91c71-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="91c71-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="91c71-108">DESCRIPTION</span></span>
<span data-ttu-id="91c71-109">To polecenie cmdlet służy do listy specyfikacji szablonów w grupie subskrypcji/zasobów lub do uzyskania określonej specyfikacji szablonu według nazwy lub identyfikatora. Podczas uzyskiwania określonej specyfikacji szablonu według nazwy/identyfikatora można opcjonalnie pobrać określoną wersję, określając nazwę wersji za pomocą **parametru -Version.**</span><span class="sxs-lookup"><span data-stu-id="91c71-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="91c71-110">W **przypadku korzystania z** wersji -Version w ciągu \* będą obecne tylko szczegóły określonej *wersji. Wersje* zwróconego obiektu Spec szablonu.</span><span class="sxs-lookup"><span data-stu-id="91c71-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="91c71-111">Jeśli podczas pobierania specyfikacji szablonu według nazwy/identyfikatora nie określono konkretnej wersji, wszystkie wersje będą obecne w pliku \**. Właściwość* Versions zwróconego obiektu.</span><span class="sxs-lookup"><span data-stu-id="91c71-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="91c71-112">**Uwaga:** podczas wymieniania wszystkich specyfikacji szablonów w ramach subskrypcji lub grupy zasobów każda zwrócona specyfikacja szablonu jest *". Właściwość Versions"* będzie mieć wartość *null.*</span><span class="sxs-lookup"><span data-stu-id="91c71-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="91c71-113">Informacje o wersji są uwzględniane tylko wtedy, gdy podano parametry -Name lub -ResourceId (np.: żądasz określonej specyfikacji/wersji szablonu).</span><span class="sxs-lookup"><span data-stu-id="91c71-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="91c71-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="91c71-114">EXAMPLES</span></span>

### <span data-ttu-id="91c71-115">Przykład 1. Specyfikacja szablonu listy w bieżącej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="91c71-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="91c71-116">Zawiera listę wszystkich specyfikacji szablonów w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="91c71-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="91c71-117">Przykład 2. Specyfikacja szablonu listy w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="91c71-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="91c71-118">Wyświetla listę wszystkich specyfikacji szablonów w grupie zasobów "myRG" bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="91c71-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="91c71-119">Przykład 3. Uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według nazwy</span><span class="sxs-lookup"><span data-stu-id="91c71-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="91c71-120">Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="91c71-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="91c71-121">**Uwaga:** Wszystkie wersje specyfikacji szablonów będą dostępne w ramach "*. Właściwość Versions*" obiektu zwracanego.</span><span class="sxs-lookup"><span data-stu-id="91c71-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="91c71-122">Przykład 4. Uzyskiwanie specyfikacji szablonu (konkretnej wersji) według nazwy</span><span class="sxs-lookup"><span data-stu-id="91c71-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="91c71-123">Pobiera informacje o wersji "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="91c71-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="91c71-124">**Uwaga:** *". Właściwość Versions"* zwróconego obiektu będzie zawierać tylko określoną żądaną wersję.</span><span class="sxs-lookup"><span data-stu-id="91c71-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="91c71-125">Przykład 5. Uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="91c71-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="91c71-126">Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="91c71-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="91c71-127">**Uwaga:** Wszystkie wersje specyfikacji szablonów będą dostępne w ramach "*. Właściwość Versions*" obiektu zwracanego.</span><span class="sxs-lookup"><span data-stu-id="91c71-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="91c71-128">Przykład 6. Uzyskiwanie specyfikacji szablonu (określonej wersji) według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="91c71-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="91c71-129">Pobiera informacje o wersji "1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" \{ podid \} subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="91c71-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="91c71-130">**Uwaga:** *". Właściwość Versions"* zwróconego obiektu będzie zawierać tylko określoną żądaną wersję.</span><span class="sxs-lookup"><span data-stu-id="91c71-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="91c71-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="91c71-131">PARAMETERS</span></span>

### <span data-ttu-id="91c71-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91c71-132">-DefaultProfile</span></span>
<span data-ttu-id="91c71-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="91c71-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91c71-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="91c71-134">-Name</span></span>
<span data-ttu-id="91c71-135">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="91c71-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="91c71-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91c71-136">-ResourceGroupName</span></span>
<span data-ttu-id="91c71-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91c71-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="91c71-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="91c71-138">-ResourceId</span></span>
<span data-ttu-id="91c71-139">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. Przykład: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="91c71-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="91c71-140">— Wersja</span><span class="sxs-lookup"><span data-stu-id="91c71-140">-Version</span></span>
<span data-ttu-id="91c71-141">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="91c71-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="91c71-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91c71-142">CommonParameters</span></span>
<span data-ttu-id="91c71-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91c71-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91c71-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="91c71-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91c71-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91c71-145">INPUTS</span></span>

### <span data-ttu-id="91c71-146">System.String</span><span class="sxs-lookup"><span data-stu-id="91c71-146">System.String</span></span>

## <span data-ttu-id="91c71-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91c71-147">OUTPUTS</span></span>

### <span data-ttu-id="91c71-148">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="91c71-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="91c71-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="91c71-149">NOTES</span></span>

## <span data-ttu-id="91c71-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91c71-150">RELATED LINKS</span></span>
