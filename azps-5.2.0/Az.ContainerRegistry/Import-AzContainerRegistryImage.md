---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346306"
---
# <span data-ttu-id="d3d43-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="d3d43-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="d3d43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d3d43-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d43-103">Importowanie obrazu z rejestru publicznego/Azure do rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d43-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="d3d43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d3d43-104">SYNTAX</span></span>

### <span data-ttu-id="d3d43-105">ImportImageByResourceId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="d3d43-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3d43-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="d3d43-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d43-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="d3d43-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3d43-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="d3d43-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d3d43-109">Opis</span><span class="sxs-lookup"><span data-stu-id="d3d43-109">DESCRIPTION</span></span>
<span data-ttu-id="d3d43-110">Importowanie obrazu z rejestru publicznego/Azure do rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d43-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="d3d43-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d3d43-111">EXAMPLES</span></span>

### <span data-ttu-id="d3d43-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3d43-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="d3d43-113">Importowanie BUSYBOX do ACR.</span><span class="sxs-lookup"><span data-stu-id="d3d43-113">Import busybox to ACR.</span></span> <span data-ttu-id="d3d43-114">Warto</span><span class="sxs-lookup"><span data-stu-id="d3d43-114">Note:</span></span> 
* <span data-ttu-id="d3d43-115">"Library/" musi być dodawany przed obrazem źródłowym.</span><span class="sxs-lookup"><span data-stu-id="d3d43-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="d3d43-116">"BUSYBOX: Najnowsza" => "Library/BUSYBOX: Najnowsza"</span><span class="sxs-lookup"><span data-stu-id="d3d43-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="d3d43-117">Poświadczenie jest wymagane, jeśli rejestr źródłowy nie jest publicznie dostępny</span><span class="sxs-lookup"><span data-stu-id="d3d43-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="d3d43-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d3d43-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="d3d43-119">Zaimportuj BusyBox z ACR źródłowego do elementu docelowego ACR.</span><span class="sxs-lookup"><span data-stu-id="d3d43-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="d3d43-120">Warto</span><span class="sxs-lookup"><span data-stu-id="d3d43-120">Note:</span></span> 
* <span data-ttu-id="d3d43-121">Poświadczenie jest wymagane, jeśli użytkownik administracyjny dla rejestru źródłowego został wyłączony.</span><span class="sxs-lookup"><span data-stu-id="d3d43-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="d3d43-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d3d43-122">PARAMETERS</span></span>

### <span data-ttu-id="d3d43-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d43-123">-DefaultProfile</span></span>
<span data-ttu-id="d3d43-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d43-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d43-125">-Mode (tryb)</span><span class="sxs-lookup"><span data-stu-id="d3d43-125">-Mode</span></span>
<span data-ttu-id="d3d43-126">Po wymuszeniu wszystkie istniejące znaczniki docelowe zostaną zastąpione.</span><span class="sxs-lookup"><span data-stu-id="d3d43-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="d3d43-127">Po wymuszeniu wszystkie istniejące znaczniki docelowe zakończą operację, zanim rozpocznie się kopiowanie.</span><span class="sxs-lookup"><span data-stu-id="d3d43-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-128">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="d3d43-128">-Password</span></span>
<span data-ttu-id="d3d43-129">Hasło używane do uwierzytelniania przy użyciu rejestru źródłowego.</span><span class="sxs-lookup"><span data-stu-id="d3d43-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-130">-Registryname</span><span class="sxs-lookup"><span data-stu-id="d3d43-130">-RegistryName</span></span>
<span data-ttu-id="d3d43-131">Nazwa rejestru docelowego.</span><span class="sxs-lookup"><span data-stu-id="d3d43-131">Target registry name.</span></span>

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

### <span data-ttu-id="d3d43-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d43-132">-ResourceGroupName</span></span>
<span data-ttu-id="d3d43-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d3d43-133">Resource group name.</span></span>

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

### <span data-ttu-id="d3d43-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="d3d43-134">-SourceImage</span></span>
<span data-ttu-id="d3d43-135">Nazwa repozytorium obrazu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="d3d43-135">Repository name of the source image.</span></span>

<span data-ttu-id="d3d43-136">Określ obraz według repozytorium ("Witaj na świecie").</span><span class="sxs-lookup"><span data-stu-id="d3d43-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="d3d43-137">Spowoduje to użycie znacznika "Najnowsza".</span><span class="sxs-lookup"><span data-stu-id="d3d43-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="d3d43-138">Określ obrazek według znacznika ("Witaj na świecie: Najnowsza").</span><span class="sxs-lookup"><span data-stu-id="d3d43-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="d3d43-139">Określ obraz na podstawie skrótu manifestu opartego na SHA256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="d3d43-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="d3d43-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="d3d43-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="d3d43-141">Identyfikator zasobu źródłowego rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d43-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="d3d43-142">-SourceRegistryUri</span></span>
<span data-ttu-id="d3d43-143">Adres rejestru źródłowego (na przykład "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="d3d43-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="d3d43-144">-TargetTag</span></span>
<span data-ttu-id="d3d43-145">Lista ciągów formularza repozytorium \[ : tag \] .</span><span class="sxs-lookup"><span data-stu-id="d3d43-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="d3d43-146">Gdy znacznik zostanie pominięty, zostanie użyte źródło (lub "Najnowsza", Jeśli znacznik źródłowy jest również pominięty).</span><span class="sxs-lookup"><span data-stu-id="d3d43-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="d3d43-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="d3d43-148">Lista ciągów nazw repozytoriów w celu wykonania kopii tylko w manifeście.</span><span class="sxs-lookup"><span data-stu-id="d3d43-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="d3d43-149">Nie zostanie utworzony żaden znacznik.</span><span class="sxs-lookup"><span data-stu-id="d3d43-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-150">-Username</span><span class="sxs-lookup"><span data-stu-id="d3d43-150">-Username</span></span>
<span data-ttu-id="d3d43-151">Nazwa użytkownika do uwierzytelnienia przy użyciu rejestru źródłowego.</span><span class="sxs-lookup"><span data-stu-id="d3d43-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3d43-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d3d43-152">-Confirm</span></span>
<span data-ttu-id="d3d43-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d43-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3d43-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3d43-154">-WhatIf</span></span>
<span data-ttu-id="d3d43-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3d43-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3d43-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d3d43-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3d43-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d43-157">CommonParameters</span></span>
<span data-ttu-id="d3d43-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d43-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d43-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3d43-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d43-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3d43-160">INPUTS</span></span>

### <span data-ttu-id="d3d43-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d3d43-161">System.String</span></span>

## <span data-ttu-id="d3d43-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d3d43-162">OUTPUTS</span></span>

### <span data-ttu-id="d3d43-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3d43-163">System.Boolean</span></span>

## <span data-ttu-id="d3d43-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d3d43-164">NOTES</span></span>

## <span data-ttu-id="d3d43-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3d43-165">RELATED LINKS</span></span>
