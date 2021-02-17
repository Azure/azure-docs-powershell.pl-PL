---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196907"
---
# <span data-ttu-id="2148e-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="2148e-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="2148e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2148e-102">SYNOPSIS</span></span>
<span data-ttu-id="2148e-103">Import image from a public/azure registry to an azure container registry.</span><span class="sxs-lookup"><span data-stu-id="2148e-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="2148e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2148e-104">SYNTAX</span></span>

### <span data-ttu-id="2148e-105">ImportImageByResourceId (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2148e-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2148e-106">ImportImageByResourceIdWithCredential</span><span class="sxs-lookup"><span data-stu-id="2148e-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2148e-107">ImportImageByRegistryUri</span><span class="sxs-lookup"><span data-stu-id="2148e-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2148e-108">ImportImageByRegistryUriWithCredential</span><span class="sxs-lookup"><span data-stu-id="2148e-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2148e-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="2148e-109">DESCRIPTION</span></span>
<span data-ttu-id="2148e-110">Import image from a public/azure registry to an azure container registry.</span><span class="sxs-lookup"><span data-stu-id="2148e-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="2148e-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2148e-111">EXAMPLES</span></span>

### <span data-ttu-id="2148e-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2148e-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="2148e-113">Importowanie zajętego pola do ACR.</span><span class="sxs-lookup"><span data-stu-id="2148e-113">Import busybox to ACR.</span></span> <span data-ttu-id="2148e-114">Uwaga:</span><span class="sxs-lookup"><span data-stu-id="2148e-114">Note:</span></span> 
* <span data-ttu-id="2148e-115">Przed obrazem źródłowym należy dodać "bibliotekę/".</span><span class="sxs-lookup"><span data-stu-id="2148e-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="2148e-116">"busybox:latest" => "library/busybox:latest"</span><span class="sxs-lookup"><span data-stu-id="2148e-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="2148e-117">Wymagane poświadczenia, jeśli rejestr źródłowy nie jest publicznie dostępny</span><span class="sxs-lookup"><span data-stu-id="2148e-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="2148e-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2148e-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="2148e-119">Importowanie zajętego pola ze źródłowego do docelowego pola ACR.</span><span class="sxs-lookup"><span data-stu-id="2148e-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="2148e-120">Uwaga:</span><span class="sxs-lookup"><span data-stu-id="2148e-120">Note:</span></span> 
* <span data-ttu-id="2148e-121">Poświadczenia są potrzebne, jeśli użytkownik administratora rejestru źródłowego został wyłączony.</span><span class="sxs-lookup"><span data-stu-id="2148e-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="2148e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2148e-122">PARAMETERS</span></span>

### <span data-ttu-id="2148e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2148e-123">-DefaultProfile</span></span>
<span data-ttu-id="2148e-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2148e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2148e-125">— tryb</span><span class="sxs-lookup"><span data-stu-id="2148e-125">-Mode</span></span>
<span data-ttu-id="2148e-126">Gdy wymusisz, wszystkie istniejące tagi docelowe zostaną zastąpione.</span><span class="sxs-lookup"><span data-stu-id="2148e-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="2148e-127">W przypadku usługi NoForce wszystkie istniejące tagi docelowe nie powiodą się przed rozpoczęciem kopiowania.</span><span class="sxs-lookup"><span data-stu-id="2148e-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

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

### <span data-ttu-id="2148e-128">— Hasło</span><span class="sxs-lookup"><span data-stu-id="2148e-128">-Password</span></span>
<span data-ttu-id="2148e-129">Hasło używane do uwierzytelniania w źródłowym rejestrze.</span><span class="sxs-lookup"><span data-stu-id="2148e-129">The password used to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="2148e-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="2148e-130">-RegistryName</span></span>
<span data-ttu-id="2148e-131">Docelowa nazwa rejestru.</span><span class="sxs-lookup"><span data-stu-id="2148e-131">Target registry name.</span></span>

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

### <span data-ttu-id="2148e-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2148e-132">-ResourceGroupName</span></span>
<span data-ttu-id="2148e-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2148e-133">Resource group name.</span></span>

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

### <span data-ttu-id="2148e-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="2148e-134">-SourceImage</span></span>
<span data-ttu-id="2148e-135">Nazwa repozytorium obrazu źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2148e-135">Repository name of the source image.</span></span>

<span data-ttu-id="2148e-136">Określanie obrazu według repozytorium (witaj świecie).</span><span class="sxs-lookup"><span data-stu-id="2148e-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="2148e-137">Spowoduje to użycie tagu "najnowszy".</span><span class="sxs-lookup"><span data-stu-id="2148e-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="2148e-138">Określanie obrazu według tagu ('hello-world:latest').</span><span class="sxs-lookup"><span data-stu-id="2148e-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="2148e-139">Określanie obrazu za pomocą pliku manifestu opartego na pliku manifestu opartego na danych sha256 (' hello-world@sha256:abc123 ').</span><span class="sxs-lookup"><span data-stu-id="2148e-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

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

### <span data-ttu-id="2148e-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="2148e-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="2148e-141">Identyfikator zasobu źródłowego rejestru Azure Container Registry.</span><span class="sxs-lookup"><span data-stu-id="2148e-141">The resource identifier of the source Azure Container Registry.</span></span>

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

### <span data-ttu-id="2148e-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="2148e-142">-SourceRegistryUri</span></span>
<span data-ttu-id="2148e-143">Adres rejestru źródłowego (np. "mcr.microsoft.com").</span><span class="sxs-lookup"><span data-stu-id="2148e-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

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

### <span data-ttu-id="2148e-144">- TargetTag</span><span class="sxs-lookup"><span data-stu-id="2148e-144">-TargetTag</span></span>
<span data-ttu-id="2148e-145">Lista ciągów w formularzu repo \[ \] :tag.</span><span class="sxs-lookup"><span data-stu-id="2148e-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="2148e-146">Jeśli tag zostanie pominięty, zostanie użyte źródło (lub "najnowszy", jeśli tag źródłowy również zostanie pominięty).</span><span class="sxs-lookup"><span data-stu-id="2148e-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

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

### <span data-ttu-id="2148e-147">-UntaggedTargetRepository</span><span class="sxs-lookup"><span data-stu-id="2148e-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="2148e-148">Lista ciągów nazw repozytoriów, które mają być kopią manifestu.</span><span class="sxs-lookup"><span data-stu-id="2148e-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="2148e-149">Nie zostanie utworzony żaden tag.</span><span class="sxs-lookup"><span data-stu-id="2148e-149">No tag will be created.</span></span>

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

### <span data-ttu-id="2148e-150">- Nazwa użytkownika</span><span class="sxs-lookup"><span data-stu-id="2148e-150">-Username</span></span>
<span data-ttu-id="2148e-151">Nazwa użytkownika do uwierzytelnienia w źródłowym rejestrze.</span><span class="sxs-lookup"><span data-stu-id="2148e-151">The username to authenticate with the source registry.</span></span>

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

### <span data-ttu-id="2148e-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2148e-152">-Confirm</span></span>
<span data-ttu-id="2148e-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2148e-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2148e-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2148e-154">-WhatIf</span></span>
<span data-ttu-id="2148e-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2148e-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2148e-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2148e-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2148e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2148e-157">CommonParameters</span></span>
<span data-ttu-id="2148e-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2148e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2148e-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2148e-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2148e-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2148e-160">INPUTS</span></span>

### <span data-ttu-id="2148e-161">System.String</span><span class="sxs-lookup"><span data-stu-id="2148e-161">System.String</span></span>

## <span data-ttu-id="2148e-162">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2148e-162">OUTPUTS</span></span>

### <span data-ttu-id="2148e-163">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2148e-163">System.Boolean</span></span>

## <span data-ttu-id="2148e-164">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2148e-164">NOTES</span></span>

## <span data-ttu-id="2148e-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2148e-165">RELATED LINKS</span></span>
