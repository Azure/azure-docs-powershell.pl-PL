---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 7a113bad74252778c32fc1273c9c3ca587bf1c2a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706078"
---
# <span data-ttu-id="09925-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="09925-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="09925-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09925-102">SYNOPSIS</span></span>
<span data-ttu-id="09925-103">Generuje ponownie poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="09925-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="09925-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09925-104">SYNTAX</span></span>

### <span data-ttu-id="09925-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="09925-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09925-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="09925-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09925-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09925-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09925-108">Opis</span><span class="sxs-lookup"><span data-stu-id="09925-108">DESCRIPTION</span></span>
<span data-ttu-id="09925-109">Polecenie cmdlet Update-AzContainerRegistryCredential ponownie generuje poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="09925-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="09925-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09925-110">EXAMPLES</span></span>

### <span data-ttu-id="09925-111">Przykład 1. Regeneruj ponownie poświadczenia logowania dla rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="09925-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="09925-112">To polecenie generuje ponownie poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="09925-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="09925-113">Administrator musi być włączony w rejestrze kontenera rejestru, \` \` Aby ponownie wygenerować poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="09925-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="09925-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09925-114">PARAMETERS</span></span>

### <span data-ttu-id="09925-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09925-115">-DefaultProfile</span></span>
<span data-ttu-id="09925-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="09925-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09925-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="09925-117">-Name</span></span>
<span data-ttu-id="09925-118">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="09925-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="09925-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="09925-119">-PasswordName</span></span>
<span data-ttu-id="09925-120">Nazwa hasła do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="09925-120">The name of password to regenerate.</span></span>
<span data-ttu-id="09925-121">Dozwolone wartości: Password (hasło), password2.</span><span class="sxs-lookup"><span data-stu-id="09925-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="09925-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="09925-122">-Registry</span></span>
<span data-ttu-id="09925-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="09925-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="09925-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09925-124">-ResourceGroupName</span></span>
<span data-ttu-id="09925-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="09925-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="09925-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09925-126">-ResourceId</span></span>
<span data-ttu-id="09925-127">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="09925-127">The container registry resource id</span></span>

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

### <span data-ttu-id="09925-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="09925-128">-Confirm</span></span>
<span data-ttu-id="09925-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09925-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09925-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09925-130">-WhatIf</span></span>
<span data-ttu-id="09925-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09925-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09925-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="09925-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09925-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09925-133">CommonParameters</span></span>
<span data-ttu-id="09925-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09925-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09925-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="09925-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09925-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09925-136">INPUTS</span></span>

### <span data-ttu-id="09925-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="09925-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="09925-138">System. String</span><span class="sxs-lookup"><span data-stu-id="09925-138">System.String</span></span>

## <span data-ttu-id="09925-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09925-139">OUTPUTS</span></span>

### <span data-ttu-id="09925-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="09925-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="09925-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09925-141">NOTES</span></span>

## <span data-ttu-id="09925-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09925-142">RELATED LINKS</span></span>

[<span data-ttu-id="09925-143">Nowe — AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="09925-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="09925-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="09925-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="09925-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="09925-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

