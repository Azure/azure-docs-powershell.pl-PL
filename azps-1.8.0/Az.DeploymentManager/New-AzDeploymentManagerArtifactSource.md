---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 09feb94b046ef6a41130c26ae5e7b996ecbd8771
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709966"
---
# <span data-ttu-id="16705-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="16705-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="16705-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16705-102">SYNOPSIS</span></span>
<span data-ttu-id="16705-103">Tworzy Źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="16705-103">Creates an artifact source.</span></span>

## <span data-ttu-id="16705-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16705-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16705-105">Opis</span><span class="sxs-lookup"><span data-stu-id="16705-105">DESCRIPTION</span></span>
<span data-ttu-id="16705-106">Polecenie cmdlet **New-AzDeploymentManagerArtifactSource** tworzy Źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="16705-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="16705-107">Określ *imię i nazwisko* , *ResourceGroupName* oraz wymagane właściwości.</span><span class="sxs-lookup"><span data-stu-id="16705-107">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="16705-108">Zwrócony obiekt można zmodyfikować lokalnie, a następnie zastosować zmiany w źródle artefaktów, korzystając z polecenia cmdlet Set-AzDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="16705-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="16705-109">Polecenie cmdlet zwraca obiekt ArtifactSource z identyfikatorem ResourceId, do którego można odwoływać się w poleceniu cmdlet New-AzDeloymentManagerServiceTopology, aby artefakty wymagane dla zasobu serviceunit, szablonu i parametrów mogły odwoływać się w tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="16705-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeloymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="16705-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16705-110">EXAMPLES</span></span>

### <span data-ttu-id="16705-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="16705-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="16705-112">Tworzy w ContosoResourceGroup Źródło artefaktu o nazwie ContosoArtifactSource z centralą centralną jako lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="16705-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="16705-113">Właściwość SasUri zapewnia identyfikator URI SAS magazynu platformy Azure dla kontenera magazynu, w którym są przechowywane artefakty.</span><span class="sxs-lookup"><span data-stu-id="16705-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="16705-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16705-114">PARAMETERS</span></span>

### <span data-ttu-id="16705-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="16705-115">-ArtifactRoot</span></span>
<span data-ttu-id="16705-116">Opcjonalne przesunięcie katalogu w kontenerze przechowywania artefaktów.</span><span class="sxs-lookup"><span data-stu-id="16705-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="16705-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16705-117">-DefaultProfile</span></span>
<span data-ttu-id="16705-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16705-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16705-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="16705-119">-Location</span></span>
<span data-ttu-id="16705-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="16705-120">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16705-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="16705-121">-Name</span></span>
<span data-ttu-id="16705-122">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="16705-122">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16705-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16705-123">-ResourceGroupName</span></span>
<span data-ttu-id="16705-124">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="16705-124">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16705-125">-SasUri</span><span class="sxs-lookup"><span data-stu-id="16705-125">-SasUri</span></span>
<span data-ttu-id="16705-126">Identyfikator URI SAS do kontenera magazynu platformy Azure, w którym są przechowywane artefakty.</span><span class="sxs-lookup"><span data-stu-id="16705-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16705-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="16705-127">-Tag</span></span>
<span data-ttu-id="16705-128">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="16705-128">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16705-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16705-129">-Confirm</span></span>
<span data-ttu-id="16705-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16705-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16705-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16705-131">-WhatIf</span></span>
<span data-ttu-id="16705-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16705-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16705-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="16705-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16705-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16705-134">CommonParameters</span></span>
<span data-ttu-id="16705-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16705-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16705-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16705-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16705-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16705-137">INPUTS</span></span>

### <span data-ttu-id="16705-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="16705-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="16705-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16705-139">OUTPUTS</span></span>

### <span data-ttu-id="16705-140">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="16705-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="16705-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16705-141">NOTES</span></span>

## <span data-ttu-id="16705-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16705-142">RELATED LINKS</span></span>