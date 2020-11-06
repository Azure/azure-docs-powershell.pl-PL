---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553604"
---
# <span data-ttu-id="6eec3-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="6eec3-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="6eec3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6eec3-102">SYNOPSIS</span></span>
<span data-ttu-id="6eec3-103">Generuje ponownie poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6eec3-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eec3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6eec3-104">SYNTAX</span></span>

### <span data-ttu-id="6eec3-105">NameResourceGroupParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6eec3-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6eec3-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eec3-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6eec3-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6eec3-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eec3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6eec3-108">DESCRIPTION</span></span>
<span data-ttu-id="6eec3-109">Polecenie cmdlet Update-AzureRmContainerRegistryCredential ponownie generuje poświadczenia logowania dla rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6eec3-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="6eec3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6eec3-110">EXAMPLES</span></span>

### <span data-ttu-id="6eec3-111">Przykład 1. Regeneruj ponownie poświadczenia logowania dla rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="6eec3-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="6eec3-112">To polecenie generuje ponownie poświadczenia logowania dla określonego rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6eec3-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="6eec3-113">Administrator musi być włączony w rejestrze kontenera rejestru, \` \` Aby ponownie wygenerować poświadczenia logowania.</span><span class="sxs-lookup"><span data-stu-id="6eec3-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="6eec3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6eec3-114">PARAMETERS</span></span>

### <span data-ttu-id="6eec3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eec3-115">-DefaultProfile</span></span>
<span data-ttu-id="6eec3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="6eec3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6eec3-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6eec3-117">-Name</span></span>
<span data-ttu-id="6eec3-118">Nazwa rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6eec3-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="6eec3-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="6eec3-119">-PasswordName</span></span>
<span data-ttu-id="6eec3-120">Nazwa hasła do ponownego wygenerowania.</span><span class="sxs-lookup"><span data-stu-id="6eec3-120">The name of password to regenerate.</span></span>
<span data-ttu-id="6eec3-121">Dozwolone wartości: Password (hasło), password2.</span><span class="sxs-lookup"><span data-stu-id="6eec3-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="6eec3-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="6eec3-122">-Registry</span></span>
<span data-ttu-id="6eec3-123">Obiekt rejestru kontenera.</span><span class="sxs-lookup"><span data-stu-id="6eec3-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="6eec3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eec3-124">-ResourceGroupName</span></span>
<span data-ttu-id="6eec3-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6eec3-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6eec3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6eec3-126">-ResourceId</span></span>
<span data-ttu-id="6eec3-127">Identyfikator zasobu rejestru kontenera</span><span class="sxs-lookup"><span data-stu-id="6eec3-127">The container registry resource id</span></span>

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

### <span data-ttu-id="6eec3-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6eec3-128">-Confirm</span></span>
<span data-ttu-id="6eec3-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eec3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eec3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eec3-130">-WhatIf</span></span>
<span data-ttu-id="6eec3-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6eec3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eec3-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6eec3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eec3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eec3-133">CommonParameters</span></span>
<span data-ttu-id="6eec3-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6eec3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eec3-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eec3-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eec3-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6eec3-136">INPUTS</span></span>

### <span data-ttu-id="6eec3-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6eec3-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="6eec3-138">Parametry: Registry (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6eec3-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="6eec3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="6eec3-139">System.String</span></span>

## <span data-ttu-id="6eec3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6eec3-140">OUTPUTS</span></span>

### <span data-ttu-id="6eec3-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="6eec3-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="6eec3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6eec3-142">NOTES</span></span>

## <span data-ttu-id="6eec3-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6eec3-143">RELATED LINKS</span></span>

[<span data-ttu-id="6eec3-144">Nowe — AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6eec3-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="6eec3-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="6eec3-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="6eec3-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="6eec3-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

