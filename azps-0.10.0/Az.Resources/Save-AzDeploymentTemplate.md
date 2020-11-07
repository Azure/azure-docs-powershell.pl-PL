---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-Azdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Save-AzDeploymentTemplate.md
ms.openlocfilehash: 82fd6ba15a240be208445493810551154e188e92
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892362"
---
# <span data-ttu-id="4e4cf-101">Save-AzDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="4e4cf-101">Save-AzDeploymentTemplate</span></span>

## <span data-ttu-id="4e4cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4e4cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4e4cf-103">Zapisuje szablon wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-103">Saves a deployment template to a file.</span></span>

## <span data-ttu-id="4e4cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4e4cf-104">SYNTAX</span></span>

### <span data-ttu-id="4e4cf-105">SaveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4e4cf-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e4cf-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4e4cf-106">SaveByDeploymentObject</span></span>
```
Save-AzDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4e4cf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4e4cf-107">DESCRIPTION</span></span>
<span data-ttu-id="4e4cf-108">Polecenie cmdlet **Save-AzDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-108">The **Save-AzDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="4e4cf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4e4cf-109">EXAMPLES</span></span>

### <span data-ttu-id="4e4cf-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4e4cf-110">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="4e4cf-111">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="4e4cf-112">Przykład 2: uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="4e4cf-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Save-AzDeploymentTemplate
```

<span data-ttu-id="4e4cf-113">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie subskrypcji i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="4e4cf-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4e4cf-114">PARAMETERS</span></span>

### <span data-ttu-id="4e4cf-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4e4cf-115">-ApiVersion</span></span>
<span data-ttu-id="4e4cf-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4e4cf-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4e4cf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e4cf-118">-DefaultProfile</span></span>
<span data-ttu-id="4e4cf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4cf-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="4e4cf-120">-DeploymentName</span></span>
<span data-ttu-id="4e4cf-121">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: SaveByDeploymentName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4cf-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4e4cf-122">-DeploymentObject</span></span>
<span data-ttu-id="4e4cf-123">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: SaveByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e4cf-124">-Force</span><span class="sxs-lookup"><span data-stu-id="4e4cf-124">-Force</span></span>
<span data-ttu-id="4e4cf-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4e4cf-126">-Path</span><span class="sxs-lookup"><span data-stu-id="4e4cf-126">-Path</span></span>
<span data-ttu-id="4e4cf-127">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="4e4cf-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="4e4cf-128">-Pre</span></span>
<span data-ttu-id="4e4cf-129">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4e4cf-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4e4cf-130">-Confirm</span></span>
<span data-ttu-id="4e4cf-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4cf-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e4cf-132">-WhatIf</span></span>
<span data-ttu-id="4e4cf-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e4cf-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e4cf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e4cf-135">CommonParameters</span></span>
<span data-ttu-id="4e4cf-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e4cf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e4cf-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e4cf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e4cf-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4e4cf-138">INPUTS</span></span>

### <span data-ttu-id="4e4cf-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4e4cf-139">System.String</span></span>

## <span data-ttu-id="4e4cf-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4e4cf-140">OUTPUTS</span></span>

### <span data-ttu-id="4e4cf-141">Microsoft. Azure. Commands. ResourceManager. aplety. SdkModels</span><span class="sxs-lookup"><span data-stu-id="4e4cf-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="4e4cf-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4e4cf-142">NOTES</span></span>

## <span data-ttu-id="4e4cf-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4e4cf-143">RELATED LINKS</span></span>
