---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308334"
---
# <span data-ttu-id="d75e9-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="d75e9-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="d75e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d75e9-102">SYNOPSIS</span></span>
<span data-ttu-id="d75e9-103">Eksportuje specyfikację szablonu do lokalnego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="d75e9-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="d75e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d75e9-104">SYNTAX</span></span>

### <span data-ttu-id="d75e9-105">ExportByNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d75e9-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75e9-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75e9-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d75e9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d75e9-107">DESCRIPTION</span></span>
<span data-ttu-id="d75e9-108">Eksportuje określoną wersję specyfikacji szablonu do lokalnego systemu plików.</span><span class="sxs-lookup"><span data-stu-id="d75e9-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="d75e9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d75e9-109">EXAMPLES</span></span>

### <span data-ttu-id="d75e9-110">Przykład 1: eksportowanie według nazwy</span><span class="sxs-lookup"><span data-stu-id="d75e9-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="d75e9-111">Eksportuje wersję "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" do lokalnego folderu wyjściowego "v1".</span><span class="sxs-lookup"><span data-stu-id="d75e9-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="d75e9-112">Przykład 2: eksportowanie według identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="d75e9-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="d75e9-113">Eksportuje wersję "v 1.0" specyfikacji szablonu o nazwie "MyTemplateSpec" w grupie zasobów "myRG" subskrypcji \{ subId \} do lokalnego folderu wyjściowego "v1".</span><span class="sxs-lookup"><span data-stu-id="d75e9-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="d75e9-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d75e9-114">PARAMETERS</span></span>

### <span data-ttu-id="d75e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75e9-115">-DefaultProfile</span></span>
<span data-ttu-id="d75e9-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d75e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d75e9-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d75e9-117">-Name</span></span>
<span data-ttu-id="d75e9-118">Nazwa specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d75e9-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75e9-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="d75e9-119">-OutputFolder</span></span>
<span data-ttu-id="d75e9-120">Ścieżka do folderu, do którego jest wyprowadzana wersja specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d75e9-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="d75e9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d75e9-121">-ResourceGroupName</span></span>
<span data-ttu-id="d75e9-122">Nazwa grupy zasobów specyfikacji szablonu.</span><span class="sxs-lookup"><span data-stu-id="d75e9-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75e9-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d75e9-123">-ResourceId</span></span>
<span data-ttu-id="d75e9-124">W pełni kwalifikowany identyfikator zasobu specyfikacji szablonu. przykład:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="d75e9-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75e9-125">-Version</span><span class="sxs-lookup"><span data-stu-id="d75e9-125">-Version</span></span>
<span data-ttu-id="d75e9-126">Wersja specyfikacji szablonu do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="d75e9-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="d75e9-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d75e9-127">-Confirm</span></span>
<span data-ttu-id="d75e9-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75e9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d75e9-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75e9-129">-WhatIf</span></span>
<span data-ttu-id="d75e9-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75e9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d75e9-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d75e9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d75e9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75e9-132">CommonParameters</span></span>
<span data-ttu-id="d75e9-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75e9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75e9-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d75e9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75e9-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d75e9-135">INPUTS</span></span>

### <span data-ttu-id="d75e9-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d75e9-136">System.String</span></span>

## <span data-ttu-id="d75e9-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d75e9-137">OUTPUTS</span></span>

### <span data-ttu-id="d75e9-138">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d75e9-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d75e9-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d75e9-139">NOTES</span></span>

## <span data-ttu-id="d75e9-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d75e9-140">RELATED LINKS</span></span>
