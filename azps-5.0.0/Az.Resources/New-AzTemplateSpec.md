---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94231511"
---
# <span data-ttu-id="6e4e0-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="6e4e0-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="6e4e0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6e4e0-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4e0-103">Tworzy nową specyfikację szablonu.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="6e4e0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6e4e0-104">SYNTAX</span></span>

### <span data-ttu-id="6e4e0-105">FromJsonStringParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6e4e0-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e4e0-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e4e0-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e4e0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="6e4e0-107">DESCRIPTION</span></span>
<span data-ttu-id="6e4e0-108">Tworzy nową wersję specyfikacji szablonu z określoną zawartością szablonu ARM.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="6e4e0-109">Zawartość może pochodzić z nieprzetworzonego ciągu JSON (za pomocą zestawu parametrów **FromJsonStringParameterSet** ) lub z określonego pliku JSON (za pomocą zestawu parametrów **FromJsonFileParameterSet** ).</span><span class="sxs-lookup"><span data-stu-id="6e4e0-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="6e4e0-110">Jeśli Specyfikacja szablonu głównego jeszcze nie istnieje, zostanie utworzona wraz z wersją specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="6e4e0-111">Jeśli istnieje już Specyfikacja szablonu o podanej nazwie, a określona wersja zostanie zaktualizowana (wszelkie inne istniejące wersje zostaną zachowane).</span><span class="sxs-lookup"><span data-stu-id="6e4e0-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="6e4e0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6e4e0-112">EXAMPLES</span></span>

### <span data-ttu-id="6e4e0-113">Przykład 1:</span><span class="sxs-lookup"><span data-stu-id="6e4e0-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="6e4e0-114">Tworzy nową wersję specyfikacji szablonu "v 1.0" w specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="6e4e0-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="6e4e0-115">Określona wersja będzie $templateJson jako zawartość szablonu ARM tej wersji.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="6e4e0-116">**Uwaga:** Szablon ARM w przykładzie to no-op, ponieważ nie zawiera rzeczywistych zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="6e4e0-117">Przykład 2:</span><span class="sxs-lookup"><span data-stu-id="6e4e0-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="6e4e0-118">Tworzy nową wersję specyfikacji szablonu "v 2.0" w specyfikacji szablonu o nazwie "myTemplateSpec".</span><span class="sxs-lookup"><span data-stu-id="6e4e0-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="6e4e0-119">Określona wersja będzie zawierać zawartość z pliku lokalnego "myTemplateContent.jswłączony" jako zawartość szablonu ARM tej wersji.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="6e4e0-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6e4e0-120">PARAMETERS</span></span>

### <span data-ttu-id="6e4e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4e0-121">-DefaultProfile</span></span>
<span data-ttu-id="6e4e0-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e4e0-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="6e4e0-123">-Description</span></span>
<span data-ttu-id="6e4e0-124">Opis specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-124">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="6e4e0-125">-DisplayName</span></span>
<span data-ttu-id="6e4e0-126">Nazwa wyświetlana specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-126">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6e4e0-127">-Force</span></span>
<span data-ttu-id="6e4e0-128">Nie pytaj o potwierdzenie podczas zastępowania istniejącej wersji.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="6e4e0-129">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6e4e0-129">-Location</span></span>
<span data-ttu-id="6e4e0-130">Lokalizacja specyfikacji szablonu. Wymagane tylko w przypadku, gdy Specyfikacja szablonu jeszcze nie istnieje.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6e4e0-131">-Name</span></span>
<span data-ttu-id="6e4e0-132">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4e0-133">-ResourceGroupName</span></span>
<span data-ttu-id="6e4e0-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-135">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="6e4e0-135">-TemplateFile</span></span>
<span data-ttu-id="6e4e0-136">Ścieżka do pliku JSON szablonu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-137">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="6e4e0-137">-TemplateJson</span></span>
<span data-ttu-id="6e4e0-138">KOD JSON szablonu Menedżera zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-138">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-139">-Version</span><span class="sxs-lookup"><span data-stu-id="6e4e0-139">-Version</span></span>
<span data-ttu-id="6e4e0-140">Wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-140">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="6e4e0-141">-VersionDescription</span></span>
<span data-ttu-id="6e4e0-142">Opis wersji.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-142">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6e4e0-143">-Confirm</span></span>
<span data-ttu-id="6e4e0-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e4e0-145">-WhatIf</span></span>
<span data-ttu-id="6e4e0-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e4e0-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e4e0-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4e0-148">CommonParameters</span></span>
<span data-ttu-id="6e4e0-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e4e0-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4e0-150">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e4e0-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4e0-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6e4e0-151">INPUTS</span></span>

### <span data-ttu-id="6e4e0-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6e4e0-152">System.String</span></span>

## <span data-ttu-id="6e4e0-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6e4e0-153">OUTPUTS</span></span>

### <span data-ttu-id="6e4e0-154">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="6e4e0-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="6e4e0-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6e4e0-155">NOTES</span></span>

## <span data-ttu-id="6e4e0-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6e4e0-156">RELATED LINKS</span></span>
