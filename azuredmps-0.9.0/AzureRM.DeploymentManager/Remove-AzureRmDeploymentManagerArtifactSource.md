---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 7473f125511995efb1f6273d3b8adb675a58d06d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523081"
---
# <span data-ttu-id="08b3b-101">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="08b3b-101">Remove-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="08b3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08b3b-102">SYNOPSIS</span></span>
<span data-ttu-id="08b3b-103">Usuwa źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="08b3b-103">Deletes an artifact source.</span></span>

## <span data-ttu-id="08b3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08b3b-104">SYNTAX</span></span>

### <span data-ttu-id="08b3b-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="08b3b-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b3b-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="08b3b-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b3b-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="08b3b-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08b3b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="08b3b-108">DESCRIPTION</span></span>
<span data-ttu-id="08b3b-109">Polecenie cmdlet **Remove-AzureRmDeploymentManagerArtifactSource** usuwa Źródło artefaktów, określając źródło artefaktu przy użyciu nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08b3b-109">The **Remove-AzureRmDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="08b3b-110">Alternatywnie możesz podać obiekt ArtifactSource lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="08b3b-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="08b3b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08b3b-111">EXAMPLES</span></span>

### <span data-ttu-id="08b3b-112">Przykład 1: Usuwanie źródła artefaktu</span><span class="sxs-lookup"><span data-stu-id="08b3b-112">Example 1: Delete an artifact source</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="08b3b-113">To polecenie usuwa Źródło artefaktu o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08b3b-113">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="08b3b-114">Przykład 2: Usuwanie źródła artefaktu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="08b3b-114">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="08b3b-115">To polecenie usuwa Źródło artefaktu o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="08b3b-115">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="08b3b-116">Przykład 3: Usuwanie źródła artefaktu przy użyciu obiektu</span><span class="sxs-lookup"><span data-stu-id="08b3b-116">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="08b3b-117">To polecenie powoduje usunięcie źródła artefaktów, których nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="08b3b-117">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="08b3b-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08b3b-118">PARAMETERS</span></span>

### <span data-ttu-id="08b3b-119">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="08b3b-119">-ArtifactSource</span></span>
<span data-ttu-id="08b3b-120">Magazyn artefaktów do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="08b3b-120">The artifact store to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08b3b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b3b-121">-DefaultProfile</span></span>
<span data-ttu-id="08b3b-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08b3b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08b3b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="08b3b-123">-Force</span></span>
<span data-ttu-id="08b3b-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="08b3b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="08b3b-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="08b3b-125">-Name</span></span>
<span data-ttu-id="08b3b-126">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="08b3b-126">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08b3b-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="08b3b-127">-PassThru</span></span>
<span data-ttu-id="08b3b-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="08b3b-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="08b3b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b3b-129">-ResourceGroupName</span></span>
<span data-ttu-id="08b3b-130">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="08b3b-130">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08b3b-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08b3b-131">-ResourceId</span></span>
<span data-ttu-id="08b3b-132">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="08b3b-132">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08b3b-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08b3b-133">-Confirm</span></span>
<span data-ttu-id="08b3b-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08b3b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b3b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08b3b-135">-WhatIf</span></span>
<span data-ttu-id="08b3b-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08b3b-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b3b-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08b3b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b3b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b3b-138">CommonParameters</span></span>
<span data-ttu-id="08b3b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b3b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b3b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="08b3b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b3b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08b3b-141">INPUTS</span></span>

### <span data-ttu-id="08b3b-142">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="08b3b-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="08b3b-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08b3b-143">OUTPUTS</span></span>

### <span data-ttu-id="08b3b-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="08b3b-144">System.Boolean</span></span>

## <span data-ttu-id="08b3b-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08b3b-145">NOTES</span></span>

## <span data-ttu-id="08b3b-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08b3b-146">RELATED LINKS</span></span>

[<span data-ttu-id="08b3b-147">Nowe — AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="08b3b-147">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="08b3b-148">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="08b3b-148">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="08b3b-149">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="08b3b-149">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)