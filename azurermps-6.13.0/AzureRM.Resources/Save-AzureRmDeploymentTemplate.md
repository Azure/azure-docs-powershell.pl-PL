---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/save-azurermdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Save-AzureRmDeploymentTemplate.md
ms.openlocfilehash: ed9309599b83079858d02fddeffe7dad4b3bb2dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552560"
---
# <span data-ttu-id="fe890-101">Save-AzureRmDeploymentTemplate</span><span class="sxs-lookup"><span data-stu-id="fe890-101">Save-AzureRmDeploymentTemplate</span></span>

## <span data-ttu-id="fe890-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe890-102">SYNOPSIS</span></span>
<span data-ttu-id="fe890-103">Zapisuje szablon wdrożenia w pliku.</span><span class="sxs-lookup"><span data-stu-id="fe890-103">Saves a deployment template to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe890-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe890-104">SYNTAX</span></span>

### <span data-ttu-id="fe890-105">SaveByDeploymentName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fe890-105">SaveByDeploymentName (Default)</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentName <String> [-Path <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe890-106">SaveByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="fe890-106">SaveByDeploymentObject</span></span>
```
Save-AzureRmDeploymentTemplate -DeploymentObject <PSDeployment> [-Path <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe890-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fe890-107">DESCRIPTION</span></span>
<span data-ttu-id="fe890-108">Polecenie cmdlet **Save-AzureRmDeploymentTemplate**  zapisuje szablon wdrożenia w pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="fe890-108">The **Save-AzureRmDeploymentTemplate**  cmdlet saves a deployment template to a JSON file.</span></span>

## <span data-ttu-id="fe890-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe890-109">EXAMPLES</span></span>

### <span data-ttu-id="fe890-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fe890-110">Example 1</span></span>
```powershell
PS C:\> Save-AzureRmDeploymentTemplate -DeploymentName "TestDeployment"
```

<span data-ttu-id="fe890-111">To polecenie pobiera szablon wdrożenia z TestDeployment i zapisuje go jako plik JSON w bieżącym katalogu.</span><span class="sxs-lookup"><span data-stu-id="fe890-111">This command gets the deployment template from TestDeployment and saves it as a JSON file in the current directory.</span></span>

### <span data-ttu-id="fe890-112">Przykład 2: uzyskiwanie wdrożenia i zapisywanie jego szablonu</span><span class="sxs-lookup"><span data-stu-id="fe890-112">Example 2: Get a deployment and save its template</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "RolesDeployment" | Save-AzureRmDeploymentTemplate
```

<span data-ttu-id="fe890-113">To polecenie pobiera wdrożenie "RolesDeployment" w bieżącym zakresie subskrypcji i zapisuje jego szablon.</span><span class="sxs-lookup"><span data-stu-id="fe890-113">This command gets the deployment "RolesDeployment" at the current subscription scope and saves its template.</span></span>

## <span data-ttu-id="fe890-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe890-114">PARAMETERS</span></span>

### <span data-ttu-id="fe890-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="fe890-115">-ApiVersion</span></span>
<span data-ttu-id="fe890-116">Po ustawieniu wskazuje wersję interfejsu API dostawcy zasobów, który ma być używany.</span><span class="sxs-lookup"><span data-stu-id="fe890-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="fe890-117">Jeśli nie określono tej funkcji, wersja interfejsu API zostanie automatycznie określona jako najnowsza dostępna.</span><span class="sxs-lookup"><span data-stu-id="fe890-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="fe890-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe890-118">-DefaultProfile</span></span>
<span data-ttu-id="fe890-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fe890-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe890-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="fe890-120">-DeploymentName</span></span>
<span data-ttu-id="fe890-121">Nazwa wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fe890-121">The deployment name.</span></span>

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

### <span data-ttu-id="fe890-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="fe890-122">-DeploymentObject</span></span>
<span data-ttu-id="fe890-123">Obiekt wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="fe890-123">The deployment object.</span></span>

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

### <span data-ttu-id="fe890-124">-Force</span><span class="sxs-lookup"><span data-stu-id="fe890-124">-Force</span></span>
<span data-ttu-id="fe890-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fe890-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fe890-126">-Path</span><span class="sxs-lookup"><span data-stu-id="fe890-126">-Path</span></span>
<span data-ttu-id="fe890-127">Ścieżka wyjściowa pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="fe890-127">The output path of the template file.</span></span>

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

### <span data-ttu-id="fe890-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="fe890-128">-Pre</span></span>
<span data-ttu-id="fe890-129">Po ustawieniu wskazuje, że polecenie cmdlet ma używać wersji wstępnych interfejsu API podczas automatycznego ustalania, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="fe890-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fe890-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fe890-130">-Confirm</span></span>
<span data-ttu-id="fe890-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe890-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe890-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe890-132">-WhatIf</span></span>
<span data-ttu-id="fe890-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe890-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe890-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fe890-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe890-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe890-135">CommonParameters</span></span>
<span data-ttu-id="fe890-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe890-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe890-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe890-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe890-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe890-138">INPUTS</span></span>

### <span data-ttu-id="fe890-139">System. String</span><span class="sxs-lookup"><span data-stu-id="fe890-139">System.String</span></span>

## <span data-ttu-id="fe890-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe890-140">OUTPUTS</span></span>

### <span data-ttu-id="fe890-141">Microsoft. Azure. Commands. ResourceManager. aplety. SdkModels</span><span class="sxs-lookup"><span data-stu-id="fe890-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels</span></span>

## <span data-ttu-id="fe890-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe890-142">NOTES</span></span>

## <span data-ttu-id="fe890-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe890-143">RELATED LINKS</span></span>