---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181418"
---
# <span data-ttu-id="ad9e6-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ad9e6-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="ad9e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad9e6-102">SYNOPSIS</span></span>
<span data-ttu-id="ad9e6-103">Ponownie generuje poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="ad9e6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad9e6-104">SYNTAX</span></span>

### <span data-ttu-id="ad9e6-105">NameResourceGroupParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ad9e6-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ad9e6-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad9e6-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad9e6-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ad9e6-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad9e6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad9e6-108">DESCRIPTION</span></span>
<span data-ttu-id="ad9e6-109">Polecenie Update-AzContainerRegistryCredential ponownie generuje poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="ad9e6-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad9e6-110">EXAMPLES</span></span>

### <span data-ttu-id="ad9e6-111">Przykład 1. Ponowne generowanie poświadczeń logowania dla rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ad9e6-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="ad9e6-112">To polecenie ponownie generuje poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="ad9e6-113">Aby generować poświadczenia logowania, użytkownik administrator musi mieć włączony kontener rejestru \` MyRegistry. \`</span><span class="sxs-lookup"><span data-stu-id="ad9e6-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="ad9e6-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad9e6-114">PARAMETERS</span></span>

### <span data-ttu-id="ad9e6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad9e6-115">-DefaultProfile</span></span>
<span data-ttu-id="ad9e6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ad9e6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ad9e6-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad9e6-117">-Name</span></span>
<span data-ttu-id="ad9e6-118">Container Registry Name (Nazwa rejestru kontenera).</span><span class="sxs-lookup"><span data-stu-id="ad9e6-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="ad9e6-119">-PasswordName</span></span>
<span data-ttu-id="ad9e6-120">Nazwa hasła do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-120">The name of password to regenerate.</span></span>
<span data-ttu-id="ad9e6-121">Dozwolone wartości: hasło, hasło2.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="ad9e6-122">-Registry</span></span>
<span data-ttu-id="ad9e6-123">Obiekt Container Registry.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad9e6-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad9e6-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ad9e6-126">-ResourceId</span></span>
<span data-ttu-id="ad9e6-127">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="ad9e6-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad9e6-128">-Confirm</span></span>
<span data-ttu-id="ad9e6-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad9e6-130">-WhatIf</span></span>
<span data-ttu-id="ad9e6-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad9e6-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad9e6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad9e6-133">CommonParameters</span></span>
<span data-ttu-id="ad9e6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad9e6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad9e6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad9e6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad9e6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad9e6-136">INPUTS</span></span>

### <span data-ttu-id="ad9e6-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad9e6-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="ad9e6-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ad9e6-138">System.String</span></span>

## <span data-ttu-id="ad9e6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad9e6-139">OUTPUTS</span></span>

### <span data-ttu-id="ad9e6-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ad9e6-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="ad9e6-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad9e6-141">NOTES</span></span>

## <span data-ttu-id="ad9e6-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad9e6-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad9e6-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad9e6-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="ad9e6-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ad9e6-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="ad9e6-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="ad9e6-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

