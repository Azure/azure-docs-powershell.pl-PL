---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308826"
---
# <span data-ttu-id="22cf4-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="22cf4-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="22cf4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22cf4-102">SYNOPSIS</span></span>
<span data-ttu-id="22cf4-103">Pobiera lub wyświetla specyfikacje szablonu</span><span class="sxs-lookup"><span data-stu-id="22cf4-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="22cf4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22cf4-104">SYNTAX</span></span>

### <span data-ttu-id="22cf4-105">ListTemplateSpecsParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22cf4-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="22cf4-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cf4-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="22cf4-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22cf4-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22cf4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="22cf4-108">DESCRIPTION</span></span>
<span data-ttu-id="22cf4-109">Za pomocą tego polecenia cmdlet można wyświetlić specyfikacje szablonu w grupie abonament/zasób lub uzyskać określoną specyfikację szablonu według nazwy lub identyfikatora. Podczas pobierania specyfikacji szablonu według nazwy/identyfikatora można opcjonalnie pobrać określoną wersję przez określenie nazwy wersji za pomocą parametru **-Version** .</span><span class="sxs-lookup"><span data-stu-id="22cf4-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="22cf4-110">Gdy używana jest **wersja** , w programie \* będą dostępne tylko szczegółowe informacje o wersji *. Wersje* w zwróconym obiekcie specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="22cf4-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="22cf4-111">Jeśli nie określono żadnej konkretnej wersji podczas pobierania specyfikacji szablonu za pomocą nazwy/identyfikatora, wszystkie wersje będą obecne w przeciągu \* *. Właściwość wersje* zwracanego obiektu.</span><span class="sxs-lookup"><span data-stu-id="22cf4-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="22cf4-112">**Uwaga** : w przypadku wymieniania wszystkich specyfikacji szablonu w ramach abonamentu lub grupy zasobów każda zwracana Specyfikacja szablonu *". Wersje "* właściwość będzie *wartością null*.</span><span class="sxs-lookup"><span data-stu-id="22cf4-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="22cf4-113">Informacje o wersji są dołączane tylko wtedy, gdy są podane parametry Name lub ResourceId (przykład: żądasz konkretnej specyfikacji/wersji szablonu).</span><span class="sxs-lookup"><span data-stu-id="22cf4-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="22cf4-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22cf4-114">EXAMPLES</span></span>

### <span data-ttu-id="22cf4-115">Przykład 1: Specyfikacja szablonu listy w bieżącym abonamentzie</span><span class="sxs-lookup"><span data-stu-id="22cf4-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="22cf4-116">Lista wszystkich specyfikacji szablonu w bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="22cf4-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="22cf4-117">Przykład 2: specyfikacje szablonu listy w grupie zasobów</span><span class="sxs-lookup"><span data-stu-id="22cf4-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="22cf4-118">Zawiera wszystkie specyfikacje szablonu w grupie zasobów "myRG" bieżącej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="22cf4-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="22cf4-119">Przykład 3: uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według nazwy</span><span class="sxs-lookup"><span data-stu-id="22cf4-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="22cf4-120">Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="22cf4-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="22cf4-121">**Uwaga** : wszystkie wersje specyfikacji szablonu będą obecne w ramach " *.* Właściwość (wersje) obiektu zwracanego.</span><span class="sxs-lookup"><span data-stu-id="22cf4-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="22cf4-122">Przykład 4: uzyskiwanie specyfikacji szablonu (określonej wersji) według nazwy</span><span class="sxs-lookup"><span data-stu-id="22cf4-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="22cf4-123">Pobiera informacje o wersji "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG".</span><span class="sxs-lookup"><span data-stu-id="22cf4-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="22cf4-124">**Uwaga** : *". Właściwość wersje "* zwróconego obiektu" będzie zawierać tylko żądaną wersję.</span><span class="sxs-lookup"><span data-stu-id="22cf4-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="22cf4-125">Przykład 5: uzyskiwanie specyfikacji szablonu (ze wszystkimi wersjami) według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="22cf4-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="22cf4-126">Pobiera informacje o specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" subskrypcji \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="22cf4-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="22cf4-127">**Uwaga** : wszystkie wersje specyfikacji szablonu będą obecne w ramach " *.* Właściwość (wersje) obiektu zwracanego.</span><span class="sxs-lookup"><span data-stu-id="22cf4-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="22cf4-128">Przykład 6: uzyskiwanie specyfikacji szablonu (określonej wersji) według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="22cf4-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="22cf4-129">Pobiera informacje o wersji "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" subskrypcji \{ subId \} .</span><span class="sxs-lookup"><span data-stu-id="22cf4-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="22cf4-130">**Uwaga** : *". Właściwość wersje "* zwróconego obiektu" będzie zawierać tylko żądaną wersję.</span><span class="sxs-lookup"><span data-stu-id="22cf4-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="22cf4-131">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22cf4-131">PARAMETERS</span></span>

### <span data-ttu-id="22cf4-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22cf4-132">-DefaultProfile</span></span>
<span data-ttu-id="22cf4-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="22cf4-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22cf4-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="22cf4-134">-Name</span></span>
<span data-ttu-id="22cf4-135">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="22cf4-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="22cf4-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22cf4-136">-ResourceGroupName</span></span>
<span data-ttu-id="22cf4-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="22cf4-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="22cf4-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22cf4-138">-ResourceId</span></span>
<span data-ttu-id="22cf4-139">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="22cf4-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="22cf4-140">-Version</span><span class="sxs-lookup"><span data-stu-id="22cf4-140">-Version</span></span>
<span data-ttu-id="22cf4-141">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="22cf4-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="22cf4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22cf4-142">CommonParameters</span></span>
<span data-ttu-id="22cf4-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22cf4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22cf4-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22cf4-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22cf4-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22cf4-145">INPUTS</span></span>

### <span data-ttu-id="22cf4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="22cf4-146">System.String</span></span>

## <span data-ttu-id="22cf4-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22cf4-147">OUTPUTS</span></span>

### <span data-ttu-id="22cf4-148">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="22cf4-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="22cf4-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22cf4-149">NOTES</span></span>

## <span data-ttu-id="22cf4-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22cf4-150">RELATED LINKS</span></span>
